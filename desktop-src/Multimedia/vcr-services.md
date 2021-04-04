---
title: Serviços de VCR
description: Serviços de VCR
ms.assetid: 140220f7-df7b-46e2-8374-e1200d873f3b
keywords:
- VISCA (arquitetura de controle do sistema de vídeo)
- VISCA (arquitetura de controle do sistema de vídeo)
- Driver MCI VISCA
- Driver VISCA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d884c38d224182db7eef8db0f0cd80b14e3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822835"
---
# <a name="vcr-services"></a>Serviços de VCR

O Windows fornece serviços de VCR por meio de um driver de dispositivo que é baseado no comando MCI definido para VCRs. Esta seção descreve o driver VISCA (arquitetura de controle do sistema de vídeo) MCI e explica como usá-lo para controlar um videocassete.

O tipo de dispositivo *VCR* controla VCRs. Para obter uma lista dos comandos MCI reconhecidos por dispositivos VCR, consulte [conjunto de comandos VCR](vcr-command-set.md).

## <a name="the-mci-visca-driver"></a>O driver MCI VISCA

O driver MCI VISCA controla o VCRs do Sony VISCA, como o CVD-1000 VDeck. O driver VISCA controla o transporte de fita, os sintonizadores de canal e os canais de entrada e saída de VCR.

## <a name="searching-and-positioning-with-a-vcr"></a>Pesquisando e posicionando com um videocassete

O driver VISCA usa dois métodos para acompanhar a movimentação de fita de vídeo no transporte de fita do VCR: *informações de código de informação* e contadores de *fita*. Informações de código de hora são informações de tempo que foram registradas na fita de vídeo. A maioria dos VCRs permite que os códigos de timesejam registrados sem destruir faixas de áudio e vídeo. Os contadores de fita estimam a quantidade de fitas que viajam além da cabeça da fita para obter uma posição.

As informações de código de tempo e os contadores de fita aumentam à medida que a fita se move do início ao fim. Devido à sua exatidão, o uso de informações de código de informação para posicionar uma fita é quase sempre preferível ao uso de contadores de fita.

Os sinalizadores de comando MCI para especificar informações de posicionamento são expressos como dependências de tempo: "formato de hora", "duração", "de", "para" e "busca". (Além disso, o comando [**status**](status.md) "posição" retorna seu valor de tempo no formato de hora atual.)

O driver VISCA usa o comando [**set**](set.md) "modo de tempo" para selecionar o tipo de posicionamento a ser usado com uma fita de vídeo. Quando o modo de hora é definido como "código de tempo", os comandos **status** "posição" e "formato de **hora" usam** o código de tempo na fita de vídeo. Quando o modo de hora é definido como "Counter", os comandos **status** "posição **" e "** formato de hora" usam contadores.

Um aplicativo pode definir o modo de tempo como "detectar" se não importa que possa haver duas fontes de informações de posição. No modo de detecção, o driver VISCA usa informações de código de erro para posicionamento quando qualquer uma das seguintes condições ocorre:

-   As informações de código de informação estão presentes quando o driver é aberto.
-   Você altera uma fita de vídeo com o comando **set** "Door Open" e as informações de código de informação estão presentes na fita de vídeo.
-   O comando [**set**](set.md) "modo de tempo" é reemitido.

Se não for possível encontrar informações de código de erro, o driver usará os contadores de fita.

Para determinar o método de posicionamento atual, emita o comando [**status**](status.md) "tipo de hora", que retorna "código de tempo" ou "contador". Você também pode identificar o modo de posicionamento atual usando o comando de **status** "modo de tempo", que retorna "Code-time", "Counter" ou "Detect".

O comando de **status** "Counter" recupera o valor do contador de fita atual, independentemente do método de posicionamento atual; no entanto, você pode usar esse contador somente leitura com o comando [**set**](set.md) "Counter".

O driver VISCA pode recuperar o formato de código de tempo nativo registrado em uma fita de vídeo usando os comandos **status** "tipo de código de período" e **status** "taxa de quadros" juntos. Por exemplo, se o tipo de código de tempo for "SMPTE" e a taxa de quadros for 25, o formato de código-chave nativo gravado na fita de vídeo será SMPTE 25.

O driver VISCA também pode recuperar a resolução do contador usando o comando **status** "resolution do contador", que retorna "Seconds" ou "frames". O formato do contador ainda pode ser definido como SMPTE 30, mas o valor de retorno retorna apenas um quadro de 0. Se o tipo de hora atual for Counter, essa resolução também se aplicará ao valor retornado pelo **status** "position".

## <a name="capturing-frames"></a>Capturando quadros

