---
description: Tipo de evento personalizado.
ms.assetid: a54a446c-0e96-467b-90f6-0f64a7c1727d
title: Evento MEExtendedType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5551110fc3637a40834a7bf9251826f151ec62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780145"
---
# <a name="meextendedtype-event"></a><span data-ttu-id="26b18-103">Evento MEExtendedType</span><span class="sxs-lookup"><span data-stu-id="26b18-103">MEExtendedType event</span></span>

<span data-ttu-id="26b18-104">Tipo de evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="26b18-104">Custom event type.</span></span> <span data-ttu-id="26b18-105">Você pode usar esse tipo de evento para definir eventos personalizados para seu componente.</span><span class="sxs-lookup"><span data-stu-id="26b18-105">You can use this event type to define custom events for your component.</span></span> <span data-ttu-id="26b18-106">Use o tipo de evento estendido para identificar o evento.</span><span class="sxs-lookup"><span data-stu-id="26b18-106">Use the extended event type to identify the event.</span></span> <span data-ttu-id="26b18-107">O tipo de evento estendido é um valor de GUID associado ao evento.</span><span class="sxs-lookup"><span data-stu-id="26b18-107">The extended event type is a GUID value associated with the event.</span></span> <span data-ttu-id="26b18-108">Para obter mais informações, consulte [**IMFMediaEvent:: getextendedattribute**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span><span class="sxs-lookup"><span data-stu-id="26b18-108">For more information, see [**IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).</span></span>

## <a name="event-values"></a><span data-ttu-id="26b18-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="26b18-109">Event values</span></span>

<span data-ttu-id="26b18-110">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="26b18-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="26b18-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="26b18-111">VARTYPE</span></span>              | <span data-ttu-id="26b18-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="26b18-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="26b18-113">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="26b18-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="26b18-114">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="26b18-114">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="26b18-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26b18-115">Requirements</span></span>



| <span data-ttu-id="26b18-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="26b18-116">Requirement</span></span> | <span data-ttu-id="26b18-117">Valor</span><span class="sxs-lookup"><span data-stu-id="26b18-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26b18-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26b18-118">Minimum supported client</span></span><br/> | <span data-ttu-id="26b18-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26b18-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="26b18-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="26b18-120">Minimum supported server</span></span><br/> | <span data-ttu-id="26b18-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26b18-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="26b18-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="26b18-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="26b18-123"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26b18-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26b18-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="26b18-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26b18-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="26b18-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




