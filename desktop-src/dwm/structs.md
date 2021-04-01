---
title: Estruturas do DWM
description: Esta seção contém informações sobre as estruturas do Gerenciador de Janelas da Área de Trabalho (DWM).
ms.assetid: 26b36617-54c2-405a-9a7d-bd86fefa94b6
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), referência
- DWM (Gerenciador de Janelas da Área de Trabalho), referência
- Gerenciador de Janelas da Área de Trabalho (DWM), estruturas
- DWM (Gerenciador de Janelas da Área de Trabalho), estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f212d248c0f70cfd51e6e47b2d37c89d24f630b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005550"
---
# <a name="dwm-structures"></a><span data-ttu-id="1a337-107">Estruturas do DWM</span><span class="sxs-lookup"><span data-stu-id="1a337-107">DWM Structures</span></span>

<span data-ttu-id="1a337-108">Esta seção contém informações sobre as estruturas do Gerenciador de Janelas da Área de Trabalho (DWM).</span><span class="sxs-lookup"><span data-stu-id="1a337-108">This section contains information about the Desktop Window Manager (DWM) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1a337-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="1a337-109">In this section</span></span>



| <span data-ttu-id="1a337-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="1a337-110">Topic</span></span>                                                                     | <span data-ttu-id="1a337-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="1a337-111">Description</span></span>                                                                                                                                               |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a337-112">**DWM \_ BLURBEHIND**</span><span class="sxs-lookup"><span data-stu-id="1a337-112">**DWM\_BLURBEHIND**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind)<br/>                      | <span data-ttu-id="1a337-113">Especifica as propriedades de desfoque do DWM.</span><span class="sxs-lookup"><span data-stu-id="1a337-113">Specifies DWM blur-behind properties.</span></span> <span data-ttu-id="1a337-114">Usado pela função [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) .</span><span class="sxs-lookup"><span data-stu-id="1a337-114">Used by the [**DwmEnableBlurBehindWindow**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenableblurbehindwindow) function.</span></span><br/>                     |
| [<span data-ttu-id="1a337-115">**\_parâmetros presentes do DWM \_**</span><span class="sxs-lookup"><span data-stu-id="1a337-115">**DWM\_PRESENT\_PARAMETERS**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_present_parameters)<br/>     | <span data-ttu-id="1a337-116">Especifica os parâmetros de quadro de vídeo do DWM para composição de quadros.</span><span class="sxs-lookup"><span data-stu-id="1a337-116">Specifies DWM video frame parameters for frame composition.</span></span> <span data-ttu-id="1a337-117">Usado pela função [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) .</span><span class="sxs-lookup"><span data-stu-id="1a337-117">Used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function.</span></span><br/>   |
| [<span data-ttu-id="1a337-118">**\_Propriedades de miniatura do DWM \_**</span><span class="sxs-lookup"><span data-stu-id="1a337-118">**DWM\_THUMBNAIL\_PROPERTIES**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties)<br/> | <span data-ttu-id="1a337-119">Especifica as propriedades de miniatura do DWM.</span><span class="sxs-lookup"><span data-stu-id="1a337-119">Specifies DWM thumbnail properties.</span></span> <span data-ttu-id="1a337-120">Usado pela função [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) .</span><span class="sxs-lookup"><span data-stu-id="1a337-120">Used by the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function.</span></span><br/>                 |
| [<span data-ttu-id="1a337-121">**\_informações de tempo do DWM \_**</span><span class="sxs-lookup"><span data-stu-id="1a337-121">**DWM\_TIMING\_INFO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_timing_info)<br/>                   | <span data-ttu-id="1a337-122">Especifica informações de tempo de composição do DWM.</span><span class="sxs-lookup"><span data-stu-id="1a337-122">Specifies DWM composition timing information.</span></span> <span data-ttu-id="1a337-123">Usado pela função [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) .</span><span class="sxs-lookup"><span data-stu-id="1a337-123">Used by the [**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo) function.</span></span><br/>         |
| [<span data-ttu-id="1a337-124">**MilMatrix3x2D**</span><span class="sxs-lookup"><span data-stu-id="1a337-124">**MilMatrix3x2D**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-milmatrix3x2d)<br/>                         | <span data-ttu-id="1a337-125">Especifica uma matriz 3x2 que descreve uma transformação.</span><span class="sxs-lookup"><span data-stu-id="1a337-125">Specifies a 3x2 matrix that describes a transform.</span></span> <br/>                                                                                            |
| [<span data-ttu-id="1a337-126">**taxa não assinada \_**</span><span class="sxs-lookup"><span data-stu-id="1a337-126">**UNSIGNED\_RATIO**</span></span>](/windows/desktop/api/Dwmapi/ns-dwmapi-unsigned_ratio)<br/>                      | <span data-ttu-id="1a337-127">Define um tipo de dados usado pelas APIs DWM.</span><span class="sxs-lookup"><span data-stu-id="1a337-127">Defines a data type used by the DWM APIs.</span></span> <span data-ttu-id="1a337-128">Ele representa uma proporção genérica e é usado para diferentes finalidades e unidades, mesmo em uma única API.</span><span class="sxs-lookup"><span data-stu-id="1a337-128">It represents a generic ratio and is used for different purposes and units even within a single API.</span></span><br/> |



 

 

 





