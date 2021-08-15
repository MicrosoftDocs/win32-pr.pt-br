---
title: Modos de visualização e sobreposição
description: Modos de visualização e sobreposição
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- WM_CAP_SET_PREVIEW mensagem
- macro capPreview
- WM_CAP_SET_PREVIEWRATE mensagem
- macro capPreviewRate
- WM_CAP_SET_SCALE mensagem
- macro capPreviewScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9359b1380c5d6efe049bc4bea52a08a92f880af5d35558f4e65e21070f20c0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118372365"
---
# <a name="preview-and-overlay-modes"></a>Modos de visualização e sobreposição

Um driver de captura pode implementar dois métodos para exibir um fluxo de vídeo de entrada: modo de visualização e modo de sobreposição. Se um driver de captura implementar os dois métodos, o usuário poderá escolher qual método usar.

O modo de visualização transfere quadros digitalizados do hardware de captura para a memória do sistema e, em seguida, exibe os quadros digitalizados na janela de captura usando as funções da interface de dispositivo de gráficos (GDI). Os aplicativos podem diminuir a taxa de visualização quando a janela pai perde o foco e aumenta a taxa de visualização quando a janela pai Obtém o foco. Essa ação melhora a capacidade de resposta geral do sistema porque a operação de visualização é intensiva no processador.

Há três mensagens para controlar a operação de visualização.

-   Use a mensagem de [**\_ \_ \_ Visualização definir Cap do WM**](wm-cap-set-preview.md) para habilitar ou desabilitar o modo de visualização enviando a (ou a macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) ) para uma janela de captura.
-   Use a mensagem do [**PREVIEWRATE da Cap do WM \_ \_ \_ set**](wm-cap-set-previewrate.md) (ou a macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) ) para definir a taxa na qual os quadros são exibidos no modo de visualização
-   Use a mensagem de [**\_ \_ \_ escala definida do WM Cap**](wm-cap-set-scale.md) (ou a macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) ) para habilitar ou desabilitar o dimensionamento do vídeo de visualização.

Quando a visualização e o dimensionamento estão habilitados, o quadro de vídeo capturado é ampliado para as dimensões da janela de captura. Habilitar o modo de visualização desabilita automaticamente o modo de sobreposição.

O modo de sobreposição é uma função de hardware que exibe o conteúdo do buffer de captura no monitor sem usar recursos de CPU. Você pode habilitar e desabilitar o modo de sobreposição enviando a mensagem de [**\_ \_ \_ sobreposição do conjunto de Cap do WM**](wm-cap-set-overlay.md) (ou a macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) ) para uma janela de captura. Habilitar o modo de sobreposição desabilita automaticamente o modo de visualização.

Você também pode definir a posição de rolagem do quadro de vídeo dentro da área do cliente da janela de captura para o modo de visualização ou o modo de sobreposição enviando a mensagem de [**\_ \_ \_ rolagem set do WM Cap**](wm-cap-set-scroll.md) (ou a macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) ) para uma janela de captura.

 

 




