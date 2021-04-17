---
title: Método IDWriteLocalFontFileLoader GetLastWriteTimeFromKey
description: Obtém a hora da última gravação do arquivo da chave de referência do arquivo de fonte.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Gravação direta do método GetLastWriteTimeFromKey
- Método GetLastWriteTimeFromKey Direct Write, interface IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader interface de gravação direta, método GetLastWriteTimeFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782826"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a><span data-ttu-id="83fa4-106">Método IDWriteLocalFontFileLoader:: GetLastWriteTimeFromKey</span><span class="sxs-lookup"><span data-stu-id="83fa4-106">IDWriteLocalFontFileLoader::GetLastWriteTimeFromKey method</span></span>

<span data-ttu-id="83fa4-107">Obtém a hora da última gravação do arquivo da chave de referência do arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="83fa4-107">Obtains the last write time of the file from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="83fa4-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="83fa4-108">Syntax</span></span>


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="83fa4-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83fa4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83fa4-110">*fontFileReferenceKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="83fa4-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83fa4-111">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="83fa4-111">Type: **const void\***</span></span>

<span data-ttu-id="83fa4-112">A chave de referência do arquivo de fonte que identifica exclusivamente o arquivo de fonte local dentro do escopo do carregador de fonte que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="83fa4-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="83fa4-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="83fa4-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="83fa4-114">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="83fa4-114">Type: **UINT32**</span></span>

<span data-ttu-id="83fa4-115">O tamanho da chave de referência do arquivo de fonte em bytes.</span><span class="sxs-lookup"><span data-stu-id="83fa4-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="83fa4-116">*LastWriteTime* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="83fa4-116">*lastWriteTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83fa4-117">Tipo: **FILETIME \***</span><span class="sxs-lookup"><span data-stu-id="83fa4-117">Type: **FILETIME\***</span></span>

<span data-ttu-id="83fa4-118">A hora da última modificação de arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="83fa4-118">The time of the last font file modification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83fa4-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83fa4-119">Return value</span></span>

<span data-ttu-id="83fa4-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="83fa4-120">Type: **HRESULT**</span></span>

<span data-ttu-id="83fa4-121">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="83fa4-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="83fa4-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="83fa4-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="83fa4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83fa4-123">Requirements</span></span>



| <span data-ttu-id="83fa4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="83fa4-124">Requirement</span></span> | <span data-ttu-id="83fa4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="83fa4-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83fa4-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="83fa4-126">Library</span></span><br/> | <dl> <span data-ttu-id="83fa4-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="83fa4-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="83fa4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="83fa4-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="83fa4-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83fa4-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83fa4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="83fa4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83fa4-131">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="83fa4-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





