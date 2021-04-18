---
description: A interface ITMediaCollection fornece acesso ao conjunto de informações de mídia em uma descrição de conferência SDP (RFC 2327).
ms.assetid: a7e7a07d-239e-432e-9984-7763f11c59ce
title: Interface ITMediaCollection (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21305e1d1729437b53c380b7712feee3827b3ba8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767751"
---
# <a name="itmediacollection-interface"></a><span data-ttu-id="5b0eb-103">Interface ITMediaCollection</span><span class="sxs-lookup"><span data-stu-id="5b0eb-103">ITMediaCollection interface</span></span>

<span data-ttu-id="5b0eb-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="5b0eb-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5b0eb-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="5b0eb-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5b0eb-106">A interface **ITMediaCollection** fornece acesso ao conjunto de informações de mídia em uma descrição de conferência SDP (RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="5b0eb-106">The **ITMediaCollection** interface provides access to the set of media information in an SDP (RFC 2327) conference description.</span></span> <span data-ttu-id="5b0eb-107">Cada descrição de mídia no SDP é descrita por uma interface [**ITMedia**](itmedia.md) .</span><span class="sxs-lookup"><span data-stu-id="5b0eb-107">Each Media description in the SDP is described by an [**ITMedia**](itmedia.md) interface.</span></span> <span data-ttu-id="5b0eb-108">O **ITMediaCollection** permite a manipulação do conjunto de informações de **ITMEDIA** para o SDP, incluindo:</span><span class="sxs-lookup"><span data-stu-id="5b0eb-108">**ITMediaCollection** allows manipulation of the set of **ITMedia** information for the SDP, including:</span></span>

-   <span data-ttu-id="5b0eb-109">Permite o acesso à mídia por índice.</span><span class="sxs-lookup"><span data-stu-id="5b0eb-109">Allows media access by index.</span></span>
-   <span data-ttu-id="5b0eb-110">Habilita a criação e a exclusão de mídia.</span><span class="sxs-lookup"><span data-stu-id="5b0eb-110">Enables creation and deletion of media.</span></span>

<span data-ttu-id="5b0eb-111">O método [**ITSdp:: get \_ mediacollection**](itsdp-get-mediacollection.md) cria a interface **ITMediaCollection** .</span><span class="sxs-lookup"><span data-stu-id="5b0eb-111">The [**ITSdp::get\_MediaCollection**](itsdp-get-mediacollection.md) method creates the **ITMediaCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="5b0eb-112">Membros</span><span class="sxs-lookup"><span data-stu-id="5b0eb-112">Members</span></span>

<span data-ttu-id="5b0eb-113">A interface **ITMediaCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="5b0eb-113">The **ITMediaCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="5b0eb-114">**ITMediaCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5b0eb-114">**ITMediaCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="5b0eb-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="5b0eb-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5b0eb-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="5b0eb-116">Methods</span></span>

<span data-ttu-id="5b0eb-117">A interface **ITMediaCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5b0eb-117">The **ITMediaCollection** interface has these methods.</span></span>



| <span data-ttu-id="5b0eb-118">Método</span><span class="sxs-lookup"><span data-stu-id="5b0eb-118">Method</span></span>                                                            | <span data-ttu-id="5b0eb-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b0eb-119">Description</span></span>                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="5b0eb-120">**Criada**</span><span class="sxs-lookup"><span data-stu-id="5b0eb-120">**Create**</span></span>](itmediacollection-create.md)                        | <span data-ttu-id="5b0eb-121">Cria uma nova mídia com propriedades padrão e a retorna.</span><span class="sxs-lookup"><span data-stu-id="5b0eb-121">Creates a new media with default properties and returns it.</span></span><br/> |
| [<span data-ttu-id="5b0eb-122">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="5b0eb-122">**Delete**</span></span>](itmediacollection-delete.md)                        | <span data-ttu-id="5b0eb-123">Exclui a mídia correspondente ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="5b0eb-123">Deletes the media corresponding to the specified index.</span></span><br/>     |
| [<span data-ttu-id="5b0eb-124">**obter \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="5b0eb-124">**get\_\_NewEnum**</span></span>](itmediacollection-get--newenum.md)          | <span data-ttu-id="5b0eb-125">Retorna um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="5b0eb-125">Returns an enumerator for the collection.</span></span><br/>                   |
| [<span data-ttu-id="5b0eb-126">**obter \_ contagem**</span><span class="sxs-lookup"><span data-stu-id="5b0eb-126">**get\_Count**</span></span>](itmediacollection-get-count.md)                 | <span data-ttu-id="5b0eb-127">Obtém o número de mídia na sessão.</span><span class="sxs-lookup"><span data-stu-id="5b0eb-127">Gets the number of media in the session.</span></span><br/>                    |
| [<span data-ttu-id="5b0eb-128">**obter \_ EnumerationIf**</span><span class="sxs-lookup"><span data-stu-id="5b0eb-128">**get\_EnumerationIf**</span></span>](itmediacollection-get-enumerationif.md) | <span data-ttu-id="5b0eb-129">Obtém o ponteiro para a interface de enumeração.</span><span class="sxs-lookup"><span data-stu-id="5b0eb-129">Gets pointer to enumeration interface.</span></span><br/>                      |
| [<span data-ttu-id="5b0eb-130">**obter \_ Item**</span><span class="sxs-lookup"><span data-stu-id="5b0eb-130">**get\_Item**</span></span>](itmediacollection-get-item.md)                   | <span data-ttu-id="5b0eb-131">Retorna a mídia correspondente ao índice especificado.</span><span class="sxs-lookup"><span data-stu-id="5b0eb-131">Returns the media corresponding to the specified index.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="5b0eb-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b0eb-132">Requirements</span></span>



| <span data-ttu-id="5b0eb-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b0eb-133">Requirement</span></span> | <span data-ttu-id="5b0eb-134">Valor</span><span class="sxs-lookup"><span data-stu-id="5b0eb-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b0eb-135">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="5b0eb-135">TAPI version</span></span><br/> | <span data-ttu-id="5b0eb-136">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="5b0eb-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5b0eb-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b0eb-137">Header</span></span><br/>       | <dl> <span data-ttu-id="5b0eb-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b0eb-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b0eb-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5b0eb-139">Library</span></span><br/>      | <dl> <span data-ttu-id="5b0eb-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b0eb-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5b0eb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5b0eb-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="5b0eb-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b0eb-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

