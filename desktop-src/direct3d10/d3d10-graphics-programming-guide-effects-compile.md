---
description: Depois que um efeito foi criado, a primeira etapa é compilar o código para verificar se há problemas de sintaxe.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Compilar um efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab6183f2f71b07c482fa24efc4f9fed199216d75
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163961"
---
# <a name="compile-an-effect-direct3d-10"></a><span data-ttu-id="beeb2-103">Compilar um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="beeb2-103">Compile an Effect (Direct3D 10)</span></span>

<span data-ttu-id="beeb2-104">Depois que um efeito foi criado, a primeira etapa é compilar o código para verificar se há problemas de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="beeb2-104">Once an effect has been authored, the first step is to compile the code to check for syntax problems.</span></span> <span data-ttu-id="beeb2-105">Isso é feito chamando uma das APIs de compilação (como D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span><span class="sxs-lookup"><span data-stu-id="beeb2-105">This is done by calling one of the compile APIs (like D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory).</span></span> <span data-ttu-id="beeb2-106">Essas APIs invocam o compilador de efeito fxc.exe que é o compilador usado para compilar o código HLSL.</span><span class="sxs-lookup"><span data-stu-id="beeb2-106">These API's invoke the effect compiler fxc.exe which is the compiler used to compile HLSL code.</span></span> <span data-ttu-id="beeb2-107">É por isso que a sintaxe do código em um efeito parece muito semelhante ao código HLSL (há algumas exceções que serão tratadas posteriormente).</span><span class="sxs-lookup"><span data-stu-id="beeb2-107">This is why the syntax for code in an effect looks very much like HLSL code (there are a few exceptions that will be handled later).</span></span> <span data-ttu-id="beeb2-108">A propósito, o compilador compilador/HLSL (fxc.exe) está no SDK na pasta Utilitários para que você possa compilar seus sombreadores (ou efeitos) offline se escolher.</span><span class="sxs-lookup"><span data-stu-id="beeb2-108">By the way, the effect compiler/hlsl compiler (fxc.exe) is in the SDK in the utilities folder so that you can compile your shaders (or effects) offline if you choose.</span></span> <span data-ttu-id="beeb2-109">Consulte a documentação para executar o compilador na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="beeb2-109">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="beeb2-110">Incluir</span><span class="sxs-lookup"><span data-stu-id="beeb2-110">Includes</span></span>](#includes)
-   [<span data-ttu-id="beeb2-111">Macros</span><span class="sxs-lookup"><span data-stu-id="beeb2-111">Macros</span></span>](#macros)
-   [<span data-ttu-id="beeb2-112">Sinalizadores do sombreador HLSL</span><span class="sxs-lookup"><span data-stu-id="beeb2-112">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="beeb2-113">Sinalizadores FX</span><span class="sxs-lookup"><span data-stu-id="beeb2-113">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="beeb2-114">Verificando erros</span><span class="sxs-lookup"><span data-stu-id="beeb2-114">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="beeb2-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="beeb2-115">Related topics</span></span>](#related-topics)

<span data-ttu-id="beeb2-116">Aqui está um exemplo de compilação de um arquivo de efeito (do exemplo BasicHLSL10).</span><span class="sxs-lookup"><span data-stu-id="beeb2-116">Here's an example of compiling an effect file (from the BasicHLSL10 sample).</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a><span data-ttu-id="beeb2-117">Includes</span><span class="sxs-lookup"><span data-stu-id="beeb2-117">Includes</span></span>

<span data-ttu-id="beeb2-118">Um parâmetro é uma interface de inclusão.</span><span class="sxs-lookup"><span data-stu-id="beeb2-118">One parameter is an include interface.</span></span> <span data-ttu-id="beeb2-119">Gere um deles se desejar incluir um comportamento personalizado ao ler um arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="beeb2-119">Generate one of these if you want to include a customized behavior when reading an include file.</span></span> <span data-ttu-id="beeb2-120">Esse comportamento personalizado é executado cada vez que um efeito (que usa o ponteiro include) é criado ou quando um efeito (que usa o ponteiro include) é compilado.</span><span class="sxs-lookup"><span data-stu-id="beeb2-120">This custom behavior is executed each time an effect (that uses the include pointer) is created or when an effect (that uses the include pointer) is compiled.</span></span> <span data-ttu-id="beeb2-121">Para implementar o comportamento de inclusão personalizado, derive uma classe da interface include.</span><span class="sxs-lookup"><span data-stu-id="beeb2-121">To implement customized include behavior, derive a class from the Include interface.</span></span> <span data-ttu-id="beeb2-122">Isso fornece a classe dois métodos: abrir e fechar.</span><span class="sxs-lookup"><span data-stu-id="beeb2-122">This provides your class two methods: Open and Close.</span></span> <span data-ttu-id="beeb2-123">Implemente o comportamento personalizado nos métodos Open e Close.</span><span class="sxs-lookup"><span data-stu-id="beeb2-123">Implement the custom behavior in the Open and Close methods.</span></span>

## <a name="macros"></a><span data-ttu-id="beeb2-124">Macros</span><span class="sxs-lookup"><span data-stu-id="beeb2-124">Macros</span></span>

<span data-ttu-id="beeb2-125">A compilação de efeito também pode usar um ponteiro para macros definidas em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="beeb2-125">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="beeb2-126">Por exemplo, suponha que você modificasse o efeito em BasicHLSL10, para usar duas macros: zero e uma.</span><span class="sxs-lookup"><span data-stu-id="beeb2-126">For example, suppose you were to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="beeb2-127">O código de efeito que usa as duas macros é mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="beeb2-127">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="beeb2-128">Aqui está a declaração para as duas macros.</span><span class="sxs-lookup"><span data-stu-id="beeb2-128">Here is the declaration for the two macros.</span></span>


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="beeb2-129">As macros são uma matriz terminada em nulo de macros; em que cada macro é definida com um struct de [**\_ \_ macro do sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .</span><span class="sxs-lookup"><span data-stu-id="beeb2-129">The macros are a NULL terminated array of macros; where each macro is defined with a [**D3D\_SHADER\_MACRO**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="beeb2-130">Por fim, modifique a chamada de efeito de compilação para obter um ponteiro para as macros.</span><span class="sxs-lookup"><span data-stu-id="beeb2-130">Lastly, modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="beeb2-131">Sinalizadores do sombreador HLSL</span><span class="sxs-lookup"><span data-stu-id="beeb2-131">HLSL Shader Flags</span></span>

<span data-ttu-id="beeb2-132">Sinalizadores de sombreador especificam restrições de sombreador para o compilador HLSL.</span><span class="sxs-lookup"><span data-stu-id="beeb2-132">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="beeb2-133">Esses sinalizadores afetam o código gerado pelo compilador do sombreador, incluindo:</span><span class="sxs-lookup"><span data-stu-id="beeb2-133">These flags impact the code generated by the shader compiler including:</span></span>

-   <span data-ttu-id="beeb2-134">Considerações de tamanho: Otimize o código.</span><span class="sxs-lookup"><span data-stu-id="beeb2-134">Size considerations: optimize the code.</span></span>
-   <span data-ttu-id="beeb2-135">Considerações de depuração: incluindo informações de depuração, impedindo o controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="beeb2-135">Debug considerations: including debug information, preventing flow control.</span></span>
-   <span data-ttu-id="beeb2-136">Considerações sobre hardware: o destino de compilação e se um sombreador pode ou não ser executado em hardware herdado.</span><span class="sxs-lookup"><span data-stu-id="beeb2-136">Hardware considerations: the compile target and whether or not a shader can run on legacy hardware.</span></span>

<span data-ttu-id="beeb2-137">Em geral, esses sinalizadores podem ser combinados logicamente, supondo que você não tenha especificado duas características conflitantes.</span><span class="sxs-lookup"><span data-stu-id="beeb2-137">In general, these flags can be logically combined, assuming you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="beeb2-138">Para obter uma lista dos sinalizadores, consulte [constantes de efeito (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="beeb2-138">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="beeb2-139">Sinalizadores FX</span><span class="sxs-lookup"><span data-stu-id="beeb2-139">FX Flags</span></span>

<span data-ttu-id="beeb2-140">Esses sinalizadores são usados ao criar um efeito para definir o comportamento de compilação ou o comportamento de efeito de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="beeb2-140">These flags used when creating an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="beeb2-141">Para obter uma lista dos sinalizadores, consulte [constantes de efeito (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span><span class="sxs-lookup"><span data-stu-id="beeb2-141">For a listing of the flags see [Effect Constants (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="beeb2-142">Verificando erros</span><span class="sxs-lookup"><span data-stu-id="beeb2-142">Checking Errors</span></span>

<span data-ttu-id="beeb2-143">Se durante a compilação, ocorre um erro, a API retorna uma interface que contém os erros retornados do compilador de efeito.</span><span class="sxs-lookup"><span data-stu-id="beeb2-143">If during compilation, an error occurs, the API returns an interface which contains the errors returned from the effect compiler.</span></span> <span data-ttu-id="beeb2-144">Essa interface é chamada de ID3D10Blob.</span><span class="sxs-lookup"><span data-stu-id="beeb2-144">This interface is called ID3D10Blob.</span></span> <span data-ttu-id="beeb2-145">No entanto, ele não é legível diretamente, retornando um ponteiro para o buffer que contém os dados (que é uma cadeia de caracteres), você pode ver quaisquer erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="beeb2-145">It is not directly readable, however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="beeb2-146">Neste exemplo, um erro foi introduzido no efeito BasicHLSL. FX copiando a primeira declaração de variável duas vezes.</span><span class="sxs-lookup"><span data-stu-id="beeb2-146">In this example, an error was introduced into the BasicHLSL.fx effect by copying the first variable declaration twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="beeb2-147">Esse erro fez com que o compilador retornasse o seguinte erro, conforme mostrado na captura de tela a seguir da janela Watch no Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="beeb2-147">This error caused the compiler to return the following error, as shown in the following screen shot of the watch window in Microsoft Visual Studio.</span></span>

![captura de tela da janela de inspeção do Visual Studio](images/effect-compile-errors-2.jpg)

<span data-ttu-id="beeb2-149&quot;>Como o erro é retornado em um ponteiro LPVOID, converta-o em uma cadeia de caracteres na janela Watch.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;beeb2-149&quot;>Since the error is returned in a LPVOID pointer, cast it to a character string in the watch window.</span></span>

<span data-ttu-id=&quot;beeb2-150&quot;>Aqui está o código usado para retornar o erro da compilação com falha.</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;beeb2-150&quot;>Here is the code used to return the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L&quot;BasicHLSL10.fx" );
hr = D3DX10CompileEffectFromFile( str, NULL, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors );

LPVOID l_pError = NULL;
if( l_pBlob_Errors )
{
    l_pError = l_pBlob_Errors->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="beeb2-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="beeb2-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beeb2-152">Renderizando um efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="beeb2-152">Rendering an Effect (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