Os comandos de captura de quadros fornecem imagens ainda para um *dispositivo de captura de quadros*. Um dispositivo de captura de quadros é uma peça separada de hardware capaz de ler e armazenar a imagem de vídeo. O driver VISCA dá suporte ao comando [**Freeze**](freeze.md) ([**\_ congelamento MCI**](mci-freeze.md)) para estabilizar uma imagem ainda para captura. Além disso, o comando [**descongelar**](unfreeze.md) ([**MCI \_ descongelar**](mci-unfreeze.md)) pode ser usado para reiniciar o transporte de fita após um comando **Freeze** .

O comando **Freeze** fornece uma imagem de alta qualidade, estabilizada e de base de tempo, corrigida para um dispositivo de captura de quadros. Esse comando existe porque um dispositivo nem sempre pode entregar sua imagem de saída de qualidade máxima durante a reprodução ou enquanto está em pausa; essa imagem de vídeo não é adequada para a captura.

O comando **descongelar** desbloqueia o transporte de fita e retoma o modo de transporte em vigor antes do comando **Freeze** .

Quando seu aplicativo precisar gravar uma imagem de vídeo no VCR, use o comando **congelar** "entrada" ou a [**indicação**](cue.md) ([**\_ indicação MCI**](mci-cue.md)) para gravar a imagem.

## <a name="selecting-inputs"></a>Selecionando entradas

O driver VISCA dá suporte a três tipos de entrada: vídeo, áudio e código de paficação. As entradas de vídeo incluem dois canais padrão (linhas 1 e 2), um canal SVideo, um canal auxiliar e um canal de um sintonizador interno. As entradas de áudio incluem dois canais padrão (linhas 1 e 2) e um canal de um sintonizador interno. A entrada de código de informações é interna ao VCR.

As saídas normais carregam as entradas atualmente selecionadas quando o VCR está gravando ou quando o transporte de fita é interrompido e carregam o conteúdo da fita quando o transporte de fita é reproduzido ou pausado. As saídas monitoradas carregam as mesmas informações que as saídas normais, além das informações atuais do código de tempo e do canal.

Supondo que as entradas externas apropriadas estejam conectadas ao seu VCR e você tenha decidido o que deseja registrar, você pode selecionar as entradas a serem registradas. Por exemplo, para gravar ou exibir no vídeo "SVIDEO" e nas entradas de áudio de "linha 1", você usaria os comandos [**setvideo**](setvideo.md) (MCI de vídeo e [**SetAudio**](setaudio.md) )[**para \_**](mci-setaudio.md)selecionar essas fontes de entrada.[**\_**](mci-setvideo.md) Você pode verificar essas seleções usando o comando [**status**](status.md) ([**\_ status do MCI**](mci-status.md)).

Por padrão, o monitor mostra exatamente o que aparece como a saída. Às vezes, no entanto, talvez você queira exibir uma fonte durante a gravação de outra. Essa é uma prática comum usando o sintonizador. Por exemplo, talvez você queira assistir ao canal 4 enquanto registra o canal 7. Nesse caso, você tem duas entradas de sintonizador lógico. Você pode configurar o VCR usando os seguintes comandos:

## <a name="to-review-one-source-while-recording-from-another"></a>Para examinar uma fonte durante a gravação de outra

1.  Use o comando [**setsintonizador**](settuner.md) ([**MCI \_ setajuster**](mci-settuner.md)) para selecionar os canais a serem observados e registrados.
2.  Use o comando **setvideo** para selecionar a fonte de gravação de vídeo.
3.  Use o comando [**SetAudio**](setaudio.md) para selecionar a fonte de gravação de áudio.
4.  Use o comando [**setvideo**](setvideo.md) para rotear a entrada de vídeo do canal 4 para a saída monitorada para exibi-la na tela.
5.  Use o comando [**SetAudio**](setaudio.md) para rotear a entrada de áudio do canal 4 para a saída monitorada para reproduzir o áudio.
6.  Verifique suas seleções usando o comando [**status**](status.md) .

O driver VISCA também dá suporte a um tipo de entrada especial para áudio e vídeo chamado *mudo*. Mudo permite a seleção de "nenhuma entrada", que é útil ao gravar um sinal em branco.

## <a name="selecting-recording-tracks"></a>Selecionando faixas de gravação

Existem três tipos de faixas de gravação em uma fita: vídeo, áudio e código de paficação. Você tem apenas uma faixa de vídeo ou código de paficação, mas pode usar mais de uma faixa de áudio. Quando você fizer isso, faça o acompanhamento 1 da faixa de áudio principal.

O driver VISCA dá suporte a dois modos de operação: montar e inserir. No *modo de montagem*, todas as faixas são selecionadas para serem registradas. No *modo de inserção*, as faixas podem ser selecionadas independentemente para gravação. A maioria dos VCRs estão no modo de montagem por padrão. Use o comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)) para alterar esses modos.

