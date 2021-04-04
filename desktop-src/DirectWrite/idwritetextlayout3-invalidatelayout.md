---
title: Método IDWriteTextLayout3 InvalidateLayout
description: Invalida o layout, forçando o layout a ser remedido antes de chamar as métricas ou as funções de desenho. Isso será útil se a localidade de uma fonte for alterada, e o layout deve ser redesenhado ou se o tamanho de um cliente implementado IDWriteInlineObject for alterado.
ms.assetid: 65b42ee1-5b67-1f6d-0e4b-ee60b192e7b7
keywords:
- Gravação direta do método InvalidateLayout
- Método InvalidateLayout Direct Write, interface IDWriteTextLayout3
- IDWriteTextLayout3 interface de gravação direta, método InvalidateLayout
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.InvalidateLayout
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5df97d4590f62f586a570d52428b6560a7d88df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085797"
---
# <a name="idwritetextlayout3invalidatelayout-method"></a><span data-ttu-id="cf7c6-107">Método IDWriteTextLayout3:: InvalidateLayout</span><span class="sxs-lookup"><span data-stu-id="cf7c6-107">IDWriteTextLayout3::InvalidateLayout method</span></span>

<span data-ttu-id="cf7c6-108">Invalida o layout, forçando o layout a ser remedido antes de chamar as métricas ou as funções de desenho.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-108">Invalidates the layout, forcing layout to remeasure before calling the metrics or drawing functions.</span></span> <span data-ttu-id="cf7c6-109">Isso será útil se a localidade de uma fonte for alterada, e o layout deve ser redesenhado ou se o tamanho de um cliente implementado IDWriteInlineObject for alterado.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-109">This is useful if the locality of a font changes, and layout should be redrawn, or if the size of a client implemented IDWriteInlineObject changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf7c6-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf7c6-110">Syntax</span></span>


```C++
HRESULT InvalidateLayout();
```



## <a name="parameters"></a><span data-ttu-id="cf7c6-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf7c6-111">Parameters</span></span>

<span data-ttu-id="cf7c6-112">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf7c6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf7c6-113">Return value</span></span>

<span data-ttu-id="cf7c6-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="cf7c6-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="cf7c6-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="cf7c6-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf7c6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf7c6-116">Requirements</span></span>



| <span data-ttu-id="cf7c6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf7c6-117">Requirement</span></span> | <span data-ttu-id="cf7c6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cf7c6-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf7c6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf7c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cf7c6-120">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf7c6-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cf7c6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf7c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cf7c6-122">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="cf7c6-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cf7c6-123">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="cf7c6-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="cf7c6-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="cf7c6-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="cf7c6-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf7c6-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf7c6-126"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf7c6-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cf7c6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="cf7c6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf7c6-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf7c6-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cf7c6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf7c6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf7c6-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="cf7c6-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





