---
title: Registro de cor de entrada
description: Registro de entrada do sombreador de pixel que contém a cor do vértice.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364484"
---
# <a name="input-color-register"></a><span data-ttu-id="a7115-103">Registro de cor de entrada</span><span class="sxs-lookup"><span data-stu-id="a7115-103">Input Color Register</span></span>

<span data-ttu-id="a7115-104">Registro de entrada do sombreador de pixel que contém a cor do vértice.</span><span class="sxs-lookup"><span data-stu-id="a7115-104">Pixel shader input register containing vertex color.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7115-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7115-105">Syntax</span></span>


```
dcl v#.writeMask
```



<span data-ttu-id="a7115-106">em que:</span><span class="sxs-lookup"><span data-stu-id="a7115-106">where:</span></span>

-   <span data-ttu-id="a7115-107">[DCL-(SM2, SM3-PS ASM)](dcl---ps.md) é uma instrução de declaração de registro.</span><span class="sxs-lookup"><span data-stu-id="a7115-107">[dcl - (sm2, sm3 - ps asm)](dcl---ps.md) is a register declaration instruction.</span></span>
-   <span data-ttu-id="a7115-108">v é um registro de entrada e \# é o número de registro.</span><span class="sxs-lookup"><span data-stu-id="a7115-108">v is an input register and \# is the register number.</span></span> <span data-ttu-id="a7115-109">O número de registros permitidos é determinado pela versão do sombreador.</span><span class="sxs-lookup"><span data-stu-id="a7115-109">The number of registers allowed is determined by the shader version.</span></span>
-   <span data-ttu-id="a7115-110">writeMask determina quais componentes (até quatro) são gravados.</span><span class="sxs-lookup"><span data-stu-id="a7115-110">writeMask determines which components (up to four) are written.</span></span> <span data-ttu-id="a7115-111">Os componentes válidos são: (x, y, z, w) ou (r, g, b, a).</span><span class="sxs-lookup"><span data-stu-id="a7115-111">Valid components are: (x,y,z,w) or (r,g,b,a).</span></span>

## <a name="remarks"></a><span data-ttu-id="a7115-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7115-112">Remarks</span></span>

<span data-ttu-id="a7115-113">Os registros de cores são registros somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a7115-113">Color registers are read-only registers.</span></span> <span data-ttu-id="a7115-114">Cada registrador contém valores RGBA de quatro componentes iterados a partir de vértices de entrada.</span><span class="sxs-lookup"><span data-stu-id="a7115-114">Each register contains four-component RGBA values iterated from input vertices.</span></span> <span data-ttu-id="a7115-115">Eles têm uma precisão menor do que a maioria dos registros, garantindo que tenham 8 bits de dados não assinados no intervalo (0, + 1).</span><span class="sxs-lookup"><span data-stu-id="a7115-115">They have lower precision than most registers, guaranteed to have 8 bits of unsigned data in the range (0, +1).</span></span> <span data-ttu-id="a7115-116">Você não pode usar mais de um em uma única instrução.</span><span class="sxs-lookup"><span data-stu-id="a7115-116">You cannot use more than one in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7115-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a7115-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7115-118">Register</span><span class="sxs-lookup"><span data-stu-id="a7115-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="a7115-119">PS \_ 1 \_ 1 \_ \_ PS \_ 1 \_ 2 PS 1 \_ \_ \_ \_ 3 \_ \_ PS \_ 1 \_ 4 registros</span><span class="sxs-lookup"><span data-stu-id="a7115-119">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="a7115-120">\_registros PS 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a7115-120">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="a7115-121">\_registros PS 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a7115-121">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="a7115-122">\_registros PS 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a7115-122">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




