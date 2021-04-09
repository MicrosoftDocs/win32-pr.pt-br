---
description: Esta página mostrará como gerar e usar um efeito.
ms.assetid: d9fdafed-5958-4995-a1b5-8881feca1291
title: Usando um efeito (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1170fde625e5eee5e9665f0759d302b5f5450a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088796"
---
# <a name="using-an-effect-direct3d-9"></a><span data-ttu-id="c0104-103">Usando um efeito (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c0104-103">Using an Effect (Direct3D 9)</span></span>

<span data-ttu-id="c0104-104">Esta página mostrará como gerar e usar um efeito.</span><span class="sxs-lookup"><span data-stu-id="c0104-104">This page will show you how to generate and use an effect.</span></span> <span data-ttu-id="c0104-105">Os tópicos abordados incluem como:</span><span class="sxs-lookup"><span data-stu-id="c0104-105">The topics covered include how to:</span></span>

-   [<span data-ttu-id="c0104-106">Criar um efeito</span><span class="sxs-lookup"><span data-stu-id="c0104-106">Create an Effect</span></span>](#create-an-effect)
-   [<span data-ttu-id="c0104-107">Renderizar um efeito</span><span class="sxs-lookup"><span data-stu-id="c0104-107">Render an Effect</span></span>](#render-an-effect)
-   [<span data-ttu-id="c0104-108">Usar a semântica para localizar parâmetros de efeito</span><span class="sxs-lookup"><span data-stu-id="c0104-108">Use Semantics to Find Effect Parameters</span></span>](#use-semantics-to-find-effect-parameters)
-   [<span data-ttu-id="c0104-109">Use identificadores para obter e definir parâmetros com eficiência</span><span class="sxs-lookup"><span data-stu-id="c0104-109">Use Handles to Get and Set Parameters Efficiently</span></span>](#use-handles-to-get-and-set-parameters-efficiently)
-   [<span data-ttu-id="c0104-110">Adicionar informações de parâmetro com anotações</span><span class="sxs-lookup"><span data-stu-id="c0104-110">Add Parameter Information with Annotations</span></span>](#add-parameter-information-with-annotations)
-   [<span data-ttu-id="c0104-111">Parâmetros de efeito de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="c0104-111">Share Effect Parameters</span></span>](#share-effect-parameters)
-   [<span data-ttu-id="c0104-112">Compilar um efeito offline</span><span class="sxs-lookup"><span data-stu-id="c0104-112">Compile an Effect Offline</span></span>](#compile-an-effect-offline)
-   [<span data-ttu-id="c0104-113">Melhorar o desempenho com preshaders</span><span class="sxs-lookup"><span data-stu-id="c0104-113">Improve Performance with Preshaders</span></span>](#improve-performance-with-preshaders)
-   [<span data-ttu-id="c0104-114">Usar blocos de parâmetro para gerenciar parâmetros de efeito</span><span class="sxs-lookup"><span data-stu-id="c0104-114">Use Parameter Blocks to Manage Effect Parameters</span></span>](#use-parameter-blocks-to-manage-effect-parameters)

## <a name="create-an-effect"></a><span data-ttu-id="c0104-115">Criar um efeito</span><span class="sxs-lookup"><span data-stu-id="c0104-115">Create an Effect</span></span>

<span data-ttu-id="c0104-116">Aqui está um exemplo de criação de um efeito obtido do [exemplo BasicHLSL](../directx-sdk--august-2009-.md).</span><span class="sxs-lookup"><span data-stu-id="c0104-116">Here is an example of creating an effect taken from the [BasicHLSL Sample](../directx-sdk--august-2009-.md).</span></span> <span data-ttu-id="c0104-117">O código de criação de efeito para criar um sombreador de depuração é de **OnCreateDevice**:</span><span class="sxs-lookup"><span data-stu-id="c0104-117">The effect creation code for creating a debug shader is from **OnCreateDevice**:</span></span>


```
ID3DXEffect* g_pEffect = NULL;
DWORD dwShaderFlags = 0;

    dwShaderFlags |= D3DXSHADER_FORCE_VS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_FORCE_PS_SOFTWARE_NOOPT;
    dwShaderFlags |= D3DXSHADER_NO_PRESHADER;

    // Read the D3DX effect file
    WCHAR str[MAX_PATH];
    DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL.fx" );

    D3DXCreateEffectFromFile( 
        pd3dDevice, 
        str, 
        NULL, // CONST D3DXMACRO* pDefines,
        NULL, // LPD3DXINCLUDE pInclude,
        dwShaderFlags, 
        NULL, // LPD3DXEFFECTPOOL pPool,
        &g_pEffect, 
        NULL );
```



<span data-ttu-id="c0104-118">Essa função usa estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c0104-118">This function takes these arguments:</span></span>

-   <span data-ttu-id="c0104-119">O dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0104-119">The device.</span></span>
-   <span data-ttu-id="c0104-120">O nome do arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="c0104-120">The file name of the effect file.</span></span>
-   <span data-ttu-id="c0104-121">Um ponteiro para uma lista terminada em nulo de \# define, a ser usado ao analisar o sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0104-121">A pointer to a NULL-terminated list of \#defines, to be used while parsing the shader.</span></span>
-   <span data-ttu-id="c0104-122">Um ponteiro opcional para um manipulador de inclusão escrito pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="c0104-122">An optional pointer to a user-written include handler.</span></span> <span data-ttu-id="c0104-123">O manipulador é chamado pelo processador sempre que ele precisa resolver um \# include.</span><span class="sxs-lookup"><span data-stu-id="c0104-123">The handler is called by the processor whenever it needs to resolve a \#include.</span></span>
-   <span data-ttu-id="c0104-124">Um sinalizador de compilação de sombreador que fornece as dicas de compilador sobre como o sombreador será usado.</span><span class="sxs-lookup"><span data-stu-id="c0104-124">A shader compile flag that gives the compiler hints about how the shader will be used.</span></span> <span data-ttu-id="c0104-125">As opções incluem:</span><span class="sxs-lookup"><span data-stu-id="c0104-125">The options include:</span></span>
    -   <span data-ttu-id="c0104-126">Ignorando a validação, se os sombreadores bons conhecidos estiverem sendo compilados.</span><span class="sxs-lookup"><span data-stu-id="c0104-126">Skipping validation, if known good shaders are being compiled.</span></span>
    -   <span data-ttu-id="c0104-127">Ignorando a otimização (às vezes usado quando as otimizações tornam a depuração mais difícil).</span><span class="sxs-lookup"><span data-stu-id="c0104-127">Skipping optimization (sometimes used when optimizations make debugging harder).</span></span>
    -   <span data-ttu-id="c0104-128">Solicitando que as informações de depuração sejam incluídas no sombreador para que ele possa ser depurado.</span><span class="sxs-lookup"><span data-stu-id="c0104-128">Requesting debug information to be included in the shader so it can be debugged.</span></span>
-   <span data-ttu-id="c0104-129">O pool de efeitos.</span><span class="sxs-lookup"><span data-stu-id="c0104-129">The effect pool.</span></span> <span data-ttu-id="c0104-130">Se mais de um efeito usar o mesmo ponteiro de pool de memória, as variáveis globais nos efeitos serão compartilhadas entre si.</span><span class="sxs-lookup"><span data-stu-id="c0104-130">If more than one effect uses the same memory pool pointer, the global variables in the effects are shared with each other.</span></span> <span data-ttu-id="c0104-131">Se não houver necessidade de compartilhar variáveis de efeito, o pool de memória poderá ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c0104-131">If there is no need to share effect variables, the memory pool can be set to **NULL**.</span></span>
-   <span data-ttu-id="c0104-132">Um ponteiro para o novo efeito.</span><span class="sxs-lookup"><span data-stu-id="c0104-132">A pointer to the new effect.</span></span>
-   <span data-ttu-id="c0104-133">Um ponteiro para um buffer para o qual os erros de validação podem ser enviados.</span><span class="sxs-lookup"><span data-stu-id="c0104-133">A pointer to a buffer to which validation errors can be sent.</span></span> <span data-ttu-id="c0104-134">Neste exemplo, o parâmetro foi definido como **nulo** e não é usado.</span><span class="sxs-lookup"><span data-stu-id="c0104-134">In this example, the parameter was set to **NULL** and not used.</span></span>

> [!Note]  
> <span data-ttu-id="c0104-135">A partir do SDK de dezembro de 2006, o compilador do DirectX 10 HLSL agora é o compilador padrão no DirectX 9 e no DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="c0104-135">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="c0104-136">Confira [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="c0104-136">See [Effect-Compiler Tool](../direct3dtools/fxc.md) for details.</span></span>

 

## <a name="render-an-effect"></a><span data-ttu-id="c0104-137">Renderizar um efeito</span><span class="sxs-lookup"><span data-stu-id="c0104-137">Render an Effect</span></span>

<span data-ttu-id="c0104-138">A sequência de chamadas para a aplicação do estado de efeito em um dispositivo é:</span><span class="sxs-lookup"><span data-stu-id="c0104-138">The sequence of calls for applying effect state to a device is:</span></span>

-   <span data-ttu-id="c0104-139">[**ID3DXEffect:: Begin**](id3dxeffect--begin.md) define a técnica ativa.</span><span class="sxs-lookup"><span data-stu-id="c0104-139">[**ID3DXEffect::Begin**](id3dxeffect--begin.md) sets the active technique.</span></span>
-   <span data-ttu-id="c0104-140">[**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) define a passagem ativa.</span><span class="sxs-lookup"><span data-stu-id="c0104-140">[**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) sets the active pass.</span></span>
-   <span data-ttu-id="c0104-141">[**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) atualiza as alterações em quaisquer chamadas Set na passagem.</span><span class="sxs-lookup"><span data-stu-id="c0104-141">[**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) updates changes to any set calls in the pass.</span></span> <span data-ttu-id="c0104-142">Isso deve ser chamado antes de qualquer chamada de desenho.</span><span class="sxs-lookup"><span data-stu-id="c0104-142">This should be called before any draw call.</span></span>
-   <span data-ttu-id="c0104-143">[**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) termina uma passagem.</span><span class="sxs-lookup"><span data-stu-id="c0104-143">[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) ends a pass.</span></span>
-   <span data-ttu-id="c0104-144">[**ID3DXEffect:: End**](id3dxeffect--end.md) termina a técnica ativa.</span><span class="sxs-lookup"><span data-stu-id="c0104-144">[**ID3DXEffect::End**](id3dxeffect--end.md) ends the active technique.</span></span>

<span data-ttu-id="c0104-145">O código de processamento de efeito também é mais simples do que o código de renderização correspondente sem um efeito.</span><span class="sxs-lookup"><span data-stu-id="c0104-145">Effect render code is also simpler than the corresponding render code without an effect.</span></span> <span data-ttu-id="c0104-146">Este é o código de renderização com um efeito:</span><span class="sxs-lookup"><span data-stu-id="c0104-146">Here's the render code with an effect:</span></span>


```
// Apply the technique contained in the effect 
g_pEffect->Begin(&cPasses, 0);

for (iPass = 0; iPass < cPasses; iPass++)
{
    g_pEffect->BeginPass(iPass);

    // Only call CommitChanges if any state changes have happened
    // after BeginPass is called
    g_pEffect->CommitChanges();

    // Render the mesh with the applied technique
    g_pMesh->DrawSubset(0);

    g_pEffect->EndPass();
}
g_pEffect->End();
```



<span data-ttu-id="c0104-147">O loop render consiste em consultar o efeito para ver quantos passagens ele contém e, em seguida, chamar todos os passos para uma técnica.</span><span class="sxs-lookup"><span data-stu-id="c0104-147">The render loop consists of querying the effect to see how many passes it contains, and then calling all the passes for a technique.</span></span> <span data-ttu-id="c0104-148">O loop de renderização pode ser expandido para chamar várias técnicas, cada uma com várias passagens.</span><span class="sxs-lookup"><span data-stu-id="c0104-148">The render loop could be expanded to call multiple techniques, each with multiple passes.</span></span>

## <a name="use-semantics-to-find-effect-parameters"></a><span data-ttu-id="c0104-149">Usar a semântica para localizar parâmetros de efeito</span><span class="sxs-lookup"><span data-stu-id="c0104-149">Use Semantics to Find Effect Parameters</span></span>

<span data-ttu-id="c0104-150">Uma semântica é um identificador que é anexado a um parâmetro de efeito para permitir que um aplicativo pesquise o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c0104-150">A semantic is an identifier that is attached to an effect parameter to allow an application to search for the parameter.</span></span> <span data-ttu-id="c0104-151">Um parâmetro pode ter no máximo uma semântica.</span><span class="sxs-lookup"><span data-stu-id="c0104-151">A parameter can have at most one semantic.</span></span> <span data-ttu-id="c0104-152">A semântica está localizada após um sinal de dois-pontos (:) após o nome do parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c0104-152">The semantic is located following a colon (:) after the parameter name.</span></span> <span data-ttu-id="c0104-153">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="c0104-153">For instance:</span></span>


```
float4x4 matWorldViewProj : WORLDVIEWPROJ;
```



<span data-ttu-id="c0104-154">Se você declarou a variável global Effect sem usar uma semântica, ela ficaria assim:</span><span class="sxs-lookup"><span data-stu-id="c0104-154">If you declared the effect global variable without using a semantic, it would look like this instead:</span></span>


```
float4x4 matWorldViewProj;
```



<span data-ttu-id="c0104-155">A interface de efeito pode usar uma semântica para obter um identificador para um parâmetro de efeito específico.</span><span class="sxs-lookup"><span data-stu-id="c0104-155">The effect interface can use a semantic to get a handle to a particular effect parameter.</span></span> <span data-ttu-id="c0104-156">Por exemplo, o seguinte retorna o identificador da matriz:</span><span class="sxs-lookup"><span data-stu-id="c0104-156">For instance, the following returns the handle of the matrix:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



<span data-ttu-id="c0104-157">Além de Pesquisar por nome semântico, a interface de efeito tem muitos outros métodos para pesquisar parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c0104-157">In addition to searching by semantic name, the effect interface has many other methods to search for parameters.</span></span>

## <a name="use-handles-to-get-and-set-parameters-efficiently"></a><span data-ttu-id="c0104-158">Use identificadores para obter e definir parâmetros com eficiência</span><span class="sxs-lookup"><span data-stu-id="c0104-158">Use Handles to Get and Set Parameters Efficiently</span></span>

<span data-ttu-id="c0104-159">Os identificadores fornecem um meio eficiente para a referência de parâmetros de efeito, técnicas, passagens e anotações com um efeito.</span><span class="sxs-lookup"><span data-stu-id="c0104-159">Handles provide an efficient means for referencing effect parameters, techniques, passes, and annotations with an effect.</span></span> <span data-ttu-id="c0104-160">Identificadores (que são do tipo D3DXHANDLE) são ponteiros de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c0104-160">Handles (which are of type D3DXHANDLE) are string pointers.</span></span> <span data-ttu-id="c0104-161">Os identificadores que são transmitidos para funções como GetParameterxxx ou GetAnnotationxxx podem estar em uma das três formas:</span><span class="sxs-lookup"><span data-stu-id="c0104-161">The handles that are passed into functions such as GetParameterxxx or GetAnnotationxxx can be in one of three forms:</span></span>

-   <span data-ttu-id="c0104-162">Um identificador retornado por uma função como GetParameterxxx.</span><span class="sxs-lookup"><span data-stu-id="c0104-162">A handle returned by a function such as GetParameterxxx.</span></span>
-   <span data-ttu-id="c0104-163">Uma cadeia de caracteres que contém o nome do parâmetro, da técnica, da passagem ou da anotação.</span><span class="sxs-lookup"><span data-stu-id="c0104-163">A string containing the name of the parameter, technique, pass, or annotation.</span></span>
-   <span data-ttu-id="c0104-164">Um identificador definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="c0104-164">A handle set to **NULL**.</span></span>

<span data-ttu-id="c0104-165">Este exemplo retorna um identificador para o parâmetro que tem a semântica WORLDVIEWPROJ anexada a ele:</span><span class="sxs-lookup"><span data-stu-id="c0104-165">This example returns a handle to the parameter that has the WORLDVIEWPROJ semantic attached to it:</span></span>


```
D3DHANDLE handle = 
    m_pEffect->GetParameterBySemantic(NULL, "WORLDVIEWPROJ");
```



## <a name="add-parameter-information-with-annotations"></a><span data-ttu-id="c0104-166">Adicionar informações de parâmetro com anotações</span><span class="sxs-lookup"><span data-stu-id="c0104-166">Add Parameter Information with Annotations</span></span>

<span data-ttu-id="c0104-167">As anotações são dados específicos do usuário que podem ser anexados a qualquer técnica, passagem ou parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c0104-167">Annotations are user-specific data that can be attached to any technique, pass, or parameter.</span></span> <span data-ttu-id="c0104-168">Uma anotação é uma maneira flexível de adicionar informações a parâmetros individuais.</span><span class="sxs-lookup"><span data-stu-id="c0104-168">An annotation is a flexible way to add information to individual parameters.</span></span> <span data-ttu-id="c0104-169">As informações podem ser lidas e usadas de qualquer forma que o aplicativo escolher.</span><span class="sxs-lookup"><span data-stu-id="c0104-169">The information can be read back and used any way the application chooses.</span></span> <span data-ttu-id="c0104-170">Uma anotação pode ser de qualquer tipo de dados e pode ser adicionada dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="c0104-170">An annotation can be of any data type and can be added dynamically.</span></span> <span data-ttu-id="c0104-171">As declarações de anotação são delimitadas por colchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="c0104-171">Annotation declarations are delimited by angle brackets.</span></span> <span data-ttu-id="c0104-172">Uma anotação contém:</span><span class="sxs-lookup"><span data-stu-id="c0104-172">An annotation contains:</span></span>

-   <span data-ttu-id="c0104-173">Um tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c0104-173">A data type.</span></span>
-   <span data-ttu-id="c0104-174">Um nome de variável.</span><span class="sxs-lookup"><span data-stu-id="c0104-174">A variable name.</span></span>
-   <span data-ttu-id="c0104-175">Um sinal de igual (=).</span><span class="sxs-lookup"><span data-stu-id="c0104-175">An equals sign (=).</span></span>
-   <span data-ttu-id="c0104-176">O valor dos dados.</span><span class="sxs-lookup"><span data-stu-id="c0104-176">The data value.</span></span>
-   <span data-ttu-id="c0104-177">Um ponto e vírgula final (;).</span><span class="sxs-lookup"><span data-stu-id="c0104-177">A ending semicolon (;).</span></span>

<span data-ttu-id="c0104-178">Por exemplo, os dois exemplos anteriores neste documento contêm esta anotação:</span><span class="sxs-lookup"><span data-stu-id="c0104-178">For instance, both of the previous examples in this paper contain this annotation:</span></span>


```
texture Tex0 < string name = "tiger.bmp"; >;
```



<span data-ttu-id="c0104-179">A anotação é anexada ao objeto de textura e especifica o arquivo de textura que deve ser usado para inicializar o objeto de textura.</span><span class="sxs-lookup"><span data-stu-id="c0104-179">The annotation is attached to the texture object and specifies the texture file that should be used to initialize the texture object.</span></span> <span data-ttu-id="c0104-180">A anotação não inicializa o objeto de textura; ela é simplesmente uma parte das informações do usuário anexadas à variável.</span><span class="sxs-lookup"><span data-stu-id="c0104-180">The annotation does not initialize the texture object, it is simply a piece of user information that is attached to the variable.</span></span> <span data-ttu-id="c0104-181">Um aplicativo pode ler a anotação com [**ID3DXBaseEffect:: GetAnnotation**](id3dxbaseeffect--getannotation.md) ou [**ID3DXBaseEffect:: GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) para retornar a cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c0104-181">An application can read the annotation with either [**ID3DXBaseEffect::GetAnnotation**](id3dxbaseeffect--getannotation.md) or [**ID3DXBaseEffect::GetAnnotationByName**](id3dxbaseeffect--getannotationbyname.md) to return the string.</span></span> <span data-ttu-id="c0104-182">As anotações também podem ser adicionadas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0104-182">Annotations can also be added by the application.</span></span>

<span data-ttu-id="c0104-183">Cada anotação:</span><span class="sxs-lookup"><span data-stu-id="c0104-183">Each annotation:</span></span>

-   <span data-ttu-id="c0104-184">Deve ser numérico ou cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="c0104-184">Must be either numeric or strings.</span></span>
-   <span data-ttu-id="c0104-185">Sempre deve ser inicializado com um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="c0104-185">Must always be initialized with a default value.</span></span>
-   <span data-ttu-id="c0104-186">Pode ser associado com [técnicas e passagens (Direct3D 9)](techniques-and-passes.md) e [parâmetros de efeito](/previous-versions/windows/desktop/ee417539(v=vs.85))de nível superior.</span><span class="sxs-lookup"><span data-stu-id="c0104-186">Can be associated with [Techniques and Passes (Direct3D 9)](techniques-and-passes.md) and top-level [Effect Parameters](/previous-versions/windows/desktop/ee417539(v=vs.85)).</span></span>
-   <span data-ttu-id="c0104-187">Podem ser gravados e lidos com o [**ID3DXEffect**](id3dxeffect.md) ou o [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="c0104-187">Can be written to and read from with either [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>
-   <span data-ttu-id="c0104-188">Pode ser adicionado com [**ID3DXEffect**](id3dxeffect.md).</span><span class="sxs-lookup"><span data-stu-id="c0104-188">Can be added with [**ID3DXEffect**](id3dxeffect.md).</span></span>
-   <span data-ttu-id="c0104-189">Não pode ser referenciado dentro do efeito.</span><span class="sxs-lookup"><span data-stu-id="c0104-189">Cannot be referenced inside the effect.</span></span>
-   <span data-ttu-id="c0104-190">Não pode ter subtipos ou subnotações.</span><span class="sxs-lookup"><span data-stu-id="c0104-190">Cannot have sub-semantics or sub-annotations.</span></span>

## <a name="share-effect-parameters"></a><span data-ttu-id="c0104-191">Parâmetros de efeito de compartilhamento</span><span class="sxs-lookup"><span data-stu-id="c0104-191">Share Effect Parameters</span></span>

<span data-ttu-id="c0104-192">Os parâmetros de efeito são todas as variáveis não estáticas declaradas em um efeito.</span><span class="sxs-lookup"><span data-stu-id="c0104-192">Effect parameters are all the non-static variables declared in an effect.</span></span> <span data-ttu-id="c0104-193">Isso pode incluir variáveis e anotações globais.</span><span class="sxs-lookup"><span data-stu-id="c0104-193">This can include global variables and annotations.</span></span> <span data-ttu-id="c0104-194">Os parâmetros de efeito podem ser compartilhados entre diferentes efeitos declarando parâmetros com a palavra-chave "Shared" e, em seguida, criando o efeito com um pool de efeitos.</span><span class="sxs-lookup"><span data-stu-id="c0104-194">Effect parameters can be shared between different effects by declaring parameters with the "shared" keyword and then creating the effect with an effect pool.</span></span>

<span data-ttu-id="c0104-195">Um pool de efeitos contém parâmetros de efeito compartilhados.</span><span class="sxs-lookup"><span data-stu-id="c0104-195">An effect pool contains shared effect parameters.</span></span> <span data-ttu-id="c0104-196">O pool é criado chamando [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), que retorna uma interface [**ID3DXEffectPool**](id3dxeffectpool.md) .</span><span class="sxs-lookup"><span data-stu-id="c0104-196">The pool is created by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md), which returns an [**ID3DXEffectPool**](id3dxeffectpool.md) interface.</span></span> <span data-ttu-id="c0104-197">A interface pode ser fornecida como uma entrada para qualquer uma das funções D3DXCreateEffectxxx quando um efeito é criado.</span><span class="sxs-lookup"><span data-stu-id="c0104-197">The interface can be supplied as an input to any of the D3DXCreateEffectxxx functions when an effect is created.</span></span> <span data-ttu-id="c0104-198">Para que um parâmetro seja compartilhado entre vários efeitos, o parâmetro deve ter o mesmo nome, tipo e semântica em cada um dos efeitos compartilhados.</span><span class="sxs-lookup"><span data-stu-id="c0104-198">For a parameter to be shared across multiple effects, the parameter must have the same name, type, and semantic in each of the shared effects.</span></span>


```
ID3DXEffectPool* g_pEffectPool = NULL;   // Effect pool for sharing parameters

    D3DXCreateEffectPool( &g_pEffectPool );
```



<span data-ttu-id="c0104-199">Efeitos que compartilham parâmetros devem usar o mesmo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c0104-199">Effects that share parameters must use the same device.</span></span> <span data-ttu-id="c0104-200">Isso é imposto para impedir o compartilhamento de parâmetros dependentes do dispositivo (como sombreadores ou texturas) em diferentes dispositivos.</span><span class="sxs-lookup"><span data-stu-id="c0104-200">This is enforced to prevent the sharing of device-dependent parameters (such as shaders or textures) across different devices.</span></span> <span data-ttu-id="c0104-201">Os parâmetros são excluídos do pool sempre que os efeitos que contêm os parâmetros compartilhados são liberados.</span><span class="sxs-lookup"><span data-stu-id="c0104-201">Parameters are deleted from the pool whenever the effects that contain the shared parameters are released.</span></span> <span data-ttu-id="c0104-202">Se os parâmetros de compartilhamento não forem necessários, forneça **NULL** para o pool de efeitos quando um efeito for criado.</span><span class="sxs-lookup"><span data-stu-id="c0104-202">If sharing parameters is not necessary, supply **NULL** for the effect pool when an effect is created.</span></span>

<span data-ttu-id="c0104-203">Os efeitos clonados usam o mesmo pool de efeitos que o efeito do qual são clonados.</span><span class="sxs-lookup"><span data-stu-id="c0104-203">Cloned effects use the same effect pool as the effect from which they are cloned.</span></span> <span data-ttu-id="c0104-204">A clonagem de um efeito faz uma cópia exata de um efeito, incluindo variáveis globais, técnicas, passagens e anotações.</span><span class="sxs-lookup"><span data-stu-id="c0104-204">Cloning an effect makes an exact copy of an effect, including global variables, techniques, passes, and annotations.</span></span>

## <a name="compile-an-effect-offline"></a><span data-ttu-id="c0104-205">Compilar um efeito offline</span><span class="sxs-lookup"><span data-stu-id="c0104-205">Compile an Effect Offline</span></span>

<span data-ttu-id="c0104-206">Você pode compilar um efeito em tempo de execução com [**D3DXCreateEffect**](d3dxcreateeffect.md), ou você pode compilar um efeito offline usando a ferramenta de compilador de linha de comando fxc.exe.</span><span class="sxs-lookup"><span data-stu-id="c0104-206">You can compile an effect at run time with [**D3DXCreateEffect**](d3dxcreateeffect.md), or you can compile an effect offline using the command-line compiler tool fxc.exe.</span></span> <span data-ttu-id="c0104-207">O efeito no [exemplo CompiledEffect](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contém um sombreador de vértice, um sombreador de pixel e uma técnica:</span><span class="sxs-lookup"><span data-stu-id="c0104-207">The effect in the [CompiledEffect Sample](https://msdn.microsoft.com/library/Ee416326(v=VS.85).aspx) contains a vertex shader, a pixel shader, and one technique:</span></span>


```
// File: CompiledEffect.fx

// Global variables
float4 g_MaterialAmbientColor;    // Material's ambient color
...

// Texture samplers
sampler RenderTargetSampler = 
   ...

// Type: Vertex shader                                      
VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0 )
{
   ...
};
// Type: Pixel shader
PS_OUTPUT RenderScenePS( VS_OUTPUT In ) 
{ 
   ...
}

// Type: Technique                                     
technique RenderScene
{
    pass P0
    {          
        ZENABLE = true;
        VertexShader = compile vs_1_1 RenderSceneVS();
        PixelShader  = compile ps_1_1 RenderScenePS();
    }
}
```



<span data-ttu-id="c0104-208">Usando a [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para compilar o sombreador para vs \_ 1 \_ 1 gerou as seguintes instruções do sombreador de assembly:</span><span class="sxs-lookup"><span data-stu-id="c0104-208">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generated the following assembly shader instructions:</span></span>


```
//
// Generated by Microsoft (R) D3DX9 Shader Compiler 4.09.02.1188
//
//   fxc /T vs_1_1 /E RenderSceneVS /Fc CompiledEffect.txt CompiledEffect.fx
//
//
// Parameters:
//
//   float4 g_LightAmbient;
//   float4 g_LightDiffuse;
//   float3 g_LightDir;
//   float4 g_MaterialAmbientColor;
//   float4 g_MaterialDiffuseColor;
//   float g_fTime;
//   float4x4 g_mWorld;
//   float4x4 g_mWorldViewProjection;
//
//
// Registers:
//
//   Name                   Reg   Size
//   ---------------------- ----- ----
//   g_mWorldViewProjection c0       4
//   g_mWorld               c4       3
//   g_MaterialAmbientColor c7       1
//   g_MaterialDiffuseColor c8       1
//   g_LightDir             c9       1
//   g_LightAmbient         c10      1
//   g_LightDiffuse         c11      1
//   g_fTime                c12      1
//
//
// Default values:
//
//   g_LightDir
//     c9   = { 0.57735, 0.57735, 0.57735, 0 };
//
//   g_LightAmbient
//     c10  = { 1, 1, 1, 1 };
//
//   g_LightDiffuse
//     c11  = { 1, 1, 1, 1 };
//

    vs_1_1
    def c13, 0.159154937, 0.25, 6.28318548, -3.14159274
    def c14, -2.52398507e-007, 2.47609005e-005, -0.00138883968, 0.0416666418
    def c15, -0.5, 1, 0.5, 0
    dcl_position v0
    dcl_normal v1
    dcl_texcoord v2
    mov r0.w, c12.x
    mad r0.w, r0.w, c13.x, c13.y
    expp r3.y, r0.w
    mov r0.w, r3.y
    mad r0.w, r0.w, c13.z, c13.w
    mul r0.w, r0.w, r0.w
    mad r1.w, r0.w, c14.x, c14.y
    mad r1.w, r0.w, r1.w, c14.z
    mad r1.w, r0.w, r1.w, c14.w
    mad r1.w, r0.w, r1.w, c15.x
    mad r0.w, r0.w, r1.w, c15.y
    mul r0.w, r0.w, v0.x
    mul r0.x, r0.w, c15.z
    dp3 r1.x, v1, c4
    dp3 r1.y, v1, c5
    dp3 r1.z, v1, c6
    mov r0.yzw, c15.w
    dp3 r2.x, r1, r1
    add r0, r0, v0
    rsq r1.w, r2.x
    dp4 oPos.x, r0, c0
    mul r1.xyz, r1, r1.w
    dp4 oPos.y, r0, c1
    dp3 r1.x, r1, c9
    dp4 oPos.z, r0, c2
    max r1.w, r1.x, c15.w
    mov r1.xyz, c8
    mul r1.xyz, r1, c11
    mov r2.xyz, c7
    mul r2.xyz, r2, c10
    dp4 oPos.w, r0, c3
    mad oD0.xyz, r1, r1.w, r2
    mov oD0.w, c15.y
    mov oT0.xy, v2

// approximately 34 instruction slots used
```



## <a name="improve-performance-with-preshaders"></a><span data-ttu-id="c0104-209">Melhorar o desempenho com preshaders</span><span class="sxs-lookup"><span data-stu-id="c0104-209">Improve Performance with Preshaders</span></span>

<span data-ttu-id="c0104-210">Um preshadr é uma técnica para aumentar a eficiência do sombreador ao calcular previamente as expressões de sombreador de constantes.</span><span class="sxs-lookup"><span data-stu-id="c0104-210">A preshader is a technique for increasing shader efficiency by pre-calculating constant shader expressions.</span></span> <span data-ttu-id="c0104-211">O compilador de efeito recebe automaticamente as computações de sombreador do corpo de um sombreador e as executa na CPU antes do sombreador em execução.</span><span class="sxs-lookup"><span data-stu-id="c0104-211">The effect compiler automatically pulls out shader computations from the body of a shader and executes them on the CPU prior to the shader running.</span></span> <span data-ttu-id="c0104-212">Consequentemente, os preshaders só funcionam com efeitos.</span><span class="sxs-lookup"><span data-stu-id="c0104-212">Consequently, preshaders only work with effects.</span></span> <span data-ttu-id="c0104-213">Por exemplo, essas duas expressões podem ser avaliadas fora do sombreador antes de ser executada.</span><span class="sxs-lookup"><span data-stu-id="c0104-213">For instance, these two expressions can be evaluated outside of the shader before it runs.</span></span>


```
mul(World,mul(View, Projection));
sin(time)
```



<span data-ttu-id="c0104-214">As computações de sombreador que podem ser movidas são aquelas associadas a parâmetros uniformes; ou seja, os cálculos não são alterados para cada vértice ou pixel.</span><span class="sxs-lookup"><span data-stu-id="c0104-214">Shader computations that can be moved are those associated with uniform parameters; that is, the computations do not change for each vertex or pixel.</span></span> <span data-ttu-id="c0104-215">Se você estiver usando efeitos, o compilador de efeito gerará e executará automaticamente um preshader para você; Não há sinalizadores a serem habilitados.</span><span class="sxs-lookup"><span data-stu-id="c0104-215">If you are using effects, the effect compiler automatically generates and runs a preshader for you; there are no flags to enable.</span></span> <span data-ttu-id="c0104-216">Os preshaders podem reduzir o número de instruções por sombreador e também podem reduzir o número de registros constantes consumidos por um sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0104-216">Preshaders can reduce the number of instructions per shader and can also reduce the number of constant registers a shader consumes.</span></span>

<span data-ttu-id="c0104-217">Imagine o compilador de efeito como um tipo de compilador com vários processadores porque ele compila o código do sombreador para dois tipos de processadores: uma CPU e uma GPU.</span><span class="sxs-lookup"><span data-stu-id="c0104-217">Think of the effect compiler as a sort of multi-processor compiler because it compiles shader code for two types of processors: a CPU and a GPU.</span></span> <span data-ttu-id="c0104-218">Além disso, o compilador de efeito foi projetado para mover o código da GPU para a CPU e, portanto, melhorar o desempenho do sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0104-218">In addition, the effect compiler is designed to move code from the GPU to the CPU and therefore improve shader performance.</span></span> <span data-ttu-id="c0104-219">Isso é muito semelhante a extrair uma expressão estática para fora de um loop.</span><span class="sxs-lookup"><span data-stu-id="c0104-219">This is very similar to pulling a static expression out of a loop.</span></span> <span data-ttu-id="c0104-220">Um sombreador que transforma a posição do espaço do mundo para o espaço de projeção e copia coordenadas de textura se pareceria com isso em HLSL:</span><span class="sxs-lookup"><span data-stu-id="c0104-220">A shader that transforms position from world space to projection space, and copies texture coordinates would look like this in HLSL:</span></span>


```
float4x4 g_mWorldViewProjection;    // World * View * Projection matrix
float4x4 g_mWorldInverse;           // Inverse World matrix
float3 g_LightDir;                  // Light direction in world space
float4 g_LightDiffuse;              // Diffuse color of the light

struct VS_OUTPUT
{
    float4 Position   : POSITION;   // vertex position 
    float2 TextureUV  : TEXCOORD0;  // vertex texture coords 
    float4 Diffuse    : COLOR0;     // vertex diffuse color
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION, 
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0)
{
    VS_OUTPUT Output;
    
    // Transform the position from object space to projection space
    Output.Position = mul(vPos, g_mWorldViewProjection);

    // Transform the light from world space to object space    
    float3 vLightObjectSpace = normalize(mul(g_LightDir, (float3x3)g_mWorldInverse)); 

    // N dot L lighting
    Output.Diffuse = max(0,dot(vNormal, vLightObjectSpace));
    
    // Copy the texture coordinate
    Output.TextureUV = vTexCoord0; 
    
    return Output;    
}
technique RenderVS
{
    pass P0
    {          
        VertexShader = compile vs_1_1 RenderSceneVS();
    }
}
```



<span data-ttu-id="c0104-221">O uso da [ferramenta de compilador de efeito](../direct3dtools/fxc.md) para compilar o sombreador para vs \_ 1 \_ 1 gera as seguintes instruções de assembly:</span><span class="sxs-lookup"><span data-stu-id="c0104-221">Using [Effect-Compiler Tool](../direct3dtools/fxc.md) to compile the shader for vs\_1\_1 generates the following assembly instructions:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //   g_mWorldInverse        c4       3
            //   g_LightDir             c7       1
            //
            
                vs_1_1
                def c8, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                mov r1.xyz, c7
                dp3 r0.x, r1, c4
                dp3 r0.y, r1, c5
                dp3 r0.z, r1, c6
                dp4 oPos.x, v0, c0
                dp3 r1.x, r0, r0
                dp4 oPos.y, v0, c1
                rsq r0.w, r1.x
                dp4 oPos.z, v0, c2
                mul r0.xyz, r0, r0.w
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, r0
                max oD0, r0.x, c8.x
                mov oT0.xy, v2
            
            // approximately 14 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="c0104-222">Isso usa aproximadamente 14 slots e consome 9 registros constantes.</span><span class="sxs-lookup"><span data-stu-id="c0104-222">This uses up approximately 14 slots and consumes 9 constant registers.</span></span> <span data-ttu-id="c0104-223">Com um preshadr, o compilador move as expressões estáticas para fora do sombreador e para o preshadr.</span><span class="sxs-lookup"><span data-stu-id="c0104-223">With a preshader, the compiler moves the static expressions out of the shader and into the preshader.</span></span> <span data-ttu-id="c0104-224">O mesmo sombreador ficaria assim com um preshadr:</span><span class="sxs-lookup"><span data-stu-id="c0104-224">The same shader would look like this with a preshader:</span></span>


```
technique RenderVS
{
    pass P0
    {
        vertexshader = 
            asm {
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float3 g_LightDir;
            //   float4x4 g_mWorldInverse;
            //
            //
            // Registers:
            //
            //   Name            Reg   Size
            //   --------------- ----- ----
            //   g_mWorldInverse c0       3
            //   g_LightDir      c3       1
            //
            
                preshader
                dot r0.x, c3.xyz, c0.xyz
                dot r0.y, c3.xyz, c1.xyz
                dot r0.z, c3.xyz, c2.xyz
                dot r1.w, r0.xyz, r0.xyz
                rsq r0.w, r1.w
                mul c4.xyz, r0.w, r0.xyz
            
            // approximately 6 instructions used
            //
            // Generated by Microsoft (R) D3DX9 Shader Compiler 9.15.779.0000
            //
            // Parameters:
            //
            //   float4x4 g_mWorldViewProjection;
            //
            //
            // Registers:
            //
            //   Name                   Reg   Size
            //   ---------------------- ----- ----
            //   g_mWorldViewProjection c0       4
            //
            
                vs_1_1
                def c5, 0, 0, 0, 0
                dcl_position v0
                dcl_normal v1
                dcl_texcoord v2
                dp4 oPos.x, v0, c0
                dp4 oPos.y, v0, c1
                dp4 oPos.z, v0, c2
                dp4 oPos.w, v0, c3
                dp3 r0.x, v1, c4
                max oD0, r0.x, c5.x
                mov oT0.xy, v2
            
            // approximately 7 instruction slots used
            };

        //No embedded pixel shader
    }
}
```



<span data-ttu-id="c0104-225">Um efeito executa um preshadr logo antes de executar um sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0104-225">An effect executes a preshader just before executing a shader.</span></span> <span data-ttu-id="c0104-226">O resultado é a mesma funcionalidade com maior desempenho de sombreador porque o número de instruções que precisam ser executadas (para cada vértice ou pixel dependendo do tipo de sombreador) foi reduzido.</span><span class="sxs-lookup"><span data-stu-id="c0104-226">The result is the same functionality with increased shader performance because the number of instructions that need to be executed (for each vertex or pixel depending on the type of shader) has been reduced.</span></span> <span data-ttu-id="c0104-227">Além disso, menos registros constantes são consumidos pelo sombreador como resultado das expressões estáticas que estão sendo movidas para o preshadr.</span><span class="sxs-lookup"><span data-stu-id="c0104-227">In addition, fewer constant registers are consumed by the shader as a result of the static expressions being moved to the preshader.</span></span> <span data-ttu-id="c0104-228">Isso significa que os sombreadores anteriormente limitados pelo número de registros constantes que eles necessitam podem agora ser compilados porque exigem menos registros constantes.</span><span class="sxs-lookup"><span data-stu-id="c0104-228">This means that shaders previously limited by the number of constant registers they required may now compile because they require fewer constant registers.</span></span> <span data-ttu-id="c0104-229">É razoável esperar uma melhoria de desempenho de 5 por cento e 20% dos preshaders.</span><span class="sxs-lookup"><span data-stu-id="c0104-229">It is reasonable to expect a 5 percent and a 20 percent performance improvement from preshaders.</span></span>

<span data-ttu-id="c0104-230">Tenha em mente que as constantes de entrada são diferentes das constantes de saída em um preshadr.</span><span class="sxs-lookup"><span data-stu-id="c0104-230">Keep in mind that the input constants are different from the output constants in a preshader.</span></span> <span data-ttu-id="c0104-231">A saída C1 não é igual à entrada C1 Register.</span><span class="sxs-lookup"><span data-stu-id="c0104-231">The output c1 is not the same as the input c1 register.</span></span> <span data-ttu-id="c0104-232">Gravar em um registro constante em um preshadr realmente grava no slot de entrada (constante) do sombreador correspondente.</span><span class="sxs-lookup"><span data-stu-id="c0104-232">Writing to a constant register in a preshader actually writes into the corresponding shader's input (constant) slot.</span></span>


```
// BaseDelta c0 1
// Refinements c1 1
preshader
mul c1.x, c0.x, (-2)
add c0.x, c0.x, c0.x
cmp c5.x, c1.x, (1), (0)
```



<span data-ttu-id="c0104-233">A instrução CMP acima lerá o valor C1 do preshadr, enquanto a instrução Mul será gravada nos registros do sombreador de hardware a serem usados pelo sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="c0104-233">The cmp instruction above will read the preshader c1 value, while the mul instruction will write to the hardware shader registers to be used by the vertex shader.</span></span>

## <a name="use-parameter-blocks-to-manage-effect-parameters"></a><span data-ttu-id="c0104-234">Usar blocos de parâmetro para gerenciar parâmetros de efeito</span><span class="sxs-lookup"><span data-stu-id="c0104-234">Use Parameter Blocks to Manage Effect Parameters</span></span>

<span data-ttu-id="c0104-235">Os blocos de parâmetro são blocos de alterações de estado de efeito.</span><span class="sxs-lookup"><span data-stu-id="c0104-235">Parameter blocks are blocks of effect state changes.</span></span> <span data-ttu-id="c0104-236">Um bloco de parâmetro pode registrar alterações de estado, para que elas possam ser aplicadas posteriormente com uma única chamada.</span><span class="sxs-lookup"><span data-stu-id="c0104-236">A parameter block can record state changes, so that they can be applied later on with a single call.</span></span> <span data-ttu-id="c0104-237">Crie um bloco de parâmetro chamando [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md):</span><span class="sxs-lookup"><span data-stu-id="c0104-237">Create a parameter block by calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md):</span></span>


```
    m_pEffect->SetTechnique( "RenderScene" );

    m_pEffect->BeginParameterBlock();
    D3DXVECTOR4 v4( Diffuse.r, Diffuse.g, Diffuse.b, Diffuse.a );
    m_pEffect->SetVector( "g_vDiffuse", &v4 );
    m_pEffect->SetFloat( "g_fReflectivity", fReflectivity );
    m_pEffect->SetFloat( "g_fAnimSpeed", fAnimSpeed );
    m_pEffect->SetFloat( "g_fSizeMul", fSize );
    m_hParameters = m_pEffect->EndParameterBlock();
```



<span data-ttu-id="c0104-238">O bloco de parâmetro salva quatro alterações aplicadas pelas chamadas à API.</span><span class="sxs-lookup"><span data-stu-id="c0104-238">The parameter block saves four changes applied by the API calls.</span></span> <span data-ttu-id="c0104-239">Chamar [**ID3DXEffect:: BeginParameterBlock**](id3dxeffect--beginparameterblock.md) começa a registrar as alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="c0104-239">Calling [**ID3DXEffect::BeginParameterBlock**](id3dxeffect--beginparameterblock.md) starts recording the state changes.</span></span> <span data-ttu-id="c0104-240">[**ID3DXEffect:: EndParameterBlock**](id3dxeffect--endparameterblock.md) para de adicionar as alterações ao bloco de parâmetro e retorna um identificador.</span><span class="sxs-lookup"><span data-stu-id="c0104-240">[**ID3DXEffect::EndParameterBlock**](id3dxeffect--endparameterblock.md) stops adding the changes to the parameter block and returns a handle.</span></span> <span data-ttu-id="c0104-241">O identificador será usado ao chamar [**ID3DXEffect:: ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).</span><span class="sxs-lookup"><span data-stu-id="c0104-241">The handle will be used when calling [**ID3DXEffect::ApplyParameterBlock**](id3dxeffect--applyparameterblock.md).</span></span>

<span data-ttu-id="c0104-242">No [exemplo de EffectParam](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), o bloco de parâmetro é aplicado na sequência de renderização:</span><span class="sxs-lookup"><span data-stu-id="c0104-242">In the [EffectParam Sample](https://msdn.microsoft.com/library/Ee417535(v=VS.85).aspx), the parameter block is applied in the render sequence:</span></span>


```
CObj g_aObj[NUM_OBJS];       // Object instances

    if( SUCCEEDED( pd3dDevice->BeginScene() ) )
    {
        // Set the shared parameters using the first mesh's effect.

        // Render the mesh objects
        for( int i = 0; i < NUM_OBJS; ++i )
        {
            ID3DXEffect *pEffect = g_aObj[i].m_pEffect;

            // Apply the parameters
            pEffect->ApplyParameterBlock( g_aObj[i].m_hParameters );

            ...

            pEffect->Begin( &cPasses, 0 );
            for( iPass = 0; iPass < cPasses; iPass++ )
            {
              ...
            }
            pEffect->End();
        }

        ...
        pd3dDevice->EndScene();
    }
```



<span data-ttu-id="c0104-243">O bloco de parâmetro define o valor de todas as quatro alterações de estado logo antes de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="c0104-243">The parameter block sets the value of all four of the state changes just before [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called.</span></span> <span data-ttu-id="c0104-244">Os blocos de parâmetro são uma maneira útil de definir várias alterações de estado com uma única chamada à API.</span><span class="sxs-lookup"><span data-stu-id="c0104-244">Parameter blocks are a handy way to set multiple state changes with a single API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0104-245">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0104-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0104-246">Effect</span><span class="sxs-lookup"><span data-stu-id="c0104-246">Effects</span></span>](effects.md)
</dt> </dl>

 

 
