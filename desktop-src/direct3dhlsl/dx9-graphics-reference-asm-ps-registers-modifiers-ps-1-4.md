---
title: '\_ \_ modificadores de registro de origem PS 1 4 para texld, texcrd'
description: Duas instruções de endereço de textura de sombreador de pixel versão 1 \_ 4, texld-PS \_ 1 \_ 4 e texcrd-PS, têm sintaxe personalizada.
ms.assetid: bbc8074f-882e-4b67-ae4d-1641ceb7f3ad
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af2097ee682aec7da0ca36df9e4b465fb360f814
ms.sourcegitcommit: b95a94ffffda33f9ebbdd41787c01866444b4cf4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/27/2019
ms.locfileid: "104084293"
---
# <a name="ps_1_4-source-register-modifiers-for-texld-texcrd"></a><span data-ttu-id="35971-103">\_ \_ modificadores de registro de origem PS 1 4 para texld, texcrd</span><span class="sxs-lookup"><span data-stu-id="35971-103">ps\_1\_4 source register modifiers for texld, texcrd</span></span>

<span data-ttu-id="35971-104">Duas instruções de endereço de textura de sombreador de pixel versão 1 \_ 4, [texld-PS \_ 1 \_ 4](texld---ps-1-4.md) e [texcrd-PS](texcrd---ps.md), têm sintaxe personalizada.</span><span class="sxs-lookup"><span data-stu-id="35971-104">Two pixel shader version 1\_4 texture address instructions, [texld - ps\_1\_4](texld---ps-1-4.md) and [texcrd - ps](texcrd---ps.md), have custom syntax.</span></span> <span data-ttu-id="35971-105">Essas instruções dão suporte a seu próprio conjunto de modificadores de registro de origem, seletores de registro de origem e máscaras de gravação de registro de destino, como mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="35971-105">These instructions support their own set of source register modifiers, source register selectors, and destination-register write masks, as shown here.</span></span>

## <a name="source-register-modifiers-for-texld-and-texcrd"></a><span data-ttu-id="35971-106">Modificadores de registro de origem para texld e texcrd</span><span class="sxs-lookup"><span data-stu-id="35971-106">Source Register Modifiers for texld and texcrd</span></span>

<span data-ttu-id="35971-107">Esses modificadores fornecem funcionalidade de divisão projetada dividindo os valores x e y pelos valores z ou w.</span><span class="sxs-lookup"><span data-stu-id="35971-107">These modifiers provide projective divide functionality by dividing the x and y values by either the z or w values.</span></span>



| <span data-ttu-id="35971-108">Modificadores de registro de origem</span><span class="sxs-lookup"><span data-stu-id="35971-108">Source register modifiers</span></span> | <span data-ttu-id="35971-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="35971-109">Description</span></span>                | <span data-ttu-id="35971-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="35971-110">Syntax</span></span>       |
|---------------------------|----------------------------|--------------|
| <span data-ttu-id="35971-111">\_DZ</span><span class="sxs-lookup"><span data-stu-id="35971-111">\_dz</span></span>                      | <span data-ttu-id="35971-112">Dividir os componentes x, y por z</span><span class="sxs-lookup"><span data-stu-id="35971-112">Divide x,y components by z</span></span> | <span data-ttu-id="35971-113">registrar \_ DZ</span><span class="sxs-lookup"><span data-stu-id="35971-113">register\_dz</span></span> |
| <span data-ttu-id="35971-114">\_db</span><span class="sxs-lookup"><span data-stu-id="35971-114">\_db</span></span>                      | <span data-ttu-id="35971-115">Dividir os componentes x, y por z</span><span class="sxs-lookup"><span data-stu-id="35971-115">Divide x,y components by z</span></span> | <span data-ttu-id="35971-116">registrar \_ BD</span><span class="sxs-lookup"><span data-stu-id="35971-116">register\_db</span></span> |
| <span data-ttu-id="35971-117">\_dw</span><span class="sxs-lookup"><span data-stu-id="35971-117">\_dw</span></span>                      | <span data-ttu-id="35971-118">Dividir os componentes x, y por w</span><span class="sxs-lookup"><span data-stu-id="35971-118">Divide x,y components by w</span></span> | <span data-ttu-id="35971-119">registrar \_ DW</span><span class="sxs-lookup"><span data-stu-id="35971-119">register\_dw</span></span> |
| <span data-ttu-id="35971-120">\_auditoria</span><span class="sxs-lookup"><span data-stu-id="35971-120">\_da</span></span>                      | <span data-ttu-id="35971-121">Dividir os componentes x, y por w</span><span class="sxs-lookup"><span data-stu-id="35971-121">Divide x,y components by w</span></span> | <span data-ttu-id="35971-122">registrar \_ da</span><span class="sxs-lookup"><span data-stu-id="35971-122">register\_da</span></span> |



 

### <a name="remarks"></a><span data-ttu-id="35971-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="35971-123">Remarks</span></span>

<span data-ttu-id="35971-124">O \_ \_ modificador DZ ou DB faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="35971-124">The \_dz or \_db modifier does the following:</span></span>


```
x' = x/z ( x' = 1.0 if z == 0)
y' = y/z ( y' = 1.0 if z == 0)
z' is undefined
w' is undefined
```



<span data-ttu-id="35971-125">O \_ modificador DW ou o \_ da é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="35971-125">The \_dw or \_da modifier does the following:</span></span>


```
x' = x/w ( x' = 1.0 if w == 0)
y' = y/w ( y' = 1.0 if w == 0)
z' is undefined
w' is undefined
```



## <a name="related-topics"></a><span data-ttu-id="35971-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35971-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35971-127">Modificadores de registro de origem do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="35971-127">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




