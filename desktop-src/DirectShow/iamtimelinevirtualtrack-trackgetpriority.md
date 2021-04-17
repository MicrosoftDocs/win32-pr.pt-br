---
description: O método TrackGetPriority recupera o nível de prioridade do objeto.
ms.assetid: f9a138e8-e9ad-4703-bdcc-c64aea4fbad0
title: 'Método IAMTimelineVirtualTrack:: TrackGetPriority (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineVirtualTrack.TrackGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 08b43fa34848e5dac41d22281c08d25ee9065831
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760084"
---
# <a name="iamtimelinevirtualtracktrackgetpriority-method"></a><span data-ttu-id="5611e-103">Método IAMTimelineVirtualTrack:: TrackGetPriority</span><span class="sxs-lookup"><span data-stu-id="5611e-103">IAMTimelineVirtualTrack::TrackGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="5611e-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5611e-104">\[Deprecated.</span></span> <span data-ttu-id="5611e-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5611e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5611e-106">O `TrackGetPriority` método recupera o nível de prioridade do objeto.</span><span class="sxs-lookup"><span data-stu-id="5611e-106">The `TrackGetPriority` method retrieves the object's priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="5611e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5611e-107">Syntax</span></span>


```C++
HRESULT TrackGetPriority(
   long *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="5611e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5611e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5611e-109">*pPriority*</span><span class="sxs-lookup"><span data-stu-id="5611e-109">*pPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="5611e-110">Ponteiro para uma variável que recebe o nível de prioridade.</span><span class="sxs-lookup"><span data-stu-id="5611e-110">Pointer to a variable that receives the priority level.</span></span> <span data-ttu-id="5611e-111">Se o objeto não fizer parte de uma linha do tempo, o valor será definido como – 1.</span><span class="sxs-lookup"><span data-stu-id="5611e-111">If the object is not part of a timeline, the value is set to –1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5611e-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5611e-112">Return value</span></span>

<span data-ttu-id="5611e-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5611e-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5611e-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5611e-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5611e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="5611e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5611e-116">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="5611e-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5611e-117">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5611e-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5611e-118">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5611e-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5611e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5611e-119">Requirements</span></span>



| <span data-ttu-id="5611e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5611e-120">Requirement</span></span> | <span data-ttu-id="5611e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5611e-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5611e-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5611e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5611e-123"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5611e-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5611e-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5611e-124">Library</span></span><br/> | <dl> <span data-ttu-id="5611e-125"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5611e-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5611e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5611e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5611e-127">**Interface IAMTimelineVirtualTrack**</span><span class="sxs-lookup"><span data-stu-id="5611e-127">**IAMTimelineVirtualTrack Interface**</span></span>](iamtimelinevirtualtrack.md)
</dt> <dt>

[<span data-ttu-id="5611e-128">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="5611e-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




