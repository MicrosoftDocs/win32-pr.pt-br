---
description: A interface IAMTimelineVirtualTrack fornece métodos para trabalhar com faixas virtuais em serviços de edição do DirectShow (DES). Composições e faixas dão suporte a essa interface.
ms.assetid: 69d1d2ea-d33f-406d-a9ca-ddfb890bed34
title: Interface IAMTimelineVirtualTrack (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2295f1c336270818242f0d992a369e6a66f9237a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779841"
---
# <a name="iamtimelinevirtualtrack-interface"></a><span data-ttu-id="33f1b-104">Interface IAMTimelineVirtualTrack</span><span class="sxs-lookup"><span data-stu-id="33f1b-104">IAMTimelineVirtualTrack interface</span></span>

> [!Note]  
> <span data-ttu-id="33f1b-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="33f1b-105">\[Deprecated.</span></span> <span data-ttu-id="33f1b-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="33f1b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="33f1b-107">A `IAMTimelineVirtualTrack` interface fornece métodos para trabalhar com faixas virtuais em des ( [serviços de edição do DirectShow](directshow-editing-services.md) ).</span><span class="sxs-lookup"><span data-stu-id="33f1b-107">The `IAMTimelineVirtualTrack` interface provides methods for working with virtual tracks in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="33f1b-108">Composições e faixas dão suporte a essa interface.</span><span class="sxs-lookup"><span data-stu-id="33f1b-108">Compositions and tracks support this interface.</span></span>

## <a name="members"></a><span data-ttu-id="33f1b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="33f1b-109">Members</span></span>

<span data-ttu-id="33f1b-110">A interface **IAMTimelineVirtualTrack** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="33f1b-110">The **IAMTimelineVirtualTrack** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="33f1b-111">**IAMTimelineVirtualTrack** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="33f1b-111">**IAMTimelineVirtualTrack** also has these types of members:</span></span>

-   [<span data-ttu-id="33f1b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="33f1b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="33f1b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="33f1b-113">Methods</span></span>

<span data-ttu-id="33f1b-114">A interface **IAMTimelineVirtualTrack** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="33f1b-114">The **IAMTimelineVirtualTrack** interface has these methods.</span></span>



| <span data-ttu-id="33f1b-115">Método</span><span class="sxs-lookup"><span data-stu-id="33f1b-115">Method</span></span>                                                               | <span data-ttu-id="33f1b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="33f1b-116">Description</span></span>                                       |
|:---------------------------------------------------------------------|:--------------------------------------------------|
| [<span data-ttu-id="33f1b-117">**SetTrackDirty**</span><span class="sxs-lookup"><span data-stu-id="33f1b-117">**SetTrackDirty**</span></span>](iamtimelinevirtualtrack-settrackdirty.md)       | <span data-ttu-id="33f1b-118">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="33f1b-118">Not supported.</span></span><br/>                         |
| [<span data-ttu-id="33f1b-119">**TrackGetPriority**</span><span class="sxs-lookup"><span data-stu-id="33f1b-119">**TrackGetPriority**</span></span>](iamtimelinevirtualtrack-trackgetpriority.md) | <span data-ttu-id="33f1b-120">Recupera o nível de prioridade do objeto.</span><span class="sxs-lookup"><span data-stu-id="33f1b-120">Retrieves the object's priority level.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="33f1b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="33f1b-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="33f1b-122">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="33f1b-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="33f1b-123">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="33f1b-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="33f1b-124">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="33f1b-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="33f1b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33f1b-125">Requirements</span></span>



| <span data-ttu-id="33f1b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="33f1b-126">Requirement</span></span> | <span data-ttu-id="33f1b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="33f1b-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33f1b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33f1b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="33f1b-129"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="33f1b-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="33f1b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33f1b-130">Library</span></span><br/> | <dl> <span data-ttu-id="33f1b-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33f1b-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
