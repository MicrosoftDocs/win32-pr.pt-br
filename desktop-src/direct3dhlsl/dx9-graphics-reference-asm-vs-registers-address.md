---
title: Registro de endereço
description: O registro a0 é um registro de endereço.
ms.assetid: ad86013c-3358-4770-a01c-544c868691f4
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e58f42848034d12063611e14b82cb2f2d132cb43
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822851"
---
# <a name="address-register"></a><span data-ttu-id="6fe9e-103">Registro de endereço</span><span class="sxs-lookup"><span data-stu-id="6fe9e-103">Address Register</span></span>

<span data-ttu-id="6fe9e-104">O registro a0 é um registro de endereço.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-104">The a0 register is an address register.</span></span> <span data-ttu-id="6fe9e-105">Um único registro está disponível na versão vs \_ 1 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-105">A single register is available in version vs\_1\_1.</span></span> <span data-ttu-id="6fe9e-106">O registro de endereço, designado como a0. x no vs \_ 1 \_ 1, pode ser usado como um deslocamento de inteiro assinado para o endereçamento relativo no arquivo de registro constante.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-106">The address register, designated as a0.x in vs\_1\_1, can be used as a signed integer offset for relative addressing into the constant register file.</span></span> <span data-ttu-id="6fe9e-107">Para versões vs \_ 2 \_ 0 e superiores, todos os quatro componentes (. x,. y,. z,. w) estão disponíveis para endereçamento relativo.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-107">For versions vs\_2\_0 and above, all four components (.x, .y, .z, .w) are available for relative addressing.</span></span>


```
c[a0.x + n]
```



<span data-ttu-id="6fe9e-108">O registro de endereço não pode ser lido por um sombreador de vértice, ele só pode ser usado para endereçamento relativo de um registro constante.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-108">The address register cannot be read by a vertex shader, it can only be used for relative addressing of a constant register.</span></span> <span data-ttu-id="6fe9e-109">A leitura de valores fora do intervalo legal retornará (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="6fe9e-109">Reading values outside of the legal range will return (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="6fe9e-110">O registro de endereço só pode ser um destino para a instrução [Mov-vs](mov---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="6fe9e-110">The address register can only be a destination for the [mov - vs](mov---vs.md) instruction.</span></span> <span data-ttu-id="6fe9e-111">Se um número de ponto flutuante for movido para um registro de número inteiro, ocorrerá uma conversão de arredondamento mais próximo.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-111">If a floating-point number is moved into an integer register, a round-to-nearest conversion happens.</span></span>

<span data-ttu-id="6fe9e-112">Todos os sombreadores devem inicializar o registro de endereço antes de usá-lo.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-112">All shaders must initialize the address register before using it.</span></span> <span data-ttu-id="6fe9e-113">Para a versão vs \_ 2 \_ 0 e superior, a instrução [mova-vs](mova---vs.md) pode mover um valor de ponto flutuante para um registro de endereço.</span><span class="sxs-lookup"><span data-stu-id="6fe9e-113">For version vs\_2\_0 and above, the [mova - vs](mova---vs.md) instruction can move a floating-point value to an address register.</span></span>



| <span data-ttu-id="6fe9e-114">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="6fe9e-114">Vertex shader versions</span></span> | <span data-ttu-id="6fe9e-115">1\_1</span><span class="sxs-lookup"><span data-stu-id="6fe9e-115">1\_1</span></span> | <span data-ttu-id="6fe9e-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fe9e-116">2\_0</span></span> | <span data-ttu-id="6fe9e-117">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fe9e-117">2\_sw</span></span> | <span data-ttu-id="6fe9e-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6fe9e-118">2\_x</span></span> | <span data-ttu-id="6fe9e-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6fe9e-119">3\_0</span></span> | <span data-ttu-id="6fe9e-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6fe9e-120">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="6fe9e-121">Registro de endereço</span><span class="sxs-lookup"><span data-stu-id="6fe9e-121">Address Register</span></span>       | <span data-ttu-id="6fe9e-122">x</span><span class="sxs-lookup"><span data-stu-id="6fe9e-122">x</span></span>    | <span data-ttu-id="6fe9e-123">x</span><span class="sxs-lookup"><span data-stu-id="6fe9e-123">x</span></span>    | <span data-ttu-id="6fe9e-124">x</span><span class="sxs-lookup"><span data-stu-id="6fe9e-124">x</span></span>     | <span data-ttu-id="6fe9e-125">x</span><span class="sxs-lookup"><span data-stu-id="6fe9e-125">x</span></span>    | <span data-ttu-id="6fe9e-126">x</span><span class="sxs-lookup"><span data-stu-id="6fe9e-126">x</span></span>    | <span data-ttu-id="6fe9e-127">x</span><span class="sxs-lookup"><span data-stu-id="6fe9e-127">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="6fe9e-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6fe9e-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fe9e-129">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="6fe9e-129">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




