---
title: Obter informações sobre os descompactores e os descompactores
description: Obter informações sobre os descompactores e os descompactores
ms.assetid: bb9773dc-a706-40e6-8703-1cd47101992c
keywords:
- VCM (gerenciador de compactação de vídeo), obter informações sobre os vcs
- VCM (gerenciador de compactação de vídeo), obter informações sobre os vcs
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
# <a name="getting-information-about-compressors-and-decompressors"></a>Obter informações sobre os descompactores e os descompactores

Para obter informações gerais sobre um descompactador ou um descompactador, seu aplicativo pode usar a [**função ICGetInfo.**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) Essa função preenche uma estrutura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) com informações sobre o descompactador ou o descompactador. Seu aplicativo deve alocar a memória para a estrutura **ICINFO** e passar um ponteiro para ela em **ICGetInfo.** A menos que seu aplicativo pesquise por um descompactador ou um descompactador específico, os sinalizadores na estrutura **ICINFO** fornecem as informações mais úteis sobre as funcionalidades de um descompactador ou um descompactador.

Para obter a taxa de quadros-chave padrão e o valor de qualidade padrão de um descompactador ou descompactador, seu aplicativo pode enviar as mensagens [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) e [**ICM \_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) (ou usar as macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality).**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality)

Para determinar o melhor formato de exibição de um visor ou descompactador, seu aplicativo pode usar a [**função ICGetDisplayFormat.**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)

Para determinar se um decorador ou descompactador pode exibir uma caixa de diálogo Sobre, envie a mensagem [**ICM \_ ABOUT**](icm-about.md) (ou use a macro [**ICQueryAbout).**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) Você também pode exibir a caixa de diálogo Sobre de um visor ou descompactador enviando a mensagem ICM ABOUT e alterando o valor do parâmetro \_ *wParam* (ou usando a macro [**ICAbout).**](/windows/desktop/api/Vfw/nf-vfw-icabout)

 

 




