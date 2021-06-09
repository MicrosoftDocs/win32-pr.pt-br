---
title: Usando sombreadores no Direct3D 10
description: Usando sombreadores no Direct3D 10
ms.assetid: cff6f901-cb9b-44d5-a75b-9a4029a37215
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c0d6212851e4603aac4db7ec85dd20714dc87774
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826284"
---
# <a name="using-shaders-in-direct3d-10"></a><span data-ttu-id="677ff-103">Usando sombreadores no Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="677ff-103">Using Shaders in Direct3D 10</span></span>

<span data-ttu-id="677ff-104">O pipeline tem três estágios de sombreador e cada um é programado com um sombreador HLSL.</span><span class="sxs-lookup"><span data-stu-id="677ff-104">The pipeline has three shader stages and each one is programmed with an HLSL shader.</span></span> <span data-ttu-id="677ff-105">Todos os sombreadores do Direct3D 10 são escritos em HLSL, direcionando o modelo de sombreador 4.</span><span class="sxs-lookup"><span data-stu-id="677ff-105">All Direct3D 10 shaders are written in HLSL, targeting shader model 4.</span></span>


<span data-ttu-id="677ff-106">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="677ff-106">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="677ff-107">Ao contrário dos modelos de sombreador do Direct3D 9 que poderiam ser criados em uma linguagem de assembly intermediária, os sombreadores do modelo do sombreador 4,0 são criados apenas no HLSL.</span><span class="sxs-lookup"><span data-stu-id="677ff-107">Unlike Direct3D 9 shader models which could be authored in an intermediate assembly language, shader model 4.0 shaders are only authored in HLSL.</span></span> <span data-ttu-id="677ff-108">A compilação offline de sombreadores em um código de bytes de consumo de dispositivo ainda tem suporte e é recomendada para a maioria dos cenários.</span><span class="sxs-lookup"><span data-stu-id="677ff-108">Offline compilation of shaders into device-consumable bytecode is still supported, and recommended for most scenarios.</span></span>



 

<span data-ttu-id="677ff-109">Este exemplo usa apenas um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="677ff-109">This example uses only a vertex shader.</span></span> <span data-ttu-id="677ff-110">Como todos os sombreadores são criados a partir do principal sombreador comum, aprender a usar um sombreador de vértice é muito semelhante a usar um sombreador ou uma geometria de pixel.</span><span class="sxs-lookup"><span data-stu-id="677ff-110">Because all shaders are built from the common shader core, learning how to use a vertex shader is very similar to using a geometry or pixel shader.</span></span>

<span data-ttu-id="677ff-111">Depois de criar um sombreador HLSL (Este exemplo usa o HLSLWithoutFX de sombreador de vértice. VSH), será necessário prepará-lo para o estágio de pipeline específico que o usará.</span><span class="sxs-lookup"><span data-stu-id="677ff-111">Once you have authored an HLSL shader (this example uses the vertex shader HLSLWithoutFX.vsh), you will need to prepare it for the particular pipeline stage that will use it.</span></span> <span data-ttu-id="677ff-112">Para fazer isso, você precisa:</span><span class="sxs-lookup"><span data-stu-id="677ff-112">To do this you need to:</span></span>

