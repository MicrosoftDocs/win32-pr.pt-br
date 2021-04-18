---
description: A interface ITParticipant é implementada pelo IPConf MSP. Ele permite que um aplicativo recupere informações sobre os participantes da conferência e obtenha ponteiros para os fluxos associados a esses participantes.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Interface ITParticipant (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781047"
---
# <a name="itparticipant-interface"></a><span data-ttu-id="b9ef5-104">Interface ITParticipant</span><span class="sxs-lookup"><span data-stu-id="b9ef5-104">ITParticipant interface</span></span>

<span data-ttu-id="b9ef5-105">\[O **ITParticipant** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b9ef5-105">\[**ITParticipant** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b9ef5-106">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b9ef5-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b9ef5-107">A interface **ITParticipant** é implementada pelo [IPConf MSP](ipconf-msp.md).</span><span class="sxs-lookup"><span data-stu-id="b9ef5-107">The **ITParticipant** interface is implemented by the [IPConf MSP](ipconf-msp.md).</span></span> <span data-ttu-id="b9ef5-108">Ele permite que um aplicativo recupere informações sobre os participantes da conferência e obtenha ponteiros para os fluxos associados a esses participantes.</span><span class="sxs-lookup"><span data-stu-id="b9ef5-108">It allows an application to retrieve information on conference participants, and get pointers to the streams associated with those participants.</span></span>

<span data-ttu-id="b9ef5-109">Essa interface é exposta no objeto de chamada quando uma chamada usa a conferência de IP.</span><span class="sxs-lookup"><span data-stu-id="b9ef5-109">This interface is exposed on the call object when a call uses the IP Conferencing.</span></span> <span data-ttu-id="b9ef5-110">Um ponteiro pode ser obtido chamando **QueryInterface** usando um ponteiro [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .</span><span class="sxs-lookup"><span data-stu-id="b9ef5-110">A pointer can be obtained by calling **QueryInterface** using an [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) pointer.</span></span>

## <a name="members"></a><span data-ttu-id="b9ef5-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b9ef5-111">Members</span></span>

<span data-ttu-id="b9ef5-112">A interface **ITParticipant** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b9ef5-112">The **ITParticipant** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b9ef5-113">**ITParticipant** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b9ef5-113">**ITParticipant** also has these types of members:</span></span>

-   [<span data-ttu-id="b9ef5-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9ef5-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b9ef5-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="b9ef5-115">Methods</span></span>

<span data-ttu-id="b9ef5-116">A interface **ITParticipant** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b9ef5-116">The **ITParticipant** interface has these methods.</span></span>



| <span data-ttu-id="b9ef5-117">Método</span><span class="sxs-lookup"><span data-stu-id="b9ef5-117">Method</span></span>                                                                      | <span data-ttu-id="b9ef5-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9ef5-118">Description</span></span>                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9ef5-119">**EnumerateStreams**</span><span class="sxs-lookup"><span data-stu-id="b9ef5-119">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)                  | <span data-ttu-id="b9ef5-120">Enumera os fluxos associados ao participante atual.</span><span class="sxs-lookup"><span data-stu-id="b9ef5-120">Enumerates streams associated with the current participant.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="b9ef5-121">**obter \_ MediaTypes**</span><span class="sxs-lookup"><span data-stu-id="b9ef5-121">**get\_MediaTypes**</span></span>](itparticipant-get-mediatypes.md)                     | <span data-ttu-id="b9ef5-122">Obtém os [**tipos de mídia**](tapimediatype--constants.md) associados a um participante.</span><span class="sxs-lookup"><span data-stu-id="b9ef5-122">Gets the [**media types**](tapimediatype--constants.md) associated with a participant.</span></span><br/>                                                                      |
| [<span data-ttu-id="b9ef5-123">**obter \_ ParticipantTypedInfo**</span><span class="sxs-lookup"><span data-stu-id="b9ef5-123">**get\_ParticipantTypedInfo**</span></span>](itparticipant-get-participanttypedinfo.md) | <span data-ttu-id="b9ef5-124">Obtém uma representação BSTR do tipo de informações necessário, como PTI \_ EmailAddress.</span><span class="sxs-lookup"><span data-stu-id="b9ef5-124">Gets a BSTR representation of the needed type of information, such as PTI\_EMAILADDRESS.</span></span><br/>                                                                     |
| [<span data-ttu-id="b9ef5-125">**obter \_ status**</span><span class="sxs-lookup"><span data-stu-id="b9ef5-125">**get\_Status**</span></span>](itparticipant-get-status.md)                             | <span data-ttu-id="b9ef5-126">Obtém o status do participante.</span><span class="sxs-lookup"><span data-stu-id="b9ef5-126">Gets the status of the participant.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="b9ef5-127">**obter \_ fluxos**</span><span class="sxs-lookup"><span data-stu-id="b9ef5-127">**get\_Streams**</span></span>](itparticipant-get-streams.md)                           | <span data-ttu-id="b9ef5-128">Cria uma coleção de fluxos associados ao participante atual.</span><span class="sxs-lookup"><span data-stu-id="b9ef5-128">Creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="b9ef5-129">Fornecido para aplicativos cliente de automação, como aqueles escritos em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b9ef5-129">Provided for Automation client applications, such as those written in Visual Basic.</span></span><br/> |
| [<span data-ttu-id="b9ef5-130">**Status de Put \_**</span><span class="sxs-lookup"><span data-stu-id="b9ef5-130">**put\_Status**</span></span>](itparticipant-put-status.md)                             | <span data-ttu-id="b9ef5-131">Define se um fluxo associado ao participante está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b9ef5-131">Sets whether a stream associated with the participant is enabled.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="b9ef5-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9ef5-132">Requirements</span></span>



| <span data-ttu-id="b9ef5-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9ef5-133">Requirement</span></span> | <span data-ttu-id="b9ef5-134">Valor</span><span class="sxs-lookup"><span data-stu-id="b9ef5-134">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b9ef5-135">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b9ef5-135">TAPI version</span></span><br/> | <span data-ttu-id="b9ef5-136">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b9ef5-136">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="b9ef5-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9ef5-137">Header</span></span><br/>       | <dl> <span data-ttu-id="b9ef5-138"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9ef5-138"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9ef5-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b9ef5-139">Library</span></span><br/>      | <dl> <span data-ttu-id="b9ef5-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9ef5-140"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="b9ef5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b9ef5-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="b9ef5-142"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9ef5-142"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9ef5-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9ef5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9ef5-144">IPConf MSP</span><span class="sxs-lookup"><span data-stu-id="b9ef5-144">IPConf MSP</span></span>](ipconf-msp.md)
</dt> <dt>

[<span data-ttu-id="b9ef5-145">Interfaces MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="b9ef5-145">IPConf MSP Interfaces</span></span>](ipconf-msp-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b9ef5-146">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="b9ef5-146">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

