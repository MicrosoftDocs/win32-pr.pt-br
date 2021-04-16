---
description: A interface IAMTimelineSplittable divide um objeto de linha do tempo em DES (serviços de edição do DirectShow). Fontes, efeitos, transições e faixas implementam essa interface.
ms.assetid: bb066d34-0ffd-495f-83ce-59ad054a7782
title: Interface IAMTimelineSplittable (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7b9544809068029b4ca583e83831f9b18ac84e44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758841"
---
# <a name="iamtimelinesplittable-interface"></a><span data-ttu-id="9ec84-104">Interface IAMTimelineSplittable</span><span class="sxs-lookup"><span data-stu-id="9ec84-104">IAMTimelineSplittable interface</span></span>

> [!Note]  
> <span data-ttu-id="9ec84-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="9ec84-105">\[Deprecated.</span></span> <span data-ttu-id="9ec84-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="9ec84-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9ec84-107">A `IAMTimelineSplittable` interface divide um objeto Timeline em [serviços de edição do DirectShow](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="9ec84-107">The `IAMTimelineSplittable` interface splits a timeline object in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="9ec84-108">Fontes, efeitos, transições e faixas implementam essa interface.</span><span class="sxs-lookup"><span data-stu-id="9ec84-108">Sources, effects, transitions, and tracks implement this interface.</span></span>

## <a name="members"></a><span data-ttu-id="9ec84-109">Membros</span><span class="sxs-lookup"><span data-stu-id="9ec84-109">Members</span></span>

<span data-ttu-id="9ec84-110">A interface **IAMTimelineSplittable** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9ec84-110">The **IAMTimelineSplittable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9ec84-111">**IAMTimelineSplittable** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9ec84-111">**IAMTimelineSplittable** also has these types of members:</span></span>

-   [<span data-ttu-id="9ec84-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9ec84-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9ec84-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="9ec84-113">Methods</span></span>

<span data-ttu-id="9ec84-114">A interface **IAMTimelineSplittable** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9ec84-114">The **IAMTimelineSplittable** interface has these methods.</span></span>



| <span data-ttu-id="9ec84-115">Método</span><span class="sxs-lookup"><span data-stu-id="9ec84-115">Method</span></span>                                             | <span data-ttu-id="9ec84-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="9ec84-116">Description</span></span>                                                                                          |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9ec84-117">**SplitAt**</span><span class="sxs-lookup"><span data-stu-id="9ec84-117">**SplitAt**</span></span>](iamtimelinesplittable-splitat.md)   | <span data-ttu-id="9ec84-118">Divide o objeto na hora especificada.</span><span class="sxs-lookup"><span data-stu-id="9ec84-118">Splits the object at the specified time.</span></span><br/>                                                  |
| [<span data-ttu-id="9ec84-119">**SplitAt2**</span><span class="sxs-lookup"><span data-stu-id="9ec84-119">**SplitAt2**</span></span>](iamtimelinesplittable-splitat2.md) | <span data-ttu-id="9ec84-120">Divide o objeto na hora especificada, especificado como um valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="9ec84-120">Splits the object at the specified time, specified as a [**REFTIME**](reftime.md) value.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9ec84-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ec84-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9ec84-122">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="9ec84-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9ec84-123">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="9ec84-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9ec84-124">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="9ec84-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9ec84-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ec84-125">Requirements</span></span>



| <span data-ttu-id="9ec84-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ec84-126">Requirement</span></span> | <span data-ttu-id="9ec84-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9ec84-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec84-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ec84-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9ec84-129"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ec84-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9ec84-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9ec84-130">Library</span></span><br/> | <dl> <span data-ttu-id="9ec84-131"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ec84-131"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
