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
3. Na aba **Chat**, peça tudo numa mensagem só, do jeito que você falaria:

   > Faz um Reel de até 45 s com a melhor parte desse vídeo, com legenda amarela no meio da tela, sem as pausas longas e com uma música calma baixinha.

   O agente monta um plano com cada item que você pediu e confere um por um antes de terminar. Ele corta seco (sem transição nem efeito entre os cortes), a menos que você peça.

4. Acompanhe. O agente leva alguns minutos e mostra o que está fazendo. No fim, aparece um cartão com o resumo e os pontos para você conferir.
5. Assista no preview. Gostou, clique em **Aplicar**. Não gostou, clique em **Descartar**, ou peça a mudança no chat.
6. Clique em **⬆ Exportar** (no alto, à direita), escolha **Reels, TikTok e Shorts** (um arquivo que serve nas três) e clique em **Exportar**. A tela mostra onde o vídeo vai ficar e, no fim, **▶ Abrir o vídeo** e **Mostrar na pasta**. As outras opções (várias sequências, só uma rede, a legenda em arquivo) ficam em **Mais opções**.

**Para navegar:** `Home` e `End` (ou ⏮ e ⏭ embaixo do vídeo) levam ao começo e ao fim; `+` e `-` dão zoom em volta da agulha. Os botões **+ @0:15** e **+ seleção** no chat mandam o momento ou os clipes marcados junto com o pedido: ficam desligados até você ligar.

## Onde ficam o vídeo e o projeto

- **O projeto se salva sozinho**, a cada mudança: não existe botão de salvar. Cada projeto é uma pasta em `Vídeos\Instelar`, com o nome dele e `.instelar` no fim (por exemplo, `Vídeos\Instelar\Rotina da manhã.instelar`).
- **O vídeo exportado** fica dentro dela, na pasta `exports` (`Vídeos\Instelar\Rotina da manhã.instelar\exports`). Para achar rápido: **⬆ Exportações**, no alto, lista todos os vídeos exportados do projeto, mesmo depois de fechar o app, com **▶ Abrir o vídeo** e **Mostrar na pasta**; ou clique no nome do projeto, no alto à esquerda, e em **Abrir a pasta dos vídeos exportados**. Exportar de novo um vídeo que não mudou devolve o mesmo arquivo na hora.
- **Para voltar a um projeto:** abra o app. A tela inicial mostra todos os seus projetos, do mais recente para o mais velho; clique no que quiser. Se ele estiver em outra pasta, use **Abrir outro projeto…** e escolha a pasta dele (a que termina em `.instelar`).
- O vídeo que você importou não é copiado para o projeto: o projeto aponta para ele. Se você mover ou apagar o vídeo original, o projeto perde esse arquivo.

## O que testar

Faça o que fizer sentido para os seus vídeos. Se puder, use um vídeo diferente em cada pedido.

