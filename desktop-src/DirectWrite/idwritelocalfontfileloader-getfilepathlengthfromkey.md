---
title: Método IDWriteLocalFontFileLoader GetFilePathLengthFromKey
description: Obtém o comprimento do caminho de arquivo absoluto da chave de referência do arquivo de fonte.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Gravação direta do método GetFilePathLengthFromKey
- Método GetFilePathLengthFromKey Direct Write, interface IDWriteLocalFontFileLoader
- IDWriteLocalFontFileLoader interface de gravação direta, método GetFilePathLengthFromKey
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750871"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a><span data-ttu-id="65eed-106">Método IDWriteLocalFontFileLoader:: GetFilePathLengthFromKey</span><span class="sxs-lookup"><span data-stu-id="65eed-106">IDWriteLocalFontFileLoader::GetFilePathLengthFromKey method</span></span>

<span data-ttu-id="65eed-107">Obtém o comprimento do caminho de arquivo absoluto da chave de referência do arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="65eed-107">Obtains the length of the absolute file path from the font file reference key.</span></span>

## <a name="syntax"></a><span data-ttu-id="65eed-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65eed-108">Syntax</span></span>


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a><span data-ttu-id="65eed-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65eed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65eed-110">*fontFileReferenceKey* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="65eed-110">*fontFileReferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65eed-111">Tipo: **const void \***</span><span class="sxs-lookup"><span data-stu-id="65eed-111">Type: **const void\***</span></span>

<span data-ttu-id="65eed-112">Chave de referência do arquivo de fonte que identifica exclusivamente o arquivo de fonte local dentro do escopo do carregador de fonte que está sendo usado.</span><span class="sxs-lookup"><span data-stu-id="65eed-112">Font file reference key that uniquely identifies the local font file within the scope of the font loader being used.</span></span>

</dd> <dt>

<span data-ttu-id="65eed-113">*fontFileReferenceKeySize*</span><span class="sxs-lookup"><span data-stu-id="65eed-113">*fontFileReferenceKeySize*</span></span> 
</dt> <dd>

<span data-ttu-id="65eed-114">Tipo: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="65eed-114">Type: **UINT32**</span></span>

<span data-ttu-id="65eed-115">Tamanho da chave de referência do arquivo de fonte em bytes.</span><span class="sxs-lookup"><span data-stu-id="65eed-115">Size of font file reference key in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="65eed-116">*filePathLength* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="65eed-116">*filePathLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65eed-117">Tipo: **UINT32 \***</span><span class="sxs-lookup"><span data-stu-id="65eed-117">Type: **UINT32\***</span></span>

<span data-ttu-id="65eed-118">Comprimento da cadeia de caracteres do caminho do arquivo, sem incluir o caractere **nulo** finalizado.</span><span class="sxs-lookup"><span data-stu-id="65eed-118">Length of the file path string, not including the terminated **NULL** character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65eed-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="65eed-119">Return value</span></span>

<span data-ttu-id="65eed-120">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="65eed-120">Type: **HRESULT**</span></span>

<span data-ttu-id="65eed-121">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="65eed-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65eed-122">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="65eed-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="65eed-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65eed-123">Requirements</span></span>



| <span data-ttu-id="65eed-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="65eed-124">Requirement</span></span> | <span data-ttu-id="65eed-125">Valor</span><span class="sxs-lookup"><span data-stu-id="65eed-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65eed-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65eed-126">Library</span></span><br/> | <dl> <span data-ttu-id="65eed-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="65eed-127"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="65eed-128">DLL</span><span class="sxs-lookup"><span data-stu-id="65eed-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="65eed-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65eed-129"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65eed-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="65eed-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65eed-131">**IDWriteLocalFontFileLoader**</span><span class="sxs-lookup"><span data-stu-id="65eed-131">**IDWriteLocalFontFileLoader**</span></span>](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





