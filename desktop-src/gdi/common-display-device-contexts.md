---
description: Um contexto de dispositivo comum é usado para desenhar na área do cliente da janela.
ms.assetid: 63c4f775-b1a3-4f7c-808b-81c596f26353
title: Contextos de dispositivo de exibição comuns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890b0235784ec1ed11c8ce3a553244629a008d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921292"
---
# <a name="common-display-device-contexts"></a>Contextos de dispositivo de exibição comuns

Um *contexto de dispositivo comum* é usado para desenhar na área do cliente da janela. O sistema fornece um contexto de dispositivo comum por padrão para qualquer janela cuja classe de janela não especifique explicitamente um estilo de contexto de dispositivo de exibição. Contextos de dispositivo comuns normalmente são usados com janelas que podem ser desenhadas sem alterações extensivas nos atributos de contexto do dispositivo. Contextos de dispositivo comuns são convenientes porque não exigem memória adicional ou recursos do sistema, mas podem ser inconvenientes se o aplicativo precisar configurar muitos atributos antes de usá-los.

O sistema recupera todos os contextos de dispositivo comuns do cache de contexto do dispositivo de vídeo. Um aplicativo pode recuperar um contexto de dispositivo comum imediatamente após a janela ser criada. Como o contexto do dispositivo comum é do cache, o aplicativo sempre deve liberar o contexto do dispositivo assim que possível após o desenho. Depois que o contexto de dispositivo comum é liberado, ele não é mais válido e o aplicativo não deve tentar desenhá-lo com ele. Para desenhar novamente, o aplicativo deve recuperar um novo contexto de dispositivo comum e continuar a recuperar e liberar um contexto de dispositivo comum cada vez que ele desenhar na janela. Se o aplicativo recuperar o identificador de contexto do dispositivo usando a função [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , ele deverá usar a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) para liberar o identificador. Da mesma forma, para cada função [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) , o aplicativo deve usar uma função [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) correspondente.

Quando o aplicativo recupera o contexto do dispositivo, o sistema ajusta a origem para que ele se alinhe ao canto superior esquerdo da área do cliente. Ele também define a região de recorte para que a saída para o contexto do dispositivo seja recortada para a área do cliente. Qualquer saída que, de outra forma, apareceria fora da área do cliente é recortada. Se o aplicativo recuperar o contexto de dispositivo comum usando [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), o sistema também incluirá a região de atualização na região de recorte para restringir ainda mais a saída.

Quando um aplicativo libera um contexto de dispositivo comum, o sistema restaura os valores padrão para os atributos do contexto do dispositivo. Um aplicativo que modifica os valores de atributo deve fazer isso sempre que recupera um contexto de dispositivo comum. Liberar o contexto do dispositivo libera todos os objetos de desenho que o aplicativo pode ter selecionado, para que o aplicativo não precise liberar esses objetos antes de liberar o contexto do dispositivo. Em todos os casos, um aplicativo nunca deve supor que o contexto de dispositivo comum retenha seleções não padrão após ser liberado.

 

 



