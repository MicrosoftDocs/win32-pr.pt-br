---
title: Método IDWriteTextLayout DetermineMinWidth
description: Determina a largura mínima possível em que o layout pode ser definido sem a interrupção de emergência entre os caracteres de palavras inteiras que estão ocorrendo.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Gravação direta do método DetermineMinWidth
- Método DetermineMinWidth Direct Write, interface IDWriteTextLayout
- IDWriteTextLayout interface de gravação direta, método DetermineMinWidth
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757862"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a><span data-ttu-id="0f4ad-106">IDWriteTextLayout: método etermineMinWidth de:D</span><span class="sxs-lookup"><span data-stu-id="0f4ad-106">IDWriteTextLayout::DetermineMinWidth method</span></span>

<span data-ttu-id="0f4ad-107">Determina a largura mínima possível em que o layout pode ser definido sem a interrupção de emergência entre os caracteres de palavras inteiras que estão ocorrendo.</span><span class="sxs-lookup"><span data-stu-id="0f4ad-107">Determines the minimum possible width the layout can be set to without emergency breaking between the characters of whole words occurring.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f4ad-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f4ad-108">Syntax</span></span>


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="0f4ad-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f4ad-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f4ad-110">*minWidth* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0f4ad-110">*minWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f4ad-111">Tipo: **float \***</span><span class="sxs-lookup"><span data-stu-id="0f4ad-111">Type: **FLOAT\***</span></span>

<span data-ttu-id="0f4ad-112">Largura mínima.</span><span class="sxs-lookup"><span data-stu-id="0f4ad-112">Minimum width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f4ad-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f4ad-113">Return value</span></span>

<span data-ttu-id="0f4ad-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0f4ad-114">Type: **HRESULT**</span></span>

<span data-ttu-id="0f4ad-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0f4ad-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0f4ad-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0f4ad-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f4ad-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f4ad-117">Requirements</span></span>



| <span data-ttu-id="0f4ad-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f4ad-118">Requirement</span></span> | <span data-ttu-id="0f4ad-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0f4ad-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f4ad-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0f4ad-120">Library</span></span><br/> | <dl> <span data-ttu-id="0f4ad-121"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f4ad-121"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="0f4ad-122">DLL</span><span class="sxs-lookup"><span data-stu-id="0f4ad-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f4ad-123"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f4ad-123"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f4ad-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f4ad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f4ad-125">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="0f4ad-125">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="0f4ad-126">**IDWriteTextLayout**</span><span class="sxs-lookup"><span data-stu-id="0f4ad-126">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

