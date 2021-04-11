---
title: Método IDWriteTextFormat2 SetLineSpacing
description: Definir espaçamento de linha. | Método IDWriteTextFormat2 SetLineSpacing
ms.assetid: 71d8c6c4-920f-a1b5-5a13-9985a7aca41e
keywords:
- Gravação direta do método SetLineSpacing
- Método SetLineSpacing Direct Write, interface IDWriteTextFormat2
- IDWriteTextFormat2 interface de gravação direta, método SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextFormat2.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3514c52c9b8a51666d36eec7ce893735635f3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172854"
---
# <a name="idwritetextformat2setlinespacing-method"></a><span data-ttu-id="4466e-107">Método IDWriteTextFormat2:: SetLineSpacing</span><span class="sxs-lookup"><span data-stu-id="4466e-107">IDWriteTextFormat2::SetLineSpacing method</span></span>

<span data-ttu-id="4466e-108">Definir espaçamento de linha.</span><span class="sxs-lookup"><span data-stu-id="4466e-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="4466e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4466e-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="4466e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4466e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4466e-111">*lineSpacingOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="4466e-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4466e-112">Tipo: **\* [**\_ \_ espaçamento de linha DWRITE**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing) const**</span><span class="sxs-lookup"><span data-stu-id="4466e-112">Type: **const [**DWRITE\_LINE\_SPACING**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)\***</span></span>

<span data-ttu-id="4466e-113">Como gerenciar o espaço entre as linhas.</span><span class="sxs-lookup"><span data-stu-id="4466e-113">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4466e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4466e-114">Return value</span></span>

<span data-ttu-id="4466e-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4466e-115">Type: **HRESULT**</span></span>

<span data-ttu-id="4466e-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4466e-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4466e-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4466e-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4466e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4466e-118">Requirements</span></span>



| <span data-ttu-id="4466e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="4466e-119">Requirement</span></span> | <span data-ttu-id="4466e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="4466e-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4466e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4466e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="4466e-122">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4466e-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4466e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4466e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="4466e-124">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="4466e-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4466e-125">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="4466e-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="4466e-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="4466e-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="4466e-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4466e-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="4466e-128"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="4466e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4466e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4466e-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4466e-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4466e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="4466e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4466e-132">**IDWriteTextFormat2**</span><span class="sxs-lookup"><span data-stu-id="4466e-132">**IDWriteTextFormat2**</span></span>](idwritetextformat2.md)
</dt> </dl>

 

 





