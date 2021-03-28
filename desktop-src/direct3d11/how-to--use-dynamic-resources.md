---
title: Como usar recursos dinâmicos
description: Você cria e usa recursos dinâmicos quando seu aplicativo precisa alterar os dados nesses recursos. Você pode criar texturas e buffers para uso dinâmico.
ms.assetid: E73EA4B0-BD14-430C-89CA-4CFCF92C7548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41e00cda7236040679c7863454e4cc18d81106b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159421"
---
# <a name="how-to-use-dynamic-resources"></a><span data-ttu-id="5399b-104">Como: usar recursos dinâmicos</span><span class="sxs-lookup"><span data-stu-id="5399b-104">How to: Use dynamic resources</span></span>

<span data-ttu-id="5399b-105">**APIs importantes**</span><span class="sxs-lookup"><span data-stu-id="5399b-105">**Important APIs**</span></span>

-   [<span data-ttu-id="5399b-106">**ID3D11DeviceContext:: map**</span><span class="sxs-lookup"><span data-stu-id="5399b-106">**ID3D11DeviceContext::Map**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)
-   [<span data-ttu-id="5399b-107">**ID3D11DeviceContext:: mapeamento**</span><span class="sxs-lookup"><span data-stu-id="5399b-107">**ID3D11DeviceContext::Unmap**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap)
-   [<span data-ttu-id="5399b-108">**Uso de D3D11 \_**</span><span class="sxs-lookup"><span data-stu-id="5399b-108">**D3D11\_USAGE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage)

<span data-ttu-id="5399b-109">Você cria e usa recursos dinâmicos quando seu aplicativo precisa alterar os dados nesses recursos.</span><span class="sxs-lookup"><span data-stu-id="5399b-109">You create and use dynamic resources when your app needs to change data in those resources.</span></span> <span data-ttu-id="5399b-110">Você pode criar texturas e buffers para uso dinâmico.</span><span class="sxs-lookup"><span data-stu-id="5399b-110">You can create textures and buffers for dynamic usage.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="5399b-111">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="5399b-111">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="5399b-112">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="5399b-112">Technologies</span></span>

