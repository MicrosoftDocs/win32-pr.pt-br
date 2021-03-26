---
title: Escala de registro de origem x 2
description: Multiplique o valor por dois antes de usá-lo na instrução.
ms.assetid: a02c9572-e03d-410b-8b65-7ea1a0bfaa0f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7e88127e4027767d23a2ab576e94802019068dc3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104967053"
---
# <a name="source-register-scale-x-2"></a><span data-ttu-id="e2fd8-103">Escala de registro de origem x 2</span><span class="sxs-lookup"><span data-stu-id="e2fd8-103">Source Register Scale x 2</span></span>

<span data-ttu-id="e2fd8-104">Multiplique o valor por dois antes de usá-lo na instrução.</span><span class="sxs-lookup"><span data-stu-id="e2fd8-104">Multiply the value by two before using it in the instruction.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2fd8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2fd8-105">Syntax</span></span>


```
register_x2
```



## <a name="register"></a><span data-ttu-id="e2fd8-106">Registre-se</span><span class="sxs-lookup"><span data-stu-id="e2fd8-106">Register</span></span>

<span data-ttu-id="e2fd8-107">Registro de origem.</span><span class="sxs-lookup"><span data-stu-id="e2fd8-107">Source register.</span></span> <span data-ttu-id="e2fd8-108">Para obter mais informações sobre tipos de registro, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="e2fd8-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e2fd8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2fd8-109">Remarks</span></span>

<span data-ttu-id="e2fd8-110">O conteúdo do registro não é alterado.</span><span class="sxs-lookup"><span data-stu-id="e2fd8-110">The contents of the register are not changed.</span></span> <span data-ttu-id="e2fd8-111">O modificador é aplicado somente aos dados lidos do registro.</span><span class="sxs-lookup"><span data-stu-id="e2fd8-111">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="e2fd8-112">Esse modificador é mutuamente exclusivo com o [registro de origem inverter](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)e, portanto, não pode ser aplicado ao mesmo registro.</span><span class="sxs-lookup"><span data-stu-id="e2fd8-112">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

<span data-ttu-id="e2fd8-113">Este modificador só está disponível para instruções aritméticas na versão 1 \_ 4.</span><span class="sxs-lookup"><span data-stu-id="e2fd8-113">This modifier is only available to arithmetic instructions in version 1\_4.</span></span>

## <a name="example"></a><span data-ttu-id="e2fd8-114">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e2fd8-114">Example</span></span>

<span data-ttu-id="e2fd8-115">Este exemplo amostra uma textura, converte dados no intervalo de-1 a + 1 e calcula um produto de ponto.</span><span class="sxs-lookup"><span data-stu-id="e2fd8-115">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
mul r0, r0, r1_x2;
```



## <a name="related-topics"></a><span data-ttu-id="e2fd8-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2fd8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2fd8-117">Modificadores de registro de origem do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="e2fd8-117">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




