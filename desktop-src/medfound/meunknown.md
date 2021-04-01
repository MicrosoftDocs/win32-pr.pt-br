---
description: Tipo de evento desconhecido. Você pode usar esse valor para inicializar variáveis do tipo MediaEventType, mas um componente nunca deve gerar o evento MEUnknown.
ms.assetid: 786b69f4-8713-41db-829a-c13512baa3f1
title: Evento MEUnknown (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a768fde2939b7e32ed8d1007d2988c2e54cc6726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921279"
---
# <a name="meunknown-event"></a><span data-ttu-id="9f756-104">Evento MEUnknown</span><span class="sxs-lookup"><span data-stu-id="9f756-104">MEUnknown event</span></span>

<span data-ttu-id="9f756-105">Tipo de evento desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9f756-105">Unknown event type.</span></span> <span data-ttu-id="9f756-106">Você pode usar esse valor para inicializar variáveis do tipo **MediaEventType**, mas um componente nunca deve gerar o evento MEUnknown</span><span class="sxs-lookup"><span data-stu-id="9f756-106">You can use this value to initialize variables of type **MediaEventType**, but a component should never raise the MEUnknown event</span></span>

## <a name="event-values"></a><span data-ttu-id="9f756-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="9f756-107">Event values</span></span>

<span data-ttu-id="9f756-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="9f756-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9f756-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9f756-109">VARTYPE</span></span>              | <span data-ttu-id="9f756-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f756-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="9f756-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="9f756-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="9f756-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="9f756-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="9f756-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f756-113">Requirements</span></span>



| <span data-ttu-id="9f756-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f756-114">Requirement</span></span> | <span data-ttu-id="9f756-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9f756-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f756-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f756-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9f756-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f756-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9f756-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f756-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9f756-119">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9f756-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9f756-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f756-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f756-121"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f756-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f756-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f756-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f756-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9f756-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




