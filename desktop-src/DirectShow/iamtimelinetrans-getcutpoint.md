---
description: O método GetCutPoint recupera o ponto de recorte.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'Método IAMTimelineTrans:: GetCutPoint (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e89cc2e7bc6d18842212a58bc5c00b6424947b66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785486"
---
# <a name="iamtimelinetransgetcutpoint-method"></a><span data-ttu-id="b04e9-103">Método IAMTimelineTrans:: GetCutPoint</span><span class="sxs-lookup"><span data-stu-id="b04e9-103">IAMTimelineTrans::GetCutPoint method</span></span>

> [!Note]  
> <span data-ttu-id="b04e9-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="b04e9-104">\[Deprecated.</span></span> <span data-ttu-id="b04e9-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b04e9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b04e9-106">O `GetCutPoint` método recupera o ponto de recorte.</span><span class="sxs-lookup"><span data-stu-id="b04e9-106">The `GetCutPoint` method retrieves the cut point.</span></span> <span data-ttu-id="b04e9-107">Se você renderizar uma transição como um recorte, o ponto de recorte é o horário em que a transição é recortada de uma origem para a outra.</span><span class="sxs-lookup"><span data-stu-id="b04e9-107">If you render a transition as a cut, the cut point is the time when the transition cuts from one source to the next.</span></span> <span data-ttu-id="b04e9-108">Por padrão, esse valor é o meio da transição.</span><span class="sxs-lookup"><span data-stu-id="b04e9-108">By default, this value is the middle of the transition.</span></span> <span data-ttu-id="b04e9-109">Por exemplo, em uma transição que abrange um segundo, o ponto de recorte padrão é de 0,5 segundos na transição.</span><span class="sxs-lookup"><span data-stu-id="b04e9-109">For example, in a transition that spans one second, the default cut point is 0.5 seconds into the transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="b04e9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b04e9-110">Syntax</span></span>


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="b04e9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b04e9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b04e9-112">*pTLTime*</span><span class="sxs-lookup"><span data-stu-id="b04e9-112">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="b04e9-113">Recebe o ponto de recorte, em relação à hora de início da transição, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="b04e9-113">Receives the cut point, relative to the start time of the transition, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b04e9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b04e9-114">Return value</span></span>

<span data-ttu-id="b04e9-115">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="b04e9-115">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="b04e9-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="b04e9-116">Return code</span></span>                                                                               | <span data-ttu-id="b04e9-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="b04e9-117">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b04e9-118"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="b04e9-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="b04e9-119">O ponto de recorte não foi definido.</span><span class="sxs-lookup"><span data-stu-id="b04e9-119">The cut point was not set.</span></span> <span data-ttu-id="b04e9-120">O valor retornado é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="b04e9-120">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="b04e9-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b04e9-121"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b04e9-122">O ponto de recorte foi definido com um valor diferente do padrão.</span><span class="sxs-lookup"><span data-stu-id="b04e9-122">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="b04e9-123"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b04e9-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b04e9-124">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="b04e9-124">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="b04e9-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b04e9-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b04e9-126">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="b04e9-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b04e9-127">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b04e9-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b04e9-128">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="b04e9-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b04e9-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b04e9-129">Requirements</span></span>



| <span data-ttu-id="b04e9-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="b04e9-130">Requirement</span></span> | <span data-ttu-id="b04e9-131">Valor</span><span class="sxs-lookup"><span data-stu-id="b04e9-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b04e9-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b04e9-132">Header</span></span><br/>  | <dl> <span data-ttu-id="b04e9-133"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="b04e9-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b04e9-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b04e9-134">Library</span></span><br/> | <dl> <span data-ttu-id="b04e9-135"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b04e9-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b04e9-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="b04e9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b04e9-137">**Interface IAMTimelineTrans**</span><span class="sxs-lookup"><span data-stu-id="b04e9-137">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="b04e9-138">**IAMTimelineTrans::SetCutPoint**</span><span class="sxs-lookup"><span data-stu-id="b04e9-138">**IAMTimelineTrans::SetCutPoint**</span></span>](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[<span data-ttu-id="b04e9-139">**IAMTimelineTrans::GetCutsOnly**</span><span class="sxs-lookup"><span data-stu-id="b04e9-139">**IAMTimelineTrans::GetCutsOnly**</span></span>](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[<span data-ttu-id="b04e9-140">**IAMTimeline::TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="b04e9-140">**IAMTimeline::TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)
</dt> <dt>

[<span data-ttu-id="b04e9-141">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="b04e9-141">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




