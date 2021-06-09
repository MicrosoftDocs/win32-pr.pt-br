---
title: packoffset
description: Palavra-chave de empacotamento constante de sombreador opcional, que usa a sintaxe a seguir
ms.assetid: f0a3031b-d385-430d-83ee-7a8142334ad7
keywords:
- packoffset HLSL
topic_type:
- apiref
api_name:
- packoffset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5c92a6375f0724a1910fc0f09b47e1593614f9f1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826075"
---
# <a name="packoffset"></a><span data-ttu-id="84b37-104">packoffset</span><span class="sxs-lookup"><span data-stu-id="84b37-104">packoffset</span></span>

<span data-ttu-id="84b37-105">Palavra-chave de empacotamento constante de sombreador opcional, que usa a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="84b37-105">Optional shader constant packing keyword, which uses the following syntax:</span></span>

<span data-ttu-id="84b37-106">: packoffset ( \[ subcomponente de c \] \[ . componente \] )</span><span class="sxs-lookup"><span data-stu-id="84b37-106">: packoffset( c\[Subcomponent\]\[.component\] )</span></span>



 

## <a name="parameters"></a><span data-ttu-id="84b37-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84b37-107">Parameters</span></span>



| <span data-ttu-id="84b37-108">Item</span><span class="sxs-lookup"><span data-stu-id="84b37-108">Item</span></span>                                                                                                                                                                                 | <span data-ttu-id="84b37-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="84b37-109">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b37-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span><span class="sxs-lookup"><span data-stu-id="84b37-110"><span id="packoffset"></span><span id="PACKOFFSET"></span>**packoffset**</span></span><br/>                                                                                                  | <span data-ttu-id="84b37-111">Palavra-chave required.</span><span class="sxs-lookup"><span data-stu-id="84b37-111">Required keyword.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="84b37-112"><span id="c"></span><span id="C"></span>**&**</span><span class="sxs-lookup"><span data-stu-id="84b37-112"><span id="c"></span><span id="C"></span>**c**</span></span><br/>                                                                                                                             | <span data-ttu-id="84b37-113">A embalagem se aplica somente a registros constantes (c).</span><span class="sxs-lookup"><span data-stu-id="84b37-113">Packing applies to constant registers (c) only.</span></span> <br/>                                                                                          |
| <span data-ttu-id="84b37-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponente \] \[ . componente\]**</span><span class="sxs-lookup"><span data-stu-id="84b37-114"><span id="_Subcomponent__.component_"></span><span id="_subcomponent__.component_"></span><span id="_SUBCOMPONENT__.COMPONENT_"></span>**\[Subcomponent\]\[.component\]**</span></span><br/> | <span data-ttu-id="84b37-115">Subcomponentes e componentes opcionais.</span><span class="sxs-lookup"><span data-stu-id="84b37-115">Optional subcomponents and components.</span></span> <span data-ttu-id="84b37-116">Um subcomponente é um número de registro, que é um inteiro.</span><span class="sxs-lookup"><span data-stu-id="84b37-116">A subcomponent is a register number, which is an integer.</span></span> <span data-ttu-id="84b37-117">Um componente está na forma de \[ . xyzw \] .</span><span class="sxs-lookup"><span data-stu-id="84b37-117">A component is in the form of \[.xyzw\].</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="84b37-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="84b37-118">Remarks</span></span>

