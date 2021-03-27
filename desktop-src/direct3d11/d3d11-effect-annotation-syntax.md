---
title: Sintaxe de anotação (Direct3D 11)
description: Uma anotação é uma informação definida pelo usuário, declarada com a sintaxe descrita nesta seção.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9583dafd3e1fb314ae6ac9e53d609bebc74a030
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917332"
---
# <a name="annotation-syntax-direct3d-11"></a><span data-ttu-id="3730a-103">Sintaxe de anotação (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="3730a-103">Annotation Syntax (Direct3D 11)</span></span>

<span data-ttu-id="3730a-104">Uma anotação é uma informação definida pelo usuário, declarada com a sintaxe descrita nesta seção.</span><span class="sxs-lookup"><span data-stu-id="3730a-104">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span>



| <span data-ttu-id="3730a-105"><Valor do *nome* do *tipo de dados*  =  ; *...* ; ></span><span class="sxs-lookup"><span data-stu-id="3730a-105"><*DataType* *Name* = *Value*; *...* ;></span></span> |
|----------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="3730a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3730a-106">Parameters</span></span>



| <span data-ttu-id="3730a-107">Item</span><span class="sxs-lookup"><span data-stu-id="3730a-107">Item</span></span>                                                                                                   | <span data-ttu-id="3730a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3730a-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3730a-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Tipo de dados*</span><span class="sxs-lookup"><span data-stu-id="3730a-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="3730a-110">\[no \] tipo de dados, que inclui qualquer tipo de [HLSL escalar](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) , bem como o [tipo de cadeia de caracteres](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span><span class="sxs-lookup"><span data-stu-id="3730a-110">\[in\] The data type, which includes any [scalar HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) type as well as the [string type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span></span><br/> |
| <span data-ttu-id="3730a-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*</span><span class="sxs-lookup"><span data-stu-id="3730a-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="3730a-112">\[em \] uma cadeia de caracteres ASCII, que representa o nome da anotação.</span><span class="sxs-lookup"><span data-stu-id="3730a-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="3730a-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Valor*</span><span class="sxs-lookup"><span data-stu-id="3730a-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="3730a-114">\[no \] valor inicial da anotação.</span><span class="sxs-lookup"><span data-stu-id="3730a-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="3730a-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="3730a-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="3730a-116">\[em \] anotações adicionais (pares nome-valor).</span><span class="sxs-lookup"><span data-stu-id="3730a-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="3730a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="3730a-117">Remarks</span></span>

<span data-ttu-id="3730a-118">Você pode adicionar mais de uma anotação dentro dos colchetes angulares, cada uma separada por um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="3730a-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="3730a-119">As APIs de estrutura de efeito reconhecem as anotações em variáveis globais; todas as outras anotações são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="3730a-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="3730a-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3730a-120">Example</span></span>

<span data-ttu-id="3730a-121">Aqui estão alguns exemplos.</span><span class="sxs-lookup"><span data-stu-id="3730a-121">Here are some examples.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3730a-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3730a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3730a-123">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="3730a-123">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="3730a-124">Sintaxe da variável de efeito</span><span class="sxs-lookup"><span data-stu-id="3730a-124">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

