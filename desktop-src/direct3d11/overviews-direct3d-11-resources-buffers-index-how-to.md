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
# <a name="how-to-create-an-index-buffer"></a>Como criar um buffer de índice

[Buffers de índice](overviews-direct3d-11-resources-buffers-intro.md) contêm dados de índice. Este tópico mostra como inicializar um [buffer de índice em](overviews-direct3d-11-resources-buffers-intro.md) preparação para renderização.

**Para inicializar um buffer de índice**

1.  Crie um buffer que contenha suas informações de índice.
2.  Crie uma descrição de buffer preenchendo uma [**estrutura D3D11 \_ BUFFER \_ DESC.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) Passe o sinalizador D3D11 BIND INDEX BUFFER para o membro BindFlags e passe o tamanho do buffer em bytes para \_ \_ o membro \_ **ByteWidth.** 
3.  Crie uma descrição de dados de sub-fonte preenchendo uma [**estrutura D3D11 \_ SUBRESOURCE \_ DATA.**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) O **membro pSysMem** deve apontar diretamente para os dados de índice criados na etapa um.
4.  Chame [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) ao passar a estrutura [**D3D11 \_ BUFFER \_ DESC,**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a estrutura [**D3D11 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e o endereço de um ponteiro para a interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) a ser inicializada.

O exemplo de código a seguir demonstra como criar um buffer de índice. Este exemplo supõe que


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

 

 




