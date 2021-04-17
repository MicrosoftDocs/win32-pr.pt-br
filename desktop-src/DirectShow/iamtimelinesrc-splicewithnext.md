---
description: O método SpliceWithNext une o objeto de origem a outro objeto de origem.
ms.assetid: 65b23466-404c-4eef-943e-8b40186f2b96
title: 'Método IAMTimelineSrc:: SpliceWithNext (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SpliceWithNext
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c17812ab5d451be639def0d07fe773d4b676570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759441"
---
# <a name="iamtimelinesrcsplicewithnext-method"></a><span data-ttu-id="f937f-103">Método IAMTimelineSrc:: SpliceWithNext</span><span class="sxs-lookup"><span data-stu-id="f937f-103">IAMTimelineSrc::SpliceWithNext method</span></span>

> [!Note]  
> <span data-ttu-id="f937f-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="f937f-104">\[Deprecated.</span></span> <span data-ttu-id="f937f-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f937f-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="f937f-106">O `SpliceWithNext` método une o objeto de origem a outro objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="f937f-106">The `SpliceWithNext` method joins the source object to another source object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f937f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f937f-107">Syntax</span></span>


```C++
HRESULT SpliceWithNext(
   IAMTimelineObj *pNext
);
```



## <a name="parameters"></a><span data-ttu-id="f937f-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f937f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f937f-109">*pNext*</span><span class="sxs-lookup"><span data-stu-id="f937f-109">*pNext*</span></span> 
</dt> <dd>

<span data-ttu-id="f937f-110">Ponteiro para a interface [**IAMTimelineObj**](iamtimelineobj.md) do objeto de origem para ingressar na fonte atual.</span><span class="sxs-lookup"><span data-stu-id="f937f-110">Pointer to the [**IAMTimelineObj**](iamtimelineobj.md) interface of the source object to join to the current source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f937f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f937f-111">Return value</span></span>

<span data-ttu-id="f937f-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f937f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f937f-113">Os possíveis valores de retorno incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f937f-113">Possible return values include the following:</span></span>



| <span data-ttu-id="f937f-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f937f-114">Return code</span></span>                                                                                   | <span data-ttu-id="f937f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f937f-115">Description</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f937f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f937f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f937f-117">Êxito.</span><span class="sxs-lookup"><span data-stu-id="f937f-117">Success.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="f937f-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f937f-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f937f-119">Argumento inválido.</span><span class="sxs-lookup"><span data-stu-id="f937f-119">Invalid argument.</span></span><br/>                                             |
| <dl> <span data-ttu-id="f937f-120"><dt>**E \_ NOinterface**</dt></span><span class="sxs-lookup"><span data-stu-id="f937f-120"><dt>**E\_NOINTERFACE**</dt></span></span> </dl> | <span data-ttu-id="f937f-121">O objeto especificado pelo parâmetro *pNext* não é um objeto de origem.</span><span class="sxs-lookup"><span data-stu-id="f937f-121">Object specified by *pNext* parameter is not a source object.</span></span><br/> |
| <dl> <span data-ttu-id="f937f-122"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="f937f-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f937f-123">Argumento de ponteiro **nulo** .</span><span class="sxs-lookup"><span data-stu-id="f937f-123">**NULL** pointer argument.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="f937f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="f937f-124">Remarks</span></span>

<span data-ttu-id="f937f-125">Como implementado atualmente, esse método descarta todos os efeitos em *pNext*.</span><span class="sxs-lookup"><span data-stu-id="f937f-125">As currently implemented, this method discards any effects on *pNext*.</span></span>

<span data-ttu-id="f937f-126">Para que esse método seja bem sucedido, *pNext* deve ser um quadro de correspondência do objeto de origem atual, definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="f937f-126">For this method to succeed, *pNext* must be a match frame of the current source object, defined as follows:</span></span>

-   <span data-ttu-id="f937f-127">Ele deve compartilhar o mesmo arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="f937f-127">It must share the same source file.</span></span>
-   <span data-ttu-id="f937f-128">A hora de início da mídia deve ser igual à hora de parada da mídia da origem atual.</span><span class="sxs-lookup"><span data-stu-id="f937f-128">The media start time must equal the media stop time of the current source.</span></span>
-   <span data-ttu-id="f937f-129">A taxa de reprodução deve ser a mesma.</span><span class="sxs-lookup"><span data-stu-id="f937f-129">The playback rate must be the same.</span></span> <span data-ttu-id="f937f-130">A taxa de reprodução é a duração da mídia dividida pela duração da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="f937f-130">Playback rate is media duration divided by timeline duration.</span></span>

> [!Note]  
> <span data-ttu-id="f937f-131">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="f937f-131">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="f937f-132">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f937f-132">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="f937f-133">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="f937f-133">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f937f-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f937f-134">Requirements</span></span>



| <span data-ttu-id="f937f-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="f937f-135">Requirement</span></span> | <span data-ttu-id="f937f-136">Valor</span><span class="sxs-lookup"><span data-stu-id="f937f-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f937f-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f937f-137">Header</span></span><br/>  | <dl> <span data-ttu-id="f937f-138"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f937f-138"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="f937f-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f937f-139">Library</span></span><br/> | <dl> <span data-ttu-id="f937f-140"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f937f-140"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f937f-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="f937f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f937f-142">**Interface IAMTimelineSrc**</span><span class="sxs-lookup"><span data-stu-id="f937f-142">**IAMTimelineSrc Interface**</span></span>](iamtimelinesrc.md)
</dt> <dt>

[<span data-ttu-id="f937f-143">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="f937f-143">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




