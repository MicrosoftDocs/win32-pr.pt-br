---
title: Sintaxe da função de efeito (Direct3D 11)
description: Uma função de efeito é escrita em HLSL e é declarada com a sintaxe descrita nesta seção.
ms.assetid: 5e12ba65-98bf-4f21-be75-602687157eb1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f569211d5f178b96cf7415478010285e7a836b58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641119"
---
# <a name="effect-function-syntax-direct3d-11"></a><span data-ttu-id="e3ae2-103">Sintaxe da função de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="e3ae2-103">Effect Function Syntax (Direct3D 11)</span></span>

<span data-ttu-id="e3ae2-104">Uma função de efeito é escrita em HLSL e é declarada com a sintaxe descrita nesta seção.</span><span class="sxs-lookup"><span data-stu-id="e3ae2-104">An effect function is written in HLSL and is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ae2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3ae2-105">Syntax</span></span>

<span data-ttu-id="e3ae2-106"> *Função* do ReturnType ( \[ *ArgumentList* \] )</span><span class="sxs-lookup"><span data-stu-id="e3ae2-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="e3ae2-107">{</span><span class="sxs-lookup"><span data-stu-id="e3ae2-107">{</span></span>

<dl> <span data-ttu-id="e3ae2-108">\[ *Instruções* \]</span><span class="sxs-lookup"><span data-stu-id="e3ae2-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="e3ae2-109">};</span><span class="sxs-lookup"><span data-stu-id="e3ae2-109">};</span></span>



| <span data-ttu-id="e3ae2-110">Name</span><span class="sxs-lookup"><span data-stu-id="e3ae2-110">Name</span></span>         | <span data-ttu-id="e3ae2-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3ae2-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ae2-112">Tipoderetorno</span><span class="sxs-lookup"><span data-stu-id="e3ae2-112">ReturnType</span></span>   | <span data-ttu-id="e3ae2-113">Qualquer [tipo de HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span><span class="sxs-lookup"><span data-stu-id="e3ae2-113">Any [HLSL type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="e3ae2-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="e3ae2-114">FunctionName</span></span> | <span data-ttu-id="e3ae2-115">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e3ae2-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="e3ae2-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="e3ae2-116">ArgumentList</span></span> | <span data-ttu-id="e3ae2-117">Um ou mais argumentos, separados por vírgulas (consulte os [argumentos da função (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span><span class="sxs-lookup"><span data-stu-id="e3ae2-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-function-parameters)).</span></span>                                                                                                                             |
| <span data-ttu-id="e3ae2-118">Instruções</span><span class="sxs-lookup"><span data-stu-id="e3ae2-118">Statements</span></span>   | <span data-ttu-id="e3ae2-119">Uma ou mais instruções (consulte [instruções (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) que compõem o corpo da função.</span><span class="sxs-lookup"><span data-stu-id="e3ae2-119">One or more statements (see [Statements (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-statements)) that make up the body of the function.</span></span> <span data-ttu-id="e3ae2-120">Se uma função for definida sem um corpo, será considerada um protótipo; e deve ser redefinido com um corpo antes de usar.</span><span class="sxs-lookup"><span data-stu-id="e3ae2-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="e3ae2-121">Uma função de efeito pode ser um sombreador ou pode simplesmente ser uma função chamada por um sombreador.</span><span class="sxs-lookup"><span data-stu-id="e3ae2-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="e3ae2-122">Uma função é identificada exclusivamente por seu nome, os tipos de seus parâmetros e a plataforma de destino; Portanto, as funções podem ser sobrecarregadas.</span><span class="sxs-lookup"><span data-stu-id="e3ae2-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="e3ae2-123">Qualquer função HLSL válida deve se ajustar a este formato; para obter uma lista mais detalhada de sintaxe para funções HLSL, consulte [funções (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span><span class="sxs-lookup"><span data-stu-id="e3ae2-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-functions).</span></span>

## <a name="example"></a><span data-ttu-id="e3ae2-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="e3ae2-124">Example</span></span>

<span data-ttu-id="e3ae2-125">Veja a seguir um exemplo de uma função de sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="e3ae2-125">The following is an example of a pixel shader function.</span></span>


```
       
PS_OUTPUT RenderScenePS( VS_OUTPUT In,
                         uniform bool bTexture ) 
{ 
    PS_OUTPUT Output;

    // Lookup mesh texture and modulate it with diffuse
    if( bTexture )
        Output.RGBColor = g_MeshTexture.Sample(MeshTextureSampler, In.TextureUV) *  
                              In.Diffuse;
    else
        Output.RGBColor = In.Diffuse;

    return Output;
}
```



## <a name="related-topics"></a><span data-ttu-id="e3ae2-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e3ae2-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3ae2-127">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="e3ae2-127">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 