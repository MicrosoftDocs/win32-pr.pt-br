---
title: Empacotando uma biblioteca de sombreador
description: Aqui, mostramos como compilar o código do sombreador, carregar o código compilado em uma biblioteca de sombreador e associar recursos dos slots de origem aos slots de destino.
ms.assetid: ED2EB1DE-3C25-4633-BFA7-C535ABBBAD28
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90124ca9753a390b924d5ba702e1986e32eee9e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988702"
---
# <a name="packaging-a-shader-library"></a>Empacotando uma biblioteca de sombreador

Aqui, mostramos como compilar o código do sombreador, carregar o código compilado em uma biblioteca de sombreador e associar recursos dos slots de origem aos slots de destino.

**Objetivo:** Para empacotar uma biblioteca de sombreador a ser usada para vinculação de sombreador.

## <a name="prerequisites"></a>Pré-requisitos

Partimos do princípio de que você conhece C++. Você também precisa ter experiência básica com conceitos de programação de elementos gráficos.

**Tempo para concluir:** 30 minutos.

## <a name="instructions"></a>Instruções

### <a name="1-compiling-your-shader-code"></a>1. compilando o código do sombreador

Compile o código do sombreador com uma das funções de compilação. Por exemplo, esse trecho de código usa [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile).

```cpp
    string source;
 
    ComPtr<ID3DBlob> codeBlob;
    ComPtr<ID3DBlob> errorBlob;
    HRESULT hr = D3DCompile(
        source.c_str(),
        source.size(),
        "ShaderModule",
        NULL,
        NULL,
        NULL,
        ("lib" + m_shaderModelSuffix).c_str(),
        D3DCOMPILE_OPTIMIZATION_LEVEL3,
        0,
        &codeBlob,
        &errorBlob
        );
```

A cadeia de caracteres de origem contém o código HLSL ASCII não compilado.

### <a name="2-load-the-compiled-code-into-a-shader-library"></a>2. Carregue o código compilado em uma biblioteca de sombreador.

Chame a função [**D3DLoadModule**](/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule) para carregar o código compilado ([**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85))) em um módulo ([**ID3D11Module**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module)) que representa uma biblioteca de sombreador.


```C++
    // Load the compiled library code into a module object.
    ComPtr<ID3D11Module> shaderLibrary;
    DX::ThrowIfFailed(D3DLoadModule(codeBlob->GetBufferPointer(), codeBlob->GetBufferSize(), &shaderLibrary));
```



### <a name="3-bind-resources-from-source-slots-to-destination-slots"></a>3. associar recursos dos slots de origem aos slots de destino.

Chame o método [**ID3D11Module:: CreateInstance**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11module-createinstance) para criar uma instância ([**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance)) da biblioteca para que você possa definir as associações de recurso para a instância.

Chame os métodos BIND de [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance) para associar os recursos necessários dos slots de origem aos slots de destino. Os recursos podem ser texturas, buffers, amostras, buffers de constantes ou UAVs. Normalmente, você usará os mesmos slots que a biblioteca de origem.


```C++
    // Create an instance of the library and define resource bindings for it.
    // In this sample we use the same slots as the source library however this is not required.
    ComPtr<ID3D11ModuleInstance> shaderLibraryInstance;
    DX::ThrowIfFailed(shaderLibrary->CreateInstance("", &shaderLibraryInstance));
    // HRESULTs for Bind methods are intentionally ignored as compiler optimizations may eliminate the source
    // bindings. In these cases, the Bind operation will fail, but the final shader will function normally.
    shaderLibraryInstance->BindResource(0, 0, 1);
    shaderLibraryInstance->BindSampler(0, 0, 1);
    shaderLibraryInstance->BindConstantBuffer(0, 0, 0);
    shaderLibraryInstance->BindConstantBuffer(1, 1, 0);
    shaderLibraryInstance->BindConstantBuffer(2, 2, 0);
```



Esse código HLSL mostra que a biblioteca de origem usa os mesmos slots (T0, S0, B0, B1 e B2) como os slots usados nos métodos de ligação anteriores de [**ID3D11ModuleInstance**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11moduleinstance).

``` syntax
// This is the default code in the fixed header section.
Texture2D<float3> Texture : register(t0);
SamplerState Anisotropic : register(s0);
cbuffer CameraData : register(b0)
{
    float4x4 Model;
    float4x4 View;
    float4x4 Projection;
};
cbuffer TimeVariantSignals : register(b1)
{
    float SineWave;
    float SquareWave;
    float TriangleWave;
    float SawtoothWave;
};

// This code is not displayed, but is used as part of the linking process.
cbuffer HiddenBuffer : register(b2)
{
    float3 LightDirection;
};
```

## <a name="summary-and-next-steps"></a>Resumo e próximas etapas

Compilamos o código do sombreador, carregamos o código compilado em uma biblioteca de sombreador e os recursos associados dos slots de origem para os slots de destino.

Em seguida, construímos o function-link-Grafs (FLGs) para sombreadores, os vinculamos ao código compilado e geram blobs de sombreador que o tempo de execução do Direct3D pode usar.

[Construindo um grafo de vinculação de função e vinculá-lo ao código compilado](constructing-a-function-linking-graph.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando vinculação de sombreador](using-shader-linking.md)
</dt> </dl>

 

 