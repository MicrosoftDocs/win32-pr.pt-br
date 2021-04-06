---
description: O fluxo de mídia usa esse evento para enviar metadados específicos do sistema de proteção para o decodificador.
ms.assetid: 249446CA-AEF7-41A1-98EB-0B9392AE4AD8
title: Evento MEContentProtectionMetadata (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1dd72289a900b9c9b96fe9a64d427dab13110d66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827419"
---
# <a name="mecontentprotectionmetadata-event"></a><span data-ttu-id="72f3f-103">Evento MEContentProtectionMetadata</span><span class="sxs-lookup"><span data-stu-id="72f3f-103">MEContentProtectionMetadata event</span></span>

<span data-ttu-id="72f3f-104">O fluxo de mídia usa esse evento para enviar metadados específicos do sistema de proteção para o decodificador.</span><span class="sxs-lookup"><span data-stu-id="72f3f-104">Media Stream uses this event to send protection system specific metadata to the decoder.</span></span>

## <a name="event-values"></a><span data-ttu-id="72f3f-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="72f3f-105">Event values</span></span>

<span data-ttu-id="72f3f-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="72f3f-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="72f3f-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="72f3f-107">VARTYPE</span></span>              | <span data-ttu-id="72f3f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="72f3f-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="72f3f-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="72f3f-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="72f3f-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="72f3f-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="72f3f-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="72f3f-111">Attributes</span></span>

<span data-ttu-id="72f3f-112">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="72f3f-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="72f3f-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="72f3f-113">Attribute</span></span>                                                                                              | <span data-ttu-id="72f3f-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="72f3f-114">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72f3f-115">\_KEYDATA de \_ metadados do fluxo de eventos MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="72f3f-115">MF\_EVENT\_STREAM\_METADATA\_KEYDATA</span></span>](mf-event-stream-metadata-keydata.md)<br/>                | <span data-ttu-id="72f3f-116">Esse é um atributo opcional.</span><span class="sxs-lookup"><span data-stu-id="72f3f-116">This is an optional attribute.</span></span> <span data-ttu-id="72f3f-117">Dados específicos do sistema de proteção.</span><span class="sxs-lookup"><span data-stu-id="72f3f-117">Protection system specific data.</span></span><br/> <br/>              |
| [<span data-ttu-id="72f3f-118">\_KEYIDS de \_ conteúdo de metadados de fluxo de eventos MF \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="72f3f-118">MF\_EVENT\_STREAM\_METADATA\_CONTENT\_KEYIDS</span></span>](mf-event-stream-metadata-content-keyids.md)<br/> | <span data-ttu-id="72f3f-119">IDs de chave de conteúdo com as quais o evento está associado.</span><span class="sxs-lookup"><span data-stu-id="72f3f-119">Content key IDs which the event is associated with.</span></span><br/> <br/>                          |
| [<span data-ttu-id="72f3f-120">\_metadados do fluxo de eventos MF \_ \_ \_ SystemId</span><span class="sxs-lookup"><span data-stu-id="72f3f-120">MF\_EVENT\_STREAM\_METADATA\_SYSTEMID</span></span>](mf-event-stream-metadata-systemid.md)<br/>              | <span data-ttu-id="72f3f-121">Esse é um atributo opcional.</span><span class="sxs-lookup"><span data-stu-id="72f3f-121">This is an optional attribute.</span></span> <span data-ttu-id="72f3f-122">ID do sistema para o qual os dados de chave se destinam.</span><span class="sxs-lookup"><span data-stu-id="72f3f-122">System ID for which the key data is intended.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="72f3f-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="72f3f-123">Remarks</span></span>

<span data-ttu-id="72f3f-124">Esse evento é usado, por exemplo, para comunicar o evento de rotação de chaves.</span><span class="sxs-lookup"><span data-stu-id="72f3f-124">This event is used, for example, for communicating key rotation event.</span></span> <span data-ttu-id="72f3f-125">Nesse caso, ele deve ser enviado o mais cedo possível para dar o tempo decodificador para se preparar antes que os exemplos criptografados com o novo ID de chave comecem a chegar.</span><span class="sxs-lookup"><span data-stu-id="72f3f-125">In this case it should be sent as early as possible to give the decoder time to prepare itself before samples encrypted with the new key ID start arriving.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f3f-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72f3f-126">Requirements</span></span>



| <span data-ttu-id="72f3f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="72f3f-127">Requirement</span></span> | <span data-ttu-id="72f3f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="72f3f-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72f3f-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72f3f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="72f3f-130">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="72f3f-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="72f3f-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72f3f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="72f3f-132">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="72f3f-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="72f3f-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72f3f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="72f3f-134"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72f3f-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72f3f-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="72f3f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72f3f-136">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="72f3f-136">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




