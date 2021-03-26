---
title: Inverter registro de origem
description: Executa um cálculo (1 valor) para cada canal do registro especificado.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104967054"
---
# <a name="source-register-invert"></a><span data-ttu-id="9abe9-103">Inverter registro de origem</span><span class="sxs-lookup"><span data-stu-id="9abe9-103">Source Register Invert</span></span>

<span data-ttu-id="9abe9-104">Executa um cálculo (1 valor) para cada canal do registro especificado.</span><span class="sxs-lookup"><span data-stu-id="9abe9-104">Performs a (1 - value) calculation for each channel of the specified register.</span></span>

## <a name="syntax"></a><span data-ttu-id="9abe9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9abe9-105">Syntax</span></span>


```
1 - register
```



## <a name="registers"></a><span data-ttu-id="9abe9-106">Registros</span><span class="sxs-lookup"><span data-stu-id="9abe9-106">Registers</span></span>

<span data-ttu-id="9abe9-107">Registro de origem.</span><span class="sxs-lookup"><span data-stu-id="9abe9-107">Source Register.</span></span> <span data-ttu-id="9abe9-108">Para obter mais informações sobre tipos de registro, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="9abe9-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9abe9-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="9abe9-109">Remarks</span></span>

<span data-ttu-id="9abe9-110">O conteúdo do registro não é alterado.</span><span class="sxs-lookup"><span data-stu-id="9abe9-110">The contents of the register are not changed.</span></span> <span data-ttu-id="9abe9-111">O modificador é aplicado somente aos dados lidos do registro.</span><span class="sxs-lookup"><span data-stu-id="9abe9-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="9abe9-112">A operação Inverter é aplicada a todos os quatro canais de cor (RGBA).</span><span class="sxs-lookup"><span data-stu-id="9abe9-112">The invert operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="9abe9-113">Esse modificador só pode ser usado com instruções aritméticas.</span><span class="sxs-lookup"><span data-stu-id="9abe9-113">This modifier can be used only with arithmetic instructions.</span></span> <span data-ttu-id="9abe9-114">Além disso, esse modificador não pode ser combinado com a outra [máscara de gravação de registro de destino](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="9abe9-114">In addition, this modifier cannot be combined with the other [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="example"></a><span data-ttu-id="9abe9-115">Exemplo</span><span class="sxs-lookup"><span data-stu-id="9abe9-115">Example</span></span>

<span data-ttu-id="9abe9-116">Este exemplo usa inversão para gerar o complemento do registro R1.</span><span class="sxs-lookup"><span data-stu-id="9abe9-116">This example uses inversion to generate the complement of register r1.</span></span>


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a><span data-ttu-id="9abe9-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9abe9-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9abe9-118">Modificadores de registro de origem do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="9abe9-118">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




