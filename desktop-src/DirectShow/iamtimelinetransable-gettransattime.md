---
description: O método GetTransAtTime recupera a transição mais próxima ao horário especificado, de acordo com as condições de limite especificadas.
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: 'Método IAMTimelineTransable:: GetTransAtTime (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 77ca7b1c9a5517d849b38ba1ba22216583d7af87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759437"
---
# <a name="iamtimelinetransablegettransattime-method"></a><span data-ttu-id="a2587-103">Método IAMTimelineTransable:: GetTransAtTime</span><span class="sxs-lookup"><span data-stu-id="a2587-103">IAMTimelineTransable::GetTransAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="a2587-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="a2587-104">\[Deprecated.</span></span> <span data-ttu-id="a2587-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a2587-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a2587-106">O `GetTransAtTime` método recupera a transição mais próxima ao horário especificado, de acordo com as condições de limite especificadas.</span><span class="sxs-lookup"><span data-stu-id="a2587-106">The `GetTransAtTime` method retrieves the transition nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2587-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2587-107">Syntax</span></span>


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="a2587-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2587-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2587-109">*ppObj* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a2587-109">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2587-110">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) da transição.</span><span class="sxs-lookup"><span data-stu-id="a2587-110">Receives a pointer to the transition's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="a2587-111">*Hora*</span><span class="sxs-lookup"><span data-stu-id="a2587-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="a2587-112">Hora a partir da qual iniciar a pesquisa, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="a2587-112">Time from which to begin the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="a2587-113">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="a2587-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="a2587-114">Membro do tipo enumerado de [**\_ sinalizadores de \_ pesquisa \_ do DEXTERF Track**](dexterf-track-search-flags.md) que especifica as condições de limite para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a2587-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2587-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2587-115">Return value</span></span>

<span data-ttu-id="a2587-116">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="a2587-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="a2587-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="a2587-117">Return code</span></span>                                                                                  | <span data-ttu-id="a2587-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2587-118">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="a2587-119"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="a2587-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="a2587-120">Nenhuma transição foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2587-120">No transition was found.</span></span><br/>   |
| <dl> <span data-ttu-id="a2587-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a2587-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a2587-122">A transição foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="a2587-122">Transition was found.</span></span><br/>      |
| <dl> <span data-ttu-id="a2587-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a2587-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a2587-124">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="a2587-124">Invalid argument.</span></span><br/>          |
| <dl> <span data-ttu-id="a2587-125"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="a2587-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="a2587-126">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="a2587-126">**NULL** pointer argument.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a2587-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2587-127">Remarks</span></span>

<span data-ttu-id="a2587-128">Se o método retornar S \_ OK, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="a2587-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="a2587-129">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="a2587-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="a2587-130">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="a2587-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a2587-131">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a2587-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a2587-132">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a2587-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a2587-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2587-133">Requirements</span></span>



| <span data-ttu-id="a2587-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2587-134">Requirement</span></span> | <span data-ttu-id="a2587-135">Valor</span><span class="sxs-lookup"><span data-stu-id="a2587-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a2587-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2587-136">Header</span></span><br/>  | <dl> <span data-ttu-id="a2587-137"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2587-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a2587-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2587-138">Library</span></span><br/> | <dl> <span data-ttu-id="a2587-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2587-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2587-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2587-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2587-141">**Interface IAMTimelineTransable**</span><span class="sxs-lookup"><span data-stu-id="a2587-141">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="a2587-142">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="a2587-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




