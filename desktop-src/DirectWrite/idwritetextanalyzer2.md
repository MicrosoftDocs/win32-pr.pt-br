---
title: Interface IDWriteTextAnalyzer2
description: Analisa várias propriedades de texto para processamento de script complexo.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- Gravação direta da interface IDWriteTextAnalyzer2
- Gravação direta da interface IDWriteTextAnalyzer2, descrita
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2548cc7961c8d866d4067e794e033701457d5b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499484"
---
# <a name="idwritetextanalyzer2-interface"></a><span data-ttu-id="5a7e8-105">Interface IDWriteTextAnalyzer2</span><span class="sxs-lookup"><span data-stu-id="5a7e8-105">IDWriteTextAnalyzer2 interface</span></span>

<span data-ttu-id="5a7e8-106">Analisa várias propriedades de texto para processamento de script complexo.</span><span class="sxs-lookup"><span data-stu-id="5a7e8-106">Analyzes various text properties for complex script processing.</span></span>

## <a name="members"></a><span data-ttu-id="5a7e8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="5a7e8-107">Members</span></span>

<span data-ttu-id="5a7e8-108">A interface **IDWriteTextAnalyzer2** herda de [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span><span class="sxs-lookup"><span data-stu-id="5a7e8-108">The **IDWriteTextAnalyzer2** interface inherits from [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span></span> <span data-ttu-id="5a7e8-109">**IDWriteTextAnalyzer2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5a7e8-109">**IDWriteTextAnalyzer2** also has these types of members:</span></span>

-   [<span data-ttu-id="5a7e8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="5a7e8-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5a7e8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="5a7e8-111">Methods</span></span>

<span data-ttu-id="5a7e8-112">A interface **IDWriteTextAnalyzer2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="5a7e8-112">The **IDWriteTextAnalyzer2** interface has these methods.</span></span>



| <span data-ttu-id="5a7e8-113">Método</span><span class="sxs-lookup"><span data-stu-id="5a7e8-113">Method</span></span>                                                                                    | <span data-ttu-id="5a7e8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a7e8-114">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a7e8-115">**CheckTypographicFeature**</span><span class="sxs-lookup"><span data-stu-id="5a7e8-115">**CheckTypographicFeature**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | <span data-ttu-id="5a7e8-116">Verifica se um recurso tipográfico está disponível para um glifo ou um conjunto de glifos.</span><span class="sxs-lookup"><span data-stu-id="5a7e8-116">Checks if a typographic feature is available for a glyph or a set of glyphs.</span></span><br/> |
| [<span data-ttu-id="5a7e8-117">**GetGlyphOrientationTransform**</span><span class="sxs-lookup"><span data-stu-id="5a7e8-117">**GetGlyphOrientationTransform**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | <span data-ttu-id="5a7e8-118">Retorna a matriz de transformação 2x3 para o respectivo ângulo para desenhar a execução de glifo.</span><span class="sxs-lookup"><span data-stu-id="5a7e8-118">Returns 2x3 transform matrix for the respective angle to draw the glyph run.</span></span><br/> |
| [<span data-ttu-id="5a7e8-119">**GetTypographicFeatures**</span><span class="sxs-lookup"><span data-stu-id="5a7e8-119">**GetTypographicFeatures**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | <span data-ttu-id="5a7e8-120">Retorna uma lista completa de recursos OpenType disponíveis para um script ou uma fonte.</span><span class="sxs-lookup"><span data-stu-id="5a7e8-120">Returns a complete list of OpenType features available for a script or font.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a7e8-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a7e8-121">Requirements</span></span>



| <span data-ttu-id="5a7e8-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a7e8-122">Requirement</span></span> | <span data-ttu-id="5a7e8-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5a7e8-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a7e8-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a7e8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="5a7e8-125">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="5a7e8-125">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="5a7e8-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5a7e8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="5a7e8-127">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="5a7e8-127">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="5a7e8-128">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="5a7e8-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="5a7e8-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="5a7e8-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="5a7e8-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a7e8-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="5a7e8-131"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a7e8-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5a7e8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5a7e8-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a7e8-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a7e8-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5a7e8-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="5a7e8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a7e8-135">**IDWriteTextAnalyzer1**</span><span class="sxs-lookup"><span data-stu-id="5a7e8-135">**IDWriteTextAnalyzer1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

