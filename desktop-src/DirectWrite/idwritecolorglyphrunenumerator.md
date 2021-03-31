---
title: Interface IDWriteColorGlyphRunEnumerator
description: Essa interface permite que o aplicativo enumere por meio das execuções de glifos de cores.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Gravação direta da interface IDWriteColorGlyphRunEnumerator
- Gravação direta da interface IDWriteColorGlyphRunEnumerator, descrita
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644834"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a><span data-ttu-id="18a6f-105">Interface IDWriteColorGlyphRunEnumerator</span><span class="sxs-lookup"><span data-stu-id="18a6f-105">IDWriteColorGlyphRunEnumerator interface</span></span>

<span data-ttu-id="18a6f-106">Essa interface permite que o aplicativo enumere por meio das execuções de glifos de cores.</span><span class="sxs-lookup"><span data-stu-id="18a6f-106">This interface allows the application to enumerate through the color glyph runs.</span></span> <span data-ttu-id="18a6f-107">O enumerador enumera as camadas de volta ao front Order para a disposição em camadas apropriada.</span><span class="sxs-lookup"><span data-stu-id="18a6f-107">The enumerator enumerates the layers in a back to front order for appropriate layering.</span></span>

## <a name="members"></a><span data-ttu-id="18a6f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="18a6f-108">Members</span></span>

<span data-ttu-id="18a6f-109">A interface **IDWriteColorGlyphRunEnumerator** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="18a6f-109">The **IDWriteColorGlyphRunEnumerator** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="18a6f-110">**IDWriteColorGlyphRunEnumerator** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="18a6f-110">**IDWriteColorGlyphRunEnumerator** also has these types of members:</span></span>

-   [<span data-ttu-id="18a6f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="18a6f-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="18a6f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="18a6f-112">Methods</span></span>

<span data-ttu-id="18a6f-113">A interface **IDWriteColorGlyphRunEnumerator** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="18a6f-113">The **IDWriteColorGlyphRunEnumerator** interface has these methods.</span></span>



| <span data-ttu-id="18a6f-114">Método</span><span class="sxs-lookup"><span data-stu-id="18a6f-114">Method</span></span>                                                                | <span data-ttu-id="18a6f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="18a6f-115">Description</span></span>                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="18a6f-116">**GetCurrentRun**</span><span class="sxs-lookup"><span data-stu-id="18a6f-116">**GetCurrentRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | <span data-ttu-id="18a6f-117">Retorna a execução de glifo atual do enumerador.</span><span class="sxs-lookup"><span data-stu-id="18a6f-117">Returns the current glyph run of the enumerator.</span></span><br/> |
| [<span data-ttu-id="18a6f-118">**MoveNext**</span><span class="sxs-lookup"><span data-stu-id="18a6f-118">**MoveNext**</span></span>](idwritecolorglyphrunenumerator-movenext.md)           | <span data-ttu-id="18a6f-119">Mover para a próxima execução de glifo no enumerador.</span><span class="sxs-lookup"><span data-stu-id="18a6f-119">Move to the next glyph run in the enumerator.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="18a6f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18a6f-120">Requirements</span></span>



| <span data-ttu-id="18a6f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="18a6f-121">Requirement</span></span> | <span data-ttu-id="18a6f-122">Valor</span><span class="sxs-lookup"><span data-stu-id="18a6f-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18a6f-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18a6f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="18a6f-124">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="18a6f-124">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="18a6f-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="18a6f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="18a6f-126">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="18a6f-126">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="18a6f-127">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="18a6f-127">Minimum supported phone</span></span><br/>  | <span data-ttu-id="18a6f-128">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="18a6f-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="18a6f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18a6f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="18a6f-130"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18a6f-130"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="18a6f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="18a6f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18a6f-132"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18a6f-132"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

