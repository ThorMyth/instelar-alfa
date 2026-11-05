# Como testar o Instelar (alfa)

O Instelar é um editor de vídeo em que quem edita é um agente de IA: você pede no chat ("faz um Reel de até 45 s com a melhor parte, com legenda") e acompanha na tela. Ele é feito para Reels, Stories, Shorts, TikTok e YouTube.

Esta é uma versão alfa, de teste. Vai ter coisa errada, e é para isso que você está aqui: quando algo travar, sair feio ou faltar, anote (como fazer está mais abaixo).

## Antes de começar

**O que você precisa:**
- Windows 10 ou 11, de 64 bits (até agora, só testado no 11: se você usa o 10, conta como foi);
- pelo menos 15 GB livres no disco (20 GB com placa NVIDIA);
- uma conta paga do Claude ou do ChatGPT. Use a sua: cada Reel gasta uma parte do limite do seu plano. Se preferir, dá para usar uma chave de API da Anthropic, em ⚙ Configurações;
- um vídeo seu com fala, de 1 a 10 minutos.

Uma placa NVIDIA com 4 GB ou mais deixa tudo mais rápido, mas não é obrigatória. Sem ela, o app funciona pelo processador, com a análise do vídeo e o export mais lentos.

**O que sai do seu computador:**
- Os vídeos e projetos ficam no seu computador, e o app não tem servidor nenhum.
- Para editar, o agente recebe o texto do que é falado e algumas imagens de quadros do vídeo. Isso vai para o Claude ou o ChatGPT, na sua conta, como numa conversa normal com eles. Se um vídeo não pode sair daí nem assim, não use ele no teste.

## Instalar

