---
description: O método ZeroBetween remove tudo da faixa entre os horários especificados. Esse método divide todos os objetos que abrangem o intervalo de tempo especificado e remove as partes que estão dentro do intervalo.
ms.assetid: df173a3c-147b-4f2d-9bcb-a8c2873f5420
title: 'Método IAMTimelineTrack:: ZeroBetween (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.ZeroBetween
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bef669bae5e5e5c4c31a49b545fcfc7f58285f97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796264"
---
# <a name="iamtimelinetrackzerobetween-method"></a><span data-ttu-id="5bf35-104">Método IAMTimelineTrack:: ZeroBetween</span><span class="sxs-lookup"><span data-stu-id="5bf35-104">IAMTimelineTrack::ZeroBetween method</span></span>

> [!Note]  
> <span data-ttu-id="5bf35-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="5bf35-105">\[Deprecated.</span></span> <span data-ttu-id="5bf35-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5bf35-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5bf35-107">O `ZeroBetween` método remove tudo da faixa entre os horários especificados.</span><span class="sxs-lookup"><span data-stu-id="5bf35-107">The `ZeroBetween` method removes everything from the track between the specified times.</span></span> <span data-ttu-id="5bf35-108">Esse método divide todos os objetos que abrangem o intervalo de tempo especificado e remove as partes que estão dentro do intervalo.</span><span class="sxs-lookup"><span data-stu-id="5bf35-108">This method splits any objects that span the specified time range and removes the pieces that fall within the range.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bf35-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5bf35-109">Syntax</span></span>


```C++
HRESULT ZeroBetween(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a><span data-ttu-id="5bf35-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bf35-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bf35-111">*rtStart*</span><span class="sxs-lookup"><span data-stu-id="5bf35-111">*rtStart*</span></span> 
</dt> <dd>

<span data-ttu-id="5bf35-112">Início do intervalo a ser limpo, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="5bf35-112">Beginning of the range to clear, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="5bf35-113">*rtEnd*</span><span class="sxs-lookup"><span data-stu-id="5bf35-113">*rtEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="5bf35-114">Fim do intervalo a ser limpo, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="5bf35-114">End of the range to clear, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bf35-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5bf35-115">Return value</span></span>

<span data-ttu-id="5bf35-116">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5bf35-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5bf35-117">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="5bf35-117">Possible values include the following.</span></span>



| <span data-ttu-id="5bf35-118">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5bf35-118">Return code</span></span>                                                                             | <span data-ttu-id="5bf35-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="5bf35-119">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="5bf35-120"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="5bf35-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="5bf35-121">O intervalo de tempo cai além de tudo na faixa.</span><span class="sxs-lookup"><span data-stu-id="5bf35-121">The time range falls beyond everything in the track.</span></span><br/> |
| <dl> <span data-ttu-id="5bf35-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5bf35-122"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="5bf35-123">Êxito.</span><span class="sxs-lookup"><span data-stu-id="5bf35-123">Success.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="5bf35-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bf35-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5bf35-125">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="5bf35-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5bf35-126">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="5bf35-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5bf35-127">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="5bf35-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5bf35-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5bf35-128">Requirements</span></span>



| <span data-ttu-id="5bf35-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bf35-129">Requirement</span></span> | <span data-ttu-id="5bf35-130">Valor</span><span class="sxs-lookup"><span data-stu-id="5bf35-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf35-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5bf35-131">Header</span></span><br/>  | <dl> <span data-ttu-id="5bf35-132"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bf35-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5bf35-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5bf35-133">Library</span></span><br/> | <dl> <span data-ttu-id="5bf35-134"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bf35-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bf35-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bf35-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bf35-136">**Interface IAMTimelineTrack**</span><span class="sxs-lookup"><span data-stu-id="5bf35-136">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="5bf35-137">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="5bf35-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