| Experimente | Exemplo de pedido |
|---|---|
| Stories | "Faz um Story com o melhor momento" (sai um trecho de até 30 s; "em 10 segundos" para um mais curto; "o vídeo inteiro nos Stories" manda tudo, em partes de até 60 s) |
| Vários cortes | "Acha os 3 melhores momentos e faz um Short de cada" |
| Ajustes depois | "Deixa a legenda maior", "tira a parte em que eu falo do preço", "começa direto na frase da pergunta" |
| Som | "Melhora o som da minha voz", "tira os silêncios e os 'é...'" |
| Visual | "Põe um título no começo", "dá um zoom quando eu falar o número", "acerta a cor" (cor estourada ele corrige sozinho; para uma cor só: "tira um pouco do vermelho") |
| Da internet | "Põe o logo do Nubank no canto", "coloca um som de whoosh na entrada do título", "uma foto de grãos de café quando eu falar do café". As imagens e sons vêm do Openverse, com licença livre; o que pede crédito vai num arquivo `.creditos.txt` ao lado do vídeo exportado. Dá para desligar em ⚙ › Internet |
| Criar | Com o ChatGPT (o Codex) no chat: "cria uma figurinha de uma xícara de café e põe no canto". A imagem é gerada na sua conta do ChatGPT e fica na pasta do projeto |
| Cabelo | Selecione um clipe e, no **Inspector**, seção **Cabelo**, clique em **Tirar o frizz** (ou peça "tira o frizz do cabelo"). Funciona melhor com fundo liso |
| Versões | "Me mostra 3 estilos de legenda". Uma barra **Versões** aparece em cima do vídeo: clique em cada uma para ver e em **Escolher esta** |
| Antes e depois | Depois de uma edição da IA, **Antes│Depois** embaixo do vídeo (ou `Shift+\`) mostra como estava; `\` alterna |
| Legenda à mão | Na aba **Legendas**, dê dois cliques numa página (ou na legenda em cima do vídeo) para corrigir o texto e aperte `Enter`. Ali também ficam os estilos (clique num deles: Caixa na palavra, Palavra pulando, Neon…), a cor, o tamanho e a posição (Em cima, No meio, Embaixo); escolha palavras e clique em **Destacar**. Ou peça: "coloca uma legenda moderna" |
| Títulos e artes | "Põe o título '3 erros da rotina' no centro com a palavra erros em destaque", "uma manchete no começo", "mostra a pergunta da Maria num balão" |
| Aparência | Em ⚙ Configurações › **Aparência**, escolha a cor do app (Azul, Violeta, Rosa, Verde-água, Âmbar, Coral, Prata) e quanto o céu se mexe (**Efeitos**: Automático, Completos, Leves, Mínimos). Num computador mais lento, **Leves** ou **Mínimos** deixam tudo mais leve |
| Onde salvar | No export, em **Onde salvar**: o nome do arquivo e **Escolher pasta…** (o app lembra a de cada projeto), ou **Salvar como…** para escolher tudo na janela do Windows. **Perguntar onde salvar a cada export** faz o app perguntar sempre |
| Editar pelo texto | Na aba **Texto**, clique na primeira palavra, `Shift`+clique na última e aperte `Delete` para cortar. `Enter` sobre o trecho riscado traz de volta |
| Mexer à mão | Os atalhos são os do Premiere (o botão **⌨ Atalhos**, embaixo do vídeo, mostra todos): `Ctrl+K` corta no playhead, `C` é a navalha, `Shift+Delete` apaga e junta. A barra em cima da timeline tem **Cortar**, **Apagar** e **Apagar e juntar**. Arraste as bordas de um clipe para aparar. `Ctrl+Z` desfaz tudo, inclusive o que o agente fez |

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

**Versão nova:** o app procura sozinho ao abrir e a cada hora e vai sempre direto para a versão mais nova, qualquer que seja a sua, baixando só o que mudou. Quando ela fica pronta, aparece o botão verde **Atualizar agora**, no alto ou na tela inicial (até a alpha.5, ele se chamava **Reiniciar para atualizar**). Clique quando puder: o app fecha, instala e abre de novo sozinho, em 2 a 4 minutos, e os projetos ficam como estão. Depois de cada atualização, aparece uma tela com as novidades: o que mudou desde a sua versão. Para ver de novo, clique em **Novidades**, no rodapé da tela inicial. Se você não clicar, a versão nova instala quando você fechar o app. Para procurar na hora, use **Procurar atualizações**, no rodapé da tela inicial ou em ⚙ › Sobre. Com um jogo ou um antivírus aberto, a instalação pode levar alguns minutos a mais; se não der, o app abre na versão antiga e tenta de novo depois.

**Para tirar o app:** use **Configurações do Windows → Aplicativos**. Para liberar também o espaço da análise de vídeo (5 a 10 GB), apague a pasta `%LOCALAPPDATA%\Instelar`. Seus projetos ficam na pasta que você escolheu ao instalar (por padrão, `Vídeos\Instelar`).

## Sobre este repositório

Aqui ficam só os instaladores e as atualizações do alfa fechado do Instelar, para quem foi convidado. O código do app não está aqui.

O Instelar é um projeto independente, sem ligação com a Anthropic ou com a OpenAI. Cada pessoa usa a própria conta ou chave.

**Licenças:** o app leva programas de terceiros, cada um com a própria licença. Os avisos ficam em `resources\licencas`, na pasta do app instalado. O código-fonte do FFmpeg (GPL-3.0) está em [fontes-ffmpeg-9a01c1cb6a](https://github.com/ThorMyth/instelar-alfa/releases/tag/fontes-ffmpeg-9a01c1cb6a). Quem usar o Instelar em nome de uma empresa com mais de 3 pessoas precisa da licença de empresa do [Remotion](https://www.remotion.dev/docs/license).
