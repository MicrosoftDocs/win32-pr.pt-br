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
# <a name="how-to-create-a-vertex-buffer"></a><span data-ttu-id="183e3-104">Como criar um buffer de vértice</span><span class="sxs-lookup"><span data-stu-id="183e3-104">How to: Create a Vertex Buffer</span></span>

<span data-ttu-id="183e3-105">Os [buffers de vértice](overviews-direct3d-11-resources-buffers-intro.md) contêm dados por vértice.</span><span class="sxs-lookup"><span data-stu-id="183e3-105">[Vertex buffers](overviews-direct3d-11-resources-buffers-intro.md) contain per vertex data.</span></span> <span data-ttu-id="183e3-106">Este tópico mostra como inicializar um buffer de [vértices](overviews-direct3d-11-resources-buffers-intro.md)estáticos, ou seja, um buffer de vértice que não é alterado.</span><span class="sxs-lookup"><span data-stu-id="183e3-106">This topic shows how to initialize a static [vertex buffer](overviews-direct3d-11-resources-buffers-intro.md), that is, a vertex buffer that does not change.</span></span> <span data-ttu-id="183e3-107">Para obter ajuda para inicializar um buffer não estático, consulte a seção [comentários](#remarks) .</span><span class="sxs-lookup"><span data-stu-id="183e3-107">For help initializing a non-static buffer, see the [remarks](#remarks) section.</span></span>

<span data-ttu-id="183e3-108">**Para inicializar um buffer de vértices estáticos**</span><span class="sxs-lookup"><span data-stu-id="183e3-108">**To initialize a static vertex buffer**</span></span>

1.  <span data-ttu-id="183e3-109">Defina uma estrutura que descreve um vértice.</span><span class="sxs-lookup"><span data-stu-id="183e3-109">Define a structure that describes a vertex.</span></span> <span data-ttu-id="183e3-110">Por exemplo, se os dados de vértice contiverem dados de posição e dados de cor, sua estrutura terá um vetor que descreve a posição e outra que descreve a cor.</span><span class="sxs-lookup"><span data-stu-id="183e3-110">For example, if your vertex data contains position data and color data, your structure would have one vector that describes the position and another that describes the color.</span></span>
2.  <span data-ttu-id="183e3-111">Aloque memória (usando malloc ou New) para a estrutura que você definiu na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="183e3-111">Allocate memory (using malloc or new) for the structure that you defined in step one.</span></span> <span data-ttu-id="183e3-112">Preencha esse buffer com os dados de vértice reais que descrevem sua geometria.</span><span class="sxs-lookup"><span data-stu-id="183e3-112">Fill this buffer with the actual vertex data that describes your geometry.</span></span>
3.  <span data-ttu-id="183e3-113">Crie uma descrição de buffer preenchendo uma estrutura [**\_ \_ desc de buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="183e3-113">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="183e3-114">Passe o \_ sinalizador de buffer de vértice de associação D3D11 \_ \_ para o membro **BindFlags** e passe o tamanho da estrutura da etapa um para o membro **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="183e3-114">Pass the D3D11\_BIND\_VERTEX\_BUFFER flag to the **BindFlags** member and pass the size of the structure from step one to the **ByteWidth** member.</span></span>
4.  <span data-ttu-id="183e3-115">Crie uma descrição de dados de subrecurso preenchendo uma estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="183e3-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="183e3-116">O membro **pSysMem** da estrutura [**de \_ \_ dados do subrecurso D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) deve apontar diretamente para os dados de recurso criados na etapa dois.</span><span class="sxs-lookup"><span data-stu-id="183e3-116">The **pSysMem** member of the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure should point directly to the resource data created in step two.</span></span>
5.  <span data-ttu-id="183e3-117">Chame [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) enquanto passa a [**estrutura \_ \_ Desc do buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , a estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e o endereço de um ponteiro para a interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) para inicializar.</span><span class="sxs-lookup"><span data-stu-id="183e3-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="183e3-118">O exemplo de código a seguir demonstra como criar um buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="183e3-118">The following code example demonstrates how to create a vertex buffer.</span></span> <span data-ttu-id="183e3-119">Este exemplo pressupõe que **g \_ pd3dDevice** é um objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido.</span><span class="sxs-lookup"><span data-stu-id="183e3-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="183e3-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="183e3-120">Remarks</span></span>

<span data-ttu-id="183e3-121">Aqui estão algumas maneiras de inicializar um buffer de vértice que muda ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="183e3-121">Here are some ways to initialize a vertex buffer that changes over time.</span></span>

1.  <span data-ttu-id="183e3-122">Crie um 2º buffer com [**\_ \_ preparo de uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); preencha o segundo buffer usando [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext:: inmapeamento**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); use [**ID3D11DeviceContext:: CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) para copiar do buffer de preparo para o buffer padrão.</span><span class="sxs-lookup"><span data-stu-id="183e3-122">Create a 2nd buffer with [**D3D11\_USAGE\_STAGING**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage); fill the second buffer using [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap); use [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) to copy from the staging buffer to the default buffer.</span></span>
2.  <span data-ttu-id="183e3-123">Use [**ID3D11DeviceContext:: UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) para copiar dados da memória.</span><span class="sxs-lookup"><span data-stu-id="183e3-123">Use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to copy data from memory.</span></span>
3.  <span data-ttu-id="183e3-124">Crie um buffer com [**D3D11 de \_ uso \_ dinâmico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)e preencha-o com [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext:: Inmapeamento**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (usando os sinalizadores descartar e não substituir adequadamente).</span><span class="sxs-lookup"><span data-stu-id="183e3-124">Create a buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), and fill it with [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map), [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) (using the Discard and NoOverwrite flags appropriately).</span></span>

<span data-ttu-id="183e3-125">\#1 e \# 2 são úteis para o conteúdo que é alterado menos de uma vez por quadro.</span><span class="sxs-lookup"><span data-stu-id="183e3-125">\#1 and \#2 are useful for content that changes less than once per frame.</span></span> <span data-ttu-id="183e3-126">Em geral, as leituras de GPU serão rápidas e as atualizações de CPU serão mais lentas.</span><span class="sxs-lookup"><span data-stu-id="183e3-126">In general, GPU reads will be fast and CPU updates will be slower.</span></span>

<span data-ttu-id="183e3-127">\#3 é útil para o conteúdo que é alterado mais de uma vez por quadro.</span><span class="sxs-lookup"><span data-stu-id="183e3-127">\#3 is useful for content that changes more than once per frame.</span></span> <span data-ttu-id="183e3-128">Em geral, as leituras de GPU serão mais lentas, mas as atualizações de CPU serão mais rápidas.</span><span class="sxs-lookup"><span data-stu-id="183e3-128">In general, GPU reads will be slower, but CPU updates will be faster.</span></span>

## <a name="related-topics"></a><span data-ttu-id="183e3-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="183e3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="183e3-130">Buffers</span><span class="sxs-lookup"><span data-stu-id="183e3-130">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="183e3-131">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="183e3-131">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




