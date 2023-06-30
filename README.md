#Google Doc to HTML

This is a Google Apps Script to convert a Google Document to clean HTML. Here's a breakdown of the key parts:

**ConvertGoogleDocToCleanHtml**: This is the main function which reads the active Google Document's content, processes each child element (paragraph, image, list, etc.) to HTML format using processItem, and then saves the HTML to Google Drive using saveHtmlToDrive.

**saveHtmlToDrive**: This function takes the HTML content and an array of image data, and saves them to a Google Drive folder. It converts the HTML string into a Google Doc file blob and stores it to a specific folder in your Google Drive. Note that you need to replace 'Your_Folder_Id_Here' with the actual ID of your Drive folder.

**createDocumentForHtml**: This function takes the HTML content and an array of image data, and creates a new Google Document with this information. It appends each image to the end of the document.

**dumpAttributes**: This function logs all of the attributes of a Google Document paragraph for debugging purposes.

**processItem**: This function converts a Google Document element to its equivalent HTML representation. It handles different types of elements such as paragraph, list, and image. It calls processText for text elements and processImage for image elements.

**processText**: This function converts a Google Document text element to its equivalent HTML representation. It applies corresponding HTML tags based on the text formatting (bold, italic, underline).

**processImage**: This function handles image elements of the document. It saves image blob data to an array and returns an img HTML tag with the image's name as the source (src). The saved image data can be used later to upload images to a server or embed in the HTML file as base64 data.

Remember to replace 'Your_Folder_Id_Here' in saveHtmlToDrive function with your actual Google Drive folder ID where you want to save the converted HTML file. Also, this script doesn't support all Google Document features, such as tables, drawings, and certain types of formatting, but it gives a good starting point for a basic converter. You may need to extend it according to your specific needs.
