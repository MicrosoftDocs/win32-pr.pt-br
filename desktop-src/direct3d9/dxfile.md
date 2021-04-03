---
description: Os sinalizadores a seguir são usados para especificar em quais canais em uma textura operar. Preterido.
ms.assetid: 6e421a0a-7e82-4640-a96c-7ec648df970d
title: Constantes DXFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f1651d17f5acb2ef24ff9dae2ef547c3df7c0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009995"
---
# <a name="dxfile-constants"></a><span data-ttu-id="09ffe-104">Constantes DXFILE</span><span class="sxs-lookup"><span data-stu-id="09ffe-104">DXFILE Constants</span></span>

<span data-ttu-id="09ffe-105">Os sinalizadores a seguir são usados para especificar em quais canais em uma textura operar.</span><span class="sxs-lookup"><span data-stu-id="09ffe-105">The following flags are used to specify which channels in a texture to operate on.</span></span> <span data-ttu-id="09ffe-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="09ffe-106">Deprecated.</span></span>

## <a name="dxfileformat"></a><span data-ttu-id="09ffe-107">DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="09ffe-107">DXFILEFORMAT</span></span>



|                          |       |                  |
|--------------------------|-------|------------------|
| <span data-ttu-id="09ffe-108">\#definir</span><span class="sxs-lookup"><span data-stu-id="09ffe-108">\#define</span></span>                 | <span data-ttu-id="09ffe-109">Valor</span><span class="sxs-lookup"><span data-stu-id="09ffe-109">Value</span></span> | <span data-ttu-id="09ffe-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="09ffe-110">Description</span></span>      |
| <span data-ttu-id="09ffe-111">DXFILEFORMAT \_ binário</span><span class="sxs-lookup"><span data-stu-id="09ffe-111">DXFILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="09ffe-112">0</span><span class="sxs-lookup"><span data-stu-id="09ffe-112">0</span></span>     | <span data-ttu-id="09ffe-113">Arquivo binário.</span><span class="sxs-lookup"><span data-stu-id="09ffe-113">Binary file.</span></span>     |
| <span data-ttu-id="09ffe-114">\_texto DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="09ffe-114">DXFILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="09ffe-115">1</span><span class="sxs-lookup"><span data-stu-id="09ffe-115">1</span></span>     | <span data-ttu-id="09ffe-116">Arquivo de texto.</span><span class="sxs-lookup"><span data-stu-id="09ffe-116">Text file.</span></span>       |
| <span data-ttu-id="09ffe-117">DXFILEFORMAT \_ compactados</span><span class="sxs-lookup"><span data-stu-id="09ffe-117">DXFILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="09ffe-118">2</span><span class="sxs-lookup"><span data-stu-id="09ffe-118">2</span></span>     | <span data-ttu-id="09ffe-119">Arquivo compactado.</span><span class="sxs-lookup"><span data-stu-id="09ffe-119">Compressed file.</span></span> |



 

<span data-ttu-id="09ffe-120">Essas \# definições são declaradas em Dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="09ffe-120">These \#defines are declared in Dxfile.h.</span></span>

## <a name="dxfileloadoptions"></a><span data-ttu-id="09ffe-121">DXFILELOADOPTIONS</span><span class="sxs-lookup"><span data-stu-id="09ffe-121">DXFILELOADOPTIONS</span></span>



|                          |       |                              |
|--------------------------|-------|------------------------------|
| <span data-ttu-id="09ffe-122">\#definir</span><span class="sxs-lookup"><span data-stu-id="09ffe-122">\#define</span></span>                 | <span data-ttu-id="09ffe-123">Valor</span><span class="sxs-lookup"><span data-stu-id="09ffe-123">Value</span></span> | <span data-ttu-id="09ffe-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="09ffe-124">Description</span></span>                  |
| <span data-ttu-id="09ffe-125">DXFILELOAD \_ defile</span><span class="sxs-lookup"><span data-stu-id="09ffe-125">DXFILELOAD\_FROMFILE</span></span>     | <span data-ttu-id="09ffe-126">0x00l</span><span class="sxs-lookup"><span data-stu-id="09ffe-126">0x00L</span></span> | <span data-ttu-id="09ffe-127">Carregar um arquivo de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="09ffe-127">Load a file from a file.</span></span>     |
| <span data-ttu-id="09ffe-128">DXFILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="09ffe-128">DXFILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="09ffe-129">0x01L</span><span class="sxs-lookup"><span data-stu-id="09ffe-129">0x01L</span></span> | <span data-ttu-id="09ffe-130">Carregar um arquivo de um recurso.</span><span class="sxs-lookup"><span data-stu-id="09ffe-130">Load a file from a resource.</span></span> |
| <span data-ttu-id="09ffe-131">DXFILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="09ffe-131">DXFILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="09ffe-132">0x02L</span><span class="sxs-lookup"><span data-stu-id="09ffe-132">0x02L</span></span> | <span data-ttu-id="09ffe-133">Carregar um arquivo da memória.</span><span class="sxs-lookup"><span data-stu-id="09ffe-133">Load a file from memory.</span></span>     |
| <span data-ttu-id="09ffe-134">DXFILELOAD \_ FROMSTREAM</span><span class="sxs-lookup"><span data-stu-id="09ffe-134">DXFILELOAD\_FROMSTREAM</span></span>   | <span data-ttu-id="09ffe-135">0x04L</span><span class="sxs-lookup"><span data-stu-id="09ffe-135">0x04L</span></span> | <span data-ttu-id="09ffe-136">Carregar um arquivo de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="09ffe-136">Load a file from a stream.</span></span>   |
| <span data-ttu-id="09ffe-137">DXFILELOAD \_ FROMURL</span><span class="sxs-lookup"><span data-stu-id="09ffe-137">DXFILELOAD\_FROMURL</span></span>      | <span data-ttu-id="09ffe-138">0x08L</span><span class="sxs-lookup"><span data-stu-id="09ffe-138">0x08L</span></span> | <span data-ttu-id="09ffe-139">Carregar um arquivo de uma URL.</span><span class="sxs-lookup"><span data-stu-id="09ffe-139">Load a file from a URL.</span></span>      |



 

<span data-ttu-id="09ffe-140">Essas \# definições são declaradas em Dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="09ffe-140">These \#defines are declared in Dxfile.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="09ffe-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="09ffe-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09ffe-142">X referência de arquivo (herdada)</span><span class="sxs-lookup"><span data-stu-id="09ffe-142">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



