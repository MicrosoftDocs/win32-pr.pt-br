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
# <a name="getting-information-about-compressors-and-decompressors"></a><span data-ttu-id="f71ce-106">Obtendo informações sobre compactadores e descompactadores</span><span class="sxs-lookup"><span data-stu-id="f71ce-106">Getting Information About Compressors and Decompressors</span></span>

<span data-ttu-id="f71ce-107">Para obter informações gerais sobre um compressor ou descompactador, seu aplicativo pode usar a função [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) .</span><span class="sxs-lookup"><span data-stu-id="f71ce-107">To get general information about a compressor or decompressor, your application can use the [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) function.</span></span> <span data-ttu-id="f71ce-108">Essa função preenche uma estrutura [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) com informações sobre o compressor ou o descompactador.</span><span class="sxs-lookup"><span data-stu-id="f71ce-108">This function fills an [**ICINFO**](/windows/desktop/api/Vfw/ns-vfw-icinfo) structure with information about the compressor or decompressor.</span></span> <span data-ttu-id="f71ce-109">Seu aplicativo deve alocar a memória para a estrutura **ICINFO** e passar um ponteiro para ela em **ICGetInfo**.</span><span class="sxs-lookup"><span data-stu-id="f71ce-109">Your application must allocate the memory for the **ICINFO** structure and pass a pointer to it in **ICGetInfo**.</span></span> <span data-ttu-id="f71ce-110">A menos que seu aplicativo procure um compactador ou descompactador específico, os sinalizadores na estrutura **ICINFO** fornecem as informações mais úteis sobre os recursos de um compressor ou descompactador.</span><span class="sxs-lookup"><span data-stu-id="f71ce-110">Unless your application searches for a particular compressor or decompressor, the flags in the **ICINFO** structure provide the most useful information about the capabilities of a compressor or decompressor.</span></span>

<span data-ttu-id="f71ce-111">Para obter a taxa padrão de quadro-chave e o valor de qualidade padrão de um compressor ou descompactador, seu aplicativo pode enviar as mensagens de [**\_ GETDEFAULTQUALITY**](icm-getdefaultquality.md) [**ICM \_ GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) e ICM (ou usar as macros [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) e [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) ).</span><span class="sxs-lookup"><span data-stu-id="f71ce-111">To get the default key-frame rate and default quality value of a compressor or decompressor, your application can send the [**ICM\_GETDEFAULTKEYFRAMERATE**](icm-getdefaultkeyframerate.md) and [**ICM\_GETDEFAULTQUALITY**](icm-getdefaultquality.md) messages (or use the [**ICGetDefaultKeyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) and [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) macros).</span></span>

<span data-ttu-id="f71ce-112">Para determinar o melhor formato de exibição de um compactador ou descompactador, seu aplicativo pode usar a função [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) .</span><span class="sxs-lookup"><span data-stu-id="f71ce-112">To determine the best display format of a compressor or decompressor, your application can use the [**ICGetDisplayFormat**](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat) function.</span></span>

<span data-ttu-id="f71ce-113">Para determinar se um compressor ou descompactador pode exibir uma caixa de diálogo sobre, envie o [**ICM \_ sobre**](icm-about.md) a mensagem (ou use a macro [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) ).</span><span class="sxs-lookup"><span data-stu-id="f71ce-113">To determine if a compressor or decompressor can display an About dialog box, send the [**ICM\_ABOUT**](icm-about.md) message (or use the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro).</span></span> <span data-ttu-id="f71ce-114">Você também pode exibir a caixa de diálogo sobre de um compressor ou descompactador enviando o ICM \_ sobre a mensagem e alterando o valor do parâmetro *wParam* (ou usando a macro [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) ).</span><span class="sxs-lookup"><span data-stu-id="f71ce-114">You can also display the About dialog box of a compressor or decompressor by sending the ICM\_ABOUT message and changing the value of the *wParam* parameter (or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro).</span></span>

 

 




