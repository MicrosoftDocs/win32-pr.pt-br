---
description: 'O método SetDefaultFPS define a taxa de quadros de saída padrão, em quadros por segundo. Os grupos usam esse valor como sua taxa de quadros padrão. Para definir a taxa de quadros de um grupo, chame o método IAMTimelineGroup:: SetOutputFPS no grupo.'
ms.assetid: a164f4b9-fbed-45ea-9156-cc64f0b21423
title: 'Método IAMTimeline:: SetDefaultFPS (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetDefaultFPS
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 20c352f40234672ceeb2d4c25ea9db04e89f712d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782846"
---
# <a name="iamtimelinesetdefaultfps-method"></a><span data-ttu-id="d80be-105">Método IAMTimeline:: SetDefaultFPS</span><span class="sxs-lookup"><span data-stu-id="d80be-105">IAMTimeline::SetDefaultFPS method</span></span>

> [!Note]  
> <span data-ttu-id="d80be-106">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d80be-106">\[Deprecated.</span></span> <span data-ttu-id="d80be-107">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d80be-107">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d80be-108">O `SetDefaultFPS` método define a taxa de quadros de saída padrão, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="d80be-108">The `SetDefaultFPS` method sets the default output frame rate, in frames per second.</span></span> <span data-ttu-id="d80be-109">Os grupos usam esse valor como sua taxa de quadros padrão.</span><span class="sxs-lookup"><span data-stu-id="d80be-109">Groups use this value as their default frame rate.</span></span> <span data-ttu-id="d80be-110">Para definir a taxa de quadros de um grupo, chame o método [**IAMTimelineGroup:: SetOutputFPS**](iamtimelinegroup-setoutputfps.md) no grupo.</span><span class="sxs-lookup"><span data-stu-id="d80be-110">To set a group's frame rate, call the [**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md) method on the group.</span></span>

## <a name="syntax"></a><span data-ttu-id="d80be-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d80be-111">Syntax</span></span>


```C++
HRESULT SetDefaultFPS(
   double FPS
);
```



## <a name="parameters"></a><span data-ttu-id="d80be-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d80be-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d80be-113">*QUADROS*</span><span class="sxs-lookup"><span data-stu-id="d80be-113">*FPS*</span></span> 
</dt> <dd>

<span data-ttu-id="d80be-114">Taxa de quadros padrão, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="d80be-114">Default frame rate, in frames per second.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d80be-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d80be-115">Return value</span></span>

<span data-ttu-id="d80be-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d80be-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d80be-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d80be-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d80be-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d80be-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d80be-119">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d80be-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d80be-120">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d80be-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d80be-121">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d80be-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d80be-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d80be-122">Requirements</span></span>



| <span data-ttu-id="d80be-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d80be-123">Requirement</span></span> | <span data-ttu-id="d80be-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d80be-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d80be-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d80be-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d80be-126"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d80be-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d80be-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d80be-127">Library</span></span><br/> | <dl> <span data-ttu-id="d80be-128"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d80be-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d80be-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d80be-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d80be-130">**Interface IAMTimeline**</span><span class="sxs-lookup"><span data-stu-id="d80be-130">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> <dt>

[<span data-ttu-id="d80be-131">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="d80be-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




