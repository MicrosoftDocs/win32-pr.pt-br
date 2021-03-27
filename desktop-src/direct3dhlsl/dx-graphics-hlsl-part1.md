---
title: Compilar um sombreador
description: Agora, vamos examinar várias maneiras de compilar o código do sombreador e as convenções de extensões de arquivo para o código do sombreador.
ms.assetid: a4e6b7cd-c5cc-4165-ba73-205155e449c9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3ea71da99dd68769324b07d3fc76a0c5ca00009d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294190"
---
# <a name="compiling-shaders"></a>Compilando sombreadores

> [!NOTE]
> Este tópico aborda o `FXC.EXE` compilador usado para os modelos de sombreador 2 a 5,1. Para o Shader Model 6, você usa `DXC.EXE` em vez disso, que está documentado em [usando dxc.exe e dxcompiler.dll](https://github.com/microsoft/DirectXShaderCompiler/wiki/Using-dxc.exe-and-dxcompiler.dll).

Microsoft Visual Studio 2012 agora pode compilar o código do sombreador de \* arquivos. HLSL que você inclui em seu projeto C++.

Como parte do processo de compilação, o Visual Studio 2012 usa o compilador de código [fxc.exe](/windows/desktop/direct3dtools/fxc) HLSL para compilar os arquivos. HLSL em arquivos de objeto de sombreador binário ou em matrizes de bytes que são definidas em arquivos de cabeçalho. Como o compilador de código HLSL compila cada arquivo. HLSL em seu projeto depende de como você especifica a propriedade de **arquivos de saída** para esse arquivo. Para obter mais informações sobre páginas de propriedades do HLSL, consulte [páginas de propriedades do HLSL](/previous-versions/visualstudio/visual-studio-2012/jj620902(v=vs.110)).

O método de compilação que você usa normalmente depende do tamanho do seu \* arquivo. HLSL. Se você incluir uma grande quantidade de código de byte em um cabeçalho, aumentará o tamanho e o tempo de carregamento inicial do seu aplicativo. Você também força todo o código de byte a residir na memória mesmo depois que o sombreador é criado, o que desperdiça recursos. Mas quando você inclui um código de byte em um cabeçalho, pode reduzir a complexidade do código e simplificar a criação do sombreador.

Agora, vamos examinar várias maneiras de compilar o código do sombreador e as convenções de extensões de arquivo para o código do sombreador.

-   [Usando extensões de arquivo de código do sombreador](#using-shader-code-file-extensions)
-   [Compilando no momento da compilação para arquivos de objeto](#compiling-at-build-time-to-object-files)
-   [Compilando no momento da compilação para arquivos de cabeçalho](#compiling-at-build-time-to-header-files)
-   [Compilando com D3DCompileFromFile](#compiling-with-d3dcompilefromfile)
-   [Tópicos relacionados](#related-topics)
-   [Tópicos relacionados](#related-topics)

## <a name="using-shader-code-file-extensions"></a>Usando extensões de arquivo de código do sombreador

Para estar de acordo com a Convenção da Microsoft, use estas extensões de arquivo para o código do sombreador:

-   Um arquivo com a extensão. HLSL contém código-fonte de[HLSL](dx-graphics-hlsl-reference.md)(linguagem de sombreamento de alto nível).
-   Um arquivo com a extensão .cso contém um objeto de sombreador compilado.
-   Um arquivo com a extensão .h é um arquivo de cabeçalho, mas, em um contexto de código de sombreador, esse arquivo de cabeçalho define uma matriz de bytes que contém dados de sombreador.

## <a name="compiling-at-build-time-to-object-files"></a>Compilando no momento da compilação para arquivos de objeto

Se você compilar seus arquivos. HLSL em arquivos de objeto de sombreador binário, seu aplicativo precisará ler os dados desses arquivos de objeto (. CSO é a extensão padrão para esses arquivos de objeto), atribuir os dados a matrizes de bytes e criar objetos de sombreador a partir dessas matrizes de bytes. Por exemplo, para criar um sombreador de vértice ([**ID3D11VertexShader**](/windows/desktop/api/d3d11/nn-d3d11-id3d11vertexshader) \* \* ), chame o método [**ID3D11Device:: CreateVertexShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createvertexshader) com uma matriz de bytes que contém o código de byte do sombreador de vértices compilado. O [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample) mostra como criar objetos de sombreador a partir de matrizes de bytes que ele obteve de arquivos de objeto de sombreador binário. cso. Neste exemplo de código do [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample), a propriedade arquivos de **saída** do arquivo SimpleVertexShader. HLSL especifica a compilação no arquivo de objeto SimpleVertexShader. cso.

```cpp
        auto vertexShaderBytecode = reader->ReadData("SimpleVertexShader.cso");
        ComPtr<ID3D11VertexShader> vertexShader;
        DX::ThrowIfFailed(
            m_d3dDevice->CreateVertexShader(
                vertexShaderBytecode->Data,
                vertexShaderBytecode->Length,
                nullptr,
                &vertexShader
                )
```

## <a name="compiling-at-build-time-to-header-files"></a>Compilando no momento da compilação para arquivos de cabeçalho

Se você compilar seus arquivos. HLSL em matrizes de bytes definidas em arquivos de cabeçalho, precisará incluir esses arquivos de cabeçalho em seu código. O [exemplo de extensões de mídia](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample) mostra como criar objetos de sombreador a partir de matrizes de bytes que são definidas em arquivos de cabeçalho e que você inclui em seu projeto no momento da compilação. Neste exemplo de código do [exemplo de extensões de mídia](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Media%20extensions%20sample), a propriedade arquivos de **saída** para o arquivo PixelShader. HLSL especifica a compilação na matriz de bytes *g \_ psshader* que é definida no arquivo de cabeçalho PixelShader. h.


```C++
#       include "PixelShader.h"
        ComPtr<ID3D11PixelShader> m_pPixelShader;
        hr = pDevice->CreatePixelShader(g_psshader, sizeof(g_psshader), nullptr, &m_pPixelShader);
```



## <a name="compiling-with-d3dcompilefromfile"></a>Compilando com D3DCompileFromFile

Você também pode usar a função [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) em tempo de execução para compilar o código do sombreador. Para obter mais informações sobre como fazer isso, consulte [como compilar um sombreador](/windows/desktop/direct3d11/how-to--compile-a-shader).

> [!Note]  
> Os aplicativos da Windows Store dão suporte ao uso do [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) para desenvolvimento, mas não para implantação.

 

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 