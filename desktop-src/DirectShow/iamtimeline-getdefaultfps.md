---
description: 'O método GetDefaultFPS recupera a taxa de quadros de saída padrão, em quadros por segundo (FPS). Os grupos usam esse valor como sua taxa de quadros padrão. Para definir a taxa de quadros de um grupo, chame o método IAMTimelineGroup:: SetOutputFPS no grupo.'
ms.assetid: 91c83512-4295-440e-b3b2-09fe3629f827
title: 'Método IAMTimeline:: GetDefaultFPS (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.GetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4e1e6aef61a34831571de345c8dd18c7aeef474d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757295"
---
# <a name="iamtimelinegetdefaultfps-method"></a><span data-ttu-id="41d64-105">Método IAMTimeline:: GetDefaultFPS</span><span class="sxs-lookup"><span data-stu-id="41d64-105">IAMTimeline::GetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="41d64-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="41d64-106">\[Deprecated.</span></span> <span data-ttu-id="41d64-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="41d64-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="41d64-108">O `GetDefaultFPS` método recupera a taxa de quadros de saída padrão, em quadros por segundo (FPS).</span><span class="sxs-lookup"><span data-stu-id="41d64-108">The `GetDefaultFPS` method retrieves the default output frame rate, in frames per second (FPS).</span></span> <span data-ttu-id="41d64-109">Os grupos usam esse valor como sua taxa de quadros padrão.</span><span class="sxs-lookup"><span data-stu-id="41d64-109">Groups use this value as their default frame rate.</span></span> <span data-ttu-id="41d64-110">Para definir a taxa de quadros de um grupo, chame o método [**IAMTimelineGroup:: SetOutputFPS**](iamtimelinegroup-setoutputfps.md) no grupo.</span><span class="sxs-lookup"><span data-stu-id="41d64-110">To set a group's frame rate, call the [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) method on the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="41d64-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="41d64-111">Syntax</span></span>


```C++
HRESULT GetDefaultFPS(
   double *pFPS
);
```



## <a name="parameters"></a><span data-ttu-id="41d64-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="41d64-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41d64-113">*pFPS*</span><span class="sxs-lookup"><span data-stu-id="41d64-113">*pFPS*</span></span> 
</dt> <dd>

<span data-ttu-id="41d64-114">Recebe a taxa de quadros padrão, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="41d64-114">Receives the default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41d64-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="41d64-115">Return value</span></span>

<span data-ttu-id="41d64-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="41d64-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="41d64-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="41d64-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="41d64-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="41d64-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="41d64-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="41d64-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="41d64-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="41d64-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="41d64-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="41d64-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="41d64-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41d64-122">Requirements</span></span>



| <span data-ttu-id="41d64-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="41d64-123">Requirement</span></span> | <span data-ttu-id="41d64-124">Valor</span><span class="sxs-lookup"><span data-stu-id="41d64-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="41d64-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="41d64-125">Header</span></span><br/>  | <dl> <span data-ttu-id="41d64-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="41d64-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="41d64-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="41d64-127">Library</span></span><br/> | <dl> <span data-ttu-id="41d64-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="41d64-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41d64-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="41d64-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41d64-130">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="41d64-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="41d64-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="41d64-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




