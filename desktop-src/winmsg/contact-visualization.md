---
description: As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um contato de entrada é detectado.
ms.assetid: 6FE8444C-A575-4E89-86D1-1873206688F5
title: Visualização de contato (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100892624f3e656e33ddf798c5795eeab6b11a17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297287"
---
# <a name="contact-visualization"></a><span data-ttu-id="c67c7-103">Visualização de contato</span><span class="sxs-lookup"><span data-stu-id="c67c7-103">Contact Visualization</span></span>

<span data-ttu-id="c67c7-104">As constantes a seguir são usadas por aplicativos ou estruturas de interface do usuário para identificar como os comentários da interface do usuário são processados quando um contato de entrada é detectado.</span><span class="sxs-lookup"><span data-stu-id="c67c7-104">The following constants are used by applications or UI frameworks to identify how UI feedback is processed when an input contact is detected.</span></span>

<span data-ttu-id="c67c7-105">Essas constantes são usadas com os parâmetros **SPI \_ GETCONTACTVISUALIZATION** e **SPI \_ SETCONTACTVISUALIZATION** e a função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) .</span><span class="sxs-lookup"><span data-stu-id="c67c7-105">These constants are used with the **SPI\_GETCONTACTVISUALIZATION** and **SPI\_SETCONTACTVISUALIZATION** parameters and the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function.</span></span>

<dl> <dt>

<span data-ttu-id="c67c7-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION \_ desativado**</span><span class="sxs-lookup"><span data-stu-id="c67c7-106"><span id="CONTACTVISUALIZATION_OFF"></span><span id="contactvisualization_off"></span>**CONTACTVISUALIZATION\_OFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c67c7-107">0x0000</span><span class="sxs-lookup"><span data-stu-id="c67c7-107">0x0000</span></span>
</dt> <dt>



<span data-ttu-id="c67c7-108">Especifica comentários da interface do usuário para todos os contatos está desativado.</span><span class="sxs-lookup"><span data-stu-id="c67c7-108">Specifies UI feedback for all contacts is off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c67c7-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION \_ em**</span><span class="sxs-lookup"><span data-stu-id="c67c7-109"><span id="CONTACTVISUALIZATION_ON"></span><span id="contactvisualization_on"></span>**CONTACTVISUALIZATION\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c67c7-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="c67c7-110">0x0001</span></span>
</dt> <dt>



<span data-ttu-id="c67c7-111">Especifica os comentários da interface do usuário para todos os contatos está ativado.</span><span class="sxs-lookup"><span data-stu-id="c67c7-111">Specifies UI feedback for all contacts is on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="c67c7-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION \_ presentationmode**</span><span class="sxs-lookup"><span data-stu-id="c67c7-112"><span id="CONTACTVISUALIZATION_PRESENTATIONMODE"></span><span id="contactvisualization_presentationmode"></span>**CONTACTVISUALIZATION\_PRESENTATIONMODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c67c7-113">0x0002</span><span class="sxs-lookup"><span data-stu-id="c67c7-113">0x0002</span></span>
</dt> <dt>



<span data-ttu-id="c67c7-114">Especifica os comentários da interface do usuário para todos os contatos estão ativados com visuais do modo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="c67c7-114">Specifies UI feedback for all contacts is on with presentation mode visuals.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c67c7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c67c7-115">Requirements</span></span>



| <span data-ttu-id="c67c7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c67c7-116">Requirement</span></span> | <span data-ttu-id="c67c7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c67c7-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c67c7-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c67c7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c67c7-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c67c7-119">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c67c7-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c67c7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c67c7-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c67c7-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c67c7-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c67c7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c67c7-123"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="c67c7-123"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c67c7-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="c67c7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c67c7-125">Constantes de configuração</span><span class="sxs-lookup"><span data-stu-id="c67c7-125">Configuration Constants</span></span>](configuration-constants.md)
</dt> <dt>

[<span data-ttu-id="c67c7-126">**Visualização do gesto**</span><span class="sxs-lookup"><span data-stu-id="c67c7-126">**Gesture Visualization**</span></span>](gesture-visualization.md)
</dt> <dt>

[<span data-ttu-id="c67c7-127">**SystemParametersInfo**</span><span class="sxs-lookup"><span data-stu-id="c67c7-127">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> <dt>

[<span data-ttu-id="c67c7-128">Configuração de comentários de entrada</span><span class="sxs-lookup"><span data-stu-id="c67c7-128">Input Feedback Configuration</span></span>](/previous-versions/windows/desktop/input_feedback/input-feedback-configuration-portal)
</dt> </dl>

 

