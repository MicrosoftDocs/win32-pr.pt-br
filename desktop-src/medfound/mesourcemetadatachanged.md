---
description: Gerado por uma origem de mídia quando ele atualiza seus metadados.
ms.assetid: 6818b0c9-9628-41e6-8dc6-dff26f4fcfd2
title: Evento MESourceMetadataChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b72463d145d7b4b4b14ac3c321f19a7f9a4c2178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921033"
---
# <a name="mesourcemetadatachanged-event"></a><span data-ttu-id="a7ba0-103">Evento MESourceMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="a7ba0-103">MESourceMetadataChanged event</span></span>

<span data-ttu-id="a7ba0-104">Gerado por uma origem de mídia quando ele atualiza seus metadados.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-104">Raised by a media source when it updates its metadata.</span></span>

## <a name="event-values"></a><span data-ttu-id="a7ba0-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="a7ba0-105">Event values</span></span>

<span data-ttu-id="a7ba0-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a7ba0-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a7ba0-107">VARTYPE</span></span>              | <span data-ttu-id="a7ba0-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7ba0-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="a7ba0-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="a7ba0-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="a7ba0-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a7ba0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7ba0-111">Remarks</span></span>

<span data-ttu-id="a7ba0-112">Se a origem da mídia não puder fornecer todos os metadados quando a origem for criada pela primeira vez, ele deverá gerar esse evento depois que os metadados estiverem disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-112">If the media source cannot provide all of the metadata when the source is first created, it should raise this event after the metadata is available.</span></span>

<span data-ttu-id="a7ba0-113">A origem da mídia deve criar um novo descritor de apresentação e copiar todos os atributos do descritor de apresentação (PD) para o objeto de evento.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-113">The media source should create a new presentation descriptor and copy all of the attributes from the presentation descriptor (PD) to the event object.</span></span> <span data-ttu-id="a7ba0-114">O aplicativo pode usar o objeto de evento para enumerar os novos atributos de PD.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-114">The application can use the event object to enumerate the new PD attributes.</span></span> <span data-ttu-id="a7ba0-115">Em particular, os valores para [a \_ \_ duração do MF PD](mf-pd-duration-attribute.md) e o [ \_ \_ \_ \_ Tamanho total do arquivo MF PD](mf-pd-total-file-size-attribute.md) podem ser desconhecidos até que o arquivo seja completamente baixado.</span><span class="sxs-lookup"><span data-stu-id="a7ba0-115">In particular, the values for [MF\_PD\_DURATION](mf-pd-duration-attribute.md) and [MF\_PD\_TOTAL\_FILE\_SIZE](mf-pd-total-file-size-attribute.md) might be unknown until the file is completely downloaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7ba0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7ba0-116">Requirements</span></span>



| <span data-ttu-id="a7ba0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7ba0-117">Requirement</span></span> | <span data-ttu-id="a7ba0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a7ba0-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ba0-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7ba0-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a7ba0-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7ba0-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a7ba0-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7ba0-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a7ba0-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a7ba0-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a7ba0-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7ba0-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7ba0-124"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7ba0-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7ba0-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7ba0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ba0-126">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a7ba0-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="a7ba0-127">Atributos do descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="a7ba0-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