<span data-ttu-id="84b37-119">Use essa palavra-chave para empacotar manualmente uma constante de sombreador ao [declarar um tipo de variável](dx-graphics-hlsl-variable-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="84b37-119">Use this keyword to manually pack a shader constant when [declaring a variable type](dx-graphics-hlsl-variable-syntax.md).</span></span>

<span data-ttu-id="84b37-120">Ao empacotar uma constante, você não pode misturar tipos constantes.</span><span class="sxs-lookup"><span data-stu-id="84b37-120">When packing a constant, you cannot mix constant types.</span></span>

<span data-ttu-id="84b37-121">O compilador se comporta de forma ligeiramente diferente para constantes globais e uniformes:</span><span class="sxs-lookup"><span data-stu-id="84b37-121">The compiler behaves slightly differently for global constants and uniform constants:</span></span>

-   <span data-ttu-id="84b37-122">Uma constante global.</span><span class="sxs-lookup"><span data-stu-id="84b37-122">A global constant.</span></span> <span data-ttu-id="84b37-123">Uma variável global é adicionada como uma constante global a um *$global* CBuffer pelo compilador.</span><span class="sxs-lookup"><span data-stu-id="84b37-123">A global variable is added as a global constant to a *$Global* cbuffer by the compiler.</span></span> <span data-ttu-id="84b37-124">Os elementos empacotados automaticamente (aqueles declarados sem packoffset) serão exibidos após a última variável de pacote manual.</span><span class="sxs-lookup"><span data-stu-id="84b37-124">Automatically packed elements (those declared without packoffset) will appear after the last manually packed variable.</span></span> <span data-ttu-id="84b37-125">Você pode misturar tipos ao empacotar constantes globais.</span><span class="sxs-lookup"><span data-stu-id="84b37-125">You may mix types when packing global constants.</span></span>
-   <span data-ttu-id="84b37-126">Uma constante uniforme.</span><span class="sxs-lookup"><span data-stu-id="84b37-126">A uniform constant.</span></span> <span data-ttu-id="84b37-127">Um parâmetro uniforme na lista de parâmetros de uma função será adicionado a um buffer de constante *$param* pelo compilador quando o sombreador for compilado fora da estrutura de efeitos.</span><span class="sxs-lookup"><span data-stu-id="84b37-127">A uniform parameter in the parameter list of a function will be added to a *$Param* constant buffer by the compiler when the shader is compiled outside of the effects framework.</span></span> <span data-ttu-id="84b37-128">Quando compilado dentro da estrutura de efeito, uma constante uniforme deve resolver para uma variável uniforme definida no escopo global.</span><span class="sxs-lookup"><span data-stu-id="84b37-128">When compiled inside the effect framework, a uniform constant must resolve to a uniform variable defined in global scope.</span></span> <span data-ttu-id="84b37-129">Uma constante uniforme não pode ser deslocada manualmente; seu uso recomendado é apenas para especialização de sombreadores em que eles fazem o alias de volta para os globais, não como um meio de passar dados de aplicativos para o sombreador.</span><span class="sxs-lookup"><span data-stu-id="84b37-129">A uniform constant cannot be manually offset; their recommend use is only for specialization of shaders where they alias back to globals, not as a means of passing application data into the shader.</span></span>

<span data-ttu-id="84b37-130">Aqui estão alguns exemplos adicionais: [constantes de empacotamento usando o modelo de sombreador 4](dx-graphics-hlsl-packing-rules.md).</span><span class="sxs-lookup"><span data-stu-id="84b37-130">Here are some additional examples: [packing constants using shader model 4](dx-graphics-hlsl-packing-rules.md).</span></span>

## <a name="examples"></a><span data-ttu-id="84b37-131">Exemplos</span><span class="sxs-lookup"><span data-stu-id="84b37-131">Examples</span></span>

<span data-ttu-id="84b37-132">Aqui estão vários exemplos de constantes de sombreador de empacotamento manual.</span><span class="sxs-lookup"><span data-stu-id="84b37-132">Here are several examples of manually packing shader constants.</span></span>

<span data-ttu-id="84b37-133">Pacotes subcomponentes de vetores e escalares cujo tamanho é grande o suficiente para evitar o cruzamento dos limites de registro.</span><span class="sxs-lookup"><span data-stu-id="84b37-133">Pack subcomponents of vectors and scalars whose size is large enough to prevent crossing register boundaries.</span></span> <span data-ttu-id="84b37-134">Por exemplo, todos eles são válidos:</span><span class="sxs-lookup"><span data-stu-id="84b37-134">For example, these are all valid:</span></span>


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
```



## <a name="see-also"></a><span data-ttu-id="84b37-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="84b37-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b37-136">Sintaxe de Variável</span><span class="sxs-lookup"><span data-stu-id="84b37-136">Variable Syntax</span></span>](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[<span data-ttu-id="84b37-137">Variáveis (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="84b37-137">Variables (DirectX HLSL)</span></span>](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 





