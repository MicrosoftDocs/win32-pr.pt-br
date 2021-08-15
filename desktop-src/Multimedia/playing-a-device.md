---
title: Como tocar um dispositivo
description: Como tocar um dispositivo
ms.assetid: 48d83e06-9e6e-498b-ad9b-0b66f235db25
keywords:
- MCI_PLAY comando
- Janela de reprodução MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9efc06b3d5f33dfb798aa4c47bf7d5a7a8bab45842de1da170c860d2a4a5f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372637"
---
# <a name="playing-a-device"></a>Como tocar um dispositivo

O [**comando play**](play.md) ([**MCI \_ PLAY**](mci-play.md)) começa a reproduzir um dispositivo. Sem sinalizadores, esse comando começa a ser reproduzindo da posição atual e reproduz até que o comando seja interrompido ou até que o final da mídia ou do arquivo seja atingido. Após a reprodução, a posição atual está no final da mídia. Você também pode usar o [**comando seek**](seek.md) ([**MCI \_ SEEK**](mci-seek.md)) para alterar a posição atual.

A maioria dos dispositivos que são **compatíveis** com o comando play também é compatível com os sinalizadores "from" (MCI FROM) e \_ "to" (MCI \_ TO). Esses sinalizadores indicam a posição na qual o dispositivo deve iniciar e parar de tocar. Por exemplo, o comando a seguir reproduz um disco de áudio cd do início da primeira faixa usando a [**função mciSendString:**](/previous-versions//dd757161(v=vs.85))


```C++
mciSendString("play cdaudio from 0", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



Alguns tipos de dispositivo estendem esse comando para explorar as funcionalidades de um dispositivo específico. Por exemplo, o comando [**play**](play.md) para o tipo de dispositivo **videodisc** inclui os sinalizadores "rápido" (MCI \_ \_ VD PLAY \_ FAST), "slow" (MCI \_ VD PLAY SLOW) e \_ \_ "scan" (MCI \_ VD PLAY \_ \_ SCAN).

> [!Note]  
> As unidades atribuídas ao valor de posição dependem do formato de tempo usado pelo dispositivo. Cada dispositivo tem um formato de hora padrão, mas você deve especificar o formato de hora usando o comando [**set**](set.md) ([**MCI \_ SET**](mci-set.md)) antes de emissão de comandos que usam valores de posição.

 

## <a name="playing-an-avi-file"></a>Como tocar um arquivo AVI

Os arquivos de Windows são feitos de pelo menos dois fluxos de dados intercalados: um fluxo de vídeo (pictorial) e um fluxo de áudio. Você pode reproduzir facilmente esses arquivos INTERcalados (AVI) de áudio-vídeo usando comandos MCI. As seções a seguir discutem a reprodução de arquivos AVI.

## <a name="setting-up-an-mciavi-playback-window"></a>Configurando uma janela de reprodução MCIAVI

Seu aplicativo pode especificar as seguintes opções para definir a janela de reprodução para reproduzir um arquivo AVI:

-   Use a janela pop-up padrão do driver MCIAVI.
-   Especifique uma janela pai e um estilo de janela que o driver MCIAVI pode usar para criar a janela de reprodução.
-   Especifique uma janela de reprodução para o driver MCIAVI a ser usado para reprodução.
-   Reproduza o arquivo AVI em uma exibição de tela inteira.

Se o aplicativo não especificar nenhuma opção de janela, o driver MCIAVI criará uma janela padrão para a reprodução da sequência. O driver cria essa janela de reprodução para o comando aberto [**(**](open.md) [**MCI \_ OPEN**](mci-open.md)), mas não exibe a janela até que seu aplicativo envie um comando para exibir a janela ou reproduzir o arquivo. Essa janela de reprodução padrão é uma janela pop-up com uma borda deizing, uma barra de título, um quadro espesso, um **menu** de janela e um botão Minimizar.

Seu aplicativo também pode especificar um alça de janela pai e um estilo de janela quando ele emite o **comando** open. Nesse caso, o driver MCIAVI cria uma janela com base nessas especificações em vez da janela pop-up padrão. Seu aplicativo pode especificar qualquer estilo de janela disponível para a [função CreateWindow.](/windows/win32/api/winuser/nf-winuser-createwindowa) Estilos que exigem uma janela pai, como WS \_ CHILD, devem incluir um alça de janela pai.

Seu aplicativo também pode criar sua própria janela e fornecer o handle para o driver MCIAVI usando o comando [**window**](window.md) ([**MCI \_ WINDOW**](mci-window.md)). O driver MCIAVI usa essa janela em vez de criar uma própria.

Quando o driver MCIAVI cria a janela de reprodução ou obtém uma alça de janela do aplicativo, ele não exibe a janela até que seu aplicativo reproduza a sequência ou envie um comando para exibir a janela. Seu aplicativo pode usar o **comando de** janela para exibir a janela sem a reprodução da sequência. Por exemplo, o comando a seguir exibe a janela usando [**mciSendString**](/previous-versions//dd757161(v=vs.85)):


```C++
mciSendString("window movie state show", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



Neste exemplo, "movie" é um alias para o dispositivo de vídeo digital.

Seu aplicativo também pode reproduzir um arquivo AVI em tela inteira. Para reproduzir a tela inteira, modifique o comando [**play**](play.md) ([**MCI \_ PLAY**](mci-play.md)) com o sinalizador "fullscreen" (MCI \_ MCIAVI \_ PLAY \_ FULLSCREEN). Quando seu aplicativo usa esse sinalizador, o driver MCIAVI usa um formato de tela inteira de 320 por 240 pixels para a reprodução da sequência. Por exemplo, o comando a seguir reproduz o arquivo aberto em tela inteira (usando "movie" como um alias):


```C++
mciSendString("play movie fullscreen", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



## <a name="changing-the-playback-state-for-an-avi-file"></a>Alterando o estado de reprodução de um arquivo AVI

Seu aplicativo pode usar o comando [**seek**](seek.md) ([**MCI \_ SEEK**](mci-seek.md)) para mover a posição atual para o início, o final ou uma posição arbitrária em um arquivo AVI. Há dois modos de busca para o driver MCIAVI: exato e inexato. Seu aplicativo pode alterar o modo de busca usando o [**comando set**](set.md) ([**MCI \_ SET**](mci-set.md)). Quando você usa **definir** "buscar exatamente em", o driver MCIAVI busca exatamente o quadro especificado pelo aplicativo. Isso poderá causar um atraso se o arquivo for compactado temporalmente e seu aplicativo não especificar um quadro-chave. Quando você usa **definir** "buscar exatamente off", o driver MCIAVI busca o quadro-chave mais próximo em um arquivo compactado temporalmente.

Alguns comandos MCI permitem que seu aplicativo altere a reprodução de um arquivo AVI de outras maneiras. Por exemplo, um arquivo AVI, por padrão, é reproduzida em sua velocidade normal, mas seu aplicativo pode aumentar ou diminuir essa velocidade usando o sinalizador de "velocidade" com o **comando set.** Para arquivos AVI, um valor de velocidade de 1000 é típico. Portanto, para reproduzir um filme com a metade de sua velocidade típica, seu aplicativo pode usar o conjunto de comandos **"velocidade** de filme 500"; como alternativa, ele pode usar **definir** "velocidade de filme 2000" para reproduzir a sequência em duas vezes sua velocidade normal.

O [**comando setaudio**](setaudio.md) ([**MCI \_ SETAUDIO**](mci-setaudio.md)) permite que seu aplicativo controle a parte de áudio de um arquivo AVI. Seu aplicativo pode mudo de áudio durante a reprodução ou, no caso de vários arquivos de fluxo de áudio, selecione o fluxo de áudio que é reproduzir.

O driver MCIAVI tem uma caixa de diálogo para controlar algumas de suas opções de reprodução. Algumas das opções disponíveis para o usuário incluem selecionar reprodução de tela inteira ou orientada a janela, selecionar o modo de busca e ampliar a imagem. Seu aplicativo pode fazer com que o MCIAVI exibe essa caixa de diálogo usando o [**comando configurar**](configure.md) ([**MCI \_ CONFIGURE**](mci-configure.md)).

## <a name="stream-handlers"></a>Manipuladores de fluxo

Os dados em um arquivo AVI são tratados como uma série de fluxos. Um arquivo AVI normalmente contém um fluxo de áudio e vídeo e também pode haver um fluxo personalizado que contém texto ou alguns outros dados personalizados. O driver MCIAVI pode usar manipuladores diferentes para esses fluxos de dados. Para obter mais informações sobre arquivos AVI personalizados, consulte [Manipuladores de arquivo e fluxo personalizados.](custom-file-and-stream-handlers.md)

 

 