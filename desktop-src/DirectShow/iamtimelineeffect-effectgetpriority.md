---
description: O método EffectGetPriority recupera o nível de prioridade do efeito. Para um determinado objeto, o mecanismo de renderização aplica efeitos em ordem de prioridade, começando com o nível de prioridade zero.
ms.assetid: 2504fa0c-f052-4d99-98c3-803b0c0d49e5
title: 'Método IAMTimelineEffect:: EffectGetPriority (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffect.EffectGetPriority
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 26ea9795e3ffe36a75c354e51ff2f7e64fae40ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782845"
---
# <a name="iamtimelineeffecteffectgetpriority-method"></a><span data-ttu-id="757ce-104">Método IAMTimelineEffect:: EffectGetPriority</span><span class="sxs-lookup"><span data-stu-id="757ce-104">IAMTimelineEffect::EffectGetPriority method</span></span>

> [!Note]  
> <span data-ttu-id="757ce-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="757ce-105">\[Deprecated.</span></span> <span data-ttu-id="757ce-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="757ce-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="757ce-107">O `EffectGetPriority` método recupera o nível de prioridade do efeito.</span><span class="sxs-lookup"><span data-stu-id="757ce-107">The `EffectGetPriority` method retrieves the effect's priority level.</span></span> <span data-ttu-id="757ce-108">Para um determinado objeto, o mecanismo de renderização aplica efeitos em ordem de prioridade, começando com o nível de prioridade zero.</span><span class="sxs-lookup"><span data-stu-id="757ce-108">For a given object, the render engine applies effects in order of priority, starting with priority level zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="757ce-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="757ce-109">Syntax</span></span>


```C++
HRESULT EffectGetPriority(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="757ce-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="757ce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="757ce-111">*pVal*</span><span class="sxs-lookup"><span data-stu-id="757ce-111">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="757ce-112">Recebe o nível de prioridade.</span><span class="sxs-lookup"><span data-stu-id="757ce-112">Receives the priority level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="757ce-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="757ce-113">Return value</span></span>

<span data-ttu-id="757ce-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="757ce-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="757ce-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="757ce-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="757ce-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="757ce-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="757ce-117">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="757ce-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="757ce-118">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="757ce-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="757ce-119">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="757ce-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="757ce-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="757ce-120">Requirements</span></span>



| <span data-ttu-id="757ce-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="757ce-121">Requirement</span></span> | <span data-ttu-id="757ce-122">Valor</span><span class="sxs-lookup"><span data-stu-id="757ce-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="757ce-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="757ce-123">Header</span></span><br/>  | <dl> <span data-ttu-id="757ce-124"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="757ce-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="757ce-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="757ce-125">Library</span></span><br/> | <dl> <span data-ttu-id="757ce-126"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="757ce-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="757ce-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="757ce-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="757ce-128">**Interface IAMTimelineEffect**</span><span class="sxs-lookup"><span data-stu-id="757ce-128">**IAMTimelineEffect Interface**</span></span>](iamtimelineeffect.md)
</dt> <dt>

[<span data-ttu-id="757ce-129">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="757ce-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




