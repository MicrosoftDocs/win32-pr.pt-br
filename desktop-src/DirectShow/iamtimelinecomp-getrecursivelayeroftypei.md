---
description: 'Não há suporte. Em vez disso, chame o método IAMTimelineComp:: GetRecursiveLayerOfType.'
ms.assetid: 857f57e2-6123-43c3-bb74-62afd0fc0b52
title: 'Método IAMTimelineComp:: GetRecursiveLayerOfTypeI (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetRecursiveLayerOfTypeI
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8aded93aa0753ee8dddf173262c80678e28037a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759446"
---
# <a name="iamtimelinecompgetrecursivelayeroftypei-method"></a><span data-ttu-id="62ce2-104">Método IAMTimelineComp:: GetRecursiveLayerOfTypeI</span><span class="sxs-lookup"><span data-stu-id="62ce2-104">IAMTimelineComp::GetRecursiveLayerOfTypeI method</span></span>

> [!Note]  
> <span data-ttu-id="62ce2-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="62ce2-105">\[Deprecated.</span></span> <span data-ttu-id="62ce2-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="62ce2-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="62ce2-107">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="62ce2-107">Not supported.</span></span> <span data-ttu-id="62ce2-108">Em vez disso, chame o método [**IAMTimelineComp:: GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) .</span><span class="sxs-lookup"><span data-stu-id="62ce2-108">Call the [**IAMTimelineComp::GetRecursiveLayerOfType**](iamtimelinecomp-getrecursivelayeroftype.md) method instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ce2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62ce2-109">Syntax</span></span>


```C++
HRESULT GetRecursiveLayerOfTypeI(
   IAMTimelineObj      **ppVirtualTrack,
   long                **pWhichLayer,
   TIMELINE_MAJOR_TYPE Type
);
```



## <a name="parameters"></a><span data-ttu-id="62ce2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62ce2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62ce2-111">*ppVirtualTrack*</span><span class="sxs-lookup"><span data-stu-id="62ce2-111">*ppVirtualTrack*</span></span> 
</dt> <dd>

<span data-ttu-id="62ce2-112">Reservado.</span><span class="sxs-lookup"><span data-stu-id="62ce2-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="62ce2-113">*pWhichLayer*</span><span class="sxs-lookup"><span data-stu-id="62ce2-113">*pWhichLayer*</span></span> 
</dt> <dd>

<span data-ttu-id="62ce2-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="62ce2-114">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="62ce2-115">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="62ce2-115">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="62ce2-116">Reservado.</span><span class="sxs-lookup"><span data-stu-id="62ce2-116">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62ce2-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62ce2-117">Return value</span></span>

<span data-ttu-id="62ce2-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="62ce2-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="62ce2-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="62ce2-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="62ce2-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="62ce2-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="62ce2-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="62ce2-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="62ce2-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="62ce2-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="62ce2-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="62ce2-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="62ce2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62ce2-124">Requirements</span></span>



| <span data-ttu-id="62ce2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="62ce2-125">Requirement</span></span> | <span data-ttu-id="62ce2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="62ce2-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62ce2-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62ce2-127">Header</span></span><br/>  | <dl> <span data-ttu-id="62ce2-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="62ce2-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="62ce2-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="62ce2-129">Library</span></span><br/> | <dl> <span data-ttu-id="62ce2-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="62ce2-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62ce2-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="62ce2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ce2-132">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="62ce2-132">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> </dl>

 

 




