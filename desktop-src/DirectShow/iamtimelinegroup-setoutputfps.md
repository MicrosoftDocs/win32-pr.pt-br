---
description: O método SetOutputFPS define a taxa de quadros de saída não compactados para esse grupo.
ms.assetid: 335ea106-d5db-43a1-b771-b027e25164a6
title: 'Método IAMTimelineGroup:: SetOutputFPS (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineGroup.SetOutputFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bbec5de572dd2ed2a0e6b3062b208f1084bafd07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760089"
---
# <a name="iamtimelinegroupsetoutputfps-method"></a><span data-ttu-id="516e1-103">Método IAMTimelineGroup:: SetOutputFPS</span><span class="sxs-lookup"><span data-stu-id="516e1-103">IAMTimelineGroup::SetOutputFPS method</span></span>

> [!Note]  
> <span data-ttu-id="516e1-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="516e1-104">\[Deprecated.</span></span> <span data-ttu-id="516e1-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="516e1-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="516e1-106">O `SetOutputFPS` método define a taxa de quadros de saída não compactados para esse grupo.</span><span class="sxs-lookup"><span data-stu-id="516e1-106">The `SetOutputFPS` method sets the uncompressed output frame rate for this group.</span></span>

## <a name="syntax"></a><span data-ttu-id="516e1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="516e1-107">Syntax</span></span>


```C++
HRESULT SetOutputFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="516e1-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="516e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="516e1-109">*QUADROS*</span><span class="sxs-lookup"><span data-stu-id="516e1-109">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="516e1-110">Taxa de quadros de saída para este grupo, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="516e1-110">Output frame rate for this group, in frames per second.</span></span> <span data-ttu-id="516e1-111">O valor não pode ser igual a zero e não pode ter mais de sete dígitos após a casa decimal.</span><span class="sxs-lookup"><span data-stu-id="516e1-111">The value cannot equal zero, and cannot have more than seven digits after the decimal place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="516e1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="516e1-112">Return value</span></span>

<span data-ttu-id="516e1-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="516e1-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="516e1-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="516e1-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="516e1-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="516e1-115">Remarks</span></span>

<span data-ttu-id="516e1-116">A saída renderizada desse grupo é executada na taxa de quadros especificada e todas as edições no material de origem são arredondadas para o limite de quadro mais próximo, conforme definido pela taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="516e1-116">Rendered output from this group runs at the specified frame rate, and all edits on the source material are rounded to the nearest frame boundary, as defined by the frame rate.</span></span> <span data-ttu-id="516e1-117">Para obter o melhor desempenho, use a mesma taxa de quadros para todos os grupos, vídeo e áudio.</span><span class="sxs-lookup"><span data-stu-id="516e1-117">For best performance, use the same frame rate for all groups, video and audio.</span></span>

<span data-ttu-id="516e1-118">O método [**IAMTimelineGroup:: SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) substitui a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="516e1-118">The [**IAMTimelineGroup::SetSmartRecompressFormat**](iamtimelinegroup-setsmartrecompressformat.md) method overwrites the frame rate.</span></span>

> [!Note]  
> <span data-ttu-id="516e1-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="516e1-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="516e1-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="516e1-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="516e1-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="516e1-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="516e1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="516e1-122">Requirements</span></span>



| <span data-ttu-id="516e1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="516e1-123">Requirement</span></span> | <span data-ttu-id="516e1-124">Valor</span><span class="sxs-lookup"><span data-stu-id="516e1-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="516e1-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="516e1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="516e1-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="516e1-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="516e1-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="516e1-127">Library</span></span><br/> | <dl> <span data-ttu-id="516e1-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="516e1-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="516e1-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="516e1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="516e1-130">**Interface IAMTimelineGroup**</span><span class="sxs-lookup"><span data-stu-id="516e1-130">**IAMTimelineGroup Interface**</span></span>](iamtimelinegroup.md)
</dt> <dt>

[<span data-ttu-id="516e1-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="516e1-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




