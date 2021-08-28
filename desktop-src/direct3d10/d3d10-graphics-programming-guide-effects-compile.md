---
description: Depois que um efeito foi criado, a primeira etapa é compilar o código para verificar se há problemas de sintaxe.
ms.assetid: b8d8a0b7-b520-44e4-8691-6eb46202c092
title: Compilar um efeito (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e0c4364fab67b0e0e7c97b7478a023f6394b5515e6f1d16cf2d352172af6c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128419"
---
# <a name="compile-an-effect-direct3d-10"></a>Compilar um efeito (Direct3D 10)

Depois que um efeito foi criado, a primeira etapa é compilar o código para verificar se há problemas de sintaxe. Isso é feito chamando uma das APIs de compilação (como D3DX10CompileEffectFromFile, D3DX10CompileEffectFromResource, D3DX10CompileEffectFromMemory). Essas APIs invocam o compilador de efeito fxc.exe que é o compilador usado para compilar o código HLSL. É por isso que a sintaxe do código em um efeito parece muito semelhante ao código HLSL (há algumas exceções que serão tratadas posteriormente). A propósito, o compilador compilador/HLSL (fxc.exe) está no SDK na pasta Utilitários para que você possa compilar seus sombreadores (ou efeitos) offline se escolher. Consulte a documentação para executar o compilador na linha de comando.

-   [Incluir](#includes)
-   [Macros](#macros)
-   [Sinalizadores do sombreador HLSL](#hlsl-shader-flags)
-   [Sinalizadores FX](#fx-flags)
-   [Verificando erros](#checking-errors)
-   [Tópicos relacionados](#related-topics)

Aqui está um exemplo de compilação de um arquivo de efeito (do exemplo BasicHLSL10).


```
WCHAR str[MAX_PATH];
DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );

hr = D3DX10CompileEffectFromFile( str, NULL, NULL, "fx_4_0", 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &l_pBlob_Effect, &l_pBlob_Errors, NULL );
```



## <a name="includes"></a>Includes

Um parâmetro é uma interface de inclusão. Gere um deles se desejar incluir um comportamento personalizado ao ler um arquivo de inclusão. Esse comportamento personalizado é executado cada vez que um efeito (que usa o ponteiro include) é criado ou quando um efeito (que usa o ponteiro include) é compilado. Para implementar o comportamento de inclusão personalizado, derive uma classe da interface include. Isso fornece a classe dois métodos: abrir e fechar. Implemente o comportamento personalizado nos métodos Open e Close.

## <a name="macros"></a>Macros

A compilação de efeito também pode usar um ponteiro para macros definidas em outro lugar. Por exemplo, suponha que você modificasse o efeito em BasicHLSL10, para usar duas macros: zero e uma. O código de efeito que usa as duas macros é mostrado aqui.


```
if( bAnimate )
    vAnimatedPos += float4(vNormal, zero) *  
        (sin(g_fTime+5.5)+0.5)*5;
        
    Output.Diffuse.a = one;         
```



Aqui está a declaração para as duas macros.


```
D3D_SHADER_MACRO Shader_Macros[3] = { "zero", "0", "one", "1.0f", NULL, NULL };
```



As macros são uma matriz terminada em nulo de macros; em que cada macro é definida com um struct de [**\_ \_ macro do sombreador D3D**](/windows/win32/api/d3dcommon/ns-d3dcommon-d3d_shader_macro) .

Por fim, modifique a chamada de efeito de compilação para obter um ponteiro para as macros.


```
D3DX10CreateEffectFromFile( str, Shader_Macros, NULL, 
    D3D10_SHADER_ENABLE_STRICTNESS, 0, pd3dDevice, NULL, NULL, 
    &g_pEffect10, NULL );
```



## <a name="hlsl-shader-flags"></a>Sinalizadores do sombreador HLSL

Sinalizadores de sombreador especificam restrições de sombreador para o compilador HLSL. Esses sinalizadores afetam o código gerado pelo compilador do sombreador, incluindo:

-   Considerações de tamanho: Otimize o código.
-   Considerações de depuração: incluindo informações de depuração, impedindo o controle de fluxo.
-   Considerações sobre hardware: o destino de compilação e se um sombreador pode ou não ser executado em hardware herdado.

Em geral, esses sinalizadores podem ser combinados logicamente, supondo que você não tenha especificado duas características conflitantes. Para obter uma lista dos sinalizadores, consulte [constantes de efeito (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="fx-flags"></a>Sinalizadores FX

Esses sinalizadores são usados ao criar um efeito para definir o comportamento de compilação ou o comportamento de efeito de tempo de execução. Para obter uma lista dos sinalizadores, consulte [constantes de efeito (Direct3D 10)](d3d10-graphics-reference-effect-constants.md).

## <a name="checking-errors"></a>Verificando erros

Se durante a compilação, ocorre um erro, a API retorna uma interface que contém os erros retornados do compilador de efeito. Essa interface é chamada de ID3D10Blob. No entanto, ele não é legível diretamente, retornando um ponteiro para o buffer que contém os dados (que é uma cadeia de caracteres), você pode ver quaisquer erros de compilação.

Neste exemplo, um erro foi introduzido no efeito BasicHLSL. FX copiando a primeira declaração de variável duas vezes.


```
//-------------------------------------------------------------------
// Global variables
//-------------------------------------------------------------------
float4 g_MaterialAmbientColor;      // Material's ambient color

// Declare the same variable twice
float4 g_MaterialAmbientColor;      // Material's ambient color
```



Esse erro fez com que o compilador retornasse o seguinte erro, conforme mostrado na captura de tela a seguir da janela Watch no Microsoft Visual Studio.

![captura de tela da janela de inspeção do Visual Studio](images/effect-compile-errors-2.jpg)

Como o erro é retornado em um ponteiro LPVOID, converta-o em uma cadeia de caracteres na janela Watch.

Aqui está o código usado para retornar o erro da compilação com falha.


```
// Read the D3DX effect file
WCHAR str[MAX_PATH];
ID3D10Blob* l_pBlob_Effect = NULL;
ID3D10Blob* l_pBlob_Errors = NULL;
hr = DXUTFindDXSDKMediaFileCch( str, MAX_PATH, L"BasicHLSL10.fx" );
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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderizando um efeito (Direct3D 10)](d3d10-graphics-programming-guide-effects-render.md)
</dt> </dl>

 

 



