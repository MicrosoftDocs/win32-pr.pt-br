---
title: Interface IDWriteFontFallbackBuilder
description: Permite que você crie mapeamentos de fallback de fonte Unicode e crie um objeto de retorno de fonte a partir desses mapeamentos.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Gravação direta da interface IDWriteFontFallbackBuilder
- Gravação direta da interface IDWriteFontFallbackBuilder, descrita
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918685"
---
# <a name="idwritefontfallbackbuilder-interface"></a><span data-ttu-id="200f8-105">Interface IDWriteFontFallbackBuilder</span><span class="sxs-lookup"><span data-stu-id="200f8-105">IDWriteFontFallbackBuilder interface</span></span>

<span data-ttu-id="200f8-106">Permite que você crie mapeamentos de fallback de fonte Unicode e crie um objeto de retorno de fonte a partir desses mapeamentos.</span><span class="sxs-lookup"><span data-stu-id="200f8-106">Allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.</span></span>

## <a name="members"></a><span data-ttu-id="200f8-107">Membros</span><span class="sxs-lookup"><span data-stu-id="200f8-107">Members</span></span>

<span data-ttu-id="200f8-108">A interface **IDWriteFontFallbackBuilder** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="200f8-108">The **IDWriteFontFallbackBuilder** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="200f8-109">**IDWriteFontFallbackBuilder** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="200f8-109">**IDWriteFontFallbackBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="200f8-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="200f8-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="200f8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="200f8-111">Methods</span></span>

<span data-ttu-id="200f8-112">A interface **IDWriteFontFallbackBuilder** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="200f8-112">The **IDWriteFontFallbackBuilder** interface has these methods.</span></span>



| <span data-ttu-id="200f8-113">Método</span><span class="sxs-lookup"><span data-stu-id="200f8-113">Method</span></span>                                                                      | <span data-ttu-id="200f8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="200f8-114">Description</span></span>                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="200f8-115">**AddMapping**</span><span class="sxs-lookup"><span data-stu-id="200f8-115">**AddMapping**</span></span>](idwritefontfallbackbuilder-addmapping.md)                 | <span data-ttu-id="200f8-116">Anexa um único mapeamento à lista.</span><span class="sxs-lookup"><span data-stu-id="200f8-116">Appends a single mapping to the list.</span></span> <span data-ttu-id="200f8-117">Chame isso uma vez para cada mapeamento adicional.</span><span class="sxs-lookup"><span data-stu-id="200f8-117">Call this once for each additional mapping.</span></span><br/> |
| [<span data-ttu-id="200f8-118">**Addmapeamentos**</span><span class="sxs-lookup"><span data-stu-id="200f8-118">**AddMappings**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | <span data-ttu-id="200f8-119">Adicione todos os mapeamentos de um objeto de fallback de fonte existente.</span><span class="sxs-lookup"><span data-stu-id="200f8-119">Add all the mappings from an existing font fallback object.</span></span><br/>                       |
| [<span data-ttu-id="200f8-120">**CreateFontFallback**</span><span class="sxs-lookup"><span data-stu-id="200f8-120">**CreateFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | <span data-ttu-id="200f8-121">Cria o objeto de fallback finalizado dos mapeamentos adicionados.</span><span class="sxs-lookup"><span data-stu-id="200f8-121">Creates the finalized fallback object from the mappings added.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="200f8-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="200f8-122">Requirements</span></span>



| <span data-ttu-id="200f8-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="200f8-123">Requirement</span></span> | <span data-ttu-id="200f8-124">Valor</span><span class="sxs-lookup"><span data-stu-id="200f8-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="200f8-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="200f8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="200f8-126">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="200f8-126">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="200f8-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="200f8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="200f8-128">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="200f8-128">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="200f8-129">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="200f8-129">Minimum supported phone</span></span><br/>  | <span data-ttu-id="200f8-130">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="200f8-130">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="200f8-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="200f8-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="200f8-132"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="200f8-132"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="200f8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="200f8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="200f8-134"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="200f8-134"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

