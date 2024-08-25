# photoclass Photo:
    def __init__(self, title, photographer, date_taken):
        self.title = title
        self.photographer = photographer
        self.date_taken = date_taken
        self.is_favorite = False

    def display_info(self):
        """Display the photo details."""
        favorite_status = "Favorite" if self.is_favorite else "Not a favorite"
        print(f"Title: {self.title}")
        print(f"Photographer: {self.photographer}")
        print(f"Date Taken: {self.date_taken}")
        print(f"Status: {favorite_status}")

    def mark_as_favorite(self):
        """Mark the photo as a favorite."""
        self.is_favorite = True
        print(f"'{self.title}' has been marked as a favorite.")

    def unmark_as_favorite(self):
        """Unmark the photo as a favorite."""
        self.is_favorite = False
        print(f"'{self.title}' is no longer a favorite.")


# Example usage
my_photo = Photo("Sunset Over the Ocean", "Jane Doe", "2024-08-25")
my_photo.display_info()         # Display initial info
my_photo.mark_as_favorite()     # Mark the photo as a favorite
my_photo.display_info()         # Display updated info
my_photo.unmark_as_favorite()   # Unmark the photo as a favorite
my_photo.display_info()         # Display updated info
