---
title: Como criar um buffer de vértice
description: Este tópico mostra como inicializar um buffer de vértices estáticos, ou seja, um buffer de vértice que não é alterado.
ms.assetid: 584a39d1-7629-429a-b451-64b1432cb48f
keywords:
- buffer de vértice, criando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e0b3d9d8f731b01e7c919105c21c8d150f864a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292387"
---
# <a name="how-to-create-a-vertex-buffer"></a>Como criar um buffer de vértice

Os [buffers de vértice](overviews-direct3d-11-resources-buffers-intro.md) contêm dados por vértice. Este tópico mostra como inicializar um buffer de [vértices](overviews-direct3d-11-resources-buffers-intro.md)estáticos, ou seja, um buffer de vértice que não é alterado. Para obter ajuda para inicializar um buffer não estático, consulte a seção [comentários](#remarks) .

**Para inicializar um buffer de vértices estáticos**

1.  Defina uma estrutura que descreve um vértice. Por exemplo, se os dados de vértice contiverem dados de posição e dados de cor, sua estrutura terá um vetor que descreve a posição e outra que descreve a cor.
2.  Aloque memória (usando malloc ou New) para a estrutura que você definiu na etapa 1. Preencha esse buffer com os dados de vértice reais que descrevem sua geometria.
3.  Crie uma descrição de buffer preenchendo uma estrutura [**\_ \_ desc de buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Passe o \_ sinalizador de buffer de vértice de associação D3D11 \_ \_ para o membro **BindFlags** e passe o tamanho da estrutura da etapa um para o membro **ByteWidth** .
4.  Crie uma descrição de dados de subrecurso preenchendo uma estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) . O membro **pSysMem** da estrutura [**de \_ \_ dados do subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) deve apontar diretamente para os dados de recurso criados na etapa dois.
5.  Chame [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) enquanto passa a [**estrutura \_ \_ Desc do buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , a estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e o endereço de um ponteiro para a interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) para inicializar.

O exemplo de código a seguir demonstra como criar um buffer de vértice. Este exemplo pressupõe que **g \_ pd3dDevice** é um objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido.


```
ID3D11Buffer*      g_pVertexBuffer;

// Define the data-type that
// describes a vertex.
struct SimpleVertexCombined
{
    XMFLOAT3 Pos;  
    XMFLOAT3 Col;  
};

// Supply the actual vertex data.
SimpleVertexCombined verticesCombo[] =
{
    XMFLOAT3( 0.0f, 0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.0f, 0.5f ),
    XMFLOAT3( 0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.5f, 0.0f, 0.0f ),
    XMFLOAT3( -0.5f, -0.5f, 0.5f ),
    XMFLOAT3( 0.0f, 0.5f, 0.0f ),
};

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage            = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
bufferDesc.BindFlags        = D3D11_BIND_VERTEX_BUFFER;
bufferDesc.CPUAccessFlags   = 0;
bufferDesc.MiscFlags        = 0;

// Fill in the subresource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = verticesCombo;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the vertex buffer.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer );
    
```



## <a name="remarks"></a>Comentários

Aqui estão algumas maneiras de inicializar um buffer de vértice que muda ao longo do tempo.

1.  Crie um 2º buffer com [**\_ \_ preparo de uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); preencha o segundo buffer usando [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext:: inmapeamento**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); use [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) para copiar do buffer de preparo para o buffer padrão.
2.  Use [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) para copiar dados da memória.
3.  Crie um buffer com [**D3D11 de \_ uso \_ dinâmico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)e preencha-o com [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext:: Inmapeamento**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (usando os sinalizadores descartar e não substituir adequadamente).

\#1 e \# 2 são úteis para o conteúdo que é alterado menos de uma vez por quadro. Em geral, as leituras de GPU serão rápidas e as atualizações de CPU serão mais lentas.

\#3 é útil para o conteúdo que é alterado mais de uma vez por quadro. Em geral, as leituras de GPU serão mais lentas, mas as atualizações de CPU serão mais rápidas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




