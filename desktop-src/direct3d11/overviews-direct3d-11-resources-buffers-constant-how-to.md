---
title: Como criar um buffer de constantes
description: Este tópico mostra como inicializar um buffer de constantes na preparação para renderização.
ms.assetid: 78694ac2-e850-402d-8c99-6afb0bd5d660
keywords:
- buffer de constantes, criando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1abb6718ad223ff389aa0b7ebf10ad1ec8bacd71
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641665"
---
# <a name="how-to-create-a-constant-buffer"></a>Como: criar um buffer de constantes

[Buffers de constantes](overviews-direct3d-11-resources-buffers-intro.md) contêm dados de constante de sombreador. Este tópico mostra como inicializar um [buffer de constantes](overviews-direct3d-11-resources-buffers-intro.md) na preparação para renderização.

**Para inicializar um buffer de constantes**

1.  Defina uma estrutura que descreve os dados constantes do sombreador de vértice.
2.  Aloque memória para a estrutura que você definiu na etapa um. Preencha esse buffer com dados constantes de sombreador de vértice. Você pode usar **malloc** ou **New** para alocar a memória ou pode alocar memória para a estrutura da pilha.
3.  Crie uma descrição de buffer preenchendo uma estrutura [**\_ \_ desc de buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Passe o \_ sinalizador de \_ buffer constante de ligação D3D11 \_ para o membro **BindFlags** e passe o tamanho da estrutura de descrição de buffer constante em bytes para o membro **ByteWidth** .

    > [!Note]  
    > O \_ sinalizador de \_ buffer constante de ligação D3D11 \_ não pode ser combinado com nenhum outro sinalizador.

     

4.  Crie uma descrição de dados de subrecurso preenchendo uma estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) . O membro **pSysMem** da estrutura **de \_ \_ dados do subrecurso D3D11** deve apontar diretamente para os dados constantes de sombreador de vértice que você criou na etapa dois.
5.  Chame [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) enquanto passa a [**estrutura \_ \_ Desc do buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , a estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e o endereço de um ponteiro para a interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) para inicializar.

Esses exemplos de código demonstram como criar um buffer constante.

Este exemplo pressupõe que **g \_ pd3dDevice** é um objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido e que **g \_ pd3dContext** é um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) válido.


```C++
ID3D11Buffer*   g_pConstantBuffer11 = NULL;

// Define the constant data used to communicate with shaders.
struct VS_CONSTANT_BUFFER
{
    XMFLOAT4X4 mWorldViewProj;                              
    XMFLOAT4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                                            
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
} VS_CONSTANT_BUFFER;

// Supply the vertex shader constant data.
VS_CONSTANT_BUFFER VsConstData;
VsConstData.mWorldViewProj = {...};
VsConstData.vSomeVectorThatMayBeNeededByASpecificShader = XMFLOAT4(1,2,3,4);
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader = 3.0f;
VsConstData.fTime = 1.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader2 = 2.0f;
VsConstData.fSomeFloatThatMayBeNeededByASpecificShader3 = 4.0f;

// Fill in a buffer description.
D3D11_BUFFER_DESC cbDesc;
cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
cbDesc.Usage = D3D11_USAGE_DYNAMIC;
cbDesc.BindFlags = D3D11_BIND_CONSTANT_BUFFER;
cbDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
cbDesc.MiscFlags = 0;
cbDesc.StructureByteStride = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = &VsConstData;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer.
hr = g_pd3dDevice->CreateBuffer( &cbDesc, &InitData, 
                                 &g_pConstantBuffer11 );

if( FAILED( hr ) )
   return hr;

// Set the buffer.
g_pd3dContext->VSSetConstantBuffers( 0, 1, &g_pConstantBuffer11 );
    
```



Este exemplo mostra a definição HLSL CBuffer associada.

``` syntax
cbuffer VS_CONSTANT_BUFFER : register(b0)
{
    matrix mWorldViewProj;
    float4  vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};
```

> [!Note]  
> Certifique-se de corresponder o \_ layout de memória de buffer de constante vs \_ em C++ com o layout HLSL. Para obter informações sobre como o HLSL manipula o layout na memória, consulte [regras de empacotamento para variáveis constantes](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 