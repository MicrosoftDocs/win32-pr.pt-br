---
description: O método FixMediaTimes arredonda os valores de tempo especificados para o limite de quadro mais próximo, conforme definido pela taxa de quadros de saída. Em geral, os aplicativos não precisam chamar esse método.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'Método IAMTimelineSrc:: FixMediaTimes (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758059"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a><span data-ttu-id="d6eed-104">Método IAMTimelineSrc:: FixMediaTimes</span><span class="sxs-lookup"><span data-stu-id="d6eed-104">IAMTimelineSrc::FixMediaTimes method</span></span>

> [!Note]  
> <span data-ttu-id="d6eed-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="d6eed-105">\[Deprecated.</span></span> <span data-ttu-id="d6eed-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d6eed-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="d6eed-107">O `FixMediaTimes` método arredonda os valores de tempo especificados para o limite de quadro mais próximo, conforme definido pela taxa de quadros de saída.</span><span class="sxs-lookup"><span data-stu-id="d6eed-107">The `FixMediaTimes` method rounds the specified time values to the nearest frame boundary, as defined by the output frame rate.</span></span> <span data-ttu-id="d6eed-108">Em geral, os aplicativos não precisam chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="d6eed-108">In general, applications do not need to call this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6eed-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6eed-109">Syntax</span></span>


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a><span data-ttu-id="d6eed-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d6eed-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6eed-111">*pStart*</span><span class="sxs-lookup"><span data-stu-id="d6eed-111">*pStart*</span></span> 
</dt> <dd>

<span data-ttu-id="d6eed-112">Ponteiro para uma variável que contém a hora de início, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="d6eed-112">Pointer to a variable that contains the start time, in 100-nanosecond units.</span></span> <span data-ttu-id="d6eed-113">Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.</span><span class="sxs-lookup"><span data-stu-id="d6eed-113">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> <dt>

<span data-ttu-id="d6eed-114">*pStop*</span><span class="sxs-lookup"><span data-stu-id="d6eed-114">*pStop*</span></span> 
</dt> <dd>

<span data-ttu-id="d6eed-115">Ponteiro para uma variável que contém a hora de parada, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="d6eed-115">Pointer to a variable that contains the stop time, in 100-nanosecond units.</span></span> <span data-ttu-id="d6eed-116">Se a chamada for realizada com sucesso, essa variável será definida como o tempo arredondado.</span><span class="sxs-lookup"><span data-stu-id="d6eed-116">If the call succeeds, this variable is set to the rounded time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6eed-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d6eed-117">Return value</span></span>

<span data-ttu-id="d6eed-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="d6eed-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d6eed-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d6eed-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6eed-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6eed-120">Remarks</span></span>

<span data-ttu-id="d6eed-121">Esse método é semelhante ao método [**IAMTimelineObj:: FixTimes**](iamtimelineobj-fixtimes.md) , mas preserva a proporção original de tempos de mídia e tempos de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="d6eed-121">This method is similar to the [**IAMTimelineObj::FixTimes**](iamtimelineobj-fixtimes.md) method, but it preserves the original ratio of media times and timeline times.</span></span> <span data-ttu-id="d6eed-122">Apenas arredondar os horários para o limite de quadro mais próximo poderia distorcer essa proporção.</span><span class="sxs-lookup"><span data-stu-id="d6eed-122">Just rounding the times to the nearest frame boundary could distort this ratio.</span></span>

> [!Note]  
> <span data-ttu-id="d6eed-123">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="d6eed-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="d6eed-124">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="d6eed-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="d6eed-125">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="d6eed-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="d6eed-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6eed-126">Requirements</span></span>



| <span data-ttu-id="d6eed-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6eed-127">Requirement</span></span> | <span data-ttu-id="d6eed-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d6eed-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6eed-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6eed-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d6eed-130"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="d6eed-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6eed-131">Library</span></span><br/> | <dl> <span data-ttu-id="d6eed-132"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6eed-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6eed-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6eed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6eed-134">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="d6eed-134">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="d6eed-135">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="d6eed-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