## <a name="recording-and-editing"></a>Gravação e edição

O comando [**Record**](record.md) ([**\_ registro MCI**](mci-record.md)) fornece uma gravação simples e precisa de aproximadamente 1 segundo da posição inicial. Para registrar-se de forma mais precisa ou se você pretende editar o conteúdo do vídeo ao operar simultaneamente vários baralhos, use o comando [**Cue**](cue.md) ([**\_ indicação MCI**](mci-cue.md)).

O comando de **indicação** prepara o dispositivo para gravação ou reprodução. Use o comando de **indicação** "entrada" para preparar o dispositivo para gravação. O comando de **indicação** é necessário porque um aplicativo deve saber quando o dispositivo está pronto para executar o comando (e porque pode levar vários minutos para se preparar para um comando de [**reprodução**](play.md) ([**\_ reprodução MCI**](mci-play.md)) ou de **registro** ).

O VCR se prepara para gravação ou reprodução ao procurar o *ponto*, que é a posição atual ou a posição especificada usando o comando **Cue** "de". Se o sinalizador "Prevert" for especificado com o comando **Cue** , no entanto, o VCR se posicionará em si mesmo a distância de preposição do ponto em questão. O sinalizador "Prevert" também indica que o VCR usa qualquer modo de edição aplicável, portanto, é importante que você use "Prevert", especialmente quando você quiser a gravação mais precisa. (Use o comando de [**capacidade**](capability.md) ([**MCI \_ GETDEVCAPS**](mci-getdevcaps.md)) com o sinalizador "pode ser prevertido" para verificar se há suporte para o modo de preroll.)

> [!Note]  
> Quando você registra usando as posições "de" e "para", a posição "de" é incluída na edição e a posição "para" não é.

 

Para obter mais informações sobre a gravação, consulte [gravando](recording.md).

## <a name="using-the-clock-while-editing"></a>Usando o relógio durante a edição

Ao editar, talvez você queira registrar segmentos de um videocassete para outro. Você pode começar a gravar em uma hora e posição específicas em um videocassete enquanto outro começa a tocar ao mesmo tempo e posição, especificando uma ação (reproduzir ou gravar), uma posição e um horário para cada VCR.

Ambos os VCRs devem usar o mesmo relógio para esse tipo de edição; o relógio ajuda a sincronizar os dois dispositivos. Você pode determinar se dois VCRs compartilham o mesmo relógio usando o comando [**status**](status.md) ([**\_ status do MCI**](mci-status.md)) com o sinalizador "ID do relógio" para consultar cada VCR. Se os números de identificação retornados pelo comando de **status** forem os mesmos, os dispositivos usarão o mesmo relógio. Como um recurso compartilhado, o relógio pode ser conectado a vários VCRs. O driver VISCA dá suporte a apenas um relógio compartilhado.

Você também pode determinar a resolução do relógio usando o comando **status** "taxa de incremento de relógio". Esse comando retorna o número de incrementos com suporte do relógio por segundo. Por exemplo, se o relógio for atualizado a cada milissegundo, o comando retornará 1000 como a taxa de incremento do relógio. A vantagem de usar a taxa de incremento é que a taxa é expressa como um inteiro; caso contrário, o incremento seria um valor de ponto flutuante (precisão simples ou dupla). Como um inteiro, manipular a taxa de incremento é uma operação simples e não é suscetível a erros de arredondamento. Você pode redefinir o relógio usando o comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)) com o sinalizador "Clock 0" (zero).

Ao emitir um comando [**Play**](play.md) ([**\_ reprodução MCI**](mci-play.md)), [**registro**](record.md) ([**\_ registro MCI**](mci-record.md)) ou [**busca**](seek.md) ([**MCI \_ Seek**](mci-seek.md)), você pode especificar quando o comando deve ser executado. As características do VCRs que está sendo usado determinam quando iniciar cada VCR. O tempo deve considerar a quantidade de cada dispositivo necessária e a quantidade de tempo necessária para concluir os comandos MCI usados para configurar a sessão de edição. Para fazer isso, recupere a hora do relógio e adicione um intervalo de espera de 5 a 10 segundos. (O intervalo de espera deve ser longo o suficiente para permitir que a preversão e os comandos MCI pendentes concluam a execução.)

Para garantir que o período de espera seja longo o suficiente, coloque o comando **gravar** por último no aplicativo e verifique o tempo imediatamente antes dele. Se o intervalo for muito curto, reinicie o comando **Play** . Como alternativa, você pode verificar o tempo imediatamente após o último comando do script para verificar se há tempo suficiente para enviar e concluir todos os comandos.

 

 