1. Baixe o instalador (cerca de 650 MB) na [página da versão mais recente](https://github.com/ThorMyth/instelar-alfa/releases/latest): é o arquivo `Instelar-…-setup.exe`. Depois, abra.
2. O Windows vai avisar que protegeu o computador, porque esta versão ainda não tem assinatura digital. Clique em **Mais informações** e depois em **Executar assim mesmo**.
3. Clique em **Instalar** e, no fim, em **Concluir**. Leva cerca de 3 minutos.
4. Na primeira abertura, o app pergunta como processar os vídeos:
   - **Com a placa NVIDIA** baixa cerca de 10 GB;
   - **Só com a CPU** baixa cerca de 5 GB.

   Pode levar de alguns minutos a meia hora, e só acontece uma vez. Se a internet cair ou você fechar o app, ele continua de onde parou.
5. Entre com a sua conta: clique em **Entrar** no Claude ou no ChatGPT. O navegador abre; se ele mostrar um código, cole na janela do app.

## Seu primeiro Reel

1. Em **Novo projeto**, dê um nome, escolha **9:16** e crie o projeto.
2. Na aba **Mídia**, clique em **Importar…** (ou solte o vídeo na janela). Espere as análises: os selos ao lado do arquivo mostram o que já ficou pronto.
3. Na aba **Chat**, peça:

   > Faz um Reel de até 45 s com a melhor parte desse vídeo, com legenda e sem as pausas longas.

4. Acompanhe. O agente leva alguns minutos e mostra o que está fazendo. No fim, aparece um cartão com o resumo e os pontos para você conferir.
5. Assista no preview. Gostou, clique em **Aplicar**. Não gostou, clique em **Descartar**, ou peça a mudança no chat.
6. Clique em **⬆ Exportar** (no alto, à direita), marque **Reels** e clique em **Exportar**. O arquivo fica na pasta `exports` do projeto.

## O que testar

Faça o que fizer sentido para os seus vídeos. Se puder, use um vídeo diferente em cada pedido.

| Experimente | Exemplo de pedido |
|---|---|
| Stories | "Transforma em Stories com a parte mais interessante, em partes de até 60 s" |
| Vários cortes | "Acha os 3 melhores momentos e faz um Short de cada" |
| Ajustes depois | "Deixa a legenda maior", "tira a parte em que eu falo do preço", "começa direto na frase da pergunta" |
| Som | "Melhora o som da minha voz", "tira os silêncios e os 'é...'" |
| Visual | "Põe um título no começo", "dá um zoom quando eu falar o número", "acerta a cor" |
| Editar pelo texto | Na aba **Texto**, clique na primeira palavra, `Shift`+clique na última e aperte `Delete` para cortar. `Enter` sobre o trecho riscado traz de volta |
| Mexer à mão | Arraste as bordas de um clipe na timeline. `Ctrl+Z` desfaz tudo, inclusive o que o agente fez |

**O que mais ajuda saber:**
- O resultado ficou bom o bastante para postar? Se não, o que faltou?
- Quantas vezes você precisou corrigir o agente?
- Quanto tempo levou, do início ao vídeo exportado?
- Em que momento você ficou sem saber o que fazer?

## Como anotar e mandar

**Anotar:** clique em **📝** na barra superior (ou `Ctrl+Shift+A`) e escreva o que aconteceu e o que você esperava. O app guarda a nota com uma captura da janela.

**Mandar:** clique em **Gerar relatório** (no 📝, na tela inicial ou nas configurações em ⚙). Ele cria um arquivo `.zip` e abre a pasta. Mande esse arquivo para quem te convidou. O app não envia nada sozinho.

**O que vai no relatório:**
- suas notas dos últimos 14 dias, com as capturas. Elas mostram a janela, inclusive o quadro do vídeo que estava aberto;
- os registros do que o app e o agente fizeram, que podem trazer trechos da fala do vídeo;
- a versão do app e os dados da máquina (placa, memória, disco).

Vídeos, projetos, senhas e chaves não vão.

## Se algo der errado

- **O agente errou uma palavra:** ele não ouve o áudio. Ele lê a transcrição e vê quadros do vídeo, então nomes e gírias podem sair trocados. Ele costuma avisar o que você deve conferir, e dá para corrigir no chat.
- **Está lento:** sem placa NVIDIA, a análise e o export levam mais tempo, e a fila mostra quanto falta. O selo **CPU** no alto diz que é esse o modo.
- **O Windows ou o antivírus reclamou:** esta versão não tem assinatura digital. Se o antivírus bloquear o app, avise quem te convidou.
- **"A engine parou" ou a janela travou:** feche e abra de novo. Seu projeto fica salvo a cada passo. Depois, clique em **Gerar relatório** na tela inicial e mande o arquivo.
- **O agente diz que você não está logado:** abra ⚙ e clique em **Entrar**.

## Atualizações e desinstalar

**Versão nova:** se aparecer **Reiniciar para atualizar** na barra superior, clique quando puder. O app fecha, instala e abre de novo sem você clicar em nada, e os projetos ficam como estão. Costuma levar de 2 a 4 minutos. Com um jogo ou um antivírus aberto, pode levar alguns minutos a mais. Se aparecer um aviso de que o app não pôde ser fechado, feche o jogo e clique para tentar de novo, ou cancele: o app volta na versão antiga e tenta de novo depois.

**Para tirar o app:** use **Configurações do Windows → Aplicativos**. Para liberar também o espaço da análise de vídeo (5 a 10 GB), apague a pasta `%LOCALAPPDATA%\Instelar`. Seus projetos ficam na pasta que você escolheu ao instalar (por padrão, `Vídeos\Instelar`).

## Sobre este repositório

Aqui ficam só os instaladores e as atualizações do alfa fechado do Instelar, para quem foi convidado. O código do app não está aqui.

O Instelar é um projeto independente, sem ligação com a Anthropic ou com a OpenAI. Cada pessoa usa a própria conta ou chave.

**Licenças:** o app leva programas de terceiros, cada um com a própria licença. Os avisos ficam em `resources\licencas`, na pasta do app instalado. O código-fonte do FFmpeg (GPL-3.0) está em [fontes-ffmpeg-9a01c1cb6a](https://github.com/ThorMyth/instelar-alfa/releases/tag/fontes-ffmpeg-9a01c1cb6a). Quem usar o Instelar em nome de uma empresa com mais de 3 pessoas precisa da licença de empresa do [Remotion](https://www.remotion.dev/docs/license).
