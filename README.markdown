# 🌱 Watsonx.ai General Chatbot with Image Upload

A visually appealing and interactive Streamlit application that integrates IBM Watsonx.ai's vision-enabled language model to create a chatbot capable of processing text and images. Perfect for urban farming enthusiasts or anyone looking to explore multimodal AI conversations!

---

## 🚀 Features

- **Text-Based Chat**: Engage in natural conversations with a Watsonx.ai-powered chatbot.
- **Image Upload & Analysis**: Upload images (PNG, JPG, JPEG) to enhance your queries, such as analyzing a terrace for urban farming.
- **Urban Farming Guidance**: Tailored advice for starting an urban farm, including plant selection, container choices, and soil recommendations.
- **Persistent Chat History**: Retains conversation history for seamless interactions using Streamlit's session state.
- **Custom Instructions**: Includes predefined guidance for urban terrace farming, with the ability to incorporate custom knowledge from text files.
- **Error Handling**: Robust error handling for image processing, API initialization, and model interactions.
- **Responsive Design**: Clean, centered layout with a sidebar for image uploads, optimized for user experience.

---

## 🛠️ Prerequisites

To run this application, ensure you have the following:

- **Python 3.8+**
- **IBM Cloud Account**: Access to Watsonx.ai with an API key and project ID.
- **Dependencies** (install via `requirements.txt`):
  - `streamlit`
  - `langchain-ibm`
  - `ibm-watsonx-ai`
  - `pillow`
  - `base64`
  - `io`

Install dependencies using:
```bash
pip install -r requirements.txt
```

---

## 📂 Project Structure

```
project_directory/
│
├── app.py                          # Main Streamlit application
├── urban_terrace_farming_knowledge.txt  # Knowledge file for urban farming
├── requirements.txt                # Python dependencies
└── README.md                       # This file
```

---

## ⚙️ Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Set Up Environment Variables**:
   Update `app.py` with your Watsonx.ai credentials:
   - `WATSONX_API_KEY`: Your IBM Cloud API key.
   - `WATSONX_PROJECT_ID`: Your Watsonx.ai project ID.
   - `WATSONX_SERVICE_URL`: Your Watsonx.ai service URL (e.g., `https://us-south.ml.cloud.ibm.com`).
   - `WATSONX_MODEL_ID`: Choose a vision-enabled model (e.g., `meta-llama/llama-3-2-90b-vision-instruct`).

3. **Prepare Knowledge File**:
   Ensure `urban_terrace_farming_knowledge.txt` is in the project directory with relevant information for the chatbot.

4. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

5. **Run the Application**:
   ```bash
   streamlit run app.py
   ```

6. **Access the App**:
   Open your browser and navigate to `http://localhost:8501`.

---

## 🌟 Usage

1. **Start Chatting**:
   - Type your message in the chat input box at the bottom of the page.
   - The chatbot responds with tailored advice, leveraging the urban farming knowledge base.

2. **Upload an Image**:
   - Use the sidebar to upload an image (e.g., a photo of your terrace).
   - The chatbot will process the image alongside your text query to provide context-aware responses.
   - The uploaded image is displayed in the sidebar and cleared after processing to avoid reuse.

3. **View Chat History**:
   - Previous messages and images are displayed in the main chat area for easy reference.

4. **Urban Farming Tips**:
   - Ask about plants, containers, or soil suitable for your terrace.
   - The chatbot uses predefined instructions and the knowledge file to provide actionable advice.

---

## 🎨 Example Interaction

**User**: *Uploads a terrace image*  
"I want to start an urban farm on this terrace. What plants should I grow?"

**Chatbot**:  
"This is a fantastic space for an urban farm! Based on the image, I see a terrace with great potential for plants that need a lot of sunlight. I recommend sun-loving vegetables like tomatoes, peppers, and eggplants, as well as herbs like rosemary, basil, and mint. Ensure your containers have good drainage and use a lightweight potting mix. Would you like specific care tips for any of these plants?"

---

## 🔧 Customization

- **Change Model Parameters**: Modify `WATSONX_MODEL_PARAMETERS` in `app.py` to adjust `temperature`, `max_new_tokens`, etc., for different response styles.
- **Update Knowledge Base**: Edit `urban_terrace_farming_knowledge.txt` to include new information or adapt for other domains.
- **Switch Models**: Update `WATSONX_MODEL_ID` to use other vision-enabled models available in your Watsonx.ai instance.

---

## 🐛 Troubleshooting

- **API Errors**: Verify your `WATSONX_API_KEY`, `WATSONX_PROJECT_ID`, and `WATSONX_SERVICE_URL` are correct.
- **Model Issues**: Ensure the selected model supports multimodal (text + image) input.
- **Image Upload Errors**: Check that uploaded images are in PNG, JPG, or JPEG format and are not corrupted.
- **Knowledge File Missing**: Ensure `urban_terrace_farming_knowledge.txt` exists in the project directory.

For further assistance, refer to the [Watsonx.ai Documentation](https://www.ibm.com/docs/en/watsonx) or contact IBM Cloud support.

---

## 🌍 Future Enhancements

- Add support for multiple knowledge files for different domains.
- Implement real-time image preview before sending.
- Enhance the UI with custom themes and additional input options.
- Integrate more advanced vision models for detailed image analysis.

---

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## 🙌 Contributing

Contributions are welcome! Please:
1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add YourFeature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.
