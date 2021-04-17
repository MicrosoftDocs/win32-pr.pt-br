---
title: Interface IDWriteFactory2
description: A interface de fábrica raiz para todos os objetos DirectWrite.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- Gravação direta da interface IDWriteFactory1
- Gravação direta da interface IDWriteFactory1, descrita
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7d5ba0f8d480981ab6ebea6dcdbd955b7b967e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105782830"
---
# <a name="idwritefactory2-interface"></a><span data-ttu-id="ff88c-105">Interface IDWriteFactory2</span><span class="sxs-lookup"><span data-stu-id="ff88c-105">IDWriteFactory2 interface</span></span>

<span data-ttu-id="ff88c-106">A interface de fábrica raiz para todos os objetos [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="ff88c-106">The root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="ff88c-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ff88c-107">Members</span></span>

<span data-ttu-id="ff88c-108">A interface **IDWriteFactory1** herda de [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span><span class="sxs-lookup"><span data-stu-id="ff88c-108">The **IDWriteFactory1** interface inherits from [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span></span> <span data-ttu-id="ff88c-109">**IDWriteFactory2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ff88c-109">**IDWriteFactory2** also has these types of members:</span></span>

-   [<span data-ttu-id="ff88c-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="ff88c-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ff88c-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="ff88c-111">Methods</span></span>

<span data-ttu-id="ff88c-112">A interface **IDWriteFactory1** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ff88c-112">The **IDWriteFactory1** interface has these methods.</span></span>



| <span data-ttu-id="ff88c-113">Método</span><span class="sxs-lookup"><span data-stu-id="ff88c-113">Method</span></span>                                                                             | <span data-ttu-id="ff88c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff88c-114">Description</span></span>                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff88c-115">**CreateCustomRenderingParams**</span><span class="sxs-lookup"><span data-stu-id="ff88c-115">**CreateCustomRenderingParams**</span></span>](idwritefactory2-createcustomrenderingparams.md) | <span data-ttu-id="ff88c-116">Cria um objeto de parâmetros de renderização com as propriedades especificadas.</span><span class="sxs-lookup"><span data-stu-id="ff88c-116">Creates a rendering parameters object with the specified properties.</span></span><br/>                            |
| [<span data-ttu-id="ff88c-117">**CreateFontFallbackBuilder**</span><span class="sxs-lookup"><span data-stu-id="ff88c-117">**CreateFontFallbackBuilder**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | <span data-ttu-id="ff88c-118">Cria um objeto do construtor de fallback de fonte.</span><span class="sxs-lookup"><span data-stu-id="ff88c-118">Creates a font fallback builder object.</span></span><br/>                                                         |
| [<span data-ttu-id="ff88c-119">**CreateGlyphRunAnalysis**</span><span class="sxs-lookup"><span data-stu-id="ff88c-119">**CreateGlyphRunAnalysis**</span></span>](idwritefactory2-createglyphrunanalysis.md)           | <span data-ttu-id="ff88c-120">Cria um objeto de análise de execução de glifos, que encapsula informações usadas para renderizar uma execução de glifo.</span><span class="sxs-lookup"><span data-stu-id="ff88c-120">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span><br/> |
| [<span data-ttu-id="ff88c-121">**GetSystemFontFallback**</span><span class="sxs-lookup"><span data-stu-id="ff88c-121">**GetSystemFontFallback**</span></span>](idwritefactory2-getsystemfontfallback.md)             | <span data-ttu-id="ff88c-122">Cria um objeto de fallback de fonte da lista de fallback de fontes do sistema.</span><span class="sxs-lookup"><span data-stu-id="ff88c-122">Creates a font fallback object from the system font fallback list.</span></span><br/>                              |
| [<span data-ttu-id="ff88c-123">**TranslateColorGlyphRun**</span><span class="sxs-lookup"><span data-stu-id="ff88c-123">**TranslateColorGlyphRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | <span data-ttu-id="ff88c-124">Esse método é chamado em uma execução de glifo para convertê-lo em várias execuções de glifos de cores.</span><span class="sxs-lookup"><span data-stu-id="ff88c-124">This method is called on a glyph run to translate it in to multiple color glyph runs.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="ff88c-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff88c-125">Requirements</span></span>



| <span data-ttu-id="ff88c-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff88c-126">Requirement</span></span> | <span data-ttu-id="ff88c-127">Valor</span><span class="sxs-lookup"><span data-stu-id="ff88c-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff88c-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff88c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ff88c-129">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ff88c-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="ff88c-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff88c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ff88c-131">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="ff88c-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="ff88c-132">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="ff88c-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="ff88c-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="ff88c-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="ff88c-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff88c-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff88c-135"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff88c-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ff88c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ff88c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff88c-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff88c-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ff88c-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff88c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff88c-139">**IDWriteFactory1**</span><span class="sxs-lookup"><span data-stu-id="ff88c-139">**IDWriteFactory1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[<span data-ttu-id="ff88c-140">**IDWriteFactory**</span><span class="sxs-lookup"><span data-stu-id="ff88c-140">**IDWriteFactory**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

