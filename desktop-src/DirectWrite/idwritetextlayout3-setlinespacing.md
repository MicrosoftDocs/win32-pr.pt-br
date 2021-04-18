---
title: Método IDWriteTextLayout3 SetLineSpacing
description: Definir espaçamento de linha. | Método IDWriteTextLayout3 SetLineSpacing
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Gravação direta do método SetLineSpacing
- Método SetLineSpacing Direct Write, interface IDWriteTextLayout3
- IDWriteTextLayout3 interface de gravação direta, método SetLineSpacing
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794df5b0dc993688c8bab15c927ae2c03bc18d69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105756947"
---
# <a name="idwritetextlayout3setlinespacing-method"></a><span data-ttu-id="86a17-107">Método IDWriteTextLayout3:: SetLineSpacing</span><span class="sxs-lookup"><span data-stu-id="86a17-107">IDWriteTextLayout3::SetLineSpacing method</span></span>

<span data-ttu-id="86a17-108">Definir espaçamento de linha.</span><span class="sxs-lookup"><span data-stu-id="86a17-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="86a17-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="86a17-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="86a17-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="86a17-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86a17-111">*lineSpacingOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="86a17-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86a17-112">Como gerenciar o espaço entre as linhas.</span><span class="sxs-lookup"><span data-stu-id="86a17-112">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86a17-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="86a17-113">Return value</span></span>

<span data-ttu-id="86a17-114">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="86a17-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="86a17-115">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="86a17-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="86a17-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86a17-116">Requirements</span></span>



| <span data-ttu-id="86a17-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="86a17-117">Requirement</span></span> | <span data-ttu-id="86a17-118">Valor</span><span class="sxs-lookup"><span data-stu-id="86a17-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86a17-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86a17-119">Minimum supported client</span></span><br/> | <span data-ttu-id="86a17-120">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="86a17-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="86a17-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="86a17-121">Minimum supported server</span></span><br/> | <span data-ttu-id="86a17-122">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="86a17-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="86a17-123">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="86a17-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="86a17-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="86a17-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="86a17-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86a17-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="86a17-126"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86a17-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="86a17-127">DLL</span><span class="sxs-lookup"><span data-stu-id="86a17-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86a17-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86a17-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="86a17-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="86a17-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86a17-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="86a17-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





