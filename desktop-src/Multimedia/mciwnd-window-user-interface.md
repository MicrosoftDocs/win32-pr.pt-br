---
title: Interface do usuário da janela do MCIWnd
description: Interface do usuário da janela do MCIWnd
ms.assetid: 422c5acb-bce5-4be2-96ba-5ab7f9dcc826
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c98c0b11b6868828625c6c6e605f005fe842d669
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005134"
---
# <a name="mciwnd-window-user-interface"></a>Interface do usuário da janela do MCIWnd

O MCIWnd fornece recursos adicionais para ajustar a aparência da janela MCIWnd, personalizar o comportamento do seu aplicativo e ajustar o desempenho da reprodução. Os seguintes recursos estão incluídos na janela MCIWnd:

-   Uma barra de ferramentas com botões **reproduzir**, **parar**, **gravar** e **menu**
-   Um TrackBar que controla o posicionamento dentro do conteúdo de reprodução
-   Um menu pop-up contendo comandos comuns
-   Uma área de reprodução para vídeo e outros dispositivos que exibem imagens

A ilustração a seguir mostra o estado inicial da reprodução de vídeo controlada pelo usuário. O arquivo de exemplo usado é CLOCK.AVI.

![clock.avi imagem](images/mciwnd1.gif)

A janela MCIWnd inclui uma área de reprodução para vídeo e outros dispositivos que exibem imagens durante a reprodução. MCIWnd omite a área de reprodução de dispositivos de onda-áudio, seqüenciadores MIDI e outros dispositivos que não gravam na exibição. A ilustração a seguir mostra a área de reprodução de wave-áudio.

![imagem da janela MCIWnd](images/mciwnd4.gif)

O botão **Play** está localizado no canto inferior esquerdo da janela MCIWnd. Ele aparece quando o conteúdo é interrompido. O usuário pode reproduzir o conteúdo das seguintes maneiras:

-   Para reproduzir o conteúdo da posição de reprodução atual, selecione o botão **reproduzir** .
-   Para reproduzir o conteúdo em tela inteira da posição de reprodução atual, selecione o botão **reproduzir** enquanto mantém a tecla Ctrl pressionada.
-   Para reproduzir o conteúdo para trás da posição de reprodução atual, selecione o botão **reproduzir** enquanto mantém a tecla Shift pressionada.

O botão de **menu** , localizado ao lado do botão **reproduzir** , ativa um menu que permite ao usuário abrir e fechar arquivos AVI (áudio-video intercalado) e ajustar o tamanho da imagem, a velocidade de reprodução e o volume. (O usuário também pode ativar o menu clicando com o botão direito do mouse sempre que o cursor estiver na área do cliente da janela.) O menu também inclui comandos para alterar a configuração do dispositivo atual, para copiar o conteúdo de reprodução para a área de transferência e para emitir comandos MCI.

O TrackBar à direita do botão de **menu** representa a duração do conteúdo de reprodução (ou gravado). O controle deslizante no TrackBar representa a posição de reprodução atual dentro do conteúdo. Quando o controle deslizante está posicionado na extremidade esquerda do TrackBar, a posição de reprodução atual é o início do conteúdo. O usuário pode mudar para locais diferentes no conteúdo, arrastando o controle deslizante ao longo do TrackBar. O botão **parar** está localizado no canto inferior esquerdo da janela MCIWnd. Ele aparece quando o conteúdo é reproduzido. A ilustração a seguir mostra a reprodução de vídeo em andamento.

![imagem de reprodução de vídeo](images/mciwnd2.gif)

Os controles MCIWnd também podem incluir um botão de **registro** para dispositivos que podem ser registrados. O botão **gravar** é marcado com um círculo vermelho e aparece somente quando o dispositivo é capaz de gravar.

> [!Note]  
> A janela de reprodução deve estar alinhada a um limite de quatro pixels para obter o melhor desempenho de reprodução de vídeo. Normalmente, o Windows alinha a janela automaticamente quando ela é criada. Se um usuário mover ou alongar a janela de sua posição inicial, a velocidade de reprodução do vídeo poderá ser reduzida pela metade.

 

 

 




