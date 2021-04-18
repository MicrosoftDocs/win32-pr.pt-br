---
description: 'O método GetSrcAtTime2 recupera o objeto de origem mais próximo ao tempo especificado, de acordo com as condições de limite especificadas. Esse método é equivalente a IAMTimelineTrack:: GetSrcAtTime, mas usa um valor de REFTIME.'
ms.assetid: 11f6545b-478b-4ffd-8344-2bf8585db2a5
title: 'Método IAMTimelineTrack:: GetSrcAtTime2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7140644f64c66b204d6a50cb8e88cb5beca41dae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758678"
---
# <a name="iamtimelinetrackgetsrcattime2-method"></a><span data-ttu-id="ee828-104">Método IAMTimelineTrack:: GetSrcAtTime2</span><span class="sxs-lookup"><span data-stu-id="ee828-104">IAMTimelineTrack::GetSrcAtTime2 method</span></span>

> [!Note]  
> <span data-ttu-id="ee828-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="ee828-105">\[Deprecated.</span></span> <span data-ttu-id="ee828-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ee828-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="ee828-107">O `GetSrcAtTime2` método recupera o objeto de origem mais próximo ao tempo especificado, de acordo com as condições de limite especificadas.</span><span class="sxs-lookup"><span data-stu-id="ee828-107">The `GetSrcAtTime2` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span> <span data-ttu-id="ee828-108">Esse método é equivalente a [**IAMTimelineTrack:: GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), mas usa um valor de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="ee828-108">This method is equivalent to [**IAMTimelineTrack::GetSrcAtTime**](iamtimelinetrack-getsrcattime.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee828-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee828-109">Syntax</span></span>


```C++
HRESULT GetSrcAtTime2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="ee828-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee828-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee828-111">*ppSrc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee828-111">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee828-112">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="ee828-112">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="ee828-113">*Hora*</span><span class="sxs-lookup"><span data-stu-id="ee828-113">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="ee828-114">Hora de início da pesquisa, em segundos.</span><span class="sxs-lookup"><span data-stu-id="ee828-114">Start time for the search, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="ee828-115">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="ee828-115">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="ee828-116">Membro do tipo enumerado de [**\_ sinalizadores de \_ pesquisa \_ do DEXTERF Track**](dexterf-track-search-flags.md) que especifica as condições de limite para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="ee828-116">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee828-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee828-117">Return value</span></span>

<span data-ttu-id="ee828-118">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="ee828-118">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="ee828-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ee828-119">Return code</span></span>                                                                                  | <span data-ttu-id="ee828-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee828-120">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="ee828-121"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="ee828-121"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="ee828-122">Não foi localizado um objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="ee828-122">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="ee828-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ee828-123"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="ee828-124">Um objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="ee828-124">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="ee828-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ee828-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ee828-126">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="ee828-126">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="ee828-127"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="ee828-127"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="ee828-128">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="ee828-128">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="ee828-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee828-129">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ee828-130">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="ee828-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="ee828-131">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="ee828-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="ee828-132">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="ee828-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ee828-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee828-133">Requirements</span></span>



| <span data-ttu-id="ee828-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee828-134">Requirement</span></span> | <span data-ttu-id="ee828-135">Valor</span><span class="sxs-lookup"><span data-stu-id="ee828-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee828-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee828-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ee828-137"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee828-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="ee828-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee828-138">Library</span></span><br/> | <dl> <span data-ttu-id="ee828-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee828-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee828-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee828-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee828-141">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="ee828-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="ee828-142">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="ee828-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




