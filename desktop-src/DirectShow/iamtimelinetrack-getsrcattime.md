---
description: O método GetSrcAtTime recupera o objeto de origem mais próximo ao tempo especificado, de acordo com as condições de limite especificadas.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: 'Método IAMTimelineTrack:: GetSrcAtTime (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b726d26efd0550df364200a27d536d60d38274a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757884"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a><span data-ttu-id="36f4b-103">Método IAMTimelineTrack:: GetSrcAtTime</span><span class="sxs-lookup"><span data-stu-id="36f4b-103">IAMTimelineTrack::GetSrcAtTime method</span></span>

> [!Note]  
> <span data-ttu-id="36f4b-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="36f4b-104">\[Deprecated.</span></span> <span data-ttu-id="36f4b-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="36f4b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="36f4b-106">O `GetSrcAtTime` método recupera o objeto de origem mais próximo ao tempo especificado, de acordo com as condições de limite especificadas.</span><span class="sxs-lookup"><span data-stu-id="36f4b-106">The `GetSrcAtTime` method retrieves the source object nearest to the specified time, according to the specified boundary conditions.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f4b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36f4b-107">Syntax</span></span>


```C++
HRESULT GetSrcAtTime(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a><span data-ttu-id="36f4b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36f4b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36f4b-109">*ppSrc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="36f4b-109">*ppSrc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="36f4b-110">Recebe um ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="36f4b-110">Receives a pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object.</span></span>

</dd> <dt>

<span data-ttu-id="36f4b-111">*Hora*</span><span class="sxs-lookup"><span data-stu-id="36f4b-111">*Time*</span></span> 
</dt> <dd>

<span data-ttu-id="36f4b-112">Hora de início da pesquisa, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="36f4b-112">Start time for the search, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="36f4b-113">*SearchDirection*</span><span class="sxs-lookup"><span data-stu-id="36f4b-113">*SearchDirection*</span></span> 
</dt> <dd>

<span data-ttu-id="36f4b-114">Membro do tipo enumerado de [**\_ sinalizadores de \_ pesquisa \_ do DEXTERF Track**](dexterf-track-search-flags.md) que especifica as condições de limite para a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="36f4b-114">Member of the [**DEXTERF\_TRACK\_SEARCH\_FLAGS**](dexterf-track-search-flags.md) enumerated type that specifies the boundary conditions for the search.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36f4b-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36f4b-115">Return value</span></span>

<span data-ttu-id="36f4b-116">Retorna um dos seguintes valores de **HRESULT** :</span><span class="sxs-lookup"><span data-stu-id="36f4b-116">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="36f4b-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="36f4b-117">Return code</span></span>                                                                                  | <span data-ttu-id="36f4b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="36f4b-118">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="36f4b-119"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="36f4b-119"><dt>**S\_FALSE**</dt></span></span> </dl>      | <span data-ttu-id="36f4b-120">Não foi localizado um objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="36f4b-120">Did not locate a source object.</span></span><br/> |
| <dl> <span data-ttu-id="36f4b-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="36f4b-121"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="36f4b-122">Um objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="36f4b-122">Located a source object.</span></span><br/>        |
| <dl> <span data-ttu-id="36f4b-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="36f4b-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="36f4b-124">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="36f4b-124">Invalid argument.</span></span><br/>               |
| <dl> <span data-ttu-id="36f4b-125"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="36f4b-125"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="36f4b-126">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="36f4b-126">**NULL** pointer argument.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="36f4b-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="36f4b-127">Remarks</span></span>

<span data-ttu-id="36f4b-128">Se o método retornar S \_ OK, a interface **IAMTimelineObj** que ele retornar terá uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="36f4b-128">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="36f4b-129">Certifique-se de liberar a interface quando terminar de usá-la.</span><span class="sxs-lookup"><span data-stu-id="36f4b-129">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="36f4b-130">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="36f4b-130">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="36f4b-131">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="36f4b-131">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="36f4b-132">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="36f4b-132">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="36f4b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36f4b-133">Requirements</span></span>



| <span data-ttu-id="36f4b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="36f4b-134">Requirement</span></span> | <span data-ttu-id="36f4b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="36f4b-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="36f4b-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36f4b-136">Header</span></span><br/>  | <dl> <span data-ttu-id="36f4b-137"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="36f4b-137"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="36f4b-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36f4b-138">Library</span></span><br/> | <dl> <span data-ttu-id="36f4b-139"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="36f4b-139"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36f4b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="36f4b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f4b-141">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="36f4b-141">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="36f4b-142">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="36f4b-142">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




