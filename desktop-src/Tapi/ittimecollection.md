---
description: A interface ITTimeCollection é uma interface específica de provedor para o objeto de blob de conferência SDP (Session Descriptor Protocol).
ms.assetid: 6309e9f2-8a73-4d42-ae0a-2165352d6244
title: Interface ITTimeCollection (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19ca297a26b0eac34396726e6145a24fba5a2ed6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760156"
---
# <a name="ittimecollection-interface"></a><span data-ttu-id="533b6-103">Interface ITTimeCollection</span><span class="sxs-lookup"><span data-stu-id="533b6-103">ITTimeCollection interface</span></span>

<span data-ttu-id="533b6-104">\[ Os controles e as interfaces da conferência de telefonia IP de reunião não estão disponíveis para uso no Windows Vista, no Windows Server 2008 e nas versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="533b6-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="533b6-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="533b6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="533b6-106">A interface **ITTimeCollection** é uma interface específica de provedor para o objeto de blob de conferência SDP (Session Descriptor Protocol).</span><span class="sxs-lookup"><span data-stu-id="533b6-106">The **ITTimeCollection** interface is a provider-specific interface for the Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="533b6-107">Essa interface permite o acesso a interfaces [**ITTime**](ittime.md) por índice e também permite a criação e a exclusão de componentes de tempo.</span><span class="sxs-lookup"><span data-stu-id="533b6-107">This interface allows access to [**ITTime**](ittime.md) interfaces by index, and also enable the creation and deletion of time components.</span></span> <span data-ttu-id="533b6-108">O método [**ITSdp:: get \_ timecollection**](itsdp-get-timecollection.md) cria a interface **ITTimeCollection** .</span><span class="sxs-lookup"><span data-stu-id="533b6-108">The [**ITSdp::get\_TimeCollection**](itsdp-get-timecollection.md) method creates the **ITTimeCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="533b6-109">Membros</span><span class="sxs-lookup"><span data-stu-id="533b6-109">Members</span></span>

<span data-ttu-id="533b6-110">A interface **ITTimeCollection** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="533b6-110">The **ITTimeCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="533b6-111">**ITTimeCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="533b6-111">**ITTimeCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="533b6-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="533b6-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="533b6-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="533b6-113">Methods</span></span>

<span data-ttu-id="533b6-114">A interface **ITTimeCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="533b6-114">The **ITTimeCollection** interface has these methods.</span></span>



| <span data-ttu-id="533b6-115">Método</span><span class="sxs-lookup"><span data-stu-id="533b6-115">Method</span></span>                                                           | <span data-ttu-id="533b6-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="533b6-116">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="533b6-117">**Criada**</span><span class="sxs-lookup"><span data-stu-id="533b6-117">**Create**</span></span>](ittimecollection-create.md)                        | <span data-ttu-id="533b6-118">Cria um componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="533b6-118">Creates an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="533b6-119">**Apagar**</span><span class="sxs-lookup"><span data-stu-id="533b6-119">**Delete**</span></span>](ittimecollection-delete.md)                        | <span data-ttu-id="533b6-120">Exclui um componente [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="533b6-120">Deletes an [**ITTime**](ittime.md) component.</span></span><br/>                                                             |
| [<span data-ttu-id="533b6-121">**obter \_ \_ NewEnum**</span><span class="sxs-lookup"><span data-stu-id="533b6-121">**get\_\_NewEnum**</span></span>](ittimecollection-get--newenum.md)          | <span data-ttu-id="533b6-122">Retorna um enumerador para a coleção.</span><span class="sxs-lookup"><span data-stu-id="533b6-122">Returns an enumerator for the collection.</span></span><br/>                                                                  |
| [<span data-ttu-id="533b6-123">**obter \_ contagem**</span><span class="sxs-lookup"><span data-stu-id="533b6-123">**get\_Count**</span></span>](ittimecollection-get-count.md)                 | <span data-ttu-id="533b6-124">Obtém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="533b6-124">Gets number of items in collection.</span></span><br/>                                                                        |
| [<span data-ttu-id="533b6-125">**obter \_ EnumerationIf**</span><span class="sxs-lookup"><span data-stu-id="533b6-125">**get\_EnumerationIf**</span></span>](ittimecollection-get-enumerationif.md) | <span data-ttu-id="533b6-126">Retorna a interface de enumeração [**IEnumTime**](ienumtime.md) que enumera [**ITTime**](ittime.md).</span><span class="sxs-lookup"><span data-stu-id="533b6-126">Returns the [**IEnumTime**](ienumtime.md) enumeration interface that enumerates [**ITTime**](ittime.md).</span></span><br/> |
| [<span data-ttu-id="533b6-127">**obter \_ Item**</span><span class="sxs-lookup"><span data-stu-id="533b6-127">**get\_Item**</span></span>](ittimecollection-get-item.md)                   | <span data-ttu-id="533b6-128">Dado um índice, retorna um item na coleção.</span><span class="sxs-lookup"><span data-stu-id="533b6-128">Given an index, returns an item in the collection.</span></span><br/>                                                         |



 

## <a name="requirements"></a><span data-ttu-id="533b6-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="533b6-129">Requirements</span></span>



| <span data-ttu-id="533b6-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="533b6-130">Requirement</span></span> | <span data-ttu-id="533b6-131">Valor</span><span class="sxs-lookup"><span data-stu-id="533b6-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="533b6-132">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="533b6-132">TAPI version</span></span><br/> | <span data-ttu-id="533b6-133">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="533b6-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="533b6-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="533b6-134">Header</span></span><br/>       | <dl> <span data-ttu-id="533b6-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="533b6-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="533b6-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="533b6-136">Library</span></span><br/>      | <dl> <span data-ttu-id="533b6-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="533b6-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="533b6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="533b6-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="533b6-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="533b6-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

