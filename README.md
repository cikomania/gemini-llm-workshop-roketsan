# LEVEL UP AI | ROKETSAN AI Hackathon
## Workshop İçeriği
### 1. LLM Pratikleri
#### Proje Oluşturulması ve Sanal Ortam

```bash
python -m venv venv
.\venv\Scripts\activate
```
```text
main.py
```

#### Kütüphane Kurulması
Workshop boyunca kullanılan kütüphaneler:
```text
langchain
langchain-google-genai
langchain-community
langchain-text-splitters
langchain-core
langgraph
faiss-cpu
python-dotenv
```
```bash
pip install -r requirements.txt
```

#### Gemini API Key

https://aistudio.google.com/api-keys  

.env dosyasına: GOOGLE_API_KEY=""

#### İlk Gemini Çağrısı
Gemini API kullanılarak ilk LLM çağrısının gerçekleştirilmesi ve modelden yanıt alınması

---

### 2. RAG
LLM'nin yalnızca kendi bilgisine bağlı kalmak yerine, verilen teknik dokümandan ilgili bilgileri bulup kullanabilmesi için RAG yapısı oluşturulmuştur.

#### Proje Yapısı
```text
mil_std_document.py
create_vector_db.py
rag.py
```
- mil_std_document.py → MIL-STD dokümanının hazırlanması
- create_vector_db.py → Dokümanların parçalara ayrılması, embedding oluşturulması ve FAISS vektör veritabanının oluşturulması
- rag.py → RAG pipeline ve soru-cevap işlemleri

#### MIL-STD Dokümanı Oluşturma
Workshop kapsamında kullanılan örnek doküman:  
https://github.com/turkiyeyapayzekaakademisi/llm-rag-memory-ai-agents/

---

### 3. AI Agents
LLM'nin kullanıcı sorusunu analiz ederek uygun aracı seçebilmesi için AI Agent yapısı oluşturulmuştur.

#### Proje Yapısı
```text
tools.py
agent.py
```
- tools.py → Agent tarafından kullanılabilecek araçların tanımlanması
- agent.py → Agent yapısının ve çalışma akışının oluşturulması

Agent iki farklı tool kullanmaktadır:

- general_question_tool → Genel bilgi, yazılım, teknoloji ve doküman dışındaki sorular
- mil_std_rag_tool → RKT-MIL-STD-001 teknik dokümanıyla ilgili sorular

---

### Tech Stack
- Python
- Google Gemini
- LangChain
- LangGraph
- FAISS
- RAG
- Prompt Engineering
- AI Agents
- Vector Databases
- Conversation Memory
