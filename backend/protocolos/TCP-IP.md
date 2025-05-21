# Protocolo TCP/IP

## 🧠O que é o protocolo TCP/IP?

O TCP/IP é o conjunto de regras que permite que dispositivos diferentes se comuniquem em redes como a internet.

Ele define como os dados são quebrados em pacotes, enviados, roteados, recebidos e reorganizados corretamente do ponto A ao ponto B.

---

## 📦Analogia com envio de cartas

Imagine que você quer enviar uma coleção de cartas para um amigo em outra cidade. Cada carta tem um pedaço da mensagem e você quer garantir que:

1. Todas as cartas cheguem no destino;
2. Elas cheguem na ordem certa;
3. Se alguma carta não chegar, ela seja reenviada;
4. Você saiba que seu amigo recebeu tudo certinho.

É isso que o TCP/IP faz com os dados que trafegam na internet!

---

## Dividido em duas partes

1.IP (Internet Protocol) - o "endereçamento e envio"

- Função: Pega os dados e os envia de um lugar para o outro.
- Como: Cada dispositivo tem um endereço IP, como se fosse um CEP;
- Problema: Ele não garante que os dados cheguem nem que cheguem na ordem.

🧭Pense no IP como o serviço de entrega dos Correios: ele leva o pacote, mas não garante que chegou corretamente.

---

2.TCP(Transmission Control Protocol) - o "garantidor da entrega"

- Função: Garante que os dados:
  - Cheguem completos;
  - Cheguem na ordem certa;
  - Sejam reenviados de algo falhar.
- Como: Quebra os dados em pacotes, numera cada um e espera a confirmação do recebimento.

✅Pense no TCP como o sistema de rastreamento e confirmação de entrega dos Correios: ele confere se o pacote chegou, senão, reenvia.

---

## 🔗Juntos: TCP/IP

TCP/IP é como um time:

- O IP leva o pacote até o destino;
- O TCP garante que tudo chegue direitinho.

---

## 🧶Exemplo Prático

Você acessa um site como `https://www.google.com.br`:

1. Seu navegador envia uma requisição via TCP/IP;
2. O IP acha o caminho até os servidores do Google;
3. O TCP quebra a mensagem, manda os pacotes e garante que todos sejam recebidos corretamente;
4. O servidor responde da mesma forma;
5. Você vê o site carregado!

---

## ✅Funções do TCP (Transmission Control Protocol)

O TCP é um protcolo de tranportes confiável e orientado a conexão. Suas principais funções são:

1.Estabelecimento de conexão (Three-Way Handshake)

- Antes de transmitir os dados, o TCP cria uma conexão entre o cliente e o servidor;
- usa três etapas:
  - SYN -> Cliente pede a conexão;
  - SYN-ACK -> Servidor aceita;
  - ACK -> Cliente confirma.

---

2.Controle de Fluxo

- Evita que o remetente envie dados mais rápido do que o receptor consegue processar;
- Usa janelas deslizantes (sliding window) para ajustar o volume de dados enviados.

---

3.Controle de Congestionamento

- Detecta e reage a situações em que a rede está congestionada;
- Reduz a taxa de envios para evitar perda de pacotes;
- Algoritmos usados: Slow start, Congestion Avoidance, Fast Retransmit, Fast Recovery;

---

4.Entrega Confiável (Reliable Delivery)

- Garante que todos os pacotes cheguem ao destino e na ordem correta;
- Se algum pacote se perder, o TCP retransmite.

---

5.Numeração de sequência

- Cada byte transmitido tem um número de sequência;
- Isso ajuda a remontar os dados na ordem certa e detectar perdas ou duplicações.

---

6.Reconhecimento (Acknowledgement)

- O receptor envia um ACK confirmando a recepção dos dados;
- Permite saber que os dados chegaram corretamente.

---

7.Detecção e Retransmissão de Pacotes Perdidos

- Usa temporizadores para retransmitir pacotes de um ACK não for recebido a tempo.

---

8.Multiplexação por Portas

- Permite múltiplas conexões simultâneas entre dois dispositivos;
- Cada conexão usa números de porta diferentes (ex: 80 para HTTP, 443 para HTTPS).

---

9.Encerramento da conexão (Four-Way Termination)

- Feita em quatro etapas (FIN e ACK) para garantir o encerramento adequado.

---

## ✅Funções do IP (Internet Protocol)