-   [<span data-ttu-id="677ff-113">Compilar um sombreador</span><span class="sxs-lookup"><span data-stu-id="677ff-113">Compile a Shader</span></span>](#compile-a-shader)
-   [<span data-ttu-id="677ff-114">Criar um objeto de sombreador</span><span class="sxs-lookup"><span data-stu-id="677ff-114">Create a Shader Object</span></span>](#create-a-shader-object)
-   [<span data-ttu-id="677ff-115">Definir o objeto do sombreador</span><span class="sxs-lookup"><span data-stu-id="677ff-115">Set the Shader Object</span></span>](#set-the-shader-object)
-   [<span data-ttu-id="677ff-116">Repetir para todos os 3 estágios de sombreador</span><span class="sxs-lookup"><span data-stu-id="677ff-116">Repeat for all 3 Shader Stages</span></span>](#repeat-for-all-3-shader-stages)

<span data-ttu-id="677ff-117">Essas etapas precisam ser repetidas para cada sombreador no pipeline.</span><span class="sxs-lookup"><span data-stu-id="677ff-117">These steps need to be repeated for each shader in the pipeline.</span></span>

## <a name="compile-a-shader"></a><span data-ttu-id="677ff-118">Compilar um sombreador</span><span class="sxs-lookup"><span data-stu-id="677ff-118">Compile a Shader</span></span>

<span data-ttu-id="677ff-119">A primeira etapa é compilar o sombreador para verificar se você códigou as instruções HLSL corretamente.</span><span class="sxs-lookup"><span data-stu-id="677ff-119">The first step is to compile the shader, to check to see that you have coded the HLSL statements correctly.</span></span> <span data-ttu-id="677ff-120">Isso é feito chamando D3D10CompileShader e fornecendo-o com vários parâmetros, conforme mostrado aqui:</span><span class="sxs-lookup"><span data-stu-id="677ff-120">This is done by calling D3D10CompileShader and supplying it with several parameters as shown here:</span></span>


```
    IPD3D10Blob * pBlob;
    
        
    // Compile the vertex shader from the file
    D3D10CompileShader( strPath, strlen( strPath ), "HLSLWithoutFX.vsh", 
        NULL, NULL, "Ripple", "vs_4_0", dwShaderFlags, &pBlob, NULL );
```



<span data-ttu-id="677ff-121">Essa função usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="677ff-121">This function takes the following parameters:</span></span>

-   <span data-ttu-id="677ff-122">O nome do arquivo (e o comprimento da cadeia de caracteres de nome em bytes) que contém o sombreador.</span><span class="sxs-lookup"><span data-stu-id="677ff-122">The name of the file ( and length of the name string in bytes ) that contains the shader.</span></span> <span data-ttu-id="677ff-123">Este exemplo usa um sombreador de vértice somente (no arquivo HLSLWithoutFX. VSH em que a extensão de arquivo. VSH é uma abreviação do sombreador de vértice).</span><span class="sxs-lookup"><span data-stu-id="677ff-123">This example uses a vertex shader only (in the file HLSLWithoutFX.vsh file where the file extension .vsh is an abbreviation for vertex shader).</span></span>
-   <span data-ttu-id="677ff-124">O nome da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="677ff-124">The shader function name.</span></span> <span data-ttu-id="677ff-125">Este exemplo compila um sombreador de vértice da função Ripple que usa uma única entrada e retorna uma struct de saída (a função é do exemplo HLSLWithoutFX):</span><span class="sxs-lookup"><span data-stu-id="677ff-125">This example compiles a vertex shader from the Ripple function which takes a single input and returns an output struct (the function is from the HLSLWithoutFX sample):</span></span>
    ```
    VS_OUTPUT Ripple( in float2 vPosition : POSITION )
    ```

    

-   <span data-ttu-id="677ff-126">Um ponteiro para todas as macros usadas pelo sombreador.</span><span class="sxs-lookup"><span data-stu-id="677ff-126">A pointer to all macros used by the shader.</span></span> <span data-ttu-id="677ff-127">Use \_ \_ a macro do sombreador d3d10 para ajudar a definir suas macros; basta criar uma cadeia de caracteres de nome que contenha todos os nomes de macro (com cada nome separado por um espaço) e uma cadeia de caracteres de definição (com cada corpo de macro separado por um espaço).</span><span class="sxs-lookup"><span data-stu-id="677ff-127">Use D3D10\_SHADER\_MACRO to help define your macros; simply create a name string that contains all the macro names (with each name separated by a space) and a definition string (with each macro body separated by a space).</span></span> <span data-ttu-id="677ff-128">As duas cadeias de caracteres precisam ser terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="677ff-128">Both strings need to be NULL terminated.</span></span>
-   <span data-ttu-id="677ff-129">Um ponteiro para qualquer outro arquivo que você precise incluir para obter os sombreadores a serem compilados.</span><span class="sxs-lookup"><span data-stu-id="677ff-129">A pointer to any other files that you need included to get your shaders to compile.</span></span> <span data-ttu-id="677ff-130">Isso usa a interface ID3D10Include que tem dois métodos implementados pelo usuário: abrir e fechar.</span><span class="sxs-lookup"><span data-stu-id="677ff-130">This uses the ID3D10Include interface which has two user-implemented methods: Open and Close.</span></span> <span data-ttu-id="677ff-131">Para fazer isso funcionar, você precisará implementar o corpo dos métodos Open e close; no método Open, adicione o código que você usaria para abrir qualquer um dos arquivos de inclusão desejados, na função fechar, adicione o código para fechar os arquivos quando terminar de usá-los.</span><span class="sxs-lookup"><span data-stu-id="677ff-131">To make this work, you will need to implement the body of the Open and Close methods; in the Open method add the code you would use to open whatever include files you want, in the Close function add the code to close the files when you are done with them.</span></span>
-   <span data-ttu-id="677ff-132">O nome da função de sombreador a ser compilada.</span><span class="sxs-lookup"><span data-stu-id="677ff-132">The name of the shader function to compile.</span></span> <span data-ttu-id="677ff-133">Este sombreador compila a função Ripple.</span><span class="sxs-lookup"><span data-stu-id="677ff-133">This shader compiles the Ripple function.</span></span>
-   <span data-ttu-id="677ff-134">O perfil do sombreador a ser direcionado durante a compilação.</span><span class="sxs-lookup"><span data-stu-id="677ff-134">The shader profile to target when compiling.</span></span> <span data-ttu-id="677ff-135">Como você pode compilar uma função em um vértice, geometria ou sombreador de pixel, o perfil informa ao compilador qual tipo de sombreador e qual modelo de sombreador comparar o código.</span><span class="sxs-lookup"><span data-stu-id="677ff-135">Since you can compile a function into a vertex, geometry, or pixel shader, the profile tells the compiler which type of shader and which shader model to compare the code against.</span></span>
-   <span data-ttu-id="677ff-136">Sinalizadores do compilador do sombreador.</span><span class="sxs-lookup"><span data-stu-id="677ff-136">Shader compiler flags.</span></span> <span data-ttu-id="677ff-137">Esses sinalizadores informam ao compilador quais informações devem ser colocadas na saída compilada e como você deseja que o código de saída seja otimizado: para velocidade, para depuração etc. Consulte [constantes de efeito (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) para obter uma lista dos sinalizadores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="677ff-137">These flags tell the compiler what information to put into the compiled output and how you want the output code optimized: for speed, for debug, etc. See [Effect Constants (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-reference-effect-constants) for a listing of the available flags.</span></span> <span data-ttu-id="677ff-138">O exemplo contém algum código que você pode usar para definir os valores de sinalizador do compilador para seu projeto – isso é principalmente uma pergunta se você deseja ou não gerar informações de depuração.</span><span class="sxs-lookup"><span data-stu-id="677ff-138">The sample contains some code you can use to set the compiler flag values for your project - this is mainly a question of whether or not you want to generate debug information.</span></span>
-   <span data-ttu-id="677ff-139">Um ponteiro para o buffer que contém o código de sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="677ff-139">A pointer to the buffer that contains the compiled shader code.</span></span> <span data-ttu-id="677ff-140">O buffer também contém qualquer informação de tabela de depuração e símbolo inserida solicitada pelos sinalizadores do compilador.</span><span class="sxs-lookup"><span data-stu-id="677ff-140">The buffer also contains any embedded debug and symbol table information requested by the compiler flags.</span></span>
-   <span data-ttu-id="677ff-141">Um ponteiro para um buffer que contém uma lista de erros e avisos que foram encontrados durante a compilação, que são as mesmas mensagens que você veria na saída de depuração se estivesse executando o depurador durante a compilação do sombreador.</span><span class="sxs-lookup"><span data-stu-id="677ff-141">A pointer to a buffer that contains a listing of errors and warnings that were encountered during the compile, which are the same messages you would see in the debug output if you were running the debugger while compiling the shader.</span></span> <span data-ttu-id="677ff-142">**NULL** é um valor aceitável quando você não deseja que os erros sejam retornados a um buffer.</span><span class="sxs-lookup"><span data-stu-id="677ff-142">**NULL** is an acceptable value when you don't want the errors returned to a buffer.</span></span>

<span data-ttu-id="677ff-143">Se o sombreador for compilado com êxito, um ponteiro para o código do sombreador será retornado como uma interface ID3D10Blob.</span><span class="sxs-lookup"><span data-stu-id="677ff-143">If the shader compiles successfully, a pointer to the shader code is returned as a ID3D10Blob interface.</span></span> <span data-ttu-id="677ff-144">Ele é chamado de interface de blob porque o ponteiro é para um local na memória composto por uma matriz de DWORD.</span><span class="sxs-lookup"><span data-stu-id="677ff-144">It is called the Blob interface because the pointer is to a location in memory that is made up of an array of DWORD's.</span></span> <span data-ttu-id="677ff-145">A interface é fornecida para que você possa obter um ponteiro para o sombreador compilado que será necessário na próxima etapa.</span><span class="sxs-lookup"><span data-stu-id="677ff-145">The interface is provided so that you can get a pointer to the compiled shader which you will need in the next step.</span></span>

<span data-ttu-id="677ff-146">A partir do SDK de dezembro de 2006, o compilador do DirectX 10 HLSL agora é o compilador padrão no DirectX 9 e no DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="677ff-146">Beginning with the December 2006 SDK, the DirectX 10 HLSL compiler is now the default compiler in both DirectX 9 and DirectX 10.</span></span> <span data-ttu-id="677ff-147">Confira [ferramenta de compilador de efeito](/windows/desktop/direct3dtools/fxc) para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="677ff-147">See [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) for details.</span></span>

### <a name="get-a-pointer-to-a-compiled-shader"></a><span data-ttu-id="677ff-148">Obter um ponteiro para um sombreador compilado</span><span class="sxs-lookup"><span data-stu-id="677ff-148">Get a Pointer to a Compiled Shader</span></span>

<span data-ttu-id="677ff-149">Vários métodos de API exigem um ponteiro para um sombreador compilado.</span><span class="sxs-lookup"><span data-stu-id="677ff-149">Several API methods require a pointer to a compiled shader.</span></span> <span data-ttu-id="677ff-150">Esse argumento é geralmente chamado de *pShaderBytecode* porque aponta para um sombreador compilado representado como uma sequência de códigos de bytes.</span><span class="sxs-lookup"><span data-stu-id="677ff-150">This argument is usually called *pShaderBytecode* because it points to a compiled shader represented as a sequence of byte codes.</span></span> <span data-ttu-id="677ff-151">Para obter um ponteiro para um sombreador compilado, primeiro compile o sombreador chamando [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) ou uma função semelhante.</span><span class="sxs-lookup"><span data-stu-id="677ff-151">To get a pointer to a compiled shader, first compile the shader by calling [**D3D10CompileShader**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10compileshader) or a similar function.</span></span> <span data-ttu-id="677ff-152">Se a compilação for bem-sucedida, o sombreador compilado será retornado em uma interface [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) .</span><span class="sxs-lookup"><span data-stu-id="677ff-152">If compilation is successful, the compiled shader is returned in an [**ID3D10Blob**](/windows/desktop/api/d3dcommon/nn-d3dcommon-id3d10blob) interface.</span></span> <span data-ttu-id="677ff-153">Por fim, use o método [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) para retornar o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="677ff-153">Finally, use the [**GetBufferPointer**](/windows/desktop/api/d3dcommon/nf-d3dcommon-id3d10blob-getbufferpointer) method to return the pointer.</span></span>

## <a name="create-a-shader-object"></a><span data-ttu-id="677ff-154">Criar um objeto de sombreador</span><span class="sxs-lookup"><span data-stu-id="677ff-154">Create a Shader Object</span></span>

<span data-ttu-id="677ff-155">Depois que o sombreador for compilado, chame CreateVertexShader para criar o objeto Shader:</span><span class="sxs-lookup"><span data-stu-id="677ff-155">Once the shader is compiled, call CreateVertexShader to create the shader object:</span></span>


```
    ID3D10VertexShader ** ppVertexShader
    ID3D10Blob pBlob;


    // Create the vertex shader
    hr = pd3dDevice->CreateVertexShader( (DWORD*)pBlob->GetBufferPointer(),
        pBlob->GetBufferSize(), &ppVertexShader );

    // Release the pointer to the compiled shader once you are done with it
    pBlob->Release();
```



<span data-ttu-id="677ff-156">Para criar o objeto Shader, passe o ponteiro para o sombreador compilado em CreateVertexShader.</span><span class="sxs-lookup"><span data-stu-id="677ff-156">To create the shader object, pass the pointer to the compiled shader into CreateVertexShader.</span></span> <span data-ttu-id="677ff-157">Como você teve que compilar o sombreador com êxito primeiro, essa chamada quase certamente será aprovada, a menos que você tenha um problema de memória em seu computador.</span><span class="sxs-lookup"><span data-stu-id="677ff-157">Since you had to successfully compile the shader first, this call will almost certainly pass, unless you have a memory problem on your machine.</span></span>

<span data-ttu-id="677ff-158">Você pode criar quantos objetos de sombreador desejar e simplesmente manter os ponteiros para eles.</span><span class="sxs-lookup"><span data-stu-id="677ff-158">You can create as many shader objects as you like and simply keep pointers to them.</span></span> <span data-ttu-id="677ff-159">Esse mesmo mecanismo funciona para os sombreadores de geometria e pixel, supondo que você corresponda aos perfis de sombreador (quando você chama o método Compile) para os nomes de interface (quando você chama o método Create).</span><span class="sxs-lookup"><span data-stu-id="677ff-159">This same mechanism works for geometry and pixel shaders assuming you match the shader profiles (when you call the compile method) to the interface names (when you call the create method).</span></span>

## <a name="set-the-shader-object"></a><span data-ttu-id="677ff-160">Definir o objeto do sombreador</span><span class="sxs-lookup"><span data-stu-id="677ff-160">Set the Shader Object</span></span>

<span data-ttu-id="677ff-161">A última etapa é definir o sombreador para o estágio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="677ff-161">The last step is set the shader to the pipeline stage.</span></span> <span data-ttu-id="677ff-162">Como há três estágios de sombreador no pipeline, você precisará fazer três chamadas à API, uma para cada estágio.</span><span class="sxs-lookup"><span data-stu-id="677ff-162">Since there are three shader stages in the pipeline, you will need to make three API calls, one for each stage.</span></span>


```
    // Set a vertex shader
    pd3dDevice->VSSetShader( g_pVS10 );
```



<span data-ttu-id="677ff-163">A chamada para VSSetShader usa o ponteiro para o sombreador de vértice criado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="677ff-163">The call to VSSetShader takes the pointer to the vertex shader created in step 1.</span></span> <span data-ttu-id="677ff-164">Isso define o sombreador no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="677ff-164">This sets the shader in the device.</span></span> <span data-ttu-id="677ff-165">O estágio do sombreador de vértice agora é inicializado com seu código de sombreador de vértice, tudo o que resta é inicializar qualquer variável de sombreador.</span><span class="sxs-lookup"><span data-stu-id="677ff-165">The vertex shader stage is now initialized with its vertex shader code, all that remains is initializing any shader variables.</span></span>

## <a name="repeat-for-all-3-shader-stages"></a><span data-ttu-id="677ff-166">Repetir para todos os 3 estágios de sombreador</span><span class="sxs-lookup"><span data-stu-id="677ff-166">Repeat for all 3 Shader Stages</span></span>

<span data-ttu-id="677ff-167">Repita esse mesmo conjunto de etapas para criar qualquer sombreador de pixel ou vértice ou até mesmo um sombreador de geometria que produz o sombreador de pixel.</span><span class="sxs-lookup"><span data-stu-id="677ff-167">Repeat these same set of steps to build any vertex or pixel shader or even a geometry shader that outputs to the pixel shader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="677ff-168">Tópicos Relacionados</span><span class="sxs-lookup"><span data-stu-id="677ff-168">Related Topics</span></span>

[<span data-ttu-id="677ff-169">Compilar um sombreador</span><span class="sxs-lookup"><span data-stu-id="677ff-169">Compiling Shaders</span></span>](dx-graphics-hlsl-part1.md)


## <a name="related-topics"></a><span data-ttu-id="677ff-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="677ff-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="677ff-171">Guia de programação para HLSL</span><span class="sxs-lookup"><span data-stu-id="677ff-171">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

