---
description: Uma anotação é uma informação definida pelo usuário, declarada com a sintaxe a seguir.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Sintaxe de anotação (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826713"
---
# <a name="annotation-syntax-direct3d-10"></a><span data-ttu-id="ba23e-103">Sintaxe de anotação (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="ba23e-103">Annotation Syntax (Direct3D 10)</span></span>

<span data-ttu-id="ba23e-104">Uma anotação é uma informação definida pelo usuário, declarada com a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba23e-104">An annotation is a user-defined piece of information, declared with the following syntax.</span></span>



| <span data-ttu-id="ba23e-105"><Valor do nome do *tipo de dados*   =  ;...; ></span><span class="sxs-lookup"><span data-stu-id="ba23e-105"><*DataType* *Name* = *Value*; ... ;></span></span> |
|--------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="ba23e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba23e-106">Parameters</span></span>



| <span data-ttu-id="ba23e-107">Item</span><span class="sxs-lookup"><span data-stu-id="ba23e-107">Item</span></span>                                                                                                   | <span data-ttu-id="ba23e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="ba23e-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba23e-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Tipo de dados*</span><span class="sxs-lookup"><span data-stu-id="ba23e-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="ba23e-110">\[no \] tipo de dados, que inclui qualquer tipo de [HLSL escalar](../direct3dhlsl/dx-graphics-hlsl-scalar.md) , bem como o [tipo de cadeia de caracteres](../direct3dhlsl/dx-graphics-hlsl-scalar.md).</span><span class="sxs-lookup"><span data-stu-id="ba23e-110">\[in\] The data type, which includes any [scalar HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) type as well as the [string type](../direct3dhlsl/dx-graphics-hlsl-scalar.md).</span></span><br/> |
| <span data-ttu-id="ba23e-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*</span><span class="sxs-lookup"><span data-stu-id="ba23e-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="ba23e-112">\[em \] uma cadeia de caracteres ASCII, que representa o nome da anotação.</span><span class="sxs-lookup"><span data-stu-id="ba23e-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="ba23e-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valor*</span><span class="sxs-lookup"><span data-stu-id="ba23e-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="ba23e-114">\[no \] valor inicial da anotação.</span><span class="sxs-lookup"><span data-stu-id="ba23e-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="ba23e-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="ba23e-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="ba23e-116">\[em \] anotações adicionais (pares nome-valor).</span><span class="sxs-lookup"><span data-stu-id="ba23e-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="ba23e-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba23e-117">Remarks</span></span>

<span data-ttu-id="ba23e-118">Você pode adicionar mais de uma anotação dentro dos colchetes angulares, cada uma separada por um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="ba23e-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="ba23e-119">As APIs de estrutura de efeito reconhecem as anotações em variáveis globais; todas as outras anotações são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="ba23e-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="ba23e-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ba23e-120">Example</span></span>

<span data-ttu-id="ba23e-121">Aqui estão alguns exemplos.</span><span class="sxs-lookup"><span data-stu-id="ba23e-121">Here are some examples.</span></span>


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a><span data-ttu-id="ba23e-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba23e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba23e-123">Sintaxe da variável de efeito</span><span class="sxs-lookup"><span data-stu-id="ba23e-123">Effect Variable Syntax</span></span>](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
