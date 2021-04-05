---
title: Constantes e enumerações do DWM
description: Esta seção contém informações sobre as constantes e enumerações usadas nas APIs do Gerenciador de Janelas da Área de Trabalho (DWM).
ms.assetid: b01f620d-ac87-4e93-88ab-f4297d8cf1d5
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), referência
- DWM (Gerenciador de Janelas da Área de Trabalho), referência
- Gerenciador de Janelas da Área de Trabalho (DWM), constantes
- DWM (Gerenciador de Janelas da Área de Trabalho), constantes
- Gerenciador de Janelas da Área de Trabalho (DWM), enumerações
- DWM (Gerenciador de Janelas da Área de Trabalho), enumerações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 280fff527f95176b47fc99f88d09453dbf579f38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636130"
---
# <a name="dwm-constants-and-enumerations"></a><span data-ttu-id="182f4-109">Constantes e enumerações do DWM</span><span class="sxs-lookup"><span data-stu-id="182f4-109">DWM Constants and Enumerations</span></span>

<span data-ttu-id="182f4-110">Esta seção contém informações sobre as constantes e enumerações usadas nas APIs do Gerenciador de Janelas da Área de Trabalho (DWM).</span><span class="sxs-lookup"><span data-stu-id="182f4-110">This section contains information about the constants and enumerations used in the Desktop Window Manager (DWM) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="182f4-111">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="182f4-111">In this section</span></span>



| <span data-ttu-id="182f4-112">Tópico</span><span class="sxs-lookup"><span data-stu-id="182f4-112">Topic</span></span>                                                                                     | <span data-ttu-id="182f4-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="182f4-113">Description</span></span>                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="182f4-114">**Desfoque de DWM por trás de constantes**</span><span class="sxs-lookup"><span data-stu-id="182f4-114">**DWM Blur Behind Constants**</span></span>](dwm-bb-constants.md)<br/>                          | <span data-ttu-id="182f4-115">Sinalizadores usados pela estrutura [**DWM \_ BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) para indicar quais dos seus membros contêm informações válidas.</span><span class="sxs-lookup"><span data-stu-id="182f4-115">Flags used by the [**DWM\_BLURBEHIND**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_blurbehind) structure to indicate which of its members contain valid information.</span></span><br/>                                                                    |
| [<span data-ttu-id="182f4-116">**Constantes de composição do DWM Enable**</span><span class="sxs-lookup"><span data-stu-id="182f4-116">**DWM Enable Composition Constants**</span></span>](dwm-ec-constants.md)<br/>                   | <span data-ttu-id="182f4-117">Sinalizadores usados pela função [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  para alterar o estado da composição do DWM.</span><span class="sxs-lookup"><span data-stu-id="182f4-117">Flags used by the [**DwmEnableComposition**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablecomposition)  function to change the state of DWM composition.</span></span><br/>                                                                             |
| [<span data-ttu-id="182f4-118">**\_amostragem do \_ quadro de origem do DWM \_**</span><span class="sxs-lookup"><span data-stu-id="182f4-118">**DWM\_SOURCE\_FRAME\_SAMPLING**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwm_source_frame_sampling)<br/>              | <span data-ttu-id="182f4-119">Sinalizadores usados pela função [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) para especificar o tipo de amostragem de quadro.</span><span class="sxs-lookup"><span data-stu-id="182f4-119">Flags used by the [**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters) function to specify the frame sampling type.</span></span><br/>                                                                            |
| [<span data-ttu-id="182f4-120">**\_requisitos da \_ janela da guia DWM \_**</span><span class="sxs-lookup"><span data-stu-id="182f4-120">**DWM\_TAB\_WINDOW\_REQUIREMENTS**</span></span>](/windows/desktop/api/dwmapi/ne-dwmapi-dwm_tab_window_requirements)<br/>          | <span data-ttu-id="182f4-121">Retornado por DwmGetUnmetTabRequirements para indicar os requisitos necessários para uma janela colocar guias na barra de título do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="182f4-121">Returned by DwmGetUnmetTabRequirements to indicate the requirements needed for a window to put tabs in the application title bar.</span></span><br/>                                                                    |
| [<span data-ttu-id="182f4-122">**Constantes do DWM \_ TNP**</span><span class="sxs-lookup"><span data-stu-id="182f4-122">**DWM\_TNP Constants**</span></span>](dwm-tnp-constants.md)<br/>                                | <span data-ttu-id="182f4-123">Sinalizadores usados pela estrutura [**de \_ \_ Propriedades de miniatura do DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) para indicar quais dos seus membros contêm informações válidas.</span><span class="sxs-lookup"><span data-stu-id="182f4-123">Flags used by the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) structure to indicate which of its members contain valid information.</span></span><br/>                                               |
| [<span data-ttu-id="182f4-124">**DWMFLIP3DWINDOWPOLICY**</span><span class="sxs-lookup"><span data-stu-id="182f4-124">**DWMFLIP3DWINDOWPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmflip3dwindowpolicy)<br/>                         | <span data-ttu-id="182f4-125">Sinalizadores usados pela função [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar a política de janela Flip3D.</span><span class="sxs-lookup"><span data-stu-id="182f4-125">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the Flip3D window policy.</span></span><br/>                                                                               |
| [<span data-ttu-id="182f4-126">**DWMNCRENDERINGPOLICY**</span><span class="sxs-lookup"><span data-stu-id="182f4-126">**DWMNCRENDERINGPOLICY**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmncrenderingpolicy)<br/>                           | <span data-ttu-id="182f4-127">Sinalizadores usados pela função [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar a política de renderização de área não cliente.</span><span class="sxs-lookup"><span data-stu-id="182f4-127">Flags used by the [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) function to specify the non-client area rendering policy.</span></span><br/>                                                                   |
| [<span data-ttu-id="182f4-128">**DWMTRANSITION \_ OWNEDWINDOW \_ target**</span><span class="sxs-lookup"><span data-stu-id="182f4-128">**DWMTRANSITION\_OWNEDWINDOW\_TARGET**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmtransition_ownedwindow_target)<br/> | <span data-ttu-id="182f4-129">Identifica o destino.</span><span class="sxs-lookup"><span data-stu-id="182f4-129">Identifies the target.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="182f4-130">**DWMWINDOWATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="182f4-130">**DWMWINDOWATTRIBUTE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-dwmwindowattribute)<br/>                               | <span data-ttu-id="182f4-131">Sinalizadores usados pelas funções [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) e [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) para especificar atributos de janela para renderização não cliente.</span><span class="sxs-lookup"><span data-stu-id="182f4-131">Flags used by the [**DwmGetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetwindowattribute) and [**DwmSetWindowAttribute**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetwindowattribute) functions to specify window attributes for non-client rendering.</span></span><br/> |
| [<span data-ttu-id="182f4-132">**tipo de gesto \_**</span><span class="sxs-lookup"><span data-stu-id="182f4-132">**GESTURE\_TYPE**</span></span>](/windows/desktop/api/Dwmapi/ne-dwmapi-gesture_type)<br/>                                          | <span data-ttu-id="182f4-133">Identifica o tipo de gesto especificado em [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span><span class="sxs-lookup"><span data-stu-id="182f4-133">Identifies the gesture type specified in [**DwmRenderGesture**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmrendergesture).</span></span><br/>                                                                                                               |



 

 

 





