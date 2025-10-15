# Karpathy-skolen

## Pensum

[ChatGPT med læringsforslag](https://chatgpt.com/share/68d8d0c7-f1a8-8002-af24-d178d26289f6)

[YouTube video](https://www.youtube.com/watch?v=kCc8FmEb1nY)

[Notebook for videoen](https://colab.research.google.com/drive/1JMLa53HDuA-i7ZBmqV7ZnA3c_fvtXnx-?usp=sharing)

[nanoGPT-repo](https://github.com/karpathy/nanoGPT)

[Repo for videoen](https://github.com/karpathy/ng-video-lecture)

## Notater

ChatGPT er et probabilistisk system. For samme promt kan det gi oss forskjellige svar.
Prompten er starten på sekvens av ord/tokens, svaret er fortsettelsen.

Attention is all you need fra 2017, “Landemerke-paper” som satte frem transformer-arkitekturen.
GPT = Generatively Pretrained Transformer. Transformeren er nevral-nettverket som gjør jobben

Det vi skal bygge her er en karakter-basert LM som ikke trenes på internet men et mindre datasett. En sammensetning av Shakespear’s samlede verker.

Trenger litt kunnskap om python, differensialregning og integralregning og statistikk.

Kan være lurt å gå tilbake til Andrejs “Make more series”

I eksempelet er enkeltkarakterer våre token, men openAI og Google f.eks. Bruker “delord” som tokens. Så vi får liten “codebook” og veldig enkel encoding og decoding, men vi får lange tekstsekvenser.

Trener ikke modellen på hele trenings-settet, ville ikke gå rundt ytelesesmessig, men biter av det (block, blocksize)

Sender det inn i batcher for å utnytte GPU-ens parallelitet, men ver del behandles uavhengig av hverandre

Bruker python BigramLanguageModel som nevralt nettverk, den enkleste han vet. Har gått gjennom den detaljert
tidligere i “Make more series”. Sender inn torch tensor til bigram. B, T, C

Kommet til 34:55 i video
