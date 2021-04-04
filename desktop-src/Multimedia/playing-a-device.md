---
title: Reproduzindo um dispositivo
description: Reproduzindo um dispositivo
ms.assetid: 48d83e06-9e6e-498b-ad9b-0b66f235db25
keywords:
- MCI_PLAY comando
- Janela de reprodução do MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73d8b6539e842a1ffa632ed1efae5c2c8d3cda1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917303"
---
# <a name="playing-a-device"></a>Reproduzindo um dispositivo

O comando [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)) começa a reproduzir um dispositivo. Sem nenhum sinalizador, esse comando inicia a reprodução a partir da posição atual e é reproduzido até que o comando seja interrompido ou até que o final da mídia ou do arquivo seja atingido. Após a reprodução, a posição atual é no final da mídia. Você também pode usar o comando [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)) para alterar a posição atual.

A maioria dos dispositivos que dão suporte ao comando **Play** também oferece suporte aos sinalizadores "de" (MCI \_ de) e "para" (MCI \_ para). Esses sinalizadores indicam a posição na qual o dispositivo deve iniciar e parar de executar. Por exemplo, o comando a seguir reproduz um disco de áudio de CD do início da primeira faixa usando a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :


```C++
mciSendString("play cdaudio from 0", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Alguns tipos de dispositivo estendem esse comando para explorar os recursos de um dispositivo específico. Por exemplo, o comando [**Play**](play.md) para o tipo de dispositivo **VIDEODISC** inclui os sinalizadores "Fast" (MCI de \_ VD \_ Play \_ Fast), "lento" (MCI de \_ VD de \_ reprodução \_ lenta) e "verificação" (MCI de \_ reprodução de VD \_ \_ ).

> [!Note]  
> As unidades atribuídas ao valor de posição dependem do formato de hora usado pelo dispositivo. Cada dispositivo tem um formato de hora padrão, mas você deve especificar o formato de hora usando o comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)) antes de emitir comandos que usam valores de posição.

 

## <a name="playing-an-avi-file"></a>Reprodução de um arquivo AVI

Os arquivos de vídeo no Windows são compostos por pelo menos dois fluxos de dados intercalados: um fluxo de vídeo (ilustração) e um fluxo de áudio. Você pode facilmente reproduzir esses arquivos AVI (áudio-vídeo intercalados) usando comandos MCI. As seções a seguir discutem a reprodução de arquivos AVI.

## <a name="setting-up-an-mciavi-playback-window"></a>Configurando uma janela de reprodução do MCIAVI

Seu aplicativo pode especificar as seguintes opções para definir a janela de reprodução para reproduzir um arquivo AVI:

-   Use a janela pop-up padrão do driver MCIAVI.
-   Especifique uma janela pai e o estilo de janela que o driver MCIAVI pode usar para criar a janela de reprodução.
-   Especifique uma janela de reprodução para o driver MCIAVI usar para reprodução.
-   Reproduza o arquivo AVI em uma exibição de tela inteira.

Se o seu aplicativo não especificar nenhuma opção de janela, o driver MCIAVI criará uma janela padrão para reproduzir a sequência. O driver cria essa janela de reprodução para o comando [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)), mas não exibe a janela até que seu aplicativo envie um comando para exibir a janela ou executar o arquivo. Essa janela de reprodução padrão é uma janela pop-up com uma borda de dimensionamento, barra de título, um quadro espesso, um menu de **janela** e um botão minimizar.

Seu aplicativo também pode especificar um identificador de janela pai e um estilo de janela quando ele emite o comando **abrir** . Nesse caso, o driver MCIAVI cria uma janela com base nessas especificações em vez da janela pop-up padrão. Seu aplicativo pode especificar qualquer estilo de janela disponível para a função [CreateWindow](/windows/win32/api/winuser/nf-winuser-createwindowa) . Os estilos que exigem uma janela pai, como WS \_ Child, devem incluir um identificador de janela pai.

Seu aplicativo também pode criar sua própria janela e fornecer o identificador para o driver MCIAVI usando o comando [**Window**](window.md) ([**\_ janela MCI**](mci-window.md)). O driver MCIAVI usa essa janela em vez de criar uma por conta própria.

Quando o driver MCIAVI cria a janela de reprodução ou Obtém um identificador de janela do seu aplicativo, ele não exibe a janela até que o aplicativo reproduza a sequência ou envie um comando para exibir a janela. Seu aplicativo pode usar o comando **Window** para exibir a janela sem reproduzir a sequência. Por exemplo, o comando a seguir exibe a janela usando [**mciSendString**](/previous-versions//dd757161(v=vs.85)):


```C++
mciSendString("window movie state show", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



Neste exemplo, "filme" é um alias para o dispositivo de vídeo digital.

Seu aplicativo também pode reproduzir um arquivo AVI de tela inteira. Para reproduzir a tela inteira, modifique o comando [**Play**](play.md) ([**MCI \_ Play**](mci-play.md)) com o sinalizador "tela inteira" (MCI \_ Mciavi \_ Play \_ fullscreen). Quando seu aplicativo usa esse sinalizador, o driver MCIAVI usa um formato de tela inteira de 240 pixels de 320 a para reproduzir a sequência. Por exemplo, o comando a seguir reproduz o arquivo aberto de tela inteira (usando "filme" como um alias):


```C++
mciSendString("play movie fullscreen", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



## <a name="changing-the-playback-state-for-an-avi-file"></a>Alterando o estado de reprodução de um arquivo AVI

Seu aplicativo pode usar o comando [**Seek**](seek.md) ([**MCI \_ Seek**](mci-seek.md)) para mover a posição atual para o início, o fim ou uma posição arbitrária em um arquivo avi. Há dois modos de busca para o driver MCIAVI: Exact e Exact. Seu aplicativo pode alterar o modo de busca usando o comando [**set**](set.md) ([**MCI \_ set**](mci-set.md)). Quando você usa **set** "Seek exactly on", o driver Mciavi busca exatamente o quadro que seu aplicativo especifica. Isso pode causar um atraso se o arquivo for compactado de temporal e seu aplicativo não especificar um quadro-chave. Quando você usa **set** "Seek exactly off", o driver Mciavi busca o quadro de chave mais próximo em um arquivo compactado de forma temporal.

Alguns comandos MCI permitem que seu aplicativo altere a reprodução de um arquivo AVI de outras maneiras. Por exemplo, um arquivo AVI, por padrão, é reproduzido em sua velocidade normal, mas seu aplicativo pode aumentar ou diminuir essa velocidade usando o sinalizador "Speed" com o comando **set** . Para arquivos AVI, um valor de velocidade de 1000 é típico. Portanto, para reproduzir um filme na metade de sua velocidade típica, seu aplicativo pode usar o **conjunto** de comandos "velocidade de filme 500"; Como alternativa, ele pode usar **set** "velocidade de filme 2000" para reproduzir a sequência em duas vezes sua velocidade normal.

O comando [**SetAudio**](setaudio.md) ([**MCI de \_ áudio**](mci-setaudio.md)) permite que seu aplicativo controle a parte de áudio de um arquivo avi. Seu aplicativo pode ativar mudo de áudio durante a reprodução ou, no caso de vários arquivos de fluxo de áudio, selecionar o fluxo de áudio que é reproduzido.

O driver MCIAVI tem uma caixa de diálogo para controlar algumas das suas opções de reprodução. Algumas das opções disponíveis para o usuário incluem seleção de reprodução orientada a janelas ou de tela inteira, seleção do modo de busca e zoom da imagem. Seu aplicativo pode fazer com que o MCIAVI exiba essa caixa de diálogo usando o comando [**Configurar**](configure.md) ([**MCI \_ Configurar**](mci-configure.md)).

## <a name="stream-handlers"></a>Manipuladores de fluxo

Os dados em um arquivo AVI são tratados como uma série de fluxos. Um arquivo AVI normalmente contém um fluxo de áudio e vídeo, e também pode haver um fluxo personalizado que contém texto ou outros dados personalizados. O driver MCIAVI pode usar manipuladores diferentes para esses fluxos de dados. Para obter mais informações sobre arquivos AVI personalizados, consulte [manipuladores de arquivo e fluxo personalizados](custom-file-and-stream-handlers.md).

 

 