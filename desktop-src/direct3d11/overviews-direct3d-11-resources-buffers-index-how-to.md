---
title: Como criar um buffer de índice
description: Este tópico mostra como inicializar um buffer de índice em preparação para renderização.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- buffer de índice, criando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d474114e5908a42a112dddd550e24c13e5e1d3bf2cec523d47dfe1d617ac0bf5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119496"
---
# <a name="how-to-create-an-index-buffer"></a>Como: criar um buffer de índice

[Buffers de índice](overviews-direct3d-11-resources-buffers-intro.md) contêm dados de índice. Este tópico mostra como inicializar um [buffer de índice](overviews-direct3d-11-resources-buffers-intro.md) em preparação para renderização.

**Para inicializar um buffer de índice**

1.  Crie um buffer que contenha as informações de índice.
2.  Crie uma descrição de buffer preenchendo uma estrutura [**\_ \_ desc de buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) . Passe o \_ sinalizador de buffer de índice de associação D3D11 \_ \_ para o membro **BindFlags** e passe o tamanho do buffer em bytes para o membro **ByteWidth** .
3.  Crie uma descrição de dados de subrecurso preenchendo uma estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) . O membro **pSysMem** deve apontar diretamente para os dados de índice criados na etapa 1.
4.  Chame [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) enquanto passa a [**estrutura \_ \_ Desc do buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , a estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e o endereço de um ponteiro para a interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) para inicializar.

O exemplo de código a seguir demonstra como criar um buffer de índice. Este exemplo pressupõe que


```
g_pd3dDevice
```



é um objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido e que


```
g_pd3dContext
```



é um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) válido.


```
ID3D11Buffer *g_pIndexBuffer = NULL;

// Create indices.
unsigned int indices[] = { 0, 1, 2 };

// Fill in a buffer description.
D3D11_BUFFER_DESC bufferDesc;
bufferDesc.Usage           = D3D11_USAGE_DEFAULT;
bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
bufferDesc.BindFlags       = D3D11_BIND_INDEX_BUFFER;
bufferDesc.CPUAccessFlags  = 0;
bufferDesc.MiscFlags       = 0;

// Define the resource data.
D3D11_SUBRESOURCE_DATA InitData;
InitData.pSysMem = indices;
InitData.SysMemPitch = 0;
InitData.SysMemSlicePitch = 0;

// Create the buffer with the device.
hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
if( FAILED( hr ) )
    return hr;

// Set the buffer.
g_pd3dContext->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
    
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




