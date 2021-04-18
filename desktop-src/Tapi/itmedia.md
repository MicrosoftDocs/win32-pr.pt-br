---
description: A interface ITMedia é uma representação de mídia em um protocolo de descritor de sessão (SDP, consulte RFC 2327).
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: Interface ITMedia (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757213"
---
# <a name="itmedia-interface"></a><span data-ttu-id="9deba-103">Interface ITMedia</span><span class="sxs-lookup"><span data-stu-id="9deba-103">ITMedia interface</span></span>

<span data-ttu-id="9deba-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9deba-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9deba-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="9deba-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9deba-106">A interface **ITMedia** é uma representação de mídia em um protocolo de descritor de sessão (SDP, consulte RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="9deba-106">The **ITMedia** interface is a representation of media in a Session Descriptor Protocol (SDP, see RFC 2327).</span></span> <span data-ttu-id="9deba-107">Essa interface exporta métodos para obter e definir propriedades básicas de mídia, como tipo.</span><span class="sxs-lookup"><span data-stu-id="9deba-107">This interface exports methods to get and set basic media properties, such as type.</span></span> <span data-ttu-id="9deba-108">Os métodos [**ITMediaCollection:: get \_ Item**](itmediacollection-get-item.md) e [**ITMediaCollection:: Create**](itmediacollection-create.md) criam a interface **ITMedia** .</span><span class="sxs-lookup"><span data-stu-id="9deba-108">The [**ITMediaCollection::get\_Item**](itmediacollection-get-item.md) and [**ITMediaCollection::Create**](itmediacollection-create.md) methods create the **ITMedia** interface.</span></span>

## <a name="members"></a><span data-ttu-id="9deba-109">Membros</span><span class="sxs-lookup"><span data-stu-id="9deba-109">Members</span></span>

<span data-ttu-id="9deba-110">A interface **ITMedia** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="9deba-110">The **ITMedia** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9deba-111">**ITMedia** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9deba-111">**ITMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="9deba-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9deba-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9deba-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="9deba-113">Methods</span></span>

<span data-ttu-id="9deba-114">A interface **ITMedia** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9deba-114">The **ITMedia** interface has these methods.</span></span>



| <span data-ttu-id="9deba-115">Método</span><span class="sxs-lookup"><span data-stu-id="9deba-115">Method</span></span>                                                          | <span data-ttu-id="9deba-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9deba-116">Description</span></span>                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9deba-117">**obter \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="9deba-117">**get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)             | <span data-ttu-id="9deba-118">Obtém a lista de códigos de formato de carga de mídia.</span><span class="sxs-lookup"><span data-stu-id="9deba-118">Gets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="9deba-119">**obter \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="9deba-119">**get\_MediaName**</span></span>](itmedia-get-medianame.md)                 | <span data-ttu-id="9deba-120">Obtém o nome da mídia.</span><span class="sxs-lookup"><span data-stu-id="9deba-120">Gets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="9deba-121">**obter \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="9deba-121">**get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)               | <span data-ttu-id="9deba-122">Obtém o título da mídia.</span><span class="sxs-lookup"><span data-stu-id="9deba-122">Gets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="9deba-123">**obter \_ NumPorts**</span><span class="sxs-lookup"><span data-stu-id="9deba-123">**get\_NumPorts**</span></span>](itmedia-get-numports.md)                   | <span data-ttu-id="9deba-124">Obtém o número de portas necessárias para a sessão.</span><span class="sxs-lookup"><span data-stu-id="9deba-124">Gets the number of ports needed for the session.</span></span><br/>                                      |
| [<span data-ttu-id="9deba-125">**obter \_ StartPort**</span><span class="sxs-lookup"><span data-stu-id="9deba-125">**get\_StartPort**</span></span>](itmedia-get-startport.md)                 | <span data-ttu-id="9deba-126">Obtém o valor da porta de 16 bits para a primeira porta.</span><span class="sxs-lookup"><span data-stu-id="9deba-126">Gets the 16-bit port value for the first port.</span></span><br/>                                        |
| [<span data-ttu-id="9deba-127">**obter \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="9deba-127">**get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md) | <span data-ttu-id="9deba-128">Obtém o protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="9deba-128">Gets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="9deba-129">**colocar \_ FormatCodes**</span><span class="sxs-lookup"><span data-stu-id="9deba-129">**put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)             | <span data-ttu-id="9deba-130">Define a lista de códigos de formato de carga de mídia.</span><span class="sxs-lookup"><span data-stu-id="9deba-130">Sets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="9deba-131">**colocar \_ MediaName**</span><span class="sxs-lookup"><span data-stu-id="9deba-131">**put\_MediaName**</span></span>](itmedia-put-medianame.md)                 | <span data-ttu-id="9deba-132">Define o nome da mídia.</span><span class="sxs-lookup"><span data-stu-id="9deba-132">Sets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="9deba-133">**colocar \_ MediaTitle**</span><span class="sxs-lookup"><span data-stu-id="9deba-133">**put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)               | <span data-ttu-id="9deba-134">Define o título da mídia.</span><span class="sxs-lookup"><span data-stu-id="9deba-134">Sets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="9deba-135">**colocar \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="9deba-135">**put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md) | <span data-ttu-id="9deba-136">Define o protocolo de transporte.</span><span class="sxs-lookup"><span data-stu-id="9deba-136">Sets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="9deba-137">**SetPortInfo**</span><span class="sxs-lookup"><span data-stu-id="9deba-137">**SetPortInfo**</span></span>](itmedia-setportinfo.md)                      | <span data-ttu-id="9deba-138">Define o valor da porta de 16 bits para a primeira porta e o número de portas necessárias para a sessão.</span><span class="sxs-lookup"><span data-stu-id="9deba-138">Sets the 16-bit port value for the first port and number of ports needed for session.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9deba-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9deba-139">Requirements</span></span>



| <span data-ttu-id="9deba-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9deba-140">Requirement</span></span> | <span data-ttu-id="9deba-141">Valor</span><span class="sxs-lookup"><span data-stu-id="9deba-141">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9deba-142">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="9deba-142">TAPI version</span></span><br/> | <span data-ttu-id="9deba-143">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="9deba-143">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="9deba-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9deba-144">Header</span></span><br/>       | <dl> <span data-ttu-id="9deba-145"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="9deba-145"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="9deba-146">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9deba-146">Library</span></span><br/>      | <dl> <span data-ttu-id="9deba-147"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9deba-147"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="9deba-148">DLL</span><span class="sxs-lookup"><span data-stu-id="9deba-148">DLL</span></span><br/>          | <dl> <span data-ttu-id="9deba-149"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9deba-149"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9deba-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="9deba-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9deba-151">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="9deba-151">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="9deba-152">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="9deba-152">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="9deba-153">**ITSDP**</span><span class="sxs-lookup"><span data-stu-id="9deba-153">**ITSDP**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="9deba-154">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="9deba-154">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

