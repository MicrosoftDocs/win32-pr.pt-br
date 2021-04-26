---
description: Constantes que descrevem os tipos de dados de vértice com suporte de um dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 094ca568554722f4da2606233f4ad2c1e59e892f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999443"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="f0dbe-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="f0dbe-103">D3DDTCAPS</span></span>

<span data-ttu-id="f0dbe-104">Constantes que descrevem os tipos de dados de vértice com suporte de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f0dbe-104">Constants describing the vertex data types supported by a device.</span></span>



| <span data-ttu-id="f0dbe-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="f0dbe-105">\#define</span></span>              | <span data-ttu-id="f0dbe-106">Valor</span><span class="sxs-lookup"><span data-stu-id="f0dbe-106">Value</span></span>       | <span data-ttu-id="f0dbe-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f0dbe-107">Description</span></span>                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0dbe-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="f0dbe-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="f0dbe-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="f0dbe-109">0x00000001L</span></span> | <span data-ttu-id="f0dbe-110">byte de 4D não assinado.</span><span class="sxs-lookup"><span data-stu-id="f0dbe-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="f0dbe-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="f0dbe-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="f0dbe-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="f0dbe-112">0x00000002L</span></span> | <span data-ttu-id="f0dbe-113">Byte normalizado, 4D não assinado.</span><span class="sxs-lookup"><span data-stu-id="f0dbe-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="f0dbe-114">Cada um dos quatro bytes é normalizado dividindo para 255,0.</span><span class="sxs-lookup"><span data-stu-id="f0dbe-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="f0dbe-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="f0dbe-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="f0dbe-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="f0dbe-116">0x00000004L</span></span> | <span data-ttu-id="f0dbe-117">Normalizado, 2D assinado por curto, expandido para (primeiro byte/32767.0, segundo byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="f0dbe-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="f0dbe-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="f0dbe-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="f0dbe-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="f0dbe-119">0x00000008L</span></span> | <span data-ttu-id="f0dbe-120">Normalizado, 4D assinado curto, expandido para (primeiro byte/32767.0, segundo byte/32767.0, terceiro byte/32767.0, quarto byte/32767.0).</span><span class="sxs-lookup"><span data-stu-id="f0dbe-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="f0dbe-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="f0dbe-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="f0dbe-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="f0dbe-122">0x00000010L</span></span> | <span data-ttu-id="f0dbe-123">Normalizado, 2D não assinado curto, expandido para (primeiro byte/65535.0, segundo byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="f0dbe-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="f0dbe-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="f0dbe-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="f0dbe-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="f0dbe-125">0x00000020L</span></span> | <span data-ttu-id="f0dbe-126">4D normalizado não assinado curto, expandido para (primeiro byte/65535.0, segundo byte/65535.0, terceiro byte/65535.0, quarto byte/65535.0).</span><span class="sxs-lookup"><span data-stu-id="f0dbe-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="f0dbe-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="f0dbe-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="f0dbe-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="f0dbe-128">0x00000040L</span></span> | <span data-ttu-id="f0dbe-129">formato de 10 10 10 não assinado 3D expandido para (valor, valor, valor, 1).</span><span class="sxs-lookup"><span data-stu-id="f0dbe-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="f0dbe-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="f0dbe-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="f0dbe-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="f0dbe-131">0x00000080L</span></span> | <span data-ttu-id="f0dbe-132">formato 10 10 10 assinado 3D normalizado e expandido para (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="f0dbe-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="f0dbe-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="f0dbe-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="f0dbe-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="f0dbe-134">0x00000100L</span></span> | <span data-ttu-id="f0dbe-135">números de ponto flutuante de 16 bits 2D.</span><span class="sxs-lookup"><span data-stu-id="f0dbe-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="f0dbe-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="f0dbe-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="f0dbe-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="f0dbe-137">0x00000200L</span></span> | <span data-ttu-id="f0dbe-138">números de ponto flutuante de 16 bits 4D.</span><span class="sxs-lookup"><span data-stu-id="f0dbe-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="f0dbe-139">Essas constantes são usadas pelo membro DeclTypes de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="f0dbe-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="f0dbe-140">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="f0dbe-140">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="f0dbe-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0dbe-141">Header</span></span>                   | <span data-ttu-id="f0dbe-142">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="f0dbe-142">d3d9caps.h</span></span> |
| <span data-ttu-id="f0dbe-143">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="f0dbe-143">Minimum operating system</span></span> | <span data-ttu-id="f0dbe-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f0dbe-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f0dbe-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f0dbe-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0dbe-146">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f0dbe-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



