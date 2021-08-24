---
title: Mostrar sons (e sinalizador de descrição de áudio)
description: Este tópico inclui informações sobre um parâmetro que indica se um aplicativo deve fornecer um alerta visual ou uma indicação quando ele usa som para transmitir informações importantes.
ms.assetid: 7b316892-76ff-48b3-bf67-34dea2e63936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dbf32dfacdf1dc0b8ed3bc51c986ae572e43300263565254ad6b3a48a981beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734316"
---
# <a name="show-sounds-and-audio-description-flag"></a>Mostrar sons (e sinalizador de descrição de áudio)

Este tópico inclui informações sobre um parâmetro que indica se um aplicativo deve fornecer um alerta visual ou uma indicação quando ele usa som para transmitir informações importantes. Ele também fornece informações sobre um sinalizador que indica se um aplicativo deve fornecer uma descrição de áudio para elementos visuais.

## <a name="show-sounds-parameter"></a>Parâmetro Show Sounds

O parâmetro show sounds indica se o usuário deseja que os aplicativos apresentem todas as informações importantes no formato visual.

O usuário controla a configuração do parâmetro show sounds usando o Central de Facilidade de Acesso no Painel de Controle ou outro aplicativo para personalizar o ambiente. Os aplicativos usam os **sinalizadores SPI \_ GETSHOWSOUNDS** e **SPI \_ SETSHOWSOUNDS** com a [**função SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obter e definir o parâmetro show sounds. Como alternativa, os aplicativos podem usar o sinalizador **SM \_ SHOWSOUNDS** com a [**função GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) para determinar o estado do parâmetro show sounds.

Determinar o estado do parâmetro show sounds é necessário apenas para aplicativos que normalmente apresentam informações importantes apenas por som. Os aplicativos deverão fornecer suporte a sons de show se usarem sons de uma das seguintes maneiras:

-   Para transmitir informações importantes para a operação do aplicativo.
-   Para alertar o usuário de que informações importantes estão sendo apresentadas visualmente. Se esse for o caso, mesmo que as informações são apresentadas visualmente, o som tem a função adicional de atrair a atenção do usuário.

Formulários de comentários visuais apropriados podem tornar o software muito mais funcional para usuários que não podem depender de som sozinho. O design dos comentários visuais é específico do aplicativo e depende das informações que serão apresentadas ao usuário. Por exemplo, para atrair a atenção do usuário quando chega um novo email eletrônico, o aplicativo pode piscar sua janela ou até mesmo piscar toda a tela. Se o aplicativo normalmente fizer som para indicar que o usuário está tentando executar uma operação ilegal, ele também poderá exibir uma mensagem apropriada em sua linha de status ou usar a [**função MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) para exibir uma mensagem de erro específica. Se o aplicativo normalmente for projetado para reproduzir marcas de som que têm significado, como fala digitalizada, ele também poderá exibir uma janela de legenda com o mesmo texto.

O uso redundante de alertas visuais e audíveis foi mostrado para aumentar a usabilidade de aplicativos de software. O parâmetro show sounds é uma solicitação de comentários visuais, mas seu uso não restringe um aplicativo a apresentar informações visualmente. Os usuários devem ser capazes de solicitar comentários visuais, independentemente de também quererem comentários audíveis.

## <a name="audio-description-flag"></a>Sinalizador de descrição de áudio

Os aplicativos usam os **sinalizadores SPI \_ GETAUDIODESCRIPTION** e **SPI \_ SETAUDIODESCRIPTION** com a [**função SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para habilitar ou desabilitar descrições de áudio. Embora seja possível que os usuários com deficiência visual escutam o áudio no conteúdo do vídeo, há muita ação em vídeo que não tem áudio correspondente. Uma descrição de áudio específica do que está acontecendo em um vídeo ajuda esses usuários a entender melhor o conteúdo. Esse sinalizador permite habilitar ou desabilitar descrições de áudio nos idiomas em que elas são fornecidas.

 

 