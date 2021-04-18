---
title: Método IDWriteInlineObject GetOverhangMetrics
description: IDWriteTextLayout chama essa função de retorno de chamada para obter as extensões visíveis (em DIPs) do objeto embutido. No caso de um bitmap simples, sem preenchimento e nenhuma folga, todas as Sobretravas serão simplesmente zeradas.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Gravação direta do método GetOverhangMetrics
- Método GetOverhangMetrics Direct Write, interface IDWriteInlineObject
- IDWriteInlineObject interface de gravação direta, método GetOverhangMetrics
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778777"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a><span data-ttu-id="fd66f-107">Método IDWriteInlineObject:: GetOverhangMetrics</span><span class="sxs-lookup"><span data-stu-id="fd66f-107">IDWriteInlineObject::GetOverhangMetrics method</span></span>

<span data-ttu-id="fd66f-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) chama essa função de retorno de chamada para obter as extensões visíveis (em DIPs) do objeto embutido.</span><span class="sxs-lookup"><span data-stu-id="fd66f-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the visible extents (in DIPs) of the inline object.</span></span> <span data-ttu-id="fd66f-109">No caso de um bitmap simples, sem preenchimento e nenhuma folga, todas as Sobretravas serão simplesmente zeradas.</span><span class="sxs-lookup"><span data-stu-id="fd66f-109">In the case of a simple bitmap, with no padding and no overhang, all the overhangs will simply be zeroes.</span></span>

<span data-ttu-id="fd66f-110">Os sobretravamentos devem ser retornados em relação ao tamanho relatado do objeto (consulte [**\_ \_ \_ métricas de objeto embutido DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) e não devem ser ajustados de linha de base.</span><span class="sxs-lookup"><span data-stu-id="fd66f-110">The overhangs should be returned relative to the reported size of the object (see [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)), and should not be baseline adjusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd66f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd66f-111">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="fd66f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd66f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd66f-113">*sobretravamentos* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fd66f-113">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd66f-114">Tipo: **[ **DWRITE \_ de \_ métricas de folga**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="fd66f-114">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="fd66f-115">Exceder as extensões visíveis (em DIPs) fora do objeto.</span><span class="sxs-lookup"><span data-stu-id="fd66f-115">Overshoot of visible extents (in DIPs) outside the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd66f-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fd66f-116">Return value</span></span>

<span data-ttu-id="fd66f-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fd66f-117">Type: **HRESULT**</span></span>

<span data-ttu-id="fd66f-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fd66f-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fd66f-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fd66f-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd66f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd66f-120">Requirements</span></span>



| <span data-ttu-id="fd66f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd66f-121">Requirement</span></span> | <span data-ttu-id="fd66f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="fd66f-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fd66f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fd66f-123">Library</span></span><br/> | <dl> <span data-ttu-id="fd66f-124"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fd66f-124"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="fd66f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fd66f-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="fd66f-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd66f-126"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd66f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd66f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd66f-128">**IDWriteInlineObject**</span><span class="sxs-lookup"><span data-stu-id="fd66f-128">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[<span data-ttu-id="fd66f-129">**IDWriteInlineObject**</span><span class="sxs-lookup"><span data-stu-id="fd66f-129">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

