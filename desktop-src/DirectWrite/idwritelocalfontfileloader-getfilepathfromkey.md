---
title: Método IDWriteLocalFontFileLoader GetFilePathFromKey
description: Obtém o caminho do arquivo de fonte absoluto da chave de referência do arquivo de fonte.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Gravação direta do método GetFilePathFromKey
- Método GetFilePathFromKey Direct Write, interface IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader interface de gravação direta, método GetFilePathFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768770"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a><span data-ttu-id="2bfa7-106">Método IDWriteLocalFontFileLoader:: GetFilePathFromKey</span><span class="sxs-lookup"><span data-stu-id="2bfa7-106">IDWriteLocalFontFileLoader::GetFilePathFromKey method</span></span>

<span data-ttu-id="2bfa7-107">Obtém o caminho do arquivo de fonte absoluto da chave de referência do arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="2bfa7-107">Obtains the absolute font file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bfa7-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2bfa7-108">Syntax</span></span>


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="2bfa7-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bfa7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bfa7-110">*fontFileReferenceKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2bfa7-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2bfa7-111">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="2bfa7-111">Type: **const void\***</span></span>

<span data-ttu-id="2bfa7-112">A chave de referência do arquivo de fonte que identifica exclusivamente o arquivo de fonte local dentro do escopo do carregador de fonte que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="2bfa7-112">The font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="2bfa7-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="2bfa7-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="2bfa7-114">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="2bfa7-114">Type: **UINT32**</span></span>

<span data-ttu-id="2bfa7-115">O tamanho da chave de referência do arquivo de fonte em bytes.</span><span class="sxs-lookup"><span data-stu-id="2bfa7-115">The size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2bfa7-116">*FilePath* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2bfa7-116">*filePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2bfa7-117">Tipo: **WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="2bfa7-117">Type: **WCHAR\***</span></span>

<span data-ttu-id="2bfa7-118">A matriz de caracteres que recebe o caminho do arquivo local.</span><span class="sxs-lookup"><span data-stu-id="2bfa7-118">The character array that receives the local file path.</span></span>

</dd> <dt>

<span data-ttu-id="2bfa7-119">*filePaths*</span><span class="sxs-lookup"><span data-stu-id="2bfa7-119">*filePathSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2bfa7-120">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="2bfa7-120">Type: **UINT32**</span></span>

<span data-ttu-id="2bfa7-121">O comprimento da matriz de caracteres do caminho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2bfa7-121">The length of the file path character array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bfa7-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2bfa7-122">Return value</span></span>

<span data-ttu-id="2bfa7-123">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="2bfa7-123">Type: **HRESULT**</span></span>

<span data-ttu-id="2bfa7-124">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2bfa7-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2bfa7-125">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2bfa7-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bfa7-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bfa7-126">Requirements</span></span>



| <span data-ttu-id="2bfa7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bfa7-127">Requirement</span></span> | <span data-ttu-id="2bfa7-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2bfa7-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bfa7-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2bfa7-129">Library</span></span><br/> | <dl> <span data-ttu-id="2bfa7-130"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bfa7-130"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="2bfa7-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2bfa7-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="2bfa7-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bfa7-132"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bfa7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bfa7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bfa7-134">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="2bfa7-134">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





