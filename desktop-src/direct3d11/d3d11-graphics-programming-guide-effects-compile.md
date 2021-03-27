---
title: Compilar um efeito (Direct3D 11)
description: Após a criação de um efeito, a próxima etapa é compilar o código para verificar se há problemas de sintaxe.
ms.assetid: 7624d55e-6466-4156-8f31-30f0d25a2883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3df304a7b657af19984008bd90a1be4bfe5219c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917421"
---
# <a name="compile-an-effect-direct3d-11"></a><span data-ttu-id="71b33-103">Compilar um efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="71b33-103">Compile an Effect (Direct3D 11)</span></span>

<span data-ttu-id="71b33-104">Após a criação de um efeito, a próxima etapa é compilar o código para verificar se há problemas de sintaxe.</span><span class="sxs-lookup"><span data-stu-id="71b33-104">After an effect has been authored, the next step is to compile the code to check for syntax problems.</span></span>

<span data-ttu-id="71b33-105">Você faz isso chamando uma das APIs de compilação ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)ou [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span><span class="sxs-lookup"><span data-stu-id="71b33-105">You do so by calling one of the compile APIs ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md), or [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ).</span></span> <span data-ttu-id="71b33-106">Essas APIs invocam o fxc.exe do compilador de efeito, que compila o código HLSL.</span><span class="sxs-lookup"><span data-stu-id="71b33-106">These APIs invoke the effect compiler fxc.exe, which compiles HLSL code.</span></span> <span data-ttu-id="71b33-107">É por isso que a sintaxe do código em um efeito parece muito parecida com o código HLSL.</span><span class="sxs-lookup"><span data-stu-id="71b33-107">This is why the syntax for code in an effect looks very much like HLSL code.</span></span> <span data-ttu-id="71b33-108">(Há algumas exceções que serão tratadas posteriormente).</span><span class="sxs-lookup"><span data-stu-id="71b33-108">(There are a few exceptions that will be handled later).</span></span> <span data-ttu-id="71b33-109">O compilador compiler/HLSL do compilador, fxc.exe, está disponível no SDK na pasta Utilities para que os sombreadores (ou efeitos) possam ser compilados offline se você escolher.</span><span class="sxs-lookup"><span data-stu-id="71b33-109">The effect compiler/hlsl compiler, fxc.exe, is available in the SDK in the utilities folder so that shaders (or effects) can be compiled offline if you choose.</span></span> <span data-ttu-id="71b33-110">Consulte a documentação para executar o compilador na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="71b33-110">See the documentation for running the compiler from the command line.</span></span>

