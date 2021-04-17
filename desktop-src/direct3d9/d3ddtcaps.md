---
description: Constantes que descrevem os tipos de dados de vértice com suporte de um dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49131fed9961782a6ade3d3ec5f541bb0fe63a50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763514"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="415d9-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="415d9-103">D3DDTCAPS</span></span>

<span data-ttu-id="415d9-104">Constantes que descrevem os tipos de dados de vértice com suporte de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="415d9-104">Constants describing the vertex data types supported by a device.</span></span>



|                       |             |                                                                                                                               |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="415d9-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="415d9-105">\#define</span></span>              | <span data-ttu-id="415d9-106">Valor</span><span class="sxs-lookup"><span data-stu-id="415d9-106">Value</span></span>       | <span data-ttu-id="415d9-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="415d9-107">Description</span></span>                                                                                                                   |
| <span data-ttu-id="415d9-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="415d9-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="415d9-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="415d9-109">0x00000001L</span></span> | <span data-ttu-id="415d9-110">byte de 4D não assinado.</span><span class="sxs-lookup"><span data-stu-id="415d9-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="415d9-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="415d9-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="415d9-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="415d9-112">0x00000002L</span></span> | <span data-ttu-id="415d9-113">Byte normalizado, 4D não assinado.</span><span class="sxs-lookup"><span data-stu-id="415d9-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="415d9-114">Cada um dos quatro bytes é normalizado dividindo para 255,0.</span><span class="sxs-lookup"><span data-stu-id="415d9-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="415d9-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="415d9-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="415d9-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="415d9-116">0x00000004L</span></span> | <span data-ttu-id="415d9-117">Normalizado, 2D assinado por curto, expandido para (primeiro byte/32767.0, segundo byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="415d9-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="415d9-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="415d9-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="415d9-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="415d9-119">0x00000008L</span></span> | <span data-ttu-id="415d9-120">Normalizado, 4D assinado curto, expandido para (primeiro byte/32767.0, segundo byte/32767.0, terceiro byte/32767.0, quarto byte/32767.0).</span><span class="sxs-lookup"><span data-stu-id="415d9-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="415d9-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="415d9-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="415d9-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="415d9-122">0x00000010L</span></span> | <span data-ttu-id="415d9-123">Normalizado, 2D não assinado curto, expandido para (primeiro byte/65535.0, segundo byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="415d9-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="415d9-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="415d9-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="415d9-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="415d9-125">0x00000020L</span></span> | <span data-ttu-id="415d9-126">4D normalizado não assinado curto, expandido para (primeiro byte/65535.0, segundo byte/65535.0, terceiro byte/65535.0, quarto byte/65535.0).</span><span class="sxs-lookup"><span data-stu-id="415d9-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="415d9-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="415d9-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="415d9-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="415d9-128">0x00000040L</span></span> | <span data-ttu-id="415d9-129">formato de 10 10 10 não assinado 3D expandido para (valor, valor, valor, 1).</span><span class="sxs-lookup"><span data-stu-id="415d9-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="415d9-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="415d9-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="415d9-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="415d9-131">0x00000080L</span></span> | <span data-ttu-id="415d9-132">formato 10 10 10 assinado 3D normalizado e expandido para (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="415d9-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="415d9-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="415d9-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="415d9-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="415d9-134">0x00000100L</span></span> | <span data-ttu-id="415d9-135">números de ponto flutuante de 16 bits 2D.</span><span class="sxs-lookup"><span data-stu-id="415d9-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="415d9-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="415d9-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="415d9-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="415d9-137">0x00000200L</span></span> | <span data-ttu-id="415d9-138">números de ponto flutuante de 16 bits 4D.</span><span class="sxs-lookup"><span data-stu-id="415d9-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="415d9-139">Essas constantes são usadas pelo membro DeclTypes de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="415d9-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="415d9-140">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="415d9-140">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="415d9-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="415d9-141">Header</span></span>                   | <span data-ttu-id="415d9-142">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="415d9-142">d3d9caps.h</span></span> |
| <span data-ttu-id="415d9-143">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="415d9-143">Minimum operating system</span></span> | <span data-ttu-id="415d9-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="415d9-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="415d9-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="415d9-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="415d9-146">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="415d9-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



