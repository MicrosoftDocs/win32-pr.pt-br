---
title: Método IDWriteTextLayout3 GetLineSpacing
description: Obtém informações de espaçamento de linha.
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- Gravação direta do método GetLineSpacing
- Método GetLineSpacing Direct Write, interface IDWriteTextLayout3
- IDWriteTextLayout3 interface de gravação direta, método GetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303030a5674f39c160804ae2dad5b91050d82f37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918683"
---
# <a name="idwritetextlayout3getlinespacing-method"></a><span data-ttu-id="f61c1-106">Método IDWriteTextLayout3:: GetLineSpacing</span><span class="sxs-lookup"><span data-stu-id="f61c1-106">IDWriteTextLayout3::GetLineSpacing method</span></span>

<span data-ttu-id="f61c1-107">Obtém informações de espaçamento de linha.</span><span class="sxs-lookup"><span data-stu-id="f61c1-107">Gets line spacing information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f61c1-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f61c1-108">Syntax</span></span>


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="f61c1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f61c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f61c1-110">*lineSpacingOptions* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f61c1-110">*lineSpacingOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f61c1-111">Como gerenciar o espaço entre as linhas.</span><span class="sxs-lookup"><span data-stu-id="f61c1-111">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f61c1-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f61c1-112">Return value</span></span>

<span data-ttu-id="f61c1-113">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f61c1-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f61c1-114">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f61c1-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f61c1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f61c1-115">Requirements</span></span>



| <span data-ttu-id="f61c1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f61c1-116">Requirement</span></span> | <span data-ttu-id="f61c1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f61c1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f61c1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f61c1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f61c1-119">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f61c1-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f61c1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f61c1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f61c1-121">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="f61c1-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f61c1-122">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="f61c1-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="f61c1-123">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="f61c1-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="f61c1-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f61c1-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="f61c1-125"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f61c1-125"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f61c1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f61c1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f61c1-127"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f61c1-127"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f61c1-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="f61c1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f61c1-129">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="f61c1-129">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





