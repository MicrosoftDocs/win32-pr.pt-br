---
description: A criação de buffers requer a definição dos dados que o buffer armazenará, fornecendo dados de inicialização e configurando sinalizadores de uso e de associação apropriados. Para criar texturas, consulte criando recursos de textura (Direct3D 10).
ms.assetid: 9787b153-9301-4a0f-bd6f-21cc6f7fc650
title: Criando recursos de buffer (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d711265775c430728fbcffecd364f746580a566
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646403"
---
# <a name="creating-buffer-resources-direct3d-10"></a><span data-ttu-id="0756d-104">Criando recursos de buffer (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0756d-104">Creating Buffer Resources (Direct3D 10)</span></span>

<span data-ttu-id="0756d-105">A criação de buffers requer a definição dos dados que o buffer armazenará, fornecendo dados de inicialização e configurando sinalizadores de uso e de associação apropriados.</span><span class="sxs-lookup"><span data-stu-id="0756d-105">Creating buffers requires defining the data that the buffer will store, providing initialization data, and setting up appropriate usage and binding flags.</span></span> <span data-ttu-id="0756d-106">Para criar texturas, consulte [criando recursos de textura (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span><span class="sxs-lookup"><span data-stu-id="0756d-106">To create textures, see [Creating Texture Resources (Direct3D 10)](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>

-   [<span data-ttu-id="0756d-107">Criar um buffer de vértice</span><span class="sxs-lookup"><span data-stu-id="0756d-107">Create a Vertex Buffer</span></span>](#create-a-vertex-buffer)
    -   [<span data-ttu-id="0756d-108">Criar uma descrição do buffer</span><span class="sxs-lookup"><span data-stu-id="0756d-108">Create a Buffer Description</span></span>](#create-a-buffer-description)
    -   [<span data-ttu-id="0756d-109">Criar os dados de inicialização para o buffer</span><span class="sxs-lookup"><span data-stu-id="0756d-109">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
    -   [<span data-ttu-id="0756d-110">Criar o buffer</span><span class="sxs-lookup"><span data-stu-id="0756d-110">Create the Buffer</span></span>](#create-the-buffer)
-   [<span data-ttu-id="0756d-111">Criar um buffer de índice</span><span class="sxs-lookup"><span data-stu-id="0756d-111">Create an Index Buffer</span></span>](#create-an-index-buffer)
-   [<span data-ttu-id="0756d-112">Criar um buffer de constantes</span><span class="sxs-lookup"><span data-stu-id="0756d-112">Create a Constant Buffer</span></span>](#create-a-constant-buffer)
-   [<span data-ttu-id="0756d-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0756d-113">Related topics</span></span>](#related-topics)

## <a name="create-a-vertex-buffer"></a><span data-ttu-id="0756d-114">Criar um buffer de vértice</span><span class="sxs-lookup"><span data-stu-id="0756d-114">Create a Vertex Buffer</span></span>

<span data-ttu-id="0756d-115">As etapas para criar um [buffer de vértice](d3d10-graphics-programming-guide-resources-types.md) são as seguintes.</span><span class="sxs-lookup"><span data-stu-id="0756d-115">The steps to creating a [vertex buffer](d3d10-graphics-programming-guide-resources-types.md) are as follows.</span></span>

-   [<span data-ttu-id="0756d-116">Criar uma descrição do buffer</span><span class="sxs-lookup"><span data-stu-id="0756d-116">Create a Buffer Description</span></span>](#create-a-buffer-description)
-   [<span data-ttu-id="0756d-117">Criar os dados de inicialização para o buffer</span><span class="sxs-lookup"><span data-stu-id="0756d-117">Create the Initialization Data for the Buffer</span></span>](#create-the-initialization-data-for-the-buffer)
-   [<span data-ttu-id="0756d-118">Criar o buffer</span><span class="sxs-lookup"><span data-stu-id="0756d-118">Create the Buffer</span></span>](#create-the-buffer)

### <a name="create-a-buffer-description"></a><span data-ttu-id="0756d-119">Criar uma descrição do buffer</span><span class="sxs-lookup"><span data-stu-id="0756d-119">Create a Buffer Description</span></span>

<span data-ttu-id="0756d-120">Ao criar um buffer de vértice, uma descrição de buffer (consulte [**\_ \_ desc buffer d3d10**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) é usada para definir como os dados são organizados dentro do buffer, como o pipeline pode acessar o buffer e como o buffer será usado.</span><span class="sxs-lookup"><span data-stu-id="0756d-120">When creating a vertex buffer, a buffer description (see [**D3D10\_BUFFER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)) is used to define how data is organized within the buffer, how the pipeline can access the buffer, and how the buffer will be used.</span></span>

<span data-ttu-id="0756d-121">O exemplo a seguir demonstra como criar uma descrição de buffer para um único triângulo com vértices que contêm valores de posição e cor.</span><span class="sxs-lookup"><span data-stu-id="0756d-121">The following example demonstrates how to create a buffer description for a single triangle with vertices that contain position and color values.</span></span>


```
struct SimpleVertex
{
    D3DXVECTOR3 Position;  
    D3DXVECTOR3 Color;  
};

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertex ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
```



<span data-ttu-id="0756d-122">Neste exemplo, a descrição do buffer é inicializada com quase todas as configurações padrão para [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**acesso à CPU**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) e [**sinalizadores diversos**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span><span class="sxs-lookup"><span data-stu-id="0756d-122">In this example, the buffer description is initialized with almost all default settings for [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), [**CPU access**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) and [**miscellaneous flags**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_resource_misc_flag).</span></span> <span data-ttu-id="0756d-123">As outras configurações são para o [**sinalizador BIND**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) que identifica o recurso como um buffer de vértice apenas e o tamanho do buffer.</span><span class="sxs-lookup"><span data-stu-id="0756d-123">The other settings are for the [**bind flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) which identifies the resource as a vertex buffer only, and the size of the buffer.</span></span>

<span data-ttu-id="0756d-124">Os sinalizadores de acesso de uso e CPU são importantes para o desempenho.</span><span class="sxs-lookup"><span data-stu-id="0756d-124">The usage and CPU access flags are important for performance.</span></span> <span data-ttu-id="0756d-125">Juntos, esses dois sinalizadores determinam a frequência com que um recurso é acessado, em que tipo de memória o recurso pode ser carregado e qual processador precisa acessar o recurso.</span><span class="sxs-lookup"><span data-stu-id="0756d-125">These two flags together determine how often a resource gets accessed, what type of memory the resource could be loaded into, and what processor needs to access the resource.</span></span> <span data-ttu-id="0756d-126">Uso padrão esse recurso não será atualizado com muita frequência.</span><span class="sxs-lookup"><span data-stu-id="0756d-126">Default usage this resource will not be updated very often.</span></span> <span data-ttu-id="0756d-127">Definir o acesso à CPU como 0 significa que a CPU não precisará ler ou gravar o recurso.</span><span class="sxs-lookup"><span data-stu-id="0756d-127">Setting CPU access to 0 means that the CPU will not need to either read or write the resource.</span></span> <span data-ttu-id="0756d-128">Em combinação, isso significa que o tempo de execução pode carregar o recurso na memória de desempenho mais alta para a GPU, já que o recurso não requer acesso à CPU.</span><span class="sxs-lookup"><span data-stu-id="0756d-128">Taken in combination, this means that the runtime can load the resource into the highest performing memory for the GPU since the resource does not require CPU access.</span></span>

<span data-ttu-id="0756d-129">Como esperado, há uma compensação entre o melhor desempenho e a acessibilidade de qualquer momento por um dos processadores.</span><span class="sxs-lookup"><span data-stu-id="0756d-129">As expected, there is a tradeoff between best performance and any-time accessibility by either processor.</span></span> <span data-ttu-id="0756d-130">Por exemplo, o uso padrão sem acesso à CPU significa que o recurso pode ser disponibilizado para a GPU exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="0756d-130">For example, the default usage with no CPU access means that the resource can be made available to the GPU exclusively.</span></span> <span data-ttu-id="0756d-131">Isso pode incluir o carregamento do recurso na memória não acessível diretamente pela CPU.</span><span class="sxs-lookup"><span data-stu-id="0756d-131">This could include loading the resource into memory not directly accessible by the CPU.</span></span> <span data-ttu-id="0756d-132">O recurso só pode ser modificado com [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span><span class="sxs-lookup"><span data-stu-id="0756d-132">The resource could only be modified with [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource).</span></span>

### <a name="create-the-initialization-data-for-the-buffer"></a><span data-ttu-id="0756d-133">Criar os dados de inicialização para o buffer</span><span class="sxs-lookup"><span data-stu-id="0756d-133">Create the Initialization Data for the Buffer</span></span>

<span data-ttu-id="0756d-134">Um buffer é apenas uma coleção de elementos e é apresentado como uma matriz 1D.</span><span class="sxs-lookup"><span data-stu-id="0756d-134">A buffer is just a collection of elements and is laid out as a 1D array.</span></span> <span data-ttu-id="0756d-135">Como resultado, a densidade de memória do sistema e a densidade da fatia da memória do sistema são as mesmas; o tamanho da declaração de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="0756d-135">As a result, the system memory pitch and system memory slice pitch are both the same; the size of the vertex data declaration.</span></span> <span data-ttu-id="0756d-136">Um aplicativo pode fornecer dados de inicialização quando um buffer é criado usando uma [**Descrição de subrecurso**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), que contém um ponteiro para os dados do recurso real e contém informações sobre o tamanho e o layout desses dados.</span><span class="sxs-lookup"><span data-stu-id="0756d-136">An application can provide initialization data when a buffer is created using a [**subresource description**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data), which contains a pointer to the actual resource data and contains information about the size and layout of that data.</span></span>

<span data-ttu-id="0756d-137">Qualquer buffer criado com uso imutável (consulte [**d3d10 \_ Usage \_ imutável**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) deve ser inicializado no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="0756d-137">Any buffer created with immutable usage (see [**D3D10\_USAGE\_IMMUTABLE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)) must be initialized at creation time.</span></span> <span data-ttu-id="0756d-138">Os buffers que usam qualquer um dos outros sinalizadores de uso podem ser atualizados após a inicialização usando [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)e [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), ou acessando sua memória subjacente usando o método [**MAP**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) .</span><span class="sxs-lookup"><span data-stu-id="0756d-138">Buffers that use any of the other usage flags can be updated after initialization using [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource), [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion), and [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource), or by accessing its underlying memory using the [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10buffer-map) method.</span></span>

### <a name="create-the-buffer"></a><span data-ttu-id="0756d-139">Criar o buffer</span><span class="sxs-lookup"><span data-stu-id="0756d-139">Create the Buffer</span></span>

<span data-ttu-id="0756d-140">Usar a descrição do buffer e os dados de inicialização (que é opcional) chamar [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) para criar um buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="0756d-140">Using the buffer description and the initialization data (which is optional) call [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) to create a vertex buffer.</span></span> <span data-ttu-id="0756d-141">O trecho de código a seguir demonstra como criar um buffer de vértice de uma matriz de dados de vértice declarada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0756d-141">The following code snippet demonstrates how to create a vertex buffer from an array of vertex data declared by the application.</span></span>


```
struct SimpleVertexCombined
{
    D3DXVECTOR3 Pos;  
    D3DXVECTOR3 Col;  
};


ID3D10InputLayout* g_pVertexLayout = NULL;
ID3D10Buffer*      g_pVertexBuffer[2] = { NULL, NULL };
ID3D10Buffer*      g_pIndexBuffer = NULL;


SimpleVertexCombined verticesCombo[] =
{
    D3DXVECTOR3( 0.0f, 0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.0f, 0.5f ),
    D3DXVECTOR3( 0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.5f, 0.0f, 0.0f ),
    D3DXVECTOR3( -0.5f, -0.5f, 0.5f ),
    D3DXVECTOR3( 0.0f, 0.5f, 0.0f ),
};


    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage            = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth        = sizeof( SimpleVertexCombined ) * 3;
    bufferDesc.BindFlags        = D3D10_BIND_VERTEX_BUFFER;
    bufferDesc.CPUAccessFlags   = 0;
    bufferDesc.MiscFlags        = 0;
    
    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = verticesCombo;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pVertexBuffer[0] );
```



## <a name="create-an-index-buffer"></a><span data-ttu-id="0756d-142">Criar um buffer de índice</span><span class="sxs-lookup"><span data-stu-id="0756d-142">Create an Index Buffer</span></span>

<span data-ttu-id="0756d-143">A criação de um buffer de índice é muito semelhante à criação de um buffer de vértice; com duas diferenças.</span><span class="sxs-lookup"><span data-stu-id="0756d-143">Creating an index buffer is very similar to creating a vertex buffer; with two differences.</span></span> <span data-ttu-id="0756d-144">Um buffer de índice contém apenas dados de 16 bits ou 32 bits (em vez da ampla gama de formatos disponíveis para um buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="0756d-144">An index buffer contains only 16-bit or 32-bit data (instead of the wide range of formats available to a vertex buffer.</span></span> <span data-ttu-id="0756d-145">Um buffer de índice também requer um sinalizador de ligação de buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="0756d-145">An index buffer also requires an index-buffer bind flag.</span></span>

<span data-ttu-id="0756d-146">O exemplo a seguir demonstra como criar um buffer de índice de uma matriz de dados de índice.</span><span class="sxs-lookup"><span data-stu-id="0756d-146">The following example demonstrates how to create an index buffer from an array of index data.</span></span>


```
ID3D10Buffer *g_pIndexBuffer = NULL;

    // Create indices
    unsigned int indices[] = { 0, 1, 2 };

    D3D10_BUFFER_DESC bufferDesc;
    bufferDesc.Usage           = D3D10_USAGE_DEFAULT;
    bufferDesc.ByteWidth       = sizeof( unsigned int ) * 3;
    bufferDesc.BindFlags       = D3D10_BIND_INDEX_BUFFER;
    bufferDesc.CPUAccessFlags  = 0;
    bufferDesc.MiscFlags       = 0;

    D3D10_SUBRESOURCE_DATA InitData;
    InitData.pSysMem = indices;
    InitData.SysMemPitch = 0;
    InitData.SysMemSlicePitch = 0;
    hr = g_pd3dDevice->CreateBuffer( &bufferDesc, &InitData, &g_pIndexBuffer );
    if( FAILED( hr ) )
        return hr;
  
    g_pd3dDevice->IASetIndexBuffer( g_pIndexBuffer, DXGI_FORMAT_R32_UINT, 0 );
```



## <a name="create-a-constant-buffer"></a><span data-ttu-id="0756d-147">Criar um buffer de constantes</span><span class="sxs-lookup"><span data-stu-id="0756d-147">Create a Constant Buffer</span></span>

<span data-ttu-id="0756d-148">O Direct3D 10 introduz um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="0756d-148">Direct3D 10 introduces a constant buffer.</span></span> <span data-ttu-id="0756d-149">Um buffer de constante, ou buffer de constante de sombreador, é um buffer que contém constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0756d-149">A constant buffer, or shader constant buffer, is a buffer that contains shader constants.</span></span> <span data-ttu-id="0756d-150">Aqui está um exemplo de criação de um buffer constante, extraído do [exemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="0756d-150">Here is an example of creating a constant buffer, taken from the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>


```
ID3D10Buffer*   g_pConstantBuffer10 = NULL;

struct VS_CONSTANT_BUFFER
{
    D3DXMATRIX mWorldViewProj;      //mWorldViewProj will probably be global to all shaders in a project.
                                    //It's a good idea not to move it around between shaders.
    D3DXVECTOR4 vSomeVectorThatMayBeNeededByASpecificShader;
    float fSomeFloatThatMayBeNeededByASpecificShader;
    float fTime;                    //fTime may also be global to all shaders in a project.
    float fSomeFloatThatMayBeNeededByASpecificShader2;
    float fSomeFloatThatMayBeNeededByASpecificShader3;
};

    D3D10_BUFFER_DESC cbDesc;
    cbDesc.ByteWidth = sizeof( VS_CONSTANT_BUFFER );
    cbDesc.Usage = D3D10_USAGE_DYNAMIC;
    cbDesc.BindFlags = D3D10_BIND_CONSTANT_BUFFER;
    cbDesc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
    cbDesc.MiscFlags = 0;
    hr = g_pd3dDevice->CreateBuffer( &cbDesc, NULL, &g_pConstantBuffer10 );
    if( FAILED( hr ) )
       return hr;

    g_pd3dDevice->VSSetConstantBuffers( 0, 1, g_pConstantBuffer10 );
```



<span data-ttu-id="0756d-151">Observe que, ao usar a interface de [**interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) , o processo de criação, associação e confirmação de um buffer constante é manipulado pela instância da **interface ID3D10Effect** .</span><span class="sxs-lookup"><span data-stu-id="0756d-151">Note that when using the [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) interface the process of creating, binding and comitting a constant buffer is handled by the **ID3D10Effect Interface** instance.</span></span> <span data-ttu-id="0756d-152">Nesse caso, só nescesary obter a variável do efeito com um dos métodos getvariance, como [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) , e atualizar a variável com um dos métodos SetVariable, como [**setmatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span><span class="sxs-lookup"><span data-stu-id="0756d-152">In that case it is only nescesary to get the variable from the effect with one of the GetVariable methods such as [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) and update the variable with one of the SetVariable methods such as [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix).</span></span> <span data-ttu-id="0756d-153">Para obter um exemplo de como usar a **interface ID3D10Effect** para gerenciar um buffer de constantes [, consulte Tutorial 7: mapeamento de textura e buffers de constantes](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="0756d-153">For an example of using **ID3D10Effect Interface** to manage a constant buffer see [Tutorial 7: Texture Mapping and Constant Buffers](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0756d-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0756d-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0756d-155">Recursos (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="0756d-155">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



