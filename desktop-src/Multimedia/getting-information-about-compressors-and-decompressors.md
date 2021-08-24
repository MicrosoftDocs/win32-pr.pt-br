---
title: Obtendo informações sobre compactadores e descompactadores
description: Obtendo informações sobre compactadores e descompactadores
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- VCM (Gerenciador de compactação de vídeo), obtendo informações sobre os compactadores
- VCM (Gerenciador de compactação de vídeo), obtendo informações sobre os compactadores
- Função ICGetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404b6acacd97b514edcf0328a8127f97152554015694eba3f8e5bf3b76214de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678606"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>Obtendo informações sobre compactadores e descompactadores

Para obter informações gerais sobre um compressor ou descompactador, seu aplicativo pode usar a função [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) . Essa função preenche uma estrutura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) com informações sobre o compressor ou o descompactador. Seu aplicativo deve alocar a memória para a estrutura **ICINFO** e passar um ponteiro para ela em **ICGetInfo**. A menos que seu aplicativo procure um compactador ou descompactador específico, os sinalizadores na estrutura **ICINFO** fornecem as informações mais úteis sobre os recursos de um compressor ou descompactador.

para obter a taxa padrão de quadro-chave e o valor de qualidade padrão de um compressor ou descompactador, seu aplicativo pode enviar o [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) e ICM mensagens de [**\_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) (ou usar as macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) ).

Para determinar o melhor formato de exibição de um compactador ou descompactador, seu aplicativo pode usar a função [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) .

para determinar se um compressor ou descompactador pode exibir uma caixa de diálogo sobre, envie a [**ICM \_ sobre**](icm-about.md) a mensagem (ou use a macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) ). você também pode exibir a caixa de diálogo sobre de um compressor ou descompactador enviando o ICM \_ sobre a mensagem e alterando o valor do parâmetro *wParam* (ou usando a macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) ).

 

 




