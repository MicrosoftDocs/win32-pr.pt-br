---
title: Método MoveNext IDWriteColorGlyphRunEnumerator
description: Mover para a próxima execução de glifo no enumerador.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- Gravação direta do método MoveNext
- Método MoveNext Direct Write, interface IDWriteColorGlyphRunEnumerator
- Gravação direta da interface IDWriteColorGlyphRunEnumerator, método MoveNext
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499486"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a><span data-ttu-id="94433-106">Método IDWriteColorGlyphRunEnumerator:: MoveNext</span><span class="sxs-lookup"><span data-stu-id="94433-106">IDWriteColorGlyphRunEnumerator::MoveNext method</span></span>

<span data-ttu-id="94433-107">Mover para a próxima execução de glifo no enumerador.</span><span class="sxs-lookup"><span data-stu-id="94433-107">Move to the next glyph run in the enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="94433-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94433-108">Syntax</span></span>


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a><span data-ttu-id="94433-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94433-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94433-110">*haveRun* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="94433-110">*haveRun* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94433-111">Tipo: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="94433-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="94433-112">Retorna _ *true*\* se houver uma próxima execução de glifo.</span><span class="sxs-lookup"><span data-stu-id="94433-112">Returns _ *TRUE*\* if there is a next glyph run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94433-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="94433-113">Return value</span></span>

<span data-ttu-id="94433-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="94433-114">Type: **HRESULT**</span></span>

<span data-ttu-id="94433-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="94433-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="94433-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="94433-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="94433-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94433-117">Requirements</span></span>



| <span data-ttu-id="94433-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="94433-118">Requirement</span></span> | <span data-ttu-id="94433-119">Valor</span><span class="sxs-lookup"><span data-stu-id="94433-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="94433-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94433-120">Minimum supported client</span></span><br/> | <span data-ttu-id="94433-121">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="94433-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="94433-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="94433-122">Minimum supported server</span></span><br/> | <span data-ttu-id="94433-123">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="94433-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="94433-124">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="94433-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="94433-125">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="94433-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="94433-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94433-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="94433-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94433-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="94433-128">DLL</span><span class="sxs-lookup"><span data-stu-id="94433-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94433-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94433-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="94433-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="94433-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94433-131">**IDWriteColorGlyphRunEnumerator**</span><span class="sxs-lookup"><span data-stu-id="94433-131">**IDWriteColorGlyphRunEnumerator**</span></span>](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





