---
title: Referência para HLSL
description: A documentação de referência do HLSL especifica as características da linguagem. Ele é dividido em várias seções.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005905"
---
# <a name="reference-for-hlsl"></a><span data-ttu-id="2afc4-104">Referência para HLSL</span><span class="sxs-lookup"><span data-stu-id="2afc4-104">Reference for HLSL</span></span>

<span data-ttu-id="2afc4-105">A documentação de referência do HLSL especifica as características da linguagem.</span><span class="sxs-lookup"><span data-stu-id="2afc4-105">The HLSL reference documentation specifies the language characteristics.</span></span> <span data-ttu-id="2afc4-106">Ele é dividido em várias seções.</span><span class="sxs-lookup"><span data-stu-id="2afc4-106">It is broken into several sections.</span></span>

-   <span data-ttu-id="2afc4-107">[Sintaxe de linguagem (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) -os sombreadores de programação no HLSL exigem que você compreenda a sintaxe da linguagem, ou seja, como você escreve o código HLSL.</span><span class="sxs-lookup"><span data-stu-id="2afc4-107">[Language Syntax (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) - Programming shaders in HLSL requires that you understand the language syntax, that is, how you write HLSL code.</span></span> <span data-ttu-id="2afc4-108">Isso inclui código para declarar e inicializar variáveis, gravar funções de sombreador definidas pelo usuário e adicionar instruções de controle de fluxo para tornar suas funções mais poderosas.</span><span class="sxs-lookup"><span data-stu-id="2afc4-108">This includes code to declare and initialize variables, write user-defined shader functions, and add flow control statements to make your functions more powerful.</span></span>
-   <span data-ttu-id="2afc4-109">[Modelos de sombreador vs. perfis de sombreador](dx-graphics-hlsl-models.md) – o compilador HLSL implementa regras e restrições com base em modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2afc4-109">[Shader Models vs Shader Profiles](dx-graphics-hlsl-models.md) - The HLSL compiler implements rules and restrictions based on shader models.</span></span> <span data-ttu-id="2afc4-110">O código em cada sombreador de vértice, o sombreador de geometria (se você estiver usando o Direct3D 10) e o sombreador de pixel são validados em relação a um modelo de sombreador que você fornece no momento da compilação.</span><span class="sxs-lookup"><span data-stu-id="2afc4-110">The code in each vertex shader, geometry shader (if you are using Direct3D 10) and pixel shader are validated against a shader model, which you supply at compile time.</span></span>
-   <span data-ttu-id="2afc4-111">[**Funções intrínsecas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) -HLSL tem muitas funções intrínsecas.</span><span class="sxs-lookup"><span data-stu-id="2afc4-111">[**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) - HLSL has many intrinsic functions.</span></span> <span data-ttu-id="2afc4-112">Eles são implementados e testados para que você possa usá-los sabendo que eles já estão depurados e têm um bom desempenho.</span><span class="sxs-lookup"><span data-stu-id="2afc4-112">These are implemented and tested so that you can use them knowing that they are already debugged and they perform well.</span></span> <span data-ttu-id="2afc4-113">Se você optar por escrever suas próprias funções, consulte a seção sintaxe de linguagem para gravar funções definidas pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="2afc4-113">If you choose to write your own functions, see the language syntax section for writing user-defined functions.</span></span>
-   <span data-ttu-id="2afc4-114">[Referência de sombreador ASM](dx9-graphics-reference-asm.md) -instruções de assembly que você pode usar para programar e depurar sombreadores.</span><span class="sxs-lookup"><span data-stu-id="2afc4-114">[Asm Shader Reference](dx9-graphics-reference-asm.md) - Assembly instructions that you can use to program and debug shaders.</span></span>
-   <span data-ttu-id="2afc4-115">[Referência de D3DCompiler](dx-graphics-d3dcompiler-reference.md) – compila a fonte HLSL bruta.</span><span class="sxs-lookup"><span data-stu-id="2afc4-115">[D3DCompiler Reference](dx-graphics-d3dcompiler-reference.md) - Compiles raw HLSL source.</span></span>
-   <span data-ttu-id="2afc4-116">[Referência de conversão de formato embutido](inline-format-conversion-reference.md) -o \_ arquivo D3DX DXGIFormatConvert. inl contém funções de conversão de formato embutido que você pode usar no sombreador de computação ou sombreador de pixel no hardware do Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="2afc4-116">[Inline Format Conversion Reference](inline-format-conversion-reference.md) - The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="2afc4-117">Você pode usar essas funções em seu aplicativo para, simultaneamente, ler e gravar em uma textura.</span><span class="sxs-lookup"><span data-stu-id="2afc4-117">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="2afc4-118">Ou seja, você pode executar a edição de imagem in-loco.</span><span class="sxs-lookup"><span data-stu-id="2afc4-118">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="2afc4-119">Para usar essas funções de conversão de formato embutido, inclua o \_ arquivo D3DX DXGIFormatConvert. inl em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2afc4-119">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>
-   <span data-ttu-id="2afc4-120">[Apêndice (DirectX HLSL)](dx-graphics-hlsl-appendix.md) -o apêndice está incluído para fins de integridade.</span><span class="sxs-lookup"><span data-stu-id="2afc4-120">[Appendix (DirectX HLSL)](dx-graphics-hlsl-appendix.md) - The appendix is included for completeness.</span></span> <span data-ttu-id="2afc4-121">Ele inclui uma listagem das palavras-chave e das senhas reservadas; essas palavras não podem ser usadas como identificadores em seus programas.</span><span class="sxs-lookup"><span data-stu-id="2afc4-121">It includes a listing of the keywords and reserved words; these words cannot be used as identifiers in your programs.</span></span> <span data-ttu-id="2afc4-122">Ele também inclui uma lista da gramática de idioma para referência.</span><span class="sxs-lookup"><span data-stu-id="2afc4-122">It also includes a listing of the language grammar for reference.</span></span>
-   <span data-ttu-id="2afc4-123">[**Erros e avisos do HLSL**](hlsl-errors-and-warnings.md) -fornece códigos de erro e de aviso que um sombreador pode retornar.</span><span class="sxs-lookup"><span data-stu-id="2afc4-123">[**HLSL errors and warnings**](hlsl-errors-and-warnings.md) - Provides error and warning codes that a shader can return.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2afc4-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2afc4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2afc4-125">HLSL</span><span class="sxs-lookup"><span data-stu-id="2afc4-125">HLSL</span></span>](dx-graphics-hlsl.md)
</dt> <dt>

[<span data-ttu-id="2afc4-126">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="2afc4-126">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




