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
# <a name="compile-an-effect-direct3d-11"></a>Compilar um efeito (Direct3D 11)

Após a criação de um efeito, a próxima etapa é compilar o código para verificar se há problemas de sintaxe.

Você faz isso chamando uma das APIs de compilação ([**D3DX11CompileFromFile**](d3dx11compilefromfile.md), [**D3DX11CompileFromMemory**](d3dx11compilefrommemory.md)ou [**D3DX11CompileFromResource**](d3dx11compilefromresource.md) ). Essas APIs invocam o fxc.exe do compilador de efeito, que compila o código HLSL. É por isso que a sintaxe do código em um efeito parece muito parecida com o código HLSL. (Há algumas exceções que serão tratadas posteriormente). O compilador compiler/HLSL do compilador, fxc.exe, está disponível no SDK na pasta Utilities para que os sombreadores (ou efeitos) possam ser compilados offline se você escolher. Consulte a documentação para executar o compilador na linha de comando.

-   [Exemplo](#example)
-   [Incluir](#includes)
-   [Procurando arquivos de inclusão](#searching-for-include-files)
-   [Macros](#macros)
-   [Sinalizadores do sombreador HLSL](#hlsl-shader-flags)
-   [Sinalizadores FX](#fx-flags)
-   [Verificando erros](#checking-errors)
-   [Tópicos relacionados](#related-topics)

## <a name="example"></a>Exemplo

Aqui está um exemplo de compilação de um arquivo de efeito.


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX11CompileFromFile( str, NULL, NULL, pFunctionName, pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, NULL, &pBlob, &pErrorBlob, NULL );
```



## <a name="includes"></a>Includes

Um parâmetro das APIs de compilação é uma interface de inclusão. Gere um deles se você quiser incluir um comportamento personalizado quando o compilador ler um arquivo de inclusão. O compilador executa esse comportamento personalizado toda vez que cria ou compila um efeito (que usa o ponteiro de inclusão). Para implementar o comportamento de inclusão personalizado, derive uma classe da interface [**ID3DInclude**](/windows/desktop/api/D3Dcommon/nn-d3dcommon-id3dinclude) . Isso fornece à sua classe dois métodos: [**abrir**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) e [**fechar**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-close). Implemente o comportamento personalizado nesses métodos.

## <a name="searching-for-include-files"></a>Procurando arquivos de inclusão

O ponteiro que o compilador passa no parâmetro *pParentData* para o método [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) do manipulador de inclusão pode não apontar para o contêiner que inclui o \# arquivo de inclusão que o compilador precisa para compilar o código do sombreador. Ou seja, o compilador pode passar **nulo** em *pParentData*. Portanto, recomendamos que seu manipulador de inclusão pesquise sua própria lista de locais de inclusão de conteúdo. O manipulador de inclusão pode adicionar dinamicamente novos locais de inclusão à medida que recebe esses locais em chamadas para seu método **Open** .

No exemplo a seguir, suponha que os arquivos de inclusão do código de sombreador sejam ambos armazenados no diretório *somewhereelse* Quando o compilador chama o método [**Open**](/windows/desktop/api/D3DCommon/nf-d3dcommon-id3dinclude-open) do manipulador include para abrir e ler o conteúdo de *somewhereelse \\ foo. h*, o manipulador de inclusão pode salvar o local do diretório **somewhereelse** . Posteriormente, quando o compilador chama o método **Open** do manipulador include para abrir e ler o conteúdo de *bar. h*, o manipulador include pode Pesquisar automaticamente no diretório *somewhereelse* para *bar. h*.


```
Main.hlsl:
#include "somewhereelse\foo.h"

Foo.h:
#include "bar.h"
```



## <a name="macros"></a>Macros

A compilação de efeito também pode usar um ponteiro para macros definidas em outro lugar. Por exemplo, suponha que você queira modificar o efeito em BasicHLSL10, para usar duas macros: zero e uma. O código de efeito que usa as duas macros é mostrado aqui.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Aqui está a declaração para as duas macros.


```
D3D10_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



As macros são uma matriz de macros terminada em nulo; em que cada macro é definida usando uma struct de [**\_ \_ macro do sombreador d3d10**](/windows/desktop/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .

Modifique a chamada de efeito de compilação para obter um ponteiro para as macros.


```
D3DX11CompileFromFile( str, Shader_Macros, NULL, pFunctionName, 
                       pProfile, D3D10_SHADER_ENABLE_STRICTNESS, NULL, 
                       NULL, &pBlob, &pErrorBlob, NULL );    
```



## <a name="hlsl-shader-flags"></a>Sinalizadores do sombreador HLSL

Sinalizadores de sombreador especificam restrições de sombreador para o compilador HLSL. Esses sinalizadores afetam o código gerado pelo compilador do sombreador das seguintes maneiras:

-   Otimize o tamanho do código.
-   Incluindo informações de depuração, que impedem o controle de fluxo.
-   Afeta o destino de compilação e se um sombreador pode ser executado em hardware herdado.

Esses sinalizadores podem ser logicamente combinados se você não tiver especificado duas características conflitantes. Para obter uma lista dos sinalizadores, [consulte \_ constantes do sombreador d3d10](/windows/desktop/direct3d10/d3d10-shader).

## <a name="fx-flags"></a>Sinalizadores FX

Use esses sinalizadores quando você criar um efeito para definir o comportamento de compilação ou o comportamento de efeito de tempo de execução. Para obter uma lista dos sinalizadores, [consulte \_ constantes de efeito d3d10](/windows/desktop/direct3d10/d3d10-effect).

## <a name="checking-errors"></a>Verificando erros

Se, durante a compilação, ocorrer um erro, a API retornará uma interface que contém os erros do compilador de efeito. Essa interface é chamada de [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)). Ele não é legível diretamente; no entanto, ao retornar um ponteiro para o buffer que contém os dados (que é uma cadeia de caracteres), você poderá ver os erros de compilação.

Este exemplo contém um erro em BasicHLSL. FX, a primeira declaração de variável ocorre duas vezes.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Esse erro faz com que o compilador retorne o seguinte erro, conforme mostrado na captura de tela a seguir do janela Inspeção em Microsoft Visual Studio.

![captura de tela da janela de inspeção do Visual Studio com um erro 0x01997fb8](images/effect-compile-errors-2.jpg)

Como o compilador retorna o erro em um ponteiro LPVOID, converta-o em uma cadeia de caracteres no janela Inspeção.

Este é o código que retorna o erro da compilação com falha.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizando um efeito (Direct3D 11)](d3d11-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 