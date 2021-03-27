---
title: Diferença de registro de origem
description: Subtraia 0,5 de todos os componentes.
ms.assetid: 6e1e96b0-e265-4b43-a9cb-8435e1fe891c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5c564dad0d4caf859ae00155dfd9619d90276cf1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916643"
---
# <a name="source-register-bias"></a><span data-ttu-id="0e751-103">Diferença de registro de origem</span><span class="sxs-lookup"><span data-stu-id="0e751-103">Source Register Bias</span></span>

<span data-ttu-id="0e751-104">Subtraia 0,5 de todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="0e751-104">Subtract 0.5 from all components.</span></span>

## <a name="registers"></a><span data-ttu-id="0e751-105">Registros</span><span class="sxs-lookup"><span data-stu-id="0e751-105">Registers</span></span>

<span data-ttu-id="0e751-106">Registro de origem.</span><span class="sxs-lookup"><span data-stu-id="0e751-106">Source register.</span></span> <span data-ttu-id="0e751-107">Para obter mais informações sobre tipos de registro, consulte [PS \_ 1 1 PS 1 2 PS 1 3 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ 4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span><span class="sxs-lookup"><span data-stu-id="0e751-107">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0e751-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e751-108">Remarks</span></span>

<span data-ttu-id="0e751-109">O conteúdo do registro não é alterado.</span><span class="sxs-lookup"><span data-stu-id="0e751-109">The contents of the register are not changed.</span></span> <span data-ttu-id="0e751-110">O modificador é aplicado somente aos dados lidos do registro.</span><span class="sxs-lookup"><span data-stu-id="0e751-110">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="0e751-111">A tendência é aplicada a todos os quatro canais de cores (RGBA) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0e751-111">The bias is applied to all four color channels (RGBA) as follows:</span></span>


```
output = (input - 0.5)
```



<span data-ttu-id="0e751-112">O efeito é modificar os dados que estavam no intervalo de 0 a 1 para que estejam no intervalo de-0,5 a 0,5.</span><span class="sxs-lookup"><span data-stu-id="0e751-112">The effect is to modify data that was in the range 0 to 1 to be in the range -0.5 to 0.5.</span></span> <span data-ttu-id="0e751-113">A aplicação de ajustes aos dados fora desse intervalo pode produzir resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="0e751-113">Applying bias to data outside this range may produce undefined results.</span></span>

> [!Note]  
> <span data-ttu-id="0e751-114">Esse modificador é mutuamente exclusivo com o [registro de origem inverter](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md)e, portanto, não pode ser aplicado ao mesmo registro.</span><span class="sxs-lookup"><span data-stu-id="0e751-114">This modifier is mutually exclusive with [Source Register Invert](dx9-graphics-reference-asm-ps-registers-modifiers-invert.md), so it cannot be applied to the same register.</span></span>

 

<span data-ttu-id="0e751-115">Este modificador é para uso com as instruções aritméticas.</span><span class="sxs-lookup"><span data-stu-id="0e751-115">This modifier is for use with the arithmetic instructions.</span></span>

## <a name="example"></a><span data-ttu-id="0e751-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="0e751-116">Example</span></span>

<span data-ttu-id="0e751-117">Este exemplo executa a mesma operação que D3DTOP \_ ADDsigned no DirectX 6,0 e 7,0 várias sintaxes de textura.</span><span class="sxs-lookup"><span data-stu-id="0e751-117">This example performs the same operation as D3DTOP\_ADDSIGNED in DirectX 6.0 and 7.0 multiple texture syntax.</span></span>


```
add r0, r0, t0_bias; Shift down by 0.5.
```



## <a name="related-topics"></a><span data-ttu-id="0e751-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e751-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e751-119">Modificadores de registro de origem do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="0e751-119">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




