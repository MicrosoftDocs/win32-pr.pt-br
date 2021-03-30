---
title: Método IDWriteTextLayout3 GetLineMetrics
description: Recupera as propriedades de cada linha.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- Gravação direta do método GetLineMetrics
- Método GetLineMetrics Direct Write, interface IDWriteTextLayout3
- IDWriteTextLayout3 interface de gravação direta, método GetLineMetrics
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455413"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a><span data-ttu-id="a4c8e-106">Método IDWriteTextLayout3:: GetLineMetrics</span><span class="sxs-lookup"><span data-stu-id="a4c8e-106">IDWriteTextLayout3::GetLineMetrics method</span></span>

<span data-ttu-id="a4c8e-107">Recupera as propriedades de cada linha.</span><span class="sxs-lookup"><span data-stu-id="a4c8e-107">Retrieves properties of each line.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c8e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4c8e-108">Syntax</span></span>


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a><span data-ttu-id="a4c8e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a4c8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4c8e-110">*lineMetrics* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a4c8e-110">*lineMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c8e-111">A matriz a ser preenchida com informações de linha.</span><span class="sxs-lookup"><span data-stu-id="a4c8e-111">The array to fill with line information.</span></span>

</dd> <dt>

<span data-ttu-id="a4c8e-112">*maxLineCount*</span><span class="sxs-lookup"><span data-stu-id="a4c8e-112">*maxLineCount*</span></span> 
</dt> <dd>

<span data-ttu-id="a4c8e-113">O tamanho máximo da matriz lineMetrics.</span><span class="sxs-lookup"><span data-stu-id="a4c8e-113">The maximum size of the lineMetrics array.</span></span>

</dd> <dt>

<span data-ttu-id="a4c8e-114">*actualLineCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a4c8e-114">*actualLineCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c8e-115">O tamanho real da matriz lineMetrics necessária.</span><span class="sxs-lookup"><span data-stu-id="a4c8e-115">The actual size of the lineMetrics array that is needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4c8e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a4c8e-116">Return value</span></span>

<span data-ttu-id="a4c8e-117">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a4c8e-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a4c8e-118">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a4c8e-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c8e-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4c8e-119">Remarks</span></span>

<span data-ttu-id="a4c8e-120">Se maxLineCount não for suficientemente grande E \_ não for \_ suficiente \_ buffer, o que é equivalente a HRESULT \_ do \_ Win32 (erro \_ buffer insuficiente \_ ), é retornado e actualLineCount é definido como o número de linhas necessárias.</span><span class="sxs-lookup"><span data-stu-id="a4c8e-120">If maxLineCount is not large enough E\_NOT\_SUFFICIENT\_BUFFER, which is equivalent to HRESULT\_FROM\_WIN32(ERROR\_INSUFFICIENT\_BUFFER), is returned and actualLineCount is set to the number of lines needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c8e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4c8e-121">Requirements</span></span>



| <span data-ttu-id="a4c8e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4c8e-122">Requirement</span></span> | <span data-ttu-id="a4c8e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a4c8e-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c8e-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4c8e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c8e-125">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="a4c8e-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a4c8e-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a4c8e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c8e-127">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="a4c8e-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a4c8e-128">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="a4c8e-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="a4c8e-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="a4c8e-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="a4c8e-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a4c8e-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a4c8e-131"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4c8e-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a4c8e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a4c8e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4c8e-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4c8e-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a4c8e-134">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a4c8e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c8e-135">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="a4c8e-135">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





