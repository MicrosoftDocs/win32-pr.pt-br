---
title: Método getmetrics IDWriteTextLayout2
description: Recupera as métricas gerais para a cadeia de caracteres formatada.
ms.assetid: EADCD83A-9FF5-44AB-8AB5-35FCB3A84889
keywords:
- Gravação direta do método getmetrics
- Método getmetrics Direct Write, interface IDWriteTextLayout2
- IDWriteTextLayout2 interface Direct Write, método getmetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout2.GetMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e393dfabb632641125d915e85f275977b20f0326
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770238"
---
# <a name="idwritetextlayout2getmetrics-method"></a><span data-ttu-id="b0722-106">Método IDWriteTextLayout2:: getmetrics</span><span class="sxs-lookup"><span data-stu-id="b0722-106">IDWriteTextLayout2::GetMetrics method</span></span>

<span data-ttu-id="b0722-107">Recupera as métricas gerais para a cadeia de caracteres formatada.</span><span class="sxs-lookup"><span data-stu-id="b0722-107">Retrieves overall metrics for the formatted string.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0722-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0722-108">Syntax</span></span>


```C++
virtual HRESULT GetMetrics(
  [out] DWRITE_TEXT_METRICS1 * textMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="b0722-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0722-109">Parameters</span></span>

<dl> <dt>

 <span data-ttu-id="b0722-110">*textMetrics* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b0722-110">*textMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0722-111">Tipo: \**[**DWRITE \_ Text \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) \** _</span><span class="sxs-lookup"><span data-stu-id="b0722-111">Type: \**[**DWRITE\_TEXT\_METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1)\** _</span></span>

<span data-ttu-id="b0722-112">Quando esse método retorna, contém as distâncias medidas do texto e do conteúdo associado depois de serem formatados.</span><span class="sxs-lookup"><span data-stu-id="b0722-112">When this method returns, contains the measured distances of text and associated content after being formatted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0722-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0722-113">Return value</span></span>

<span data-ttu-id="b0722-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b0722-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b0722-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b0722-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b0722-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b0722-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0722-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0722-117">Requirements</span></span>



| <span data-ttu-id="b0722-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0722-118">Requirement</span></span> | <span data-ttu-id="b0722-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b0722-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0722-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0722-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b0722-121">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b0722-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="b0722-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0722-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b0722-123">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="b0722-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="b0722-124">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="b0722-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="b0722-125">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="b0722-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="b0722-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0722-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0722-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0722-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b0722-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b0722-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0722-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0722-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b0722-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0722-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0722-131">**IDWriteTextLayout2**</span><span class="sxs-lookup"><span data-stu-id="b0722-131">**IDWriteTextLayout2**</span></span>](idwritetextlayout2.md)
</dt> </dl>

 

 





