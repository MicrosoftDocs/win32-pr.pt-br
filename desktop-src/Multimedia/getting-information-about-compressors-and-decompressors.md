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
ms.openlocfilehash: 5c619d13559d99b570af200298f29fcd8238c7d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916317"
---
# <a name="getting-information-about-compressors-and-decompressors"></a>Obtendo informações sobre compactadores e descompactadores

Para obter informações gerais sobre um compressor ou descompactador, seu aplicativo pode usar a função [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) . Essa função preenche uma estrutura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) com informações sobre o compressor ou o descompactador. Seu aplicativo deve alocar a memória para a estrutura **ICINFO** e passar um ponteiro para ela em **ICGetInfo**. A menos que seu aplicativo procure um compactador ou descompactador específico, os sinalizadores na estrutura **ICINFO** fornecem as informações mais úteis sobre os recursos de um compressor ou descompactador.

Para obter a taxa padrão de quadro-chave e o valor de qualidade padrão de um compressor ou descompactador, seu aplicativo pode enviar as mensagens de [**\_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) e ICM (ou usar as macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) ).

Para determinar o melhor formato de exibição de um compactador ou descompactador, seu aplicativo pode usar a função [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) .

Para determinar se um compressor ou descompactador pode exibir uma caixa de diálogo sobre, envie o [**ICM \_ sobre**](icm-about.md) a mensagem (ou use a macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) ). Você também pode exibir a caixa de diálogo sobre de um compressor ou descompactador enviando o ICM \_ sobre a mensagem e alterando o valor do parâmetro *wParam* (ou usando a macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) ).

 

 




