---
description: Uma função de efeito é escrita em HLSL e é declarada com a sintaxe a seguir.
ms.assetid: 5ac85f09-50ac-4e8f-b4d2-ae8306b59348
title: Sintaxe da função de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88521eeb85d1e5f54500a045fe5dcfd81d6be2cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456994"
---
# <a name="effect-function-syntax-direct3d-10"></a><span data-ttu-id="98083-103">Sintaxe da função de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="98083-103">Effect Function Syntax (Direct3D 10)</span></span>

<span data-ttu-id="98083-104">Uma função de efeito é escrita em HLSL e é declarada com a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="98083-104">An effect function is written in HLSL and is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="98083-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98083-105">Syntax</span></span>

<span data-ttu-id="98083-106"> *Função* do ReturnType ( \[ *ArgumentList* \] )</span><span class="sxs-lookup"><span data-stu-id="98083-106">*ReturnType* *FunctionName* ( \[ *ArgumentList* \] )</span></span>

<span data-ttu-id="98083-107">{</span><span class="sxs-lookup"><span data-stu-id="98083-107">{</span></span>

<dl> <span data-ttu-id="98083-108">\[ *Instruções* \]</span><span class="sxs-lookup"><span data-stu-id="98083-108">\[ *Statements* \]</span></span>
</dl>

<span data-ttu-id="98083-109">};</span><span class="sxs-lookup"><span data-stu-id="98083-109">};</span></span>



| <span data-ttu-id="98083-110">Nome</span><span class="sxs-lookup"><span data-stu-id="98083-110">Name</span></span>         | <span data-ttu-id="98083-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="98083-111">Description</span></span>                                                                                                                                                                                                                                                          |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98083-112">Tipoderetorno</span><span class="sxs-lookup"><span data-stu-id="98083-112">ReturnType</span></span>   | <span data-ttu-id="98083-113">Qualquer [tipo de HLSL](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span><span class="sxs-lookup"><span data-stu-id="98083-113">Any [HLSL type](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md)</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="98083-114">FunctionName</span><span class="sxs-lookup"><span data-stu-id="98083-114">FunctionName</span></span> | <span data-ttu-id="98083-115">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="98083-115">An ASCII string that uniquely identifies the name of the shader function.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="98083-116">ArgumentList</span><span class="sxs-lookup"><span data-stu-id="98083-116">ArgumentList</span></span> | <span data-ttu-id="98083-117">Um ou mais argumentos, separados por vírgulas (consulte os [argumentos da função (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span><span class="sxs-lookup"><span data-stu-id="98083-117">One or more arguments, separated by commas (see [Function Arguments (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-function-parameters.md)).</span></span>                                                                                                                             |
| <span data-ttu-id="98083-118">Instruções</span><span class="sxs-lookup"><span data-stu-id="98083-118">Statements</span></span>   | <span data-ttu-id="98083-119">Uma ou mais instruções (consulte [instruções (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) que compõem o corpo da função.</span><span class="sxs-lookup"><span data-stu-id="98083-119">One or more statements (see [Statements (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-statements.md)) that make up the body of the function.</span></span> <span data-ttu-id="98083-120">Se uma função for definida sem um corpo, será considerada um protótipo; e deve ser redefinido com um corpo antes de usar.</span><span class="sxs-lookup"><span data-stu-id="98083-120">If a function is defined without a body, it is considered to be a prototype; and must be redefined with a body before use.</span></span> |



 

<span data-ttu-id="98083-121">Uma função de efeito pode ser um sombreador ou pode simplesmente ser uma função chamada por um sombreador.</span><span class="sxs-lookup"><span data-stu-id="98083-121">An effect function may be a shader or it may simply be a function called by a shader.</span></span> <span data-ttu-id="98083-122">Uma função é identificada exclusivamente por seu nome, os tipos de seus parâmetros e a plataforma de destino; Portanto, as funções podem ser sobrecarregadas.</span><span class="sxs-lookup"><span data-stu-id="98083-122">A function is uniquely identified by its name, the types of its parameters, and the target platform; therefore, functions can be overloaded.</span></span> <span data-ttu-id="98083-123">Qualquer função HLSL válida deve se ajustar a este formato; para obter uma lista mais detalhada de sintaxe para funções HLSL, consulte [funções (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span><span class="sxs-lookup"><span data-stu-id="98083-123">Any valid HLSL function should fit this format; for a more detailed list of syntax for HLSL functions, see [Functions (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-functions.md).</span></span>

## <a name="example"></a><span data-ttu-id="98083-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="98083-124">Example</span></span>

<span data-ttu-id="98083-125">O [exemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa um sombreador de pixel e um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="98083-125">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses both a pixel shader and a vertex shader.</span></span> <span data-ttu-id="98083-126">A função de sombreador de pixel é chamada de RenderScenePS e é mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="98083-126">The pixel shader function is called RenderScenePS and is shown below.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="98083-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="98083-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98083-128">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="98083-128">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 
