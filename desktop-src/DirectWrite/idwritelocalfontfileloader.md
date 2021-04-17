---
title: Interface IDWriteLocalFontFileLoader
description: Uma implementação interna da interface IDWriteFontFileLoader, que opera em arquivos de fonte locais e expõe informações de arquivo de fonte local da chave de referência do arquivo de fonte.
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- Gravação direta da interface IDWriteLocalFontFileLoader
- Gravação direta da interface IDWriteLocalFontFileLoader, descrita
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65f537dc2a4a96161a11d85ae0a4e1869a331e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757167"
---
# <a name="idwritelocalfontfileloader-interface"></a><span data-ttu-id="c3253-105">Interface IDWriteLocalFontFileLoader</span><span class="sxs-lookup"><span data-stu-id="c3253-105">IDWriteLocalFontFileLoader interface</span></span>

<span data-ttu-id="c3253-106">Uma implementação interna da interface [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , que opera em arquivos de fonte locais e expõe informações de arquivo de fonte local da chave de referência do arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="c3253-106">A built-in implementation of the [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) interface, that operates on local font files and exposes local font file information from the font file reference key.</span></span> <span data-ttu-id="c3253-107">Referências de arquivo de fonte criadas usando [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) usam este carregador de arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="c3253-107">Font file references created using [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) use this font file loader.</span></span>

## <a name="members"></a><span data-ttu-id="c3253-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c3253-108">Members</span></span>

<span data-ttu-id="c3253-109">A interface **IDWriteLocalFontFileLoader** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c3253-109">The **IDWriteLocalFontFileLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c3253-110">**IDWriteLocalFontFileLoader** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c3253-110">**IDWriteLocalFontFileLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="c3253-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="c3253-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c3253-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="c3253-112">Methods</span></span>

<span data-ttu-id="c3253-113">A interface **IDWriteLocalFontFileLoader** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c3253-113">The **IDWriteLocalFontFileLoader** interface has these methods.</span></span>



| <span data-ttu-id="c3253-114">Método</span><span class="sxs-lookup"><span data-stu-id="c3253-114">Method</span></span>                                                                                  | <span data-ttu-id="c3253-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3253-115">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3253-116">**GetFilePathFromKey**</span><span class="sxs-lookup"><span data-stu-id="c3253-116">**GetFilePathFromKey**</span></span>](idwritelocalfontfileloader-getfilepathfromkey.md)             | <span data-ttu-id="c3253-117">Obtém o caminho do arquivo de fonte absoluto da chave de referência do arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="c3253-117">Obtains the absolute font file path from the font file reference key.</span></span><br/>          |
| [<span data-ttu-id="c3253-118">**GetFilePathLengthFromKey**</span><span class="sxs-lookup"><span data-stu-id="c3253-118">**GetFilePathLengthFromKey**</span></span>](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | <span data-ttu-id="c3253-119">Obtém o comprimento do caminho de arquivo absoluto da chave de referência do arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="c3253-119">Obtains the length of the absolute file path from the font file reference key.</span></span><br/> |
| [<span data-ttu-id="c3253-120">**GetLastWriteTimeFromKey**</span><span class="sxs-lookup"><span data-stu-id="c3253-120">**GetLastWriteTimeFromKey**</span></span>](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | <span data-ttu-id="c3253-121">Obtém a hora da última gravação do arquivo da chave de referência do arquivo de fonte.</span><span class="sxs-lookup"><span data-stu-id="c3253-121">Obtains the last write time of the file from the font file reference key.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="c3253-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3253-122">Requirements</span></span>



| <span data-ttu-id="c3253-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3253-123">Requirement</span></span> | <span data-ttu-id="c3253-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c3253-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3253-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3253-125">Library</span></span><br/> | <dl> <span data-ttu-id="c3253-126"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c3253-126"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="c3253-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c3253-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3253-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3253-128"><dt>Dwrite.dll</dt></span></span> </dl> |



 

