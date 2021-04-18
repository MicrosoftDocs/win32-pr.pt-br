---
description: A interface IAMTimelineTransable adiciona transições a um objeto nos serviços de edição do DirectShow (DES).
ms.assetid: 1be9adaa-4145-447c-b307-dabb4419c86c
title: Interface IAMTimelineTransable (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d083b768e8dcf54236945755f4b26ecf13409b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792547"
---
# <a name="iamtimelinetransable-interface"></a><span data-ttu-id="5205a-103">Interface IAMTimelineTransable</span><span class="sxs-lookup"><span data-stu-id="5205a-103">IAMTimelineTransable interface</span></span>

> [!Note]  
> <span data-ttu-id="5205a-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5205a-104">\[Deprecated.</span></span> <span data-ttu-id="5205a-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5205a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5205a-106">A `IAMTimelineTransable` interface adiciona transições a um objeto nos [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="5205a-106">The `IAMTimelineTransable` interface adds transitions to an object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="5205a-107">Essa interface é exposta por qualquer objeto que possa ter transições aplicadas a ela, incluindo faixas, composições e grupos.</span><span class="sxs-lookup"><span data-stu-id="5205a-107">This interface is exposed by any object that can have transitions applied to it, including tracks, compositions, and groups.</span></span> <span data-ttu-id="5205a-108">Um objeto que implementa essa interface pode ter qualquer número de transições, mas as transições não devem se sobrepor no tempo.</span><span class="sxs-lookup"><span data-stu-id="5205a-108">An object that implements this interface can have any number of transitions, but the transitions must not overlap in time.</span></span>

> [!Note]  
> <span data-ttu-id="5205a-109">O áudio não oferece suporte a transições.</span><span class="sxs-lookup"><span data-stu-id="5205a-109">Audio does not support transitions.</span></span> <span data-ttu-id="5205a-110">Os objetos nos grupos de áudio podem expor a `IAMTimelineTransable` interface, mas o aplicativo não deve adicionar transições a eles.</span><span class="sxs-lookup"><span data-stu-id="5205a-110">Objects within audio groups can expose the `IAMTimelineTransable` interface, but the application should not add transitions to them.</span></span>

 

## <a name="members"></a><span data-ttu-id="5205a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="5205a-111">Members</span></span>

<span data-ttu-id="5205a-112">A interface **IAMTimelineTransable** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5205a-112">The **IAMTimelineTransable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5205a-113">**IAMTimelineTransable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5205a-113">**IAMTimelineTransable** also has these types of members:</span></span>

-   [<span data-ttu-id="5205a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="5205a-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5205a-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="5205a-115">Methods</span></span>

<span data-ttu-id="5205a-116">A interface **IAMTimelineTransable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5205a-116">The **IAMTimelineTransable** interface has these methods.</span></span>



| <span data-ttu-id="5205a-117">Método</span><span class="sxs-lookup"><span data-stu-id="5205a-117">Method</span></span>                                                          | <span data-ttu-id="5205a-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5205a-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5205a-119">**GetNextTrans**</span><span class="sxs-lookup"><span data-stu-id="5205a-119">**GetNextTrans**</span></span>](iamtimelinetransable-getnexttrans.md)       | <span data-ttu-id="5205a-120">Recupera a primeira transição que aparece na hora especificada ou posteriormente.</span><span class="sxs-lookup"><span data-stu-id="5205a-120">Retrieves the first transition that appears at the specified time or later.</span></span><br/>                                             |
| [<span data-ttu-id="5205a-121">**GetNextTrans2**</span><span class="sxs-lookup"><span data-stu-id="5205a-121">**GetNextTrans2**</span></span>](iamtimelinetransable-getnexttrans2.md)     | <span data-ttu-id="5205a-122">Recupera a primeira transição que aparece na hora especificada ou posteriormente, com o tempo fornecido como um valor de **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="5205a-122">Retrieves the first transition that appears at the specified time or later, with the time given as a **REFTIME** value.</span></span><br/> |
| [<span data-ttu-id="5205a-123">**GetTransAtTime**</span><span class="sxs-lookup"><span data-stu-id="5205a-123">**GetTransAtTime**</span></span>](iamtimelinetransable-gettransattime.md)   | <span data-ttu-id="5205a-124">Recupera a transição mais próxima ao tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="5205a-124">Retrieves the transition nearest to the specified time.</span></span><br/>                                                                 |
| [<span data-ttu-id="5205a-125">**GetTransAtTime2**</span><span class="sxs-lookup"><span data-stu-id="5205a-125">**GetTransAtTime2**</span></span>](iamtimelinetransable-gettransattime2.md) | <span data-ttu-id="5205a-126">Recupera a transição mais próxima ao tempo especificado, dado como um valor **REFTIME** .</span><span class="sxs-lookup"><span data-stu-id="5205a-126">Retrieves the transition nearest to the specified time, given as a **REFTIME** value.</span></span><br/>                                   |
| [<span data-ttu-id="5205a-127">**TransAdd**</span><span class="sxs-lookup"><span data-stu-id="5205a-127">**TransAdd**</span></span>](iamtimelinetransable-transadd.md)               | <span data-ttu-id="5205a-128">Adiciona uma transição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="5205a-128">Adds a transition to the object.</span></span><br/>                                                                                        |
| [<span data-ttu-id="5205a-129">**TransGetCount**</span><span class="sxs-lookup"><span data-stu-id="5205a-129">**TransGetCount**</span></span>](iamtimelinetransable-transgetcount.md)     | <span data-ttu-id="5205a-130">Recupera o número de transições neste objeto.</span><span class="sxs-lookup"><span data-stu-id="5205a-130">Retrieves the number of transitions on this object.</span></span><br/>                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="5205a-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="5205a-131">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5205a-132">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="5205a-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5205a-133">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5205a-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5205a-134">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5205a-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5205a-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5205a-135">Requirements</span></span>



| <span data-ttu-id="5205a-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5205a-136">Requirement</span></span> | <span data-ttu-id="5205a-137">Valor</span><span class="sxs-lookup"><span data-stu-id="5205a-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5205a-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5205a-138">Header</span></span><br/>  | <dl> <span data-ttu-id="5205a-139"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5205a-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5205a-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5205a-140">Library</span></span><br/> | <dl> <span data-ttu-id="5205a-141"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5205a-141"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
