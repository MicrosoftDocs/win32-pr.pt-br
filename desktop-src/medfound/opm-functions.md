---
description: As funções a seguir são usadas com o Gerenciador de proteção de saída (OPM).
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Funções OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32b4ef210ace3f7f179b59980cedb962a5bee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772578"
---
# <a name="opm-functions"></a><span data-ttu-id="2e68c-103">Funções OPM</span><span class="sxs-lookup"><span data-stu-id="2e68c-103">OPM Functions</span></span>

<span data-ttu-id="2e68c-104">As funções a seguir são usadas com o [Gerenciador de proteção de saída](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="2e68c-104">The following functions are used with [Output Protection Manager](output-protection-manager.md) (OPM).</span></span>



| <span data-ttu-id="2e68c-105">Função</span><span class="sxs-lookup"><span data-stu-id="2e68c-105">Function</span></span>                                                                                             | <span data-ttu-id="2e68c-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e68c-106">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e68c-107">**OPMGetVideoOutputForTarget**</span><span class="sxs-lookup"><span data-stu-id="2e68c-107">**OPMGetVideoOutputForTarget**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | <span data-ttu-id="2e68c-108">Retorna um objeto de saída de vídeo para o destino VidPN no adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="2e68c-108">Returns a video output object for the VidPN target on the specified adapter.</span></span>                                                          |
| [<span data-ttu-id="2e68c-109">**OPMGetVideoOutputsFromHMONITOR**</span><span class="sxs-lookup"><span data-stu-id="2e68c-109">**OPMGetVideoOutputsFromHMONITOR**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | <span data-ttu-id="2e68c-110">Cria um objeto do Gerenciador de proteção de saída (OPM) para cada monitor físico associado a um determinado identificador de **HMONITOR** .</span><span class="sxs-lookup"><span data-stu-id="2e68c-110">Creates an Output Protection Manager (OPM) object for each physical monitor that is associated with a particular **HMONITOR** handle.</span></span> |
| [<span data-ttu-id="2e68c-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span><span class="sxs-lookup"><span data-stu-id="2e68c-111">**OPMGetVideoOutputsFromIDirect3DDevice9Object**</span></span>](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | <span data-ttu-id="2e68c-112">Cria um objeto OPM para cada monitor físico associado a um dispositivo Direct3D específico.</span><span class="sxs-lookup"><span data-stu-id="2e68c-112">Creates an OPM object for each physical monitor that is associated with a particular Direct3D device.</span></span>                                 |



 

<span data-ttu-id="2e68c-113">As funções a seguir são usadas pelo OPM para acessar a funcionalidade no driver de vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e68c-113">The following functions are used by OPM to access functionality in the display driver.</span></span> <span data-ttu-id="2e68c-114">Os aplicativos não devem chamar essas funções.</span><span class="sxs-lookup"><span data-stu-id="2e68c-114">Applications should not call these functions.</span></span>

-   [<span data-ttu-id="2e68c-115">**ConfigureOPMProtectedOutput**</span><span class="sxs-lookup"><span data-stu-id="2e68c-115">**ConfigureOPMProtectedOutput**</span></span>](configureopmprotectedoutput.md)
-   [<span data-ttu-id="2e68c-116">**CreateOPMProtectedOutputs**</span><span class="sxs-lookup"><span data-stu-id="2e68c-116">**CreateOPMProtectedOutputs**</span></span>](createopmprotectedoutputs.md)
-   [<span data-ttu-id="2e68c-117">**DestroyOPMProtectedOutput**</span><span class="sxs-lookup"><span data-stu-id="2e68c-117">**DestroyOPMProtectedOutput**</span></span>](destroyopmprotectedoutput.md)
-   [<span data-ttu-id="2e68c-118">**GetCertificate**</span><span class="sxs-lookup"><span data-stu-id="2e68c-118">**GetCertificate**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [<span data-ttu-id="2e68c-119">**Getcertificate**</span><span class="sxs-lookup"><span data-stu-id="2e68c-119">**GetCertificateSize**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [<span data-ttu-id="2e68c-120">**GetCOPPCompatibleOPMInformation**</span><span class="sxs-lookup"><span data-stu-id="2e68c-120">**GetCOPPCompatibleOPMInformation**</span></span>](getcoppcompatibleopminformation.md)
-   [<span data-ttu-id="2e68c-121">**GetOPMInformation**</span><span class="sxs-lookup"><span data-stu-id="2e68c-121">**GetOPMInformation**</span></span>](getopminformation.md)
-   [<span data-ttu-id="2e68c-122">**GetOPMRandomNumber**</span><span class="sxs-lookup"><span data-stu-id="2e68c-122">**GetOPMRandomNumber**</span></span>](getopmrandomnumber.md)
-   [<span data-ttu-id="2e68c-123">**GetSuggestedOPMProtectedOutputArraySize**</span><span class="sxs-lookup"><span data-stu-id="2e68c-123">**GetSuggestedOPMProtectedOutputArraySize**</span></span>](getsuggestedopmprotectedoutputarraysize.md)
-   [<span data-ttu-id="2e68c-124">**SetOPMSigningKeyAndSequenceNumbers**</span><span class="sxs-lookup"><span data-stu-id="2e68c-124">**SetOPMSigningKeyAndSequenceNumbers**</span></span>](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a><span data-ttu-id="2e68c-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e68c-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e68c-126">Referência de programação de OPM</span><span class="sxs-lookup"><span data-stu-id="2e68c-126">OPM Programming Reference</span></span>](opm-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="2e68c-127">Gerenciador de proteção de saída</span><span class="sxs-lookup"><span data-stu-id="2e68c-127">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



