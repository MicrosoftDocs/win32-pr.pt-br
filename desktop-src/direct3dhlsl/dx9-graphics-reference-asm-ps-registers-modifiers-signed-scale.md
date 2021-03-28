---
title: Dimensionamento assinado do registro de origem
description: Subtrai 0,5 de cada canal e dimensiona o resultado por 2,0. O nome BX2 vem de tendência e escala – vezes-dois, que é a operação que ele executa.
ms.assetid: ad94145a-2687-4c20-b3ed-70270a0c53bf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 214f4fcb6ad4f382a97b8c8d75a733124c31d68a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160502"
---
# <a name="source-register-signed-scaling"></a><span data-ttu-id="35818-104">Dimensionamento assinado do registro de origem</span><span class="sxs-lookup"><span data-stu-id="35818-104">Source Register Signed Scaling</span></span>

<span data-ttu-id="35818-105">Subtrai 0,5 de cada canal e dimensiona o resultado por 2,0.</span><span class="sxs-lookup"><span data-stu-id="35818-105">Subtracts 0.5 from each channel and scales the result by 2.0.</span></span> <span data-ttu-id="35818-106">O nome BX2 vem de tendência e escala – vezes-dois, que é a operação que ele executa.</span><span class="sxs-lookup"><span data-stu-id="35818-106">The name bx2 comes from bias and scale-times-two, which is the operation it performs.</span></span>

## <a name="syntax"></a><span data-ttu-id="35818-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="35818-107">Syntax</span></span>


```
source register_bx2
```



## <a name="register"></a><span data-ttu-id="35818-108">Registre-se</span><span class="sxs-lookup"><span data-stu-id="35818-108">Register</span></span>

<span data-ttu-id="35818-109">Registro de origem.</span><span class="sxs-lookup"><span data-stu-id="35818-109">Source Register.</span></span> <span data-ttu-id="35818-110">Para obter mais informações sobre tipos de registro, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="35818-110">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="35818-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="35818-111">Remarks</span></span>

<span data-ttu-id="35818-112">Essa operação é normalmente usada para expandir dados de \[ 0,0 para 1,0 \] para \[ -1,0 a 1,0 \] .</span><span class="sxs-lookup"><span data-stu-id="35818-112">This operation is commonly used to expand data from \[0.0 to 1.0\] to \[-1.0 to 1.0\].</span></span> <span data-ttu-id="35818-113">Esse modificador foi projetado para uso com as instruções aritméticas.</span><span class="sxs-lookup"><span data-stu-id="35818-113">This modifier is designed for use with the arithmetic instructions.</span></span> <span data-ttu-id="35818-114">Esse modificador é normalmente usado em entradas para a instrução de produto dot ([DP3-PS](dp3---ps.md)).</span><span class="sxs-lookup"><span data-stu-id="35818-114">This modifier is commonly used on inputs to the dot product instruction ([dp3 - ps](dp3---ps.md)).</span></span> <span data-ttu-id="35818-115">\_O uso de BX2 em dados fora do intervalo de 0 a 1 pode produzir resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="35818-115">Using \_bx2 on data outside the range 0 to 1 may produce undefined results.</span></span>

<span data-ttu-id="35818-116">A operação de dimensionamento assinado é aplicada aos dados lidos do registro antes da execução da próxima instrução.</span><span class="sxs-lookup"><span data-stu-id="35818-116">The signed scaling operation is applied to the data read from the register before the next instruction is run.</span></span> <span data-ttu-id="35818-117">A operação é aplicada a todos os quatro canais de cores (RGBA) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="35818-117">The operation is applied to all four color channels (RGBA) as follows:</span></span>


```
y = 2(x - 0.5)
```



<span data-ttu-id="35818-118">O conteúdo do registro não é alterado.</span><span class="sxs-lookup"><span data-stu-id="35818-118">The contents of the register are not changed.</span></span> <span data-ttu-id="35818-119">O modificador é aplicado somente aos dados lidos do registro.</span><span class="sxs-lookup"><span data-stu-id="35818-119">The modifier is applied only to the data read from the register.</span></span>

<span data-ttu-id="35818-120">Esse modificador é mutuamente exclusivo com o [registro de origem inverter](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) para que não possa ser aplicado ao mesmo registro.</span><span class="sxs-lookup"><span data-stu-id="35818-120">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md) so it cannot be applied to the same register.</span></span>

<span data-ttu-id="35818-121">Informações de versão:</span><span class="sxs-lookup"><span data-stu-id="35818-121">Version information:</span></span>

-   <span data-ttu-id="35818-122">Para \_ o PS 1 \_ 0 e \_ o PS 1 \_ 1, você pode usar \_ BX2 em qualquer registro de origem para obter instruções de textura do formulário texm3x2 \* e texm3x3 \* .</span><span class="sxs-lookup"><span data-stu-id="35818-122">For ps\_1\_0 and ps\_1\_1, you can use \_bx2 on any source register for texture instructions of the form texm3x2\* and texm3x3\*.</span></span> <span data-ttu-id="35818-123">\_BX2 não pode ser usado em nenhuma das outras instruções de textura, como [texreg2ar-PS](texreg2ar---ps.md) ou [texreg2gb-PS](texreg2gb---ps.md).</span><span class="sxs-lookup"><span data-stu-id="35818-123">\_bx2 cannot be used on any of the other texture instructions such as [texreg2ar - ps](texreg2ar---ps.md) or [texreg2gb - ps](texreg2gb---ps.md).</span></span>
-   <span data-ttu-id="35818-124">Para \_ o PS 1 \_ 2 e \_ o PS 1 \_ 3, você pode usar \_ BX2 em qualquer registro de origem para qualquer \* instrução Tex, exceto: [texreg2ar-PS](texreg2ar---ps.md), [texreg2gb-PS](texreg2gb---ps.md), [texbem-PS](texbem---ps.md) ou [texbeml-PS](texbeml---ps.md).</span><span class="sxs-lookup"><span data-stu-id="35818-124">For ps\_1\_2 and ps\_1\_3, you can use \_bx2 on any source register for any tex\* instruction except: [texreg2ar - ps](texreg2ar---ps.md), [texreg2gb - ps](texreg2gb---ps.md), [texbem - ps](texbem---ps.md) or [texbeml - ps](texbeml---ps.md).</span></span>

## <a name="example"></a><span data-ttu-id="35818-125">Exemplo</span><span class="sxs-lookup"><span data-stu-id="35818-125">Example</span></span>

<span data-ttu-id="35818-126">Este exemplo amostra uma textura, converte dados no intervalo de-1 a + 1 e calcula um produto de ponto.</span><span class="sxs-lookup"><span data-stu-id="35818-126">This example samples a texture, converts data to the range of -1 to +1, and calculates a dot product.</span></span>


```
tex t0                        ; Read a texture color.
dp3_sat r0, t0_bx2, v0_bx2    ; Calculate a dot product.
```



## <a name="related-topics"></a><span data-ttu-id="35818-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="35818-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35818-128">Modificadores de registro de origem do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="35818-128">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




