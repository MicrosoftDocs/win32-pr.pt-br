---
description: 'O método ZeroBetween2 remove tudo da faixa entre os horários especificados. Esse método é equivalente a IAMTimelineTrack:: ZeroBetween, mas usa os valores de REFTIME.'
ms.assetid: 56b9be30-cc3f-4843-bf35-910498242d71
title: 'Método IAMTimelineTrack:: ZeroBetween2 (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 27e3ab5cc2a631cb54c926824c2f3410413cd981
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759440"
---
# <a name="iamtimelinetrackzerobetween2-method"></a><span data-ttu-id="94426-104">Método IAMTimelineTrack:: ZeroBetween2</span><span class="sxs-lookup"><span data-stu-id="94426-104">IAMTimelineTrack::ZeroBetween2 method</span></span>

> [!Note]  
> <span data-ttu-id="94426-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="94426-105">\[Deprecated.</span></span> <span data-ttu-id="94426-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="94426-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="94426-107">O `ZeroBetween2` método remove tudo da faixa entre os horários especificados.</span><span class="sxs-lookup"><span data-stu-id="94426-107">The `ZeroBetween2` method removes everything from the track between the specified times.</span></span> <span data-ttu-id="94426-108">Esse método é equivalente a [**IAMTimelineTrack:: ZeroBetween**](iamtimelinetrack-zerobetween.md), mas usa os valores de [**REFTIME**](reftime.md) .</span><span class="sxs-lookup"><span data-stu-id="94426-108">This method is equivalent to [**IAMTimelineTrack::ZeroBetween**](iamtimelinetrack-zerobetween.md), but takes [**REFTIME**](reftime.md) values.</span></span>

## <a name="syntax"></a><span data-ttu-id="94426-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94426-109">Syntax</span></span>


```C++
HRESULT ZeroBetween2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="94426-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94426-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94426-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="94426-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="94426-112">Início do intervalo a ser limpo, em segundos.</span><span class="sxs-lookup"><span data-stu-id="94426-112">Beginning of the range to clear, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="94426-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="94426-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="94426-114">Fim do intervalo a ser limpo, em segundos.</span><span class="sxs-lookup"><span data-stu-id="94426-114">End of the range to clear, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94426-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94426-115">Return value</span></span>

<span data-ttu-id="94426-116">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="94426-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="94426-117">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="94426-117">Possible values include the following.</span></span>



| <span data-ttu-id="94426-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="94426-118">Return code</span></span>                                                                             | <span data-ttu-id="94426-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="94426-119">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="94426-120"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="94426-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="94426-121">O intervalo de tempo cai além de tudo na faixa.</span><span class="sxs-lookup"><span data-stu-id="94426-121">The time range falls beyond everything in the track.</span></span><br/> |
| <dl> <span data-ttu-id="94426-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="94426-122"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="94426-123">Êxito.</span><span class="sxs-lookup"><span data-stu-id="94426-123">Success.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="94426-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="94426-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="94426-125">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="94426-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="94426-126">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="94426-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="94426-127">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="94426-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="94426-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94426-128">Requirements</span></span>



| <span data-ttu-id="94426-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="94426-129">Requirement</span></span> | <span data-ttu-id="94426-130">Valor</span><span class="sxs-lookup"><span data-stu-id="94426-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94426-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94426-131">Header</span></span><br/>  | <dl> <span data-ttu-id="94426-132"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="94426-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="94426-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94426-133">Library</span></span><br/> | <dl> <span data-ttu-id="94426-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94426-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94426-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="94426-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94426-136">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="94426-136">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="94426-137">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="94426-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




