---
description: Gerado pelo mecanismo de política quando a aquisição de licença está prestes a começar. A aquisição de licença é realizada usando a implementação de aplicativos da interface IMFContentProtectionManager.
ms.assetid: c328743c-a69b-431e-8a05-0e140aad9b4d
title: Evento MELicenseAcquisitionStart (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 914d2580c95cf40986a844a994c1e284c5ad9e22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811089"
---
# <a name="melicenseacquisitionstart-event"></a><span data-ttu-id="45d42-104">Evento MELicenseAcquisitionStart</span><span class="sxs-lookup"><span data-stu-id="45d42-104">MELicenseAcquisitionStart event</span></span>

<span data-ttu-id="45d42-105">Gerado pelo mecanismo de política quando a aquisição de licença está prestes a começar.</span><span class="sxs-lookup"><span data-stu-id="45d42-105">Raised by the policy engine when license acquisition is about to begin.</span></span> <span data-ttu-id="45d42-106">A aquisição de licença é realizada usando a implementação do aplicativo da interface [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) .</span><span class="sxs-lookup"><span data-stu-id="45d42-106">License acquisition is performed using the application's implementation of the [**IMFContentProtectionManager**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

## <a name="event-values"></a><span data-ttu-id="45d42-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="45d42-107">Event values</span></span>

<span data-ttu-id="45d42-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="45d42-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="45d42-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="45d42-109">VARTYPE</span></span>              | <span data-ttu-id="45d42-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="45d42-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="45d42-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="45d42-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="45d42-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="45d42-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="45d42-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="45d42-113">Remarks</span></span>

<span data-ttu-id="45d42-114">Quando a aquisição de licença é concluída, o mecanismo de política gera o evento [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="45d42-114">When license acquisition is completed, the policy engine raises the [MELicenseAcquisitionCompleted](melicenseacquisitioncompleted.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="45d42-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45d42-115">Requirements</span></span>



| <span data-ttu-id="45d42-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="45d42-116">Requirement</span></span> | <span data-ttu-id="45d42-117">Valor</span><span class="sxs-lookup"><span data-stu-id="45d42-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45d42-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45d42-118">Minimum supported client</span></span><br/> | <span data-ttu-id="45d42-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45d42-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="45d42-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="45d42-120">Minimum supported server</span></span><br/> | <span data-ttu-id="45d42-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45d42-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="45d42-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45d42-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="45d42-123"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45d42-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45d42-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="45d42-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45d42-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="45d42-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




