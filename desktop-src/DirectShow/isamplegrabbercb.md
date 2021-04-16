---
description: 'A interface ISampleGrabberCB fornece métodos de retorno de chamada para o método ISampleGrabber:: SetCallback. Se seu aplicativo chamar esse método, ele deverá implementar essa interface. Para obter mais informações, consulte ISampleGrabber.'
ms.assetid: 30166d1b-cc37-43c4-8f64-681d8f2013b9
title: Interface ISampleGrabberCB (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabberCB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5c39d11e6560bc5e50a4c8a9b42a1cbb095b4b71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758463"
---
# <a name="isamplegrabbercb-interface"></a><span data-ttu-id="793ee-105">Interface ISampleGrabberCB</span><span class="sxs-lookup"><span data-stu-id="793ee-105">ISampleGrabberCB interface</span></span>

> [!Note]  
> <span data-ttu-id="793ee-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="793ee-106">\[Deprecated.</span></span> <span data-ttu-id="793ee-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="793ee-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="793ee-108">A `ISampleGrabberCB` interface fornece métodos de retorno de chamada para o método [**ISampleGrabber:: SetCallback**](isamplegrabber-setcallback.md) .</span><span class="sxs-lookup"><span data-stu-id="793ee-108">The `ISampleGrabberCB` interface provides callback methods for the [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) method.</span></span> <span data-ttu-id="793ee-109">Se seu aplicativo chamar esse método, ele deverá implementar essa interface.</span><span class="sxs-lookup"><span data-stu-id="793ee-109">If your application calls that method, it must implement this interface.</span></span> <span data-ttu-id="793ee-110">Para obter mais informações, consulte [**ISampleGrabber**](isamplegrabber.md).</span><span class="sxs-lookup"><span data-stu-id="793ee-110">For more information, see [**ISampleGrabber**](isamplegrabber.md).</span></span>

## <a name="members"></a><span data-ttu-id="793ee-111">Membros</span><span class="sxs-lookup"><span data-stu-id="793ee-111">Members</span></span>

<span data-ttu-id="793ee-112">A interface **ISampleGrabberCB** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="793ee-112">The **ISampleGrabberCB** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="793ee-113">**ISampleGrabberCB** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="793ee-113">**ISampleGrabberCB** also has these types of members:</span></span>

-   [<span data-ttu-id="793ee-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="793ee-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="793ee-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="793ee-115">Methods</span></span>

<span data-ttu-id="793ee-116">A interface **ISampleGrabberCB** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="793ee-116">The **ISampleGrabberCB** interface has these methods.</span></span>



| <span data-ttu-id="793ee-117">Método</span><span class="sxs-lookup"><span data-stu-id="793ee-117">Method</span></span>                                        | <span data-ttu-id="793ee-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="793ee-118">Description</span></span>                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="793ee-119">**BufferCB**</span><span class="sxs-lookup"><span data-stu-id="793ee-119">**BufferCB**</span></span>](isamplegrabbercb-buffercb.md) | <span data-ttu-id="793ee-120">Método de retorno de chamada que recebe um ponteiro para o buffer de exemplo.</span><span class="sxs-lookup"><span data-stu-id="793ee-120">Callback method that receives a pointer to the sample buffer.</span></span><br/> |
| [<span data-ttu-id="793ee-121">**SampleCB**</span><span class="sxs-lookup"><span data-stu-id="793ee-121">**SampleCB**</span></span>](isamplegrabbercb-samplecb.md) | <span data-ttu-id="793ee-122">Método de retorno de chamada que recebe um ponteiro para o exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="793ee-122">Callback method that receives a pointer to the media sample.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="793ee-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="793ee-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="793ee-124">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="793ee-124">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="793ee-125">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="793ee-125">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="793ee-126">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="793ee-126">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="793ee-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="793ee-127">Requirements</span></span>



| <span data-ttu-id="793ee-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="793ee-128">Requirement</span></span> | <span data-ttu-id="793ee-129">Valor</span><span class="sxs-lookup"><span data-stu-id="793ee-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="793ee-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="793ee-130">Header</span></span><br/>  | <dl> <span data-ttu-id="793ee-131"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="793ee-131"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="793ee-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="793ee-132">Library</span></span><br/> | <dl> <span data-ttu-id="793ee-133"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="793ee-133"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
