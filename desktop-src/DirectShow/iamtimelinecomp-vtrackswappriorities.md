---
description: O método VTrackSwapPriorities alterna os níveis de prioridade de duas faixas.
ms.assetid: 87085060-5165-4c32-b5b0-895ae487e7ef
title: 'Método IAMTimelineComp:: VTrackSwapPriorities (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.VTrackSwapPriorities
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: df90fe3f4c481f454c6cc743f09de9538a2c892d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758845"
---
# <a name="iamtimelinecompvtrackswappriorities-method"></a><span data-ttu-id="ba165-103">Método IAMTimelineComp:: VTrackSwapPriorities</span><span class="sxs-lookup"><span data-stu-id="ba165-103">IAMTimelineComp::VTrackSwapPriorities method</span></span>

> [!Note]  
> <span data-ttu-id="ba165-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="ba165-104">\[Deprecated.</span></span> <span data-ttu-id="ba165-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ba165-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ba165-106">O `VTrackSwapPriorities` método alterna os níveis de prioridade de duas faixas.</span><span class="sxs-lookup"><span data-stu-id="ba165-106">The `VTrackSwapPriorities` method switches the priority levels of two tracks.</span></span>

<span data-ttu-id="ba165-107">Considerando dois níveis de prioridade, esse método alterna as faixas virtuais nessas prioridades.</span><span class="sxs-lookup"><span data-stu-id="ba165-107">Given two priority levels, this method switches the virtual tracks at those priorities.</span></span> <span data-ttu-id="ba165-108">Quando o método retorna, a faixa que estava no primeiro nível de prioridade é agora no segundo nível de prioridade, e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="ba165-108">When the method returns, the track that was at the first priority level is now at the second priority level, and vice versa.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba165-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba165-109">Syntax</span></span>


```C++
HRESULT VTrackSwapPriorities(
   long VirtualTrackA,
   long VirtualTrackB
);
```



## <a name="parameters"></a><span data-ttu-id="ba165-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba165-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba165-111">*VirtualTrackA*</span><span class="sxs-lookup"><span data-stu-id="ba165-111">*VirtualTrackA*</span></span> 
</dt> <dd>

<span data-ttu-id="ba165-112">Primeiro nível de prioridade no qual trocar faixas virtuais.</span><span class="sxs-lookup"><span data-stu-id="ba165-112">First priority level at which to swap virtual tracks.</span></span>

</dd> <dt>

<span data-ttu-id="ba165-113">*VirtualTrackB*</span><span class="sxs-lookup"><span data-stu-id="ba165-113">*VirtualTrackB*</span></span> 
</dt> <dd>

<span data-ttu-id="ba165-114">Segundo nível de prioridade no qual trocar faixas virtuais.</span><span class="sxs-lookup"><span data-stu-id="ba165-114">Second priority level at which to swap virtual tracks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba165-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba165-115">Return value</span></span>

<span data-ttu-id="ba165-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ba165-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ba165-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ba165-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba165-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba165-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ba165-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="ba165-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ba165-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ba165-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ba165-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ba165-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ba165-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba165-122">Requirements</span></span>



| <span data-ttu-id="ba165-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba165-123">Requirement</span></span> | <span data-ttu-id="ba165-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ba165-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba165-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba165-125">Header</span></span><br/>  | <dl> <span data-ttu-id="ba165-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba165-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ba165-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba165-127">Library</span></span><br/> | <dl> <span data-ttu-id="ba165-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba165-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba165-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba165-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba165-130">**Interface IAMTimelineComp**</span><span class="sxs-lookup"><span data-stu-id="ba165-130">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="ba165-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="ba165-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




