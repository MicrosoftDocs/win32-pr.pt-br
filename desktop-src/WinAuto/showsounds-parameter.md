---
title: Mostrar sons (e sinalizador de descrição de áudio)
description: Este tópico inclui informações sobre um parâmetro que indica se um aplicativo deve fornecer um alerta visual ou uma indicação quando ele usa som para transmitir informações importantes.
ms.assetid: 7b316892-76ff-48b3-bf67-34dea2e63936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d01e3fda902c23c86279a9a4d75889ebfeff4d55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105763162"
---
# <a name="show-sounds-and-audio-description-flag"></a>Mostrar sons (e sinalizador de descrição de áudio)

Este tópico inclui informações sobre um parâmetro que indica se um aplicativo deve fornecer um alerta visual ou uma indicação quando ele usa som para transmitir informações importantes. Ele também fornece informações sobre um sinalizador que indica se um aplicativo deve fornecer uma descrição de áudio para elementos visuais.

## <a name="show-sounds-parameter"></a>Mostrar parâmetro de sons

O parâmetro show Sounds indica se o usuário deseja que os aplicativos apresentem todas as informações importantes no formato visual.

O usuário controla a configuração do parâmetro show Sounds usando a central de facilidade de acesso no painel de controle ou outro aplicativo para personalizar o ambiente. Os aplicativos usam os sinalizadores **SPI \_ GETSHOWSOUNDS** e **SPI \_ SETSHOWSOUNDS** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro show Sounds. Como alternativa, os aplicativos podem usar o sinalizador de apresentação do **SM \_** com a função [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para determinar o estado do parâmetro mostrar sons.

A determinação do estado do parâmetro mostrar sons é necessária apenas para aplicativos que normalmente apresentarão informações importantes apenas por som. Os aplicativos devem fornecer suporte a mostrar sons se usarem sons de uma das seguintes maneiras:

-   Para transmitir informações que são importantes para a operação do aplicativo.
-   Para alertar o usuário de que informações importantes estão sendo apresentadas visualmente. Se esse for o caso, embora as informações sejam apresentadas visualmente, o som tem a função adicional de atrair a atenção do usuário.

Os formulários de comentários visuais apropriados podem tornar o software muito mais funcional para os usuários que não podem confiar apenas no som. O design dos comentários visuais é específico do aplicativo e depende das informações que serão apresentadas ao usuário. Por exemplo, para atrair a atenção do usuário quando novas mensagens eletrônicas chegam, o aplicativo pode piscar sua janela ou até mesmo piscar a tela inteira. Se o aplicativo normalmente faz soar para indicar que o usuário está tentando executar uma operação ilegal, ele também pode exibir uma mensagem apropriada em sua linha de status ou usar a função [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) para exibir uma mensagem de erro específica. Se o aplicativo for normalmente projetado para reproduzir bites de som que trazem significado, como fala digitalizada, também poderá exibir uma janela de legendas com o mesmo texto.

O uso redundante de alertas audíveis e visuais foi mostrado para aumentar a usabilidade de aplicativos de software. O parâmetro show Sounds é uma solicitação de comentários visuais, mas seu uso não restringe um aplicativo para apresentar informações visualmente. Os usuários devem ser capazes de solicitar comentários visuais, independentemente se também desejarem comentários audíveis.

## <a name="audio-description-flag"></a>Sinalizador de descrição de áudio

Os aplicativos usam os sinalizadores **SPI \_ GETAUDIODESCRIPTION** e **SPI \_ SETAUDIODESCRIPTION** com a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para habilitar ou desabilitar descrições de áudio. Embora seja possível que os usuários com deficiência visual escutem o áudio no conteúdo de vídeo, há muitas ações em vídeo que não têm áudio correspondente. A descrição de áudio específica do que está acontecendo em um vídeo ajuda esses usuários a entender melhor o conteúdo. Esse sinalizador permite habilitar ou desabilitar as descrições de áudio nos idiomas em que são fornecidas.

 

 