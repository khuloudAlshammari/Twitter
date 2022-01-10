# App-Khuloud
#The application is a program similar to the Twitter application so that a person can share posts and reply to a post
**this code is responsible for logging in the user as a guest**
`func prepare(for segue: UIStoryboardSegue, sender: Any?) {
        if segue.identifier == "logoutSegue"{
            UserManager.loggedInUser = nil`
  # This code is responsible for adding a new post and an image
  ` func addButtonClicked(_ sender: Any) {
        if let user = UserManager.loggedInUser {
            addButton.setTitle("", for: .normal)
            loaderView.startAnimating()
            PostAPI.addNewPost( imageURL:postImageTextField.text!, text: postTextField.text!, userId: user.id) {
                self.loaderView.stopAnimating()
                self.addButton.setTitle("Add", for: .normal)
                NotificationCenter.default.post(name: NSNotification.Name("NewPostAdded"), object: nil,userInfo: nil)
                self.dismiss(animated: true, completion: nil)
        <img width="332" alt="‏لقطة الشاشة ١٤٤٣-٠٦-٠٧ في ١ ٢٠ ١٧ ص" src="https://user-images.githubusercontent.com/95877163/148755773-27a86706-a8f8-4418-a803-9d1c49ca8e00.png">
}
        }`