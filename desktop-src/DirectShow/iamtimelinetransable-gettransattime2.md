---
description: 'O método GetTransAtTime2 recupera a transição mais próxima ao horário especificado, de acordo com as condições de limite especificadas. Esse método é equivalente a IAMTimelineTransable:: GetTransAtTime, mas usa um parâmetro REFTIME.'
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'Método IAMTimelineTransable:: GetTransAtTime2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760085"
---
# <a name="iamtimelinetransablegettransattime2-method"></a><span data-ttu-id="96cbe-104">Método IAMTimelineTransable:: GetTransAtTime2</span><span class="sxs-lookup"><span data-stu-id="96cbe-104">IAMTimelineTransable::GetTransAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="96cbe-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="96cbe-105">\[Deprecated.</span></span> <span data-ttu-id="96cbe-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="96cbe-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="96cbe-107">O `GetTransAtTime2` método recupera a transição mais próxima ao horário especificado, de acordo com as condições de limite especificadas.</span><span class="sxs-lookup"><span data-stu-id="96cbe-107">The `GetTransAtTime2` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="96cbe-108">Esse método é equivalente a [**IAMTimelineTransable:: GetTransAtTime**](iamtimelinetransable-gettransattime.md), mas usa um parâmetro [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="96cbe-108">This method is equivalent to [**IAMTimelineTransable::GetTransAtTime**](iamtimelinetransable-gettransattime.md), but takes a [**REFTIME**](reftime.md) parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="96cbe-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96cbe-109">Syntax</span></span>


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="96cbe-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96cbe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96cbe-111">*ppObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="96cbe-111">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96cbe-112">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) da transição.</span><span class="sxs-lookup"><span data-stu-id="96cbe-112">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="96cbe-113">*Hora*</span><span class="sxs-lookup"><span data-stu-id="96cbe-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="96cbe-114">Hora a partir da qual iniciar a pesquisa, em segundos.</span><span class="sxs-lookup"><span data-stu-id="96cbe-114">Time from which to begin the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="96cbe-115">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="96cbe-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="96cbe-116">Membro do tipo enumerado de [**\_ sinalizadores de \_ pesquisa \_ do DEXTERF Track**](dexterf-track-search-flags.md) que especifica as condições de limite para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="96cbe-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96cbe-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96cbe-117">Return value</span></span>

<span data-ttu-id="96cbe-118">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="96cbe-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="96cbe-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="96cbe-119">Return code</span></span>                                                                                  | <span data-ttu-id="96cbe-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="96cbe-120">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="96cbe-121"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="96cbe-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="96cbe-122">Nenhuma transição foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="96cbe-122">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="96cbe-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="96cbe-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="96cbe-124">A transição foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="96cbe-124">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="96cbe-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="96cbe-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="96cbe-126">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="96cbe-126">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="96cbe-127"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="96cbe-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="96cbe-128">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="96cbe-128">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="96cbe-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="96cbe-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="96cbe-130">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="96cbe-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="96cbe-131">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="96cbe-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="96cbe-132">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="96cbe-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="96cbe-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96cbe-133">Requirements</span></span>



| <span data-ttu-id="96cbe-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="96cbe-134">Requirement</span></span> | <span data-ttu-id="96cbe-135">Valor</span><span class="sxs-lookup"><span data-stu-id="96cbe-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96cbe-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96cbe-136">Header</span></span><br/>  | <dl> <span data-ttu-id="96cbe-137"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="96cbe-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="96cbe-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96cbe-138">Library</span></span><br/> | <dl> <span data-ttu-id="96cbe-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96cbe-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96cbe-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="96cbe-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96cbe-141">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="96cbe-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="96cbe-142">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="96cbe-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




