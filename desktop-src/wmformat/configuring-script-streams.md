---
title: Configurando fluxos de script
description: Configurando fluxos de script
ms.assetid: f8f1656e-69c6-47f7-a8eb-c1039a84ebf3
keywords:
- fluxos, configurando fluxos de script
- codecs, configurando fluxos de script
- fluxos de script, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e063865b301c8c7c2a4171aa530a89464306c0ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005391"
---
# <a name="configuring-script-streams"></a><span data-ttu-id="1dffc-106">Configurando fluxos de script</span><span class="sxs-lookup"><span data-stu-id="1dffc-106">Configuring Script Streams</span></span>

<span data-ttu-id="1dffc-107">Como todos os tipos de fluxo arbitrários, os fluxos de script precisam ter uma taxa de bits e uma janela de buffer definidas para eles.</span><span class="sxs-lookup"><span data-stu-id="1dffc-107">Like all arbitrary stream types, script streams need to have a bit rate and buffer window defined for them.</span></span> <span data-ttu-id="1dffc-108">O tipo de mídia principal na estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) deve ser definido como WMMEDIATYPE \_ script.</span><span class="sxs-lookup"><span data-stu-id="1dffc-108">The major media type in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure must be set to WMMEDIATYPE\_Script.</span></span>

<span data-ttu-id="1dffc-109">Fluxos de script precisam ter o membro **formatType** do **\_ \_ tipo de mídia do WM** definido como WMFORMAT \_ script, que indica que o membro **pbFormat** aponta para uma estrutura [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) .</span><span class="sxs-lookup"><span data-stu-id="1dffc-109">Script streams need to have the **formattype** member of **WM\_MEDIA\_TYPE** set to WMFORMAT\_Script, which indicates that the **pbFormat** member points to a [**WMSCRIPTFORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat) structure.</span></span>

<span data-ttu-id="1dffc-110">Há apenas um tipo de script com suporte, WMSCRIPTTYPE \_ TwoStrings.</span><span class="sxs-lookup"><span data-stu-id="1dffc-110">There is only one supported script type, WMSCRIPTTYPE\_TwoStrings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1dffc-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1dffc-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1dffc-112">**Configuração comum a todos os fluxos**</span><span class="sxs-lookup"><span data-stu-id="1dffc-112">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="1dffc-113">**Configurando tipos de fluxo arbitrários**</span><span class="sxs-lookup"><span data-stu-id="1dffc-113">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="1dffc-114">**Comandos de script**</span><span class="sxs-lookup"><span data-stu-id="1dffc-114">**Script Commands**</span></span>](script-commands.md)
</dt> </dl>

 

 




