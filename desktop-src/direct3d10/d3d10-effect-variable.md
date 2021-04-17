---
description: Essas constantes se aplicam a variáveis de efeito.
ms.assetid: ef996443-b558-4aa6-acc1-38f8a89c9855
title: D3D10_EFFECT_VARIABLE constantes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6367fe89f66ff90991b8493a03a6d1b4244f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784562"
---
# <a name="d3d10_effect_variable-constants"></a><span data-ttu-id="e7751-103">\_Constantes variáveis de efeito d3d10 \_</span><span class="sxs-lookup"><span data-stu-id="e7751-103">D3D10\_EFFECT\_VARIABLE Constants</span></span>

<span data-ttu-id="e7751-104">Essas constantes se aplicam a variáveis de efeito.</span><span class="sxs-lookup"><span data-stu-id="e7751-104">These constants apply to effect variables.</span></span>



| <span data-ttu-id="e7751-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="e7751-105">\#define</span></span>                                       | <span data-ttu-id="e7751-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="e7751-106">Description</span></span>  | <span data-ttu-id="e7751-107">Valor</span><span class="sxs-lookup"><span data-stu-id="e7751-107">Value</span></span>                                                                                                                                                                                                                                                             |
|------------------------------------------------|--------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7751-108">\_Anotação de \_ variável de efeito d3d10 \_</span><span class="sxs-lookup"><span data-stu-id="e7751-108">D3D10\_EFFECT\_VARIABLE\_ANNOTATION</span></span>            | <span data-ttu-id="e7751-109">1 << 0</span><span class="sxs-lookup"><span data-stu-id="e7751-109">1 << 0</span></span> | <span data-ttu-id="e7751-110">Indica que esta é uma anotação ou uma variável global.</span><span class="sxs-lookup"><span data-stu-id="e7751-110">Indicates that this is an annotation or a global variable.</span></span>                                                                                                                                                                                                        |
| <span data-ttu-id="e7751-111">Variável de efeito de D3D10 em \_ \_ \_ pool</span><span class="sxs-lookup"><span data-stu-id="e7751-111">D3D10\_EFFECT\_VARIABLE\_POOLED</span></span>                | <span data-ttu-id="e7751-112">1 << 1</span><span class="sxs-lookup"><span data-stu-id="e7751-112">1 << 1</span></span> | <span data-ttu-id="e7751-113">Indica que essa variável ou buffer de constante reside em um pool de efeitos.</span><span class="sxs-lookup"><span data-stu-id="e7751-113">Indicates that this variable or constant buffer resides in an effect pool.</span></span> <span data-ttu-id="e7751-114">Se esse sinalizador não for definido, a variável residirá em um efeito autônomo ou um efeito filho (os efeitos autônomos retornarão false de [**ID3D10Effect:: ispool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool).</span><span class="sxs-lookup"><span data-stu-id="e7751-114">If this flag is not set, then the variable resides in a standalone effect or a child effect (standalone effects return false from [**ID3D10Effect::IsPool**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-ispool).</span></span> |
| <span data-ttu-id="e7751-115">\_Ponto de \_ \_ ligação explícito \_ da variável de efeito d3d10 \_</span><span class="sxs-lookup"><span data-stu-id="e7751-115">D3D10\_EFFECT\_VARIABLE\_EXPLICIT\_BIND\_POINT</span></span> | <span data-ttu-id="e7751-116">1 << 2</span><span class="sxs-lookup"><span data-stu-id="e7751-116">1 << 2</span></span> | <span data-ttu-id="e7751-117">Indica que a variável foi explicitamente associada usando a palavra-chave Register.</span><span class="sxs-lookup"><span data-stu-id="e7751-117">Indicates that the variable has been explicitly bound using the register keyword.</span></span>                                                                                                                                                                                 |



 

<span data-ttu-id="e7751-118">Esses sinalizadores são definidos como macros em d3d10effect. h.</span><span class="sxs-lookup"><span data-stu-id="e7751-118">These flags are defined as macros in d3d10effect.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7751-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7751-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7751-120">Constantes de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="e7751-120">Effect Constants (Direct3D 10)</span></span>](d3d10-graphics-reference-effect-constants.md)
</dt> </dl>

 

 



