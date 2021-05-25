---
description: Constantes que descrevem os tipos de dados de vértice com suporte de um dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ded570b8f451ea7e99050467f70f945d202bd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343222"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="7fe01-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="7fe01-103">D3DDTCAPS</span></span>

<span data-ttu-id="7fe01-104">Constantes que descrevem os tipos de dados de vértice com suporte de um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7fe01-104">Constants describing the vertex data types supported by a device.</span></span>



| <span data-ttu-id="7fe01-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="7fe01-105">\#define</span></span>              | <span data-ttu-id="7fe01-106">Valor</span><span class="sxs-lookup"><span data-stu-id="7fe01-106">Value</span></span>       | <span data-ttu-id="7fe01-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7fe01-107">Description</span></span>                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe01-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="7fe01-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="7fe01-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="7fe01-109">0x00000001L</span></span> | <span data-ttu-id="7fe01-110">byte de 4D não assinado.</span><span class="sxs-lookup"><span data-stu-id="7fe01-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="7fe01-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="7fe01-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="7fe01-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="7fe01-112">0x00000002L</span></span> | <span data-ttu-id="7fe01-113">Byte normalizado, 4D não assinado.</span><span class="sxs-lookup"><span data-stu-id="7fe01-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="7fe01-114">Cada um dos quatro bytes é normalizado dividindo para 255,0.</span><span class="sxs-lookup"><span data-stu-id="7fe01-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="7fe01-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="7fe01-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="7fe01-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="7fe01-116">0x00000004L</span></span> | <span data-ttu-id="7fe01-117">Normalizado, 2D assinado por curto, expandido para (primeiro byte/32767.0, segundo byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="7fe01-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="7fe01-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="7fe01-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="7fe01-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="7fe01-119">0x00000008L</span></span> | <span data-ttu-id="7fe01-120">Normalizado, 4D assinado curto, expandido para (primeiro byte/32767.0, segundo byte/32767.0, terceiro byte/32767.0, quarto byte/32767.0).</span><span class="sxs-lookup"><span data-stu-id="7fe01-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="7fe01-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="7fe01-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="7fe01-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="7fe01-122">0x00000010L</span></span> | <span data-ttu-id="7fe01-123">Normalizado, 2D não assinado curto, expandido para (primeiro byte/65535.0, segundo byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="7fe01-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="7fe01-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="7fe01-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="7fe01-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="7fe01-125">0x00000020L</span></span> | <span data-ttu-id="7fe01-126">4D normalizado não assinado curto, expandido para (primeiro byte/65535.0, segundo byte/65535.0, terceiro byte/65535.0, quarto byte/65535.0).</span><span class="sxs-lookup"><span data-stu-id="7fe01-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="7fe01-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="7fe01-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="7fe01-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="7fe01-128">0x00000040L</span></span> | <span data-ttu-id="7fe01-129">Formato 3D sem assinatura 10 10 10 expandido para (valor, valor, valor, 1).</span><span class="sxs-lookup"><span data-stu-id="7fe01-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="7fe01-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="7fe01-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="7fe01-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="7fe01-131">0x00000080L</span></span> | <span data-ttu-id="7fe01-132">Formato 3D assinado 10 10 10 normalizado e expandido para (v \[ 0 \] /511.0, v \[ 1 \] /511.0, v \[ 2 \] /511.0, 1).</span><span class="sxs-lookup"><span data-stu-id="7fe01-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="7fe01-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="7fe01-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="7fe01-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="7fe01-134">0x00000100L</span></span> | <span data-ttu-id="7fe01-135">Números de ponto flutuante de 16 bits 2D.</span><span class="sxs-lookup"><span data-stu-id="7fe01-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="7fe01-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="7fe01-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="7fe01-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="7fe01-137">0x00000200L</span></span> | <span data-ttu-id="7fe01-138">Números de ponto flutuante de 16 bits 4D.</span><span class="sxs-lookup"><span data-stu-id="7fe01-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="7fe01-139">Essas constantes são usadas pelo membro DeclTypes de [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="7fe01-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="7fe01-140">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="7fe01-140">Constant Information</span></span>



|  <span data-ttu-id="7fe01-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fe01-141">Requirement</span></span>                        | <span data-ttu-id="7fe01-142">Valor</span><span class="sxs-lookup"><span data-stu-id="7fe01-142">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="7fe01-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7fe01-143">Header</span></span>                   | <span data-ttu-id="7fe01-144">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="7fe01-144">d3d9caps.h</span></span> |
| <span data-ttu-id="7fe01-145">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="7fe01-145">Minimum operating system</span></span> | <span data-ttu-id="7fe01-146">Windows 98</span><span class="sxs-lookup"><span data-stu-id="7fe01-146">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="7fe01-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7fe01-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fe01-148">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="7fe01-148">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



