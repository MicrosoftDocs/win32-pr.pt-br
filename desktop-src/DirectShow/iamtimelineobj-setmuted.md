---
description: O método com mudo definido define o estado mudo do objeto. Um objeto sem áudio não é renderizado, mas permanece na linha do tempo.
ms.assetid: 5dcd8533-8e58-4553-ac01-928723485f5d
title: 'Método IAMTimelineObj:: setmudoed (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ac3f5b798ef56251fa64b55a92ae1e94e2fd61b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758680"
---
# <a name="iamtimelineobjsetmuted-method"></a><span data-ttu-id="6f811-104">Método IAMTimelineObj:: setmudoed</span><span class="sxs-lookup"><span data-stu-id="6f811-104">IAMTimelineObj::SetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="6f811-105">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="6f811-105">\[Deprecated.</span></span> <span data-ttu-id="6f811-106">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6f811-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6f811-107">O `SetMuted` método define o estado mudo do objeto.</span><span class="sxs-lookup"><span data-stu-id="6f811-107">The `SetMuted` method sets the object's muted state.</span></span> <span data-ttu-id="6f811-108">Um objeto sem áudio não é renderizado, mas permanece na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="6f811-108">A muted object is not rendered, but it remains in the timeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f811-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f811-109">Syntax</span></span>


```C++
HRESULT SetMuted(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="6f811-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f811-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f811-111">*newVal*</span><span class="sxs-lookup"><span data-stu-id="6f811-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="6f811-112">Sinalizador que especifica o estado mudo.</span><span class="sxs-lookup"><span data-stu-id="6f811-112">Flag that specifies the muted state.</span></span> <span data-ttu-id="6f811-113">Se **for true**, o objeto e todos os seus filhos ficarão sem áudio.</span><span class="sxs-lookup"><span data-stu-id="6f811-113">If **TRUE**, the object and all of its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f811-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f811-114">Return value</span></span>

<span data-ttu-id="6f811-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6f811-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f811-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f811-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f811-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f811-117">Remarks</span></span>

<span data-ttu-id="6f811-118">Mudo de um objeto também desativa todos os filhos contidos no objeto.</span><span class="sxs-lookup"><span data-stu-id="6f811-118">Muting an object also mutes any children contained in the object.</span></span> <span data-ttu-id="6f811-119">Por exemplo, se você ativar mudo de uma faixa, as transições, as fontes e os efeitos nessa faixa também ficarão sem áudio.</span><span class="sxs-lookup"><span data-stu-id="6f811-119">For example, if you mute a track, the transitions, sources, and effects in that track are also muted.</span></span> <span data-ttu-id="6f811-120">Depois que o objeto não estiver mais mudo, seus filhos serão revertidos para seu estado anterior, o que pode estar mudo ou sem áudio.</span><span class="sxs-lookup"><span data-stu-id="6f811-120">Once the object is no longer muted, its children revert to their previous state, which might be muted or unmuted.</span></span>

> [!Note]  
> <span data-ttu-id="6f811-121">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="6f811-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6f811-122">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6f811-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6f811-123">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="6f811-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6f811-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f811-124">Requirements</span></span>



| <span data-ttu-id="6f811-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f811-125">Requirement</span></span> | <span data-ttu-id="6f811-126">Valor</span><span class="sxs-lookup"><span data-stu-id="6f811-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f811-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f811-127">Header</span></span><br/>  | <dl> <span data-ttu-id="6f811-128"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f811-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6f811-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f811-129">Library</span></span><br/> | <dl> <span data-ttu-id="6f811-130"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f811-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f811-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f811-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f811-132">**Interface IAMTimelineObj**</span><span class="sxs-lookup"><span data-stu-id="6f811-132">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="6f811-133">Códigos de erro e êxito</span><span class="sxs-lookup"><span data-stu-id="6f811-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




