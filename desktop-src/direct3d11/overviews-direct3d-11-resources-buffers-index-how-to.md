---
title: Como criar um buffer de índice
description: Este tópico mostra como inicializar um buffer de índice em preparação para renderização.
ms.assetid: 4b33d32a-27fd-4652-87ac-3b7268881f89
keywords:
- buffer de índice, criando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c4c99639748876a5f5fd84e546aaf299885c76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160131"
---
# <a name="how-to-create-an-index-buffer"></a><span data-ttu-id="f13a9-104">Como: criar um buffer de índice</span><span class="sxs-lookup"><span data-stu-id="f13a9-104">How to: Create an Index Buffer</span></span>

<span data-ttu-id="f13a9-105">[Buffers de índice](overviews-direct3d-11-resources-buffers-intro.md) contêm dados de índice.</span><span class="sxs-lookup"><span data-stu-id="f13a9-105">[Index buffers](overviews-direct3d-11-resources-buffers-intro.md) contain index data.</span></span> <span data-ttu-id="f13a9-106">Este tópico mostra como inicializar um [buffer de índice](overviews-direct3d-11-resources-buffers-intro.md) em preparação para renderização.</span><span class="sxs-lookup"><span data-stu-id="f13a9-106">This topic shows how to initialize an [index buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="f13a9-107">**Para inicializar um buffer de índice**</span><span class="sxs-lookup"><span data-stu-id="f13a9-107">**To initialize an index buffer**</span></span>

1.  <span data-ttu-id="f13a9-108">Crie um buffer que contenha as informações de índice.</span><span class="sxs-lookup"><span data-stu-id="f13a9-108">Create a buffer that contains your index information.</span></span>
2.  <span data-ttu-id="f13a9-109">Crie uma descrição de buffer preenchendo uma estrutura [**\_ \_ desc de buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="f13a9-109">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="f13a9-110">Passe o \_ sinalizador de buffer de índice de associação D3D11 \_ \_ para o membro **BindFlags** e passe o tamanho do buffer em bytes para o membro **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="f13a9-110">Pass the D3D11\_BIND\_INDEX\_BUFFER flag to the **BindFlags** member and pass the size of the buffer in bytes to the **ByteWidth** member.</span></span>
3.  <span data-ttu-id="f13a9-111">Crie uma descrição de dados de subrecurso preenchendo uma estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="f13a9-111">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="f13a9-112">O membro **pSysMem** deve apontar diretamente para os dados de índice criados na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="f13a9-112">The **pSysMem** member should point directly to the index data created in step one.</span></span>
4.  <span data-ttu-id="f13a9-113">Chame [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) enquanto passa a [**estrutura \_ \_ Desc do buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , a estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e o endereço de um ponteiro para a interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) para inicializar.</span><span class="sxs-lookup"><span data-stu-id="f13a9-113">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="f13a9-114">O exemplo de código a seguir demonstra como criar um buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="f13a9-114">The following code example demonstrates how to create an index buffer.</span></span> <span data-ttu-id="f13a9-115">Este exemplo pressupõe que</span><span class="sxs-lookup"><span data-stu-id="f13a9-115">This example assumes that</span></span>


```
g_pd3dDevice
```



<span data-ttu-id="f13a9-116">é um objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido e que</span><span class="sxs-lookup"><span data-stu-id="f13a9-116">is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that</span></span>


```
g_pd3dContext
```



<span data-ttu-id="f13a9-117">é um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) válido.</span><span class="sxs-lookup"><span data-stu-id="f13a9-117">is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f13a9-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f13a9-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f13a9-119">Buffers</span><span class="sxs-lookup"><span data-stu-id="f13a9-119">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="f13a9-120">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="f13a9-120">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