-   [<span data-ttu-id="5399b-113">Como: criar uma textura</span><span class="sxs-lookup"><span data-stu-id="5399b-113">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
-   [<span data-ttu-id="5399b-114">Como: inicializar uma textura programaticamente</span><span class="sxs-lookup"><span data-stu-id="5399b-114">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
-   [<span data-ttu-id="5399b-115">Como: criar um buffer de constantes</span><span class="sxs-lookup"><span data-stu-id="5399b-115">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)

### <a name="prerequisites"></a><span data-ttu-id="5399b-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="5399b-116">Prerequisites</span></span>

<span data-ttu-id="5399b-117">Partimos do princípio de que você conhece C++.</span><span class="sxs-lookup"><span data-stu-id="5399b-117">We assume that you are familiar with C++.</span></span> <span data-ttu-id="5399b-118">Você também precisa ter experiência básica com conceitos de programação de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="5399b-118">You also need basic experience with graphics programming concepts.</span></span>

## <a name="instructions"></a><span data-ttu-id="5399b-119">Instruções</span><span class="sxs-lookup"><span data-stu-id="5399b-119">Instructions</span></span>

### <a name="step-1-specify-dynamic-usage"></a><span data-ttu-id="5399b-120">Etapa 1: especificar o uso dinâmico</span><span class="sxs-lookup"><span data-stu-id="5399b-120">Step 1: Specify dynamic usage</span></span>

<span data-ttu-id="5399b-121">Se você quiser que seu aplicativo seja capaz de fazer alterações nos recursos, deverá especificar esses recursos como dinâmicos e graváveis ao criá-los.</span><span class="sxs-lookup"><span data-stu-id="5399b-121">If you want your app to be able to make changes to resources, you must specify those resources as dynamic and writable when you create them.</span></span>

<span data-ttu-id="5399b-122">**Para especificar o uso dinâmico**</span><span class="sxs-lookup"><span data-stu-id="5399b-122">**To specify dynamic usage**</span></span>

1.  <span data-ttu-id="5399b-123">Especifique o uso do recurso como dinâmico.</span><span class="sxs-lookup"><span data-stu-id="5399b-123">Specify the resource usage as dynamic.</span></span> <span data-ttu-id="5399b-124">Por exemplo, especifique o [**valor \_ \_ dinâmico de uso de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) no membro de **uso** do [**buffer de D3D11 \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para um vértice ou um buffer de constante e especifique o valor **dinâmico de \_ uso \_ de D3D11** no membro de **uso** de [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) para uma textura 2D.</span><span class="sxs-lookup"><span data-stu-id="5399b-124">For example, specify the [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) value in the **Usage** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) for a vertex or constant buffer and specify the **D3D11\_USAGE\_DYNAMIC** value in the **Usage** member of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) for a 2D texture.</span></span>
2.  <span data-ttu-id="5399b-125">Especifique o recurso como gravável.</span><span class="sxs-lookup"><span data-stu-id="5399b-125">Specify the resource as writable.</span></span> <span data-ttu-id="5399b-126">Por exemplo, especifique o valor de [**gravação de \_ acesso de CPU \_ \_ D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) no membro **CPUAccessFlags** de [**D3D11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) ou [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span><span class="sxs-lookup"><span data-stu-id="5399b-126">For example, specify the [**D3D11\_CPU\_ACCESS\_WRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cpu_access_flag) value in the **CPUAccessFlags** member of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) or [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc).</span></span>
3.  <span data-ttu-id="5399b-127">Passe a descrição do recurso para a função de criação.</span><span class="sxs-lookup"><span data-stu-id="5399b-127">Pass the resource description to the creation function.</span></span> <span data-ttu-id="5399b-128">Por exemplo, passe o endereço do [**\_ buffer D3D11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) e passe o endereço de [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) para [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span><span class="sxs-lookup"><span data-stu-id="5399b-128">For example, pass the address of [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) to [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) and pass the address of [**D3D11\_TEXTURE2D\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc) to [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d).</span></span>

<span data-ttu-id="5399b-129">Aqui está um exemplo de criação de um buffer de vértice dinâmico:</span><span class="sxs-lookup"><span data-stu-id="5399b-129">Here is an example of creating a dynamic vertex buffer:</span></span>


```C++
    // Create a vertex buffer for a triangle.

    float2 triangleVertices[] =
    {
        float2(-0.5f, -0.5f),
        float2(0.0f, 0.5f),
        float2(0.5f, -0.5f),
    };

    D3D11_BUFFER_DESC vertexBufferDesc = { 0 };
    vertexBufferDesc.ByteWidth = sizeof(float2)* ARRAYSIZE(triangleVertices);
    vertexBufferDesc.Usage = D3D11_USAGE_DYNAMIC;
    vertexBufferDesc.BindFlags = D3D11_BIND_VERTEX_BUFFER;
    vertexBufferDesc.CPUAccessFlags = D3D11_CPU_ACCESS_WRITE;
    vertexBufferDesc.MiscFlags = 0;
    vertexBufferDesc.StructureByteStride = 0;

    D3D11_SUBRESOURCE_DATA vertexBufferData;
    vertexBufferData.pSysMem = triangleVertices;
    vertexBufferData.SysMemPitch = 0;
    vertexBufferData.SysMemSlicePitch = 0;

    DX::ThrowIfFailed(
        m_d3dDevice->CreateBuffer(
        &vertexBufferDesc,
        &vertexBufferData,
        &vertexBuffer2
        )
        );

```



### <a name="step-2-change-a-dynamic-resource"></a><span data-ttu-id="5399b-130">Etapa 2: alterar um recurso dinâmico</span><span class="sxs-lookup"><span data-stu-id="5399b-130">Step 2: Change a dynamic resource</span></span>

<span data-ttu-id="5399b-131">Se você especificou um recurso como dinâmico e gravável quando o criou, poderá fazer alterações posteriormente nesse recurso.</span><span class="sxs-lookup"><span data-stu-id="5399b-131">If you specified a resource as dynamic and writable when you created it, you can later make changes to that resource.</span></span>

<span data-ttu-id="5399b-132">**Para alterar dados em um recurso dinâmico**</span><span class="sxs-lookup"><span data-stu-id="5399b-132">**To change data in a dynamic resource**</span></span>

1.  <span data-ttu-id="5399b-133">Configure os novos dados para o recurso.</span><span class="sxs-lookup"><span data-stu-id="5399b-133">Set up the new data for the resource.</span></span> <span data-ttu-id="5399b-134">Declare uma variável de tipo de [**\_ \_ subrecurso mapeado D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) e inicialize-a como zero.</span><span class="sxs-lookup"><span data-stu-id="5399b-134">Declare a [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) type variable and initialize it to zero.</span></span> <span data-ttu-id="5399b-135">Você usará essa variável para alterar o recurso.</span><span class="sxs-lookup"><span data-stu-id="5399b-135">You'll use this variable to change the resource.</span></span>
2.  <span data-ttu-id="5399b-136">Desabilite o acesso à GPU (unidade de processamento gráfico) aos dados que você deseja alterar e obtenha um ponteiro para a memória que contém os dados.</span><span class="sxs-lookup"><span data-stu-id="5399b-136">Disable graphics processing unit (GPU) access to the data that you want to change and get a pointer to the memory that contains the data.</span></span> <span data-ttu-id="5399b-137">Para obter esse ponteiro, passe [**D3D11 \_ map \_ Write \_ Discard**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) para o parâmetro *MapType* ao chamar [**ID3D11DeviceContext:: map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span><span class="sxs-lookup"><span data-stu-id="5399b-137">To get this pointer, pass [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) to the *MapType* parameter when you call [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span> <span data-ttu-id="5399b-138">Defina esse ponteiro para o endereço da variável [**de \_ \_ subrecurso mapeado D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) da etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="5399b-138">Set this pointer to the address of the [**D3D11\_MAPPED\_SUBRESOURCE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) variable from the previous step.</span></span>
3.  <span data-ttu-id="5399b-139">Grave os novos dados na memória.</span><span class="sxs-lookup"><span data-stu-id="5399b-139">Write the new data to the memory.</span></span>
4.  <span data-ttu-id="5399b-140">Chame [**ID3D11DeviceContext:: inmapeamento**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) para reabilitar o acesso de GPU aos dados quando terminar de gravar os novos dados.</span><span class="sxs-lookup"><span data-stu-id="5399b-140">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) to reenable GPU access to the data when you're finished writing the new data.</span></span>

<span data-ttu-id="5399b-141">Aqui está um exemplo de alteração de um buffer de vértice dinâmico:</span><span class="sxs-lookup"><span data-stu-id="5399b-141">Here is an example of changing a dynamic vertex buffer:</span></span>


```C++
// This might get called as the result of a click event to double the size of the triangle.
void TriangleRenderer::MapDoubleVertices()
{
    D3D11_MAPPED_SUBRESOURCE mappedResource;
    ZeroMemory(&mappedResource, sizeof(D3D11_MAPPED_SUBRESOURCE));
    float2 vertices[] =
    {
        float2(-1.0f, -1.0f),
        float2(0.0f, 1.0f),
        float2(1.0f, -1.0f),
    };
    //  Disable GPU access to the vertex buffer data.
    auto m_d3dContext = m_deviceResources->GetD3DDeviceContext();
    m_d3dContext->Map(vertexBuffer2.Get(), 0, D3D11_MAP_WRITE_DISCARD, 0, &mappedResource);
    //  Update the vertex buffer here.
    memcpy(mappedResource.pData, vertices, sizeof(vertices));
    //  Reenable GPU access to the vertex buffer data.
    m_d3dContext->Unmap(vertexBuffer2.Get(), 0);
}
```



## <a name="remarks"></a><span data-ttu-id="5399b-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="5399b-142">Remarks</span></span>

### <a name="using-dynamic-textures"></a><span data-ttu-id="5399b-143">Usando texturas dinâmicas</span><span class="sxs-lookup"><span data-stu-id="5399b-143">Using dynamic textures</span></span>

<span data-ttu-id="5399b-144">É recomendável que você crie apenas uma textura dinâmica por formato e, possivelmente por tamanho.</span><span class="sxs-lookup"><span data-stu-id="5399b-144">We recommend that you create only one dynamic texture per format and possibly per size.</span></span> <span data-ttu-id="5399b-145">Não recomendamos a criação de mipmaps, cubos e volumes dinâmicos devido à sobrecarga adicional no mapeamento de cada nível.</span><span class="sxs-lookup"><span data-stu-id="5399b-145">We don't recommend creating dynamic mipmaps, cubes, and volumes because of the additional overhead in mapping every level.</span></span> <span data-ttu-id="5399b-146">Para mipmaps, você pode especificar [**o \_ \_ \_ descarte de gravação do mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) somente no nível superior.</span><span class="sxs-lookup"><span data-stu-id="5399b-146">For mipmaps, you can specify [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) only on the top level.</span></span> <span data-ttu-id="5399b-147">Todos os níveis são descartados Mapeando apenas o nível superior.</span><span class="sxs-lookup"><span data-stu-id="5399b-147">All levels are discarded by mapping just the top level.</span></span> <span data-ttu-id="5399b-148">Esse comportamento é o mesmo para volumes e cubos.</span><span class="sxs-lookup"><span data-stu-id="5399b-148">This behavior is the same for volumes and cubes.</span></span> <span data-ttu-id="5399b-149">Para cubos, o nível superior e a face 0 são mapeados.</span><span class="sxs-lookup"><span data-stu-id="5399b-149">For cubes, the top level and face 0 are mapped.</span></span>

### <a name="using-dynamic-buffers"></a><span data-ttu-id="5399b-150">Usando buffers dinâmicos</span><span class="sxs-lookup"><span data-stu-id="5399b-150">Using dynamic buffers</span></span>

<span data-ttu-id="5399b-151">Quando você chama [**MAP**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) em um buffer de vértice estático enquanto a GPU está usando o buffer, você obtém uma penalidade de desempenho significativa.</span><span class="sxs-lookup"><span data-stu-id="5399b-151">When you call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) on a static vertex buffer while the GPU is using the buffer, you get a significant performance penalty.</span></span> <span data-ttu-id="5399b-152">Nessa situação, o **mapa** deve aguardar até que a GPU termine de ler os dados de vértice ou de índice do buffer antes que o **mapa** possa retornar ao aplicativo de chamada, o que causa um atraso significativo.</span><span class="sxs-lookup"><span data-stu-id="5399b-152">In this situation, **Map** must wait until the GPU is finished reading vertex or index data from the buffer before **Map** can return to the calling app, which causes a significant delay.</span></span> <span data-ttu-id="5399b-153">Chamar **MAP** e, em seguida, renderizar de um buffer estático várias vezes por quadro também impede a GPU de armazenar em buffer comandos de renderização porque ele deve concluir os comandos antes de retornar o ponteiro de mapa.</span><span class="sxs-lookup"><span data-stu-id="5399b-153">Calling **Map** and then rendering from a static buffer several times per frame also prevents the GPU from buffering rendering commands because it must finish commands before returning the map pointer.</span></span> <span data-ttu-id="5399b-154">Sem comandos armazenados em buffer, a GPU permanece ociosa até que o aplicativo termine de preencher o buffer de vértice ou o buffer de índice e emita um comando de renderização.</span><span class="sxs-lookup"><span data-stu-id="5399b-154">Without buffered commands, the GPU remains idle until after the app is finished filling the vertex buffer or index buffer and issues a rendering command.</span></span>

<span data-ttu-id="5399b-155">Idealmente, os dados de vértice ou de índice nunca seriam alterados, mas isso nem sempre é possível.</span><span class="sxs-lookup"><span data-stu-id="5399b-155">Ideally the vertex or index data would never change, but this is not always possible.</span></span> <span data-ttu-id="5399b-156">Há muitas situações em que o aplicativo precisa alterar os dados do vértice ou do índice a cada quadro, talvez até várias vezes por quadro.</span><span class="sxs-lookup"><span data-stu-id="5399b-156">There are many situations where the app needs to change vertex or index data every frame, perhaps even multiple times per frame.</span></span> <span data-ttu-id="5399b-157">Para essas situações, recomendamos que você crie o vértice ou o buffer de índice com o [**uso de D3D11 \_ \_ dinâmico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span><span class="sxs-lookup"><span data-stu-id="5399b-157">For these situations, we recommend that you create the vertex or index buffer with [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage).</span></span> <span data-ttu-id="5399b-158">Esse sinalizador de uso faz com que o tempo de execução Otimize para operações de mapeamento frequentes.</span><span class="sxs-lookup"><span data-stu-id="5399b-158">This usage flag causes the runtime to optimize for frequent map operations.</span></span> <span data-ttu-id="5399b-159">**D3D11 \_ O uso \_ dinâmico** só é útil quando o buffer é mapeado com frequência; Se os dados permanecerem constantes, coloque-os em um buffer estático de um vértice ou de índice.</span><span class="sxs-lookup"><span data-stu-id="5399b-159">**D3D11\_USAGE\_DYNAMIC** is only useful when the buffer is mapped frequently; if data is to remain constant, place that data in a static vertex or index buffer.</span></span>

<span data-ttu-id="5399b-160">Para receber uma melhoria de desempenho quando você usa buffers de vértice dinâmicos, seu aplicativo deve chamar [**MAP**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) com os valores de [**\_ mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) apropriados.</span><span class="sxs-lookup"><span data-stu-id="5399b-160">To receive a performance improvement when you use dynamic vertex buffers, your app must call [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) with the appropriate [**D3D11\_MAP**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) values.</span></span> <span data-ttu-id="5399b-161">[**D3D11 \_ O \_ \_ descarte de gravação de mapa**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica que o aplicativo não precisa manter o vértice antigo ou os dados de índice no buffer.</span><span class="sxs-lookup"><span data-stu-id="5399b-161">[**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app doesn't need to keep the old vertex or index data in the buffer.</span></span> <span data-ttu-id="5399b-162">Se a GPU ainda estiver usando o buffer quando você chamar **MAP** com **\_ descarte de \_ gravação \_ de mapa D3D11**, o tempo de execução retornará um ponteiro para uma nova região de memória em vez dos dados de buffer antigos.</span><span class="sxs-lookup"><span data-stu-id="5399b-162">If the GPU is still using the buffer when you call **Map** with **D3D11\_MAP\_WRITE\_DISCARD**, the runtime returns a pointer to a new region of memory instead of the old buffer data.</span></span> <span data-ttu-id="5399b-163">Isso permite que a GPU continue usando os dados antigos enquanto o aplicativo coloca os dados no novo buffer.</span><span class="sxs-lookup"><span data-stu-id="5399b-163">This allows the GPU to continue using the old data while the app places data in the new buffer.</span></span> <span data-ttu-id="5399b-164">Nenhum gerenciamento de memória adicional é necessário no aplicativo; o buffer antigo é reutilizado ou destruído automaticamente quando a GPU é concluída com ele.</span><span class="sxs-lookup"><span data-stu-id="5399b-164">No additional memory management is required in the app; the old buffer is reused or destroyed automatically when the GPU is finished with it.</span></span>

> [!Note]  
> <span data-ttu-id="5399b-165">Quando você mapeia um buffer com [**\_ descarte de \_ gravação \_ de mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), o tempo de execução sempre descarta todo o buffer.</span><span class="sxs-lookup"><span data-stu-id="5399b-165">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map), the runtime always discards the entire buffer.</span></span> <span data-ttu-id="5399b-166">Não é possível preservar as informações em áreas não mapeadas do buffer especificando um campo de tamanho limitado ou um deslocamento diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="5399b-166">You can't preserve info in unmapped areas of the buffer by specifying a nonzero offset or limited size field.</span></span>

 

<span data-ttu-id="5399b-167">Há casos em que a quantidade de dados que o aplicativo precisa armazenar por mapa é pequena, como adicionar quatro vértices para renderizar um Sprite.</span><span class="sxs-lookup"><span data-stu-id="5399b-167">There are cases where the amount of data the app needs to store per map is small, such as adding four vertices to render a sprite.</span></span> <span data-ttu-id="5399b-168">[**D3D11 \_ Gravação de mapeamento \_ \_ sem \_ substituição**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indica que o aplicativo não substituirá os dados que já estão em uso no buffer dinâmico.</span><span class="sxs-lookup"><span data-stu-id="5399b-168">[**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) indicates that the app will not overwrite data already in use in the dynamic buffer.</span></span> <span data-ttu-id="5399b-169">A chamada de [**mapa**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) retornará um ponteiro para os dados antigos, o que permitirá que o aplicativo Adicione novos dados em regiões não utilizadas do vértice ou buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="5399b-169">The [**Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) call will return a pointer to the old data, which will allow the app to add new data in unused regions of the vertex or index buffer.</span></span> <span data-ttu-id="5399b-170">O aplicativo não deve modificar vértices ou índices que são usados em uma operação de desenho, pois eles ainda podem estar em uso pela GPU.</span><span class="sxs-lookup"><span data-stu-id="5399b-170">The app must not modify vertices or indices that are used in a draw operation as they might still be in use by the GPU.</span></span> <span data-ttu-id="5399b-171">Recomendamos que o aplicativo use o [**\_ descarte de \_ gravação \_ do mapa D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) depois que o buffer dinâmico estiver cheio para receber uma nova região de memória, o que descartará os dados antigos do vértice ou do índice depois que a GPU for concluída.</span><span class="sxs-lookup"><span data-stu-id="5399b-171">We recommend that the app then use [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) after the dynamic buffer is full to receive a new region of memory, which discards the old vertex or index data after the GPU is finished.</span></span>

<span data-ttu-id="5399b-172">O mecanismo de consulta assíncrona é útil para determinar se os vértices ainda estão em uso pela GPU.</span><span class="sxs-lookup"><span data-stu-id="5399b-172">The asynchronous query mechanism is useful to determine if vertices are still in use by the GPU.</span></span> <span data-ttu-id="5399b-173">Emita uma consulta do tipo [**\_ \_ evento de consulta D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) após a última chamada de desenho que usa os vértices.</span><span class="sxs-lookup"><span data-stu-id="5399b-173">Issue a query of type [**D3D11\_QUERY\_EVENT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_query) after the last draw call that uses the vertices.</span></span> <span data-ttu-id="5399b-174">Os vértices não estão mais em uso quando [**ID3D11DeviceContext:: GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5399b-174">The vertices are no longer in use when [**ID3D11DeviceContext::GetData**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-getdata) returns S\_OK.</span></span> <span data-ttu-id="5399b-175">Ao mapear um buffer com o [**D3D11 \_ map \_ Write \_ Discard**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) ou nenhum valor de mapa, você sempre garante que os vértices sejam sincronizados corretamente com a GPU.</span><span class="sxs-lookup"><span data-stu-id="5399b-175">When you map a buffer with [**D3D11\_MAP\_WRITE\_DISCARD**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map) or no map values, you are always guaranteed that the vertices are synchronized properly with the GPU.</span></span> <span data-ttu-id="5399b-176">Mas, ao mapear sem valores de mapa, você incorrerá na penalidade de desempenho descrita anteriormente.</span><span class="sxs-lookup"><span data-stu-id="5399b-176">But, when you map without map values, you will incur the performance penalty described earlier.</span></span>

> [!Note]  
> <span data-ttu-id="5399b-177">O tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8, permite o mapeamento de buffers de constantes dinâmicas e SRVs (exibições de recursos do sombreador) de buffers dinâmicos com o [**mapa de D3D11 \_ \_ gravação \_ sem \_ substituição**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span><span class="sxs-lookup"><span data-stu-id="5399b-177">The Direct3D 11.1 runtime, which is available starting with Windows 8, enables mapping dynamic constant buffers and shader resource views (SRVs) of dynamic buffers with [**D3D11\_MAP\_WRITE\_NO\_OVERWRITE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_map).</span></span> <span data-ttu-id="5399b-178">Os tempos de execução do Direct3D 11 e anteriores não limitavam o mapeamento parcial da atualização para os buffers de vértice ou de índice.</span><span class="sxs-lookup"><span data-stu-id="5399b-178">The Direct3D 11 and earlier runtimes limited no-overwrite partial-update mapping to vertex or index buffers.</span></span> <span data-ttu-id="5399b-179">Para determinar se um dispositivo Direct3D dá suporte a esses recursos, chame [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) com [**Opções do D3D11 \_ Feature \_ D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span><span class="sxs-lookup"><span data-stu-id="5399b-179">To determine if a Direct3D device supports these features, call [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) with [**D3D11\_FEATURE\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature).</span></span> <span data-ttu-id="5399b-180">**CheckFeatureSupport** preenche os membros de uma estrutura de [**Opções de D3D11 de \_ dados de recurso \_ \_ \_ D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) com os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5399b-180">**CheckFeatureSupport** fills members of a [**D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) structure with the device's features.</span></span> <span data-ttu-id="5399b-181">Os membros relevantes aqui são **MapNoOverwriteOnDynamicConstantBuffer** e **MapNoOverwriteOnDynamicBufferSRV**.</span><span class="sxs-lookup"><span data-stu-id="5399b-181">The relevant members here are **MapNoOverwriteOnDynamicConstantBuffer** and **MapNoOverwriteOnDynamicBufferSRV**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5399b-182">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5399b-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5399b-183">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5399b-183">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