-   [<span data-ttu-id="71b33-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="71b33-111">Example</span></span>](#example)
-   [<span data-ttu-id="71b33-112">Incluir</span><span class="sxs-lookup"><span data-stu-id="71b33-112">Includes</span></span>](#includes)
-   [<span data-ttu-id="71b33-113">Procurando arquivos de inclusão</span><span class="sxs-lookup"><span data-stu-id="71b33-113">Searching for Include Files</span></span>](#searching-for-include-files)
-   [<span data-ttu-id="71b33-114">Macros</span><span class="sxs-lookup"><span data-stu-id="71b33-114">Macros</span></span>](#macros)
-   [<span data-ttu-id="71b33-115">Sinalizadores do sombreador HLSL</span><span class="sxs-lookup"><span data-stu-id="71b33-115">HLSL Shader Flags</span></span>](#hlsl-shader-flags)
-   [<span data-ttu-id="71b33-116">Sinalizadores FX</span><span class="sxs-lookup"><span data-stu-id="71b33-116">FX Flags</span></span>](#fx-flags)
-   [<span data-ttu-id="71b33-117">Verificando erros</span><span class="sxs-lookup"><span data-stu-id="71b33-117">Checking Errors</span></span>](#checking-errors)
-   [<span data-ttu-id="71b33-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71b33-118">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="71b33-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="71b33-119">Example</span></span>

<span data-ttu-id="71b33-120">Aqui está um exemplo de compilação de um arquivo de efeito.</span><span class="sxs-lookup"><span data-stu-id="71b33-120">Here's an example of compiling an effect file.</span></span>


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a><span data-ttu-id="71b33-121">Includes</span><span class="sxs-lookup"><span data-stu-id="71b33-121">Includes</span></span>

<span data-ttu-id="71b33-122">Um parâmetro das APIs de compilação é uma interface de inclusão.</span><span class="sxs-lookup"><span data-stu-id="71b33-122">One parameter of the compile APIs is an include interface.</span></span> <span data-ttu-id="71b33-123">Gere um deles se você quiser incluir um comportamento personalizado quando o compilador ler um arquivo de inclusão.</span><span class="sxs-lookup"><span data-stu-id="71b33-123">Generate one of these if you want to include a customized behavior when the compiler reads an include file.</span></span> <span data-ttu-id="71b33-124">O compilador executa esse comportamento personalizado toda vez que cria ou compila um efeito (que usa o ponteiro de inclusão).</span><span class="sxs-lookup"><span data-stu-id="71b33-124">The compiler executes this custom behavior each time it creates or compiles an effect (that uses the include pointer).</span></span> <span data-ttu-id="71b33-125">Para implementar o comportamento de inclusão personalizado, derive uma classe da interface [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) .</span><span class="sxs-lookup"><span data-stu-id="71b33-125">To implement customized include behavior, derive a class from the [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) interface.</span></span> <span data-ttu-id="71b33-126">Isso fornece à sua classe dois métodos: [**abrir**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) e [**fechar**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span><span class="sxs-lookup"><span data-stu-id="71b33-126">This provides your class with two methods: [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) and [**Close**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close).</span></span> <span data-ttu-id="71b33-127">Implemente o comportamento personalizado nesses métodos.</span><span class="sxs-lookup"><span data-stu-id="71b33-127">Implement the custom behavior in these methods.</span></span>

## <a name="searching-for-include-files"></a><span data-ttu-id="71b33-128">Procurando arquivos de inclusão</span><span class="sxs-lookup"><span data-stu-id="71b33-128">Searching for Include Files</span></span>

<span data-ttu-id="71b33-129">O ponteiro que o compilador passa no parâmetro *pParentData* para o método [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) do manipulador de inclusão pode não apontar para o contêiner que inclui o \# arquivo de inclusão que o compilador precisa para compilar o código do sombreador.</span><span class="sxs-lookup"><span data-stu-id="71b33-129">The pointer that the compiler passes in the *pParentData* parameter to your include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method might not point to the container that includes the \#include file that the compiler needs to compile your shader code.</span></span> <span data-ttu-id="71b33-130">Ou seja, o compilador pode passar **nulo** em *pParentData*.</span><span class="sxs-lookup"><span data-stu-id="71b33-130">That is, the compiler might pass **NULL** in *pParentData*.</span></span> <span data-ttu-id="71b33-131">Portanto, recomendamos que seu manipulador de inclusão pesquise sua própria lista de locais de inclusão de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="71b33-131">Therefore, we recommend that your include handler search its own list of include locations for content.</span></span> <span data-ttu-id="71b33-132">O manipulador de inclusão pode adicionar dinamicamente novos locais de inclusão à medida que recebe esses locais em chamadas para seu método **Open** .</span><span class="sxs-lookup"><span data-stu-id="71b33-132">Your include handler can dynamically add new include locations as it receives those locations in calls to its **Open** method.</span></span>

<span data-ttu-id="71b33-133">No exemplo a seguir, suponha que os arquivos de inclusão do código de sombreador sejam ambos armazenados no diretório *somewhereelse*</span><span class="sxs-lookup"><span data-stu-id="71b33-133">In the following example, suppose that the shader code's include files are both stored in the *somewhereelse* directory.</span></span> <span data-ttu-id="71b33-134">Quando o compilador chama o método [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) do manipulador include para abrir e ler o conteúdo de *somewhereelse \\ foo. h*, o manipulador de inclusão pode salvar o local do diretório **somewhereelse** .</span><span class="sxs-lookup"><span data-stu-id="71b33-134">When the compiler calls the include handler's [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) method to open and read the contents of *somewhereelse\\foo.h*, the include handler can save the location of the **somewhereelse** directory.</span></span> <span data-ttu-id="71b33-135">Posteriormente, quando o compilador chama o método **Open** do manipulador include para abrir e ler o conteúdo de *bar. h*, o manipulador include pode Pesquisar automaticamente no diretório *somewhereelse* para *bar. h*.</span><span class="sxs-lookup"><span data-stu-id="71b33-135">Later, when the compiler calls the include handler's **Open** method to open and read the contents of *bar.h*, the include handler can automatically search in the *somewhereelse* directory for *bar.h*.</span></span>


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a><span data-ttu-id="71b33-136">Macros</span><span class="sxs-lookup"><span data-stu-id="71b33-136">Macros</span></span>

<span data-ttu-id="71b33-137">A compilação de efeito também pode usar um ponteiro para macros definidas em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="71b33-137">Effect compilation can also take a pointer to macros that are defined elsewhere.</span></span> <span data-ttu-id="71b33-138">Por exemplo, suponha que você queira modificar o efeito em BasicHLSL10, para usar duas macros: zero e uma.</span><span class="sxs-lookup"><span data-stu-id="71b33-138">For example, suppose you want to modify the effect in BasicHLSL10, to use two macros: zero and one.</span></span> <span data-ttu-id="71b33-139">O código de efeito que usa as duas macros é mostrado aqui.</span><span class="sxs-lookup"><span data-stu-id="71b33-139">The effect code that uses the two macros is shown here.</span></span>


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



<span data-ttu-id="71b33-140">Aqui está a declaração para as duas macros.</span><span class="sxs-lookup"><span data-stu-id="71b33-140">Here is the declaration for the two macros.</span></span>


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



<span data-ttu-id="71b33-141">As macros são uma matriz de macros terminada em nulo; em que cada macro é definida usando uma struct de [**\_ \_ macro do sombreador d3d10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .</span><span class="sxs-lookup"><span data-stu-id="71b33-141">The macros are a NULL-terminated array of macros; where each macro is defined by using a [**D3D10\_SHADER\_MACRO**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) struct.</span></span>

<span data-ttu-id="71b33-142">Modifique a chamada de efeito de compilação para obter um ponteiro para as macros.</span><span class="sxs-lookup"><span data-stu-id="71b33-142">Modify the compile effect call to take a pointer to the macros.</span></span>


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a><span data-ttu-id="71b33-143">Sinalizadores do sombreador HLSL</span><span class="sxs-lookup"><span data-stu-id="71b33-143">HLSL Shader Flags</span></span>

<span data-ttu-id="71b33-144">Sinalizadores de sombreador especificam restrições de sombreador para o compilador HLSL.</span><span class="sxs-lookup"><span data-stu-id="71b33-144">Shader flags specify shader constraints to the HLSL compiler.</span></span> <span data-ttu-id="71b33-145">Esses sinalizadores afetam o código gerado pelo compilador do sombreador das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="71b33-145">These flags affect the code generated by the shader compiler in the following ways:</span></span>

-   <span data-ttu-id="71b33-146">Otimize o tamanho do código.</span><span class="sxs-lookup"><span data-stu-id="71b33-146">Optimize the code size.</span></span>
-   <span data-ttu-id="71b33-147">Incluindo informações de depuração, que impedem o controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="71b33-147">Including debug information, which prevents flow control.</span></span>
-   <span data-ttu-id="71b33-148">Afeta o destino de compilação e se um sombreador pode ser executado em hardware herdado.</span><span class="sxs-lookup"><span data-stu-id="71b33-148">Affects the compile target and whether a shader can run on legacy hardware.</span></span>

<span data-ttu-id="71b33-149">Esses sinalizadores podem ser logicamente combinados se você não tiver especificado duas características conflitantes.</span><span class="sxs-lookup"><span data-stu-id="71b33-149">These flags can be logically combined if you have not specified two conflicting characteristics.</span></span> <span data-ttu-id="71b33-150">Para obter uma lista dos sinalizadores, [consulte \_ constantes do sombreador d3d10](/windows/desktop/direct3d10/d3d10-shader).</span><span class="sxs-lookup"><span data-stu-id="71b33-150">For a listing of the flags see [D3D10\_SHADER Constants](/windows/desktop/direct3d10/d3d10-shader).</span></span>

## <a name="fx-flags"></a><span data-ttu-id="71b33-151">Sinalizadores FX</span><span class="sxs-lookup"><span data-stu-id="71b33-151">FX Flags</span></span>

<span data-ttu-id="71b33-152">Use esses sinalizadores quando você criar um efeito para definir o comportamento de compilação ou o comportamento de efeito de tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="71b33-152">Use these flags when you create an effect to define either compilation behavior or runtime effect behavior.</span></span> <span data-ttu-id="71b33-153">Para obter uma lista dos sinalizadores, [consulte \_ constantes de efeito d3d10](/windows/desktop/direct3d10/d3d10-effect).</span><span class="sxs-lookup"><span data-stu-id="71b33-153">For a listing of the flags see [D3D10\_EFFECT Constants](/windows/desktop/direct3d10/d3d10-effect).</span></span>

## <a name="checking-errors"></a><span data-ttu-id="71b33-154">Verificando erros</span><span class="sxs-lookup"><span data-stu-id="71b33-154">Checking Errors</span></span>

<span data-ttu-id="71b33-155">Se, durante a compilação, ocorrer um erro, a API retornará uma interface que contém os erros do compilador de efeito.</span><span class="sxs-lookup"><span data-stu-id="71b33-155">If during compilation an error occurs, the API returns an interface that contains the errors from the effect compiler.</span></span> <span data-ttu-id="71b33-156">Essa interface é chamada de [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="71b33-156">This interface is called [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)).</span></span> <span data-ttu-id="71b33-157">Ele não é legível diretamente; no entanto, ao retornar um ponteiro para o buffer que contém os dados (que é uma cadeia de caracteres), você poderá ver os erros de compilação.</span><span class="sxs-lookup"><span data-stu-id="71b33-157">It is not directly readable; however, by returning a pointer to the buffer that contains the data (which is a string), you can see any compilation errors.</span></span>

<span data-ttu-id="71b33-158">Este exemplo contém um erro em BasicHLSL. FX, a primeira declaração de variável ocorre duas vezes.</span><span class="sxs-lookup"><span data-stu-id="71b33-158">This example contains an error in the BasicHLSL.fx, the first variable declaration occurs twice.</span></span>


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



<span data-ttu-id="71b33-159">Esse erro faz com que o compilador retorne o seguinte erro, conforme mostrado na captura de tela a seguir do janela Inspeção em Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="71b33-159">This error causes the compiler to return the following error, as shown in the following screen shot of the Watch window in Microsoft Visual Studio.</span></span>

![captura de tela da janela de inspeção do Visual Studio com um erro 0x01997fb8](images/effect-compile-errors-2.jpg)

<span data-ttu-id="71b33-161">Como o compilador retorna o erro em um ponteiro LPVOID, converta-o em uma cadeia de caracteres no janela Inspeção.</span><span class="sxs-lookup"><span data-stu-id="71b33-161">Because the compiler returns the error in a LPVOID pointer, cast it to a character string in the Watch window.</span></span>

<span data-ttu-id="71b33-162">Este é o código que retorna o erro da compilação com falha.</span><span class="sxs-lookup"><span data-stu-id="71b33-162">Here is the code that returns the error from the failed compile.</span></span>


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3DBlob*   l_pBlob_Effect = NULL;
ID3DBlob*   l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );      

LPVOID l_pError = NULL;
if( pErrorBlob )
{
    l_pError = pErrorBlob->GetBufferPointer();
    // then cast to a char* to see it in the locals window
}
```



## <a name="related-topics"></a><span data-ttu-id="71b33-163">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71b33-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71b33-164">Renderizando um efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="71b33-164">Rendering an Effect (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 