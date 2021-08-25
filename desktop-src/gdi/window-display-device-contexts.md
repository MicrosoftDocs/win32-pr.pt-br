---
description: Um contexto de dispositivo de janela permite que um aplicativo desenhe em qualquer lugar em uma janela, incluindo a área não cliente.
ms.assetid: 7b3c6352-51d5-4fdf-82c2-7a28194f607f
title: Janela exibir contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfed34646323114ffcfb7753331b1b5c305a7a0c01a475795a7918f6e5a2dd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965086"
---
# <a name="window-display-device-contexts"></a>Janela exibir contextos de dispositivo

Um *contexto de dispositivo de janela* permite que um aplicativo desenhe em qualquer lugar em uma janela, incluindo a área não cliente. Os contextos de dispositivo de janela normalmente são usados por aplicativos que processam as mensagens do [**WM \_ NCPAINT**](wm-ncpaint.md) e do [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) para Windows com áreas personalizadas que não são do cliente. O uso de um contexto de dispositivo de janela não é recomendado para nenhuma outra finalidade.

Um aplicativo pode recuperar um contexto de dispositivo de janela usando a função [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) com a \_ opção de janela DCX especificada. A função recupera um contexto de dispositivo de janela do cache de contexto do dispositivo de vídeo. Uma janela que usa um contexto de dispositivo de janela deve liberá-lo após o desenho usando a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) assim que possível. Contextos de dispositivo de janela são sempre do cache; os \_ estilos de classe cs OWNDC e cs \_ CLASSDC não afetam o contexto do dispositivo.

Quando um aplicativo recupera um contexto de dispositivo de janela, o sistema define a origem do dispositivo para o canto superior esquerdo da janela, em vez do canto superior esquerdo da área do cliente. Ele também define a região de recorte para incluir a janela inteira, não apenas a área do cliente. O sistema define os valores de atributo atuais de um contexto de dispositivo de janela para os mesmos valores padrão que um contexto de dispositivo comum. Um aplicativo pode alterar os valores de atributo, mas o sistema não preserva nenhuma alteração quando o contexto do dispositivo é liberado.

 

 
