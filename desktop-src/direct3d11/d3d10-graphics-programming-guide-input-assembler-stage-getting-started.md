---
title: Introdução com o estágio de Input-Assembler
description: Há algumas etapas necessárias para inicializar o estágio de IA (assembler de entrada).
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901b3facfef781e3f44acf75bee737f280dece55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366256"
---
# <a name="getting-started-with-the-input-assembler-stage"></a><span data-ttu-id="58158-103">Introdução com o estágio de Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="58158-103">Getting Started with the Input-Assembler Stage</span></span>

<span data-ttu-id="58158-104">Há algumas etapas necessárias para inicializar o estágio de IA (assembler de entrada).</span><span class="sxs-lookup"><span data-stu-id="58158-104">There are a few steps necessary to initialize the input-assembler (IA) stage.</span></span> <span data-ttu-id="58158-105">Por exemplo, você precisa criar recursos de buffer com os dados de vértice que o pipeline precisa, dizer ao estágio IA onde estão os buffers e que tipo de dados eles contêm, e especificar o tipo de primitivas a serem montadas dos dados.</span><span class="sxs-lookup"><span data-stu-id="58158-105">For example, you need to create buffer resources with the vertex data that the pipeline needs, tell the IA stage where the buffers are and what type of data they contain, and specify the type of primitives to assemble from the data.</span></span>

<span data-ttu-id="58158-106">As etapas básicas envolvidas na configuração do estágio IA, mostrada na tabela a seguir, são abordadas neste tópico.</span><span class="sxs-lookup"><span data-stu-id="58158-106">The basic steps involved in setting up the IA stage, shown in the following table, are covered in this topic.</span></span>



| <span data-ttu-id="58158-107">Etapa</span><span class="sxs-lookup"><span data-stu-id="58158-107">Step</span></span>                                                                                    | <span data-ttu-id="58158-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="58158-108">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58158-109">Criar buffers de entrada</span><span class="sxs-lookup"><span data-stu-id="58158-109">Create Input Buffers</span></span>](#create-input-buffers)                                           | <span data-ttu-id="58158-110">Crie e inicialize buffers de entrada com dados de vértice de entrada.</span><span class="sxs-lookup"><span data-stu-id="58158-110">Create and initialize input buffers with input vertex data.</span></span>                                           |
| [<span data-ttu-id="58158-111">Criar o objeto Input-Layout</span><span class="sxs-lookup"><span data-stu-id="58158-111">Create the Input-Layout Object</span></span>](#create-the-input-layout-object)                       | <span data-ttu-id="58158-112">Defina como os dados de buffer de vértice serão transmitidos para o estágio IA usando um objeto de layout de entrada.</span><span class="sxs-lookup"><span data-stu-id="58158-112">Define how the vertex buffer data will be streamed into the IA stage by using an input-layout object.</span></span> |
| [<span data-ttu-id="58158-113">Associar objetos ao estágio de Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="58158-113">Bind Objects to the Input-Assembler Stage</span></span>](#bind-objects-to-the-input-assembler-stage) | <span data-ttu-id="58158-114">Associe os objetos criados (buffers de entrada e o objeto de layout de entrada) ao estágio IA.</span><span class="sxs-lookup"><span data-stu-id="58158-114">Bind the created objects (input buffers and the input-layout object) to the IA stage.</span></span>                 |
| [<span data-ttu-id="58158-115">Especificar o tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="58158-115">Specify the Primitive Type</span></span>](#specify-the-primitive-type)                               | <span data-ttu-id="58158-116">Identifique como os vértices serão montados em primitivos.</span><span class="sxs-lookup"><span data-stu-id="58158-116">Identify how the vertices will be assembled into primitives.</span></span>                                          |
| [<span data-ttu-id="58158-117">Chamar métodos Draw</span><span class="sxs-lookup"><span data-stu-id="58158-117">Call Draw Methods</span></span>](#call-draw-methods)                                                 | <span data-ttu-id="58158-118">Envie os dados associados ao estágio IA por meio do pipeline.</span><span class="sxs-lookup"><span data-stu-id="58158-118">Send the data bound to the IA stage through the pipeline.</span></span>                                             |



 

<span data-ttu-id="58158-119">Depois de entender essas etapas, vá para [usando System-Generated valores](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span><span class="sxs-lookup"><span data-stu-id="58158-119">After you understand these steps, move on to [Using System-Generated Values](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span></span>

## <a name="create-input-buffers"></a><span data-ttu-id="58158-120">Criar buffers de entrada</span><span class="sxs-lookup"><span data-stu-id="58158-120">Create Input Buffers</span></span>

<span data-ttu-id="58158-121">Há dois tipos de buffers de entrada: [buffers de vértices](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e buffers de índice.</span><span class="sxs-lookup"><span data-stu-id="58158-121">There are two types of input buffers: [vertex buffers](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and index buffers.</span></span> <span data-ttu-id="58158-122">Os buffers de vértice fornecem dados de vértice para o estágio IA.</span><span class="sxs-lookup"><span data-stu-id="58158-122">Vertex buffers supply vertex data to the IA stage.</span></span> <span data-ttu-id="58158-123">Buffers de índice são opcionais; Eles fornecem índices para vértices do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="58158-123">Index buffers are optional; they provide indices to vertices from the vertex buffer.</span></span> <span data-ttu-id="58158-124">Você pode criar um ou mais buffers de vértice e, opcionalmente, um buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="58158-124">You may create one or more vertex buffers and, optionally, an index buffer.</span></span>

<span data-ttu-id="58158-125">Depois de criar os recursos de buffer, você precisa criar um objeto de layout de entrada para descrever o layout de dados para o estágio IA e, em seguida, você precisa associar os recursos de buffer ao estágio IA.</span><span class="sxs-lookup"><span data-stu-id="58158-125">After you create the buffer resources, you need to create an input-layout object to describe the data layout to the IA stage, and then you need to bind the buffer resources to the IA stage.</span></span> <span data-ttu-id="58158-126">A criação e a associação de buffers não são necessárias se os sombreadores não usam buffers.</span><span class="sxs-lookup"><span data-stu-id="58158-126">Creating and binding buffers is not necessary if your shaders don't use buffers.</span></span> <span data-ttu-id="58158-127">Para obter um exemplo de um vértice simples e um sombreador de pixel que desenha um único triângulo, consulte [usando o estágio de Input-Assembler sem buffers](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="58158-127">For an example of a simple vertex and pixel shader that draws a single triangle, see [Using the Input-Assembler Stage without Buffers](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span></span>

<span data-ttu-id="58158-128">Para obter ajuda com a criação de um buffer de vértice, consulte [criar um buffer de vértice](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="58158-128">For help with creating a vertex buffer, see [Create a Vertex Buffer](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span> <span data-ttu-id="58158-129">Para obter ajuda com a criação de um buffer de índice, consulte criar um buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="58158-129">For help with creating an index buffer, see Create an Index Buffer.</span></span>

## <a name="create-the-input-layout-object"></a><span data-ttu-id="58158-130">Criar o objeto Input-Layout</span><span class="sxs-lookup"><span data-stu-id="58158-130">Create the Input-Layout Object</span></span>

<span data-ttu-id="58158-131">O objeto de layout de entrada encapsula o estado de entrada do estágio IA.</span><span class="sxs-lookup"><span data-stu-id="58158-131">The input-layout object encapsulates the input state of the IA stage.</span></span> <span data-ttu-id="58158-132">Isso inclui uma descrição dos dados de entrada que estão associados ao estágio IA.</span><span class="sxs-lookup"><span data-stu-id="58158-132">This includes a description of the input data that is bound to the IA stage.</span></span> <span data-ttu-id="58158-133">Os dados são transmitidos para o estágio IA da memória, de um ou mais buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="58158-133">The data is streamed into the IA stage from memory, from one or more vertex buffers.</span></span> <span data-ttu-id="58158-134">A descrição identifica os dados de entrada que são associados de um ou mais buffers de vértice e dá ao tempo de execução a capacidade de verificar os tipos de dados de entrada em relação aos tipos de parâmetro de entrada do sombreador.</span><span class="sxs-lookup"><span data-stu-id="58158-134">The description identifies the input data that is bound from one or more vertex buffers and gives the runtime the ability to check the input data types against the shader input parameter types.</span></span> <span data-ttu-id="58158-135">Essa verificação de tipo não apenas verifica se os tipos são compatíveis, mas também se cada um dos elementos que o sombreador exige está disponível nos recursos de buffer.</span><span class="sxs-lookup"><span data-stu-id="58158-135">This type checking not only verifies that the types are compatible, but also that each of the elements that the shader requires is available in the buffer resources.</span></span>

<span data-ttu-id="58158-136">Um objeto de layout de entrada é criado a partir de uma matriz de descrições de elementos de entrada e um ponteiro para o sombreador compilado (consulte [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span><span class="sxs-lookup"><span data-stu-id="58158-136">An input-layout object is created from an array of input-element descriptions and a pointer to the compiled shader (see [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span></span> <span data-ttu-id="58158-137">A matriz contém um ou mais elementos de entrada; cada elemento input descreve um único elemento de dados Vertex de um único buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="58158-137">The array contains one or more input elements; each input element describes a single vertex-data element from a single vertex buffer.</span></span> <span data-ttu-id="58158-138">O conjunto inteiro de descrições de elementos de entrada descreve todos os elementos de dados de vértice de todos os buffers de vértices que serão associados ao estágio IA.</span><span class="sxs-lookup"><span data-stu-id="58158-138">The entire set of input-element descriptions describes all of the vertex-data elements from all of the vertex buffers that will be bound to the IA stage.</span></span>

<span data-ttu-id="58158-139">A descrição de layout a seguir descreve um único buffer de vértice que contém três elementos de dados de vértice:</span><span class="sxs-lookup"><span data-stu-id="58158-139">The following layout description describes a single vertex buffer that contains three vertex-data elements:</span></span>


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



<span data-ttu-id="58158-140">Uma descrição de elemento de entrada descreve cada elemento contido por um único vértice em um buffer de vértice, incluindo tamanho, tipo, local e finalidade.</span><span class="sxs-lookup"><span data-stu-id="58158-140">An input-element description describes each element contained by a single vertex in a vertex buffer, including size, type, location, and purpose.</span></span> <span data-ttu-id="58158-141">Cada linha identifica o tipo de dados usando a semântica, o índice semântico e o formato de dados.</span><span class="sxs-lookup"><span data-stu-id="58158-141">Each row identifies the type of data by using the semantic, the semantic index, and the data format.</span></span> <span data-ttu-id="58158-142">Uma [semântica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) é uma cadeia de texto que identifica como os dados serão usados.</span><span class="sxs-lookup"><span data-stu-id="58158-142">A [semantic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) is a text string that identifies how the data will be used.</span></span> <span data-ttu-id="58158-143">Neste exemplo, a primeira linha identifica os dados de posição de 3 componentes (*XYZ*, por exemplo); a segunda linha identifica dados de textura de dois componentes (*UV*, por exemplo); e a terceira linha identifica dados normais.</span><span class="sxs-lookup"><span data-stu-id="58158-143">In this example, the first row identifies 3-component position data (*xyz*, for example); the second row identifies 2-component texture data (*UV*, for example); and the third row identifies normal data.</span></span>

<span data-ttu-id="58158-144">Neste exemplo de uma descrição de elemento de entrada, o índice semântico (que é o segundo parâmetro) é definido como zero para todas as três linhas.</span><span class="sxs-lookup"><span data-stu-id="58158-144">In this example of an input-element description, the semantic index (which is the second parameter) is set to zero for all three rows.</span></span> <span data-ttu-id="58158-145">O índice semântico ajuda a distinguir entre duas linhas que usam a mesma semântica.</span><span class="sxs-lookup"><span data-stu-id="58158-145">The semantic index helps distinguish between two rows that use the same semantics.</span></span> <span data-ttu-id="58158-146">Como não há semântica semelhante neste exemplo, o índice semântico pode ser definido como seu valor padrão, zero.</span><span class="sxs-lookup"><span data-stu-id="58158-146">Since there are no similar semantics in this example, the semantic index can be set to its default value, zero.</span></span>

<span data-ttu-id="58158-147">O terceiro parâmetro é o *formato*.</span><span class="sxs-lookup"><span data-stu-id="58158-147">The third parameter is the *format*.</span></span> <span data-ttu-id="58158-148">O formato (consulte [**o \_ formato dxgi**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) especifica o número de componentes por elemento e o tipo de dados, que define o tamanho dos dados para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="58158-148">The format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) specifies the number of components per element, and the data type, which defines the size of the data for each element.</span></span> <span data-ttu-id="58158-149">O formato pode ser totalmente digitado no momento da criação do recurso ou você pode criar um recurso usando um **\_ formato dxgi**, que identifica o número de componentes em um elemento, mas deixa o tipo de dados indefinido.</span><span class="sxs-lookup"><span data-stu-id="58158-149">The format can be fully typed at the time of resource creation, or you may create a resource by using a **DXGI\_FORMAT**, which identifies the number of components in an element, but leaves the data type undefined.</span></span>

### <a name="input-slots"></a><span data-ttu-id="58158-150">Slots de entrada</span><span class="sxs-lookup"><span data-stu-id="58158-150">Input Slots</span></span>

<span data-ttu-id="58158-151">Os dados entram no estágio IA por meio de entradas chamadas de *Slots de entrada*, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="58158-151">Data enters the IA stage through inputs called *input slots*, as shown in the following illustration.</span></span> <span data-ttu-id="58158-152">O estágio IA tem *n* slots de entrada, que são projetados para acomodar até *n* buffers de vértices que fornecem dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="58158-152">The IA stage has *n* input slots, which are designed to accommodate up to *n* vertex buffers that provide input data.</span></span> <span data-ttu-id="58158-153">Cada buffer de vértice deve ser atribuído a um slot diferente; essas informações são armazenadas na declaração de layout de entrada quando o objeto de layout de entrada é criado.</span><span class="sxs-lookup"><span data-stu-id="58158-153">Each vertex buffer must be assigned to a different slot; this information is stored in the input-layout declaration when the input-layout object is created.</span></span> <span data-ttu-id="58158-154">Você também pode especificar um deslocamento do início de cada buffer para o primeiro elemento no buffer a ser lido.</span><span class="sxs-lookup"><span data-stu-id="58158-154">You may also specify an offset from the start of each buffer to the first element in the buffer to be read.</span></span>

![Ilustração dos slots de entrada para o estágio ia](images/d3d10-ia-slots.png)

<span data-ttu-id="58158-156">Os próximos dois parâmetros são o *slot de entrada* e o *deslocamento de entrada*.</span><span class="sxs-lookup"><span data-stu-id="58158-156">The next two parameters are the *input slot* and the *input offset*.</span></span> <span data-ttu-id="58158-157">Ao usar vários buffers, você pode associá-los a um ou mais slots de entrada.</span><span class="sxs-lookup"><span data-stu-id="58158-157">When you use multiple buffers, you can bind them to one or more input slots.</span></span> <span data-ttu-id="58158-158">O deslocamento de entrada é o número de bytes entre o início do buffer e o início dos dados.</span><span class="sxs-lookup"><span data-stu-id="58158-158">The input offset is the number of bytes between the start of the buffer and the beginning of the data.</span></span>

### <a name="reusing-input-layout-objects"></a><span data-ttu-id="58158-159">Reutilizando Input-Layout objetos</span><span class="sxs-lookup"><span data-stu-id="58158-159">Reusing Input-Layout Objects</span></span>

<span data-ttu-id="58158-160">Cada objeto de layout de entrada é criado com base em uma assinatura de sombreador; Isso permite que a API valide os elementos Input-layout-Object em relação à assinatura de entrada do sombreador para garantir que haja uma correspondência exata dos tipos e da semântica.</span><span class="sxs-lookup"><span data-stu-id="58158-160">Each input-layout object is created based on a shader signature; this allows the API to validate the input-layout-object elements against the shader-input signature to make sure that there is an exact match of types and semantics.</span></span> <span data-ttu-id="58158-161">Você pode criar um único objeto de layout de entrada para muitos sombreadores, desde que todas as assinaturas de entrada de sombreador tenham correspondência exata.</span><span class="sxs-lookup"><span data-stu-id="58158-161">You can create a single input-layout object for many shaders, as long as all of the shader-input signatures exactly match.</span></span>

## <a name="bind-objects-to-the-input-assembler-stage"></a><span data-ttu-id="58158-162">Associar objetos ao estágio de Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="58158-162">Bind Objects to the Input-Assembler Stage</span></span>

<span data-ttu-id="58158-163">Depois de criar os recursos de buffer de vértice e um objeto de layout de entrada, você pode associá-los ao estágio IA chamando [**ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) e [**ID3D11DeviceContext:: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span><span class="sxs-lookup"><span data-stu-id="58158-163">After you create vertex buffer resources and an input layout object, you can bind them to the IA stage by calling [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) and [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span></span> <span data-ttu-id="58158-164">O exemplo a seguir mostra a associação de um único buffer de vértice e um objeto de layout de entrada ao estágio IA:</span><span class="sxs-lookup"><span data-stu-id="58158-164">The following example shows the binding of a single vertex buffer and an input-layout object to the IA stage:</span></span>


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



<span data-ttu-id="58158-165">A vinculação do objeto de layout de entrada requer apenas um ponteiro para o objeto.</span><span class="sxs-lookup"><span data-stu-id="58158-165">Binding the input-layout object only requires a pointer to the object.</span></span>

<span data-ttu-id="58158-166">No exemplo anterior, um único buffer de vértice é associado; no entanto, vários buffers de vértice podem ser associados por uma única chamada para [**ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), e o código a seguir mostra tal chamada para associar os buffers de três vértices:</span><span class="sxs-lookup"><span data-stu-id="58158-166">In the preceding example, a single vertex buffer is bound; however, multiple vertex buffers can be bound by a single call to [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), and the following code shows such a call to bind three vertex buffers:</span></span>


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



<span data-ttu-id="58158-167">Um buffer de índice é associado ao estágio IA chamando [**ID3D11DeviceContext:: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span><span class="sxs-lookup"><span data-stu-id="58158-167">An index buffer is bound to the IA stage by calling [**ID3D11DeviceContext::IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span></span>

## <a name="specify-the-primitive-type"></a><span data-ttu-id="58158-168">Especificar o tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="58158-168">Specify the Primitive Type</span></span>

<span data-ttu-id="58158-169">Depois que os buffers de entrada tiverem sido associados, o estágio IA deve ser informado como montar os vértices em primitivos.</span><span class="sxs-lookup"><span data-stu-id="58158-169">After the input buffers have been bound, the IA stage must be told how to assemble the vertices into primitives.</span></span> <span data-ttu-id="58158-170">Isso é feito especificando o [tipo primitivo](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) chamando [**ID3D11DeviceContext:: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); o código a seguir chama essa função para definir os dados como uma lista de triângulo sem adjacências:</span><span class="sxs-lookup"><span data-stu-id="58158-170">This is done by specifying the [primitive type](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) by calling [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); the following code calls this function to define the data as a triangle list without adjacency:</span></span>


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



<span data-ttu-id="58158-171">O restante dos tipos primitivos são listados na [**\_ \_ topologia primitiva do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span><span class="sxs-lookup"><span data-stu-id="58158-171">The rest of the primitive types are listed in [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span></span>

## <a name="call-draw-methods"></a><span data-ttu-id="58158-172">Chamar métodos Draw</span><span class="sxs-lookup"><span data-stu-id="58158-172">Call Draw Methods</span></span>

<span data-ttu-id="58158-173">Depois que os recursos de entrada tiverem sido associados ao pipeline, um aplicativo chamará um método Draw para renderizar primitivos.</span><span class="sxs-lookup"><span data-stu-id="58158-173">After input resources have been bound to the pipeline, an application calls a draw method to render primitives.</span></span> <span data-ttu-id="58158-174">Há vários métodos de desenho, que são mostrados na tabela a seguir; alguns buffers de índice de uso, alguns usam dados de instância, e alguns dados de reutilização do estágio de saída de streaming como entrada para o estágio de Assembler de entrada.</span><span class="sxs-lookup"><span data-stu-id="58158-174">There are several draw methods, which are shown in the following table; some use index buffers, some use instance data, and some reuse data from the streaming-output stage as input to the input-assembler stage.</span></span>



| <span data-ttu-id="58158-175">Métodos Draw</span><span class="sxs-lookup"><span data-stu-id="58158-175">Draw Methods</span></span>                                                                                  | <span data-ttu-id="58158-176">Description</span><span class="sxs-lookup"><span data-stu-id="58158-176">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58158-177">**ID3D11DeviceContext::Draw**</span><span class="sxs-lookup"><span data-stu-id="58158-177">**ID3D11DeviceContext::Draw**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | <span data-ttu-id="58158-178">Desenhe primitivos não indexados e não de instância.</span><span class="sxs-lookup"><span data-stu-id="58158-178">Draw non-indexed, non-instanced primitives.</span></span>                                                            |
| [<span data-ttu-id="58158-179">**ID3D11DeviceContext::DrawInstanced**</span><span class="sxs-lookup"><span data-stu-id="58158-179">**ID3D11DeviceContext::DrawInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | <span data-ttu-id="58158-180">Desenhe primitivos com instância não indexada.</span><span class="sxs-lookup"><span data-stu-id="58158-180">Draw non-indexed, instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="58158-181">**ID3D11DeviceContext::DrawIndexed**</span><span class="sxs-lookup"><span data-stu-id="58158-181">**ID3D11DeviceContext::DrawIndexed**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | <span data-ttu-id="58158-182">Desenhe primitivos indexados e não-instância.</span><span class="sxs-lookup"><span data-stu-id="58158-182">Draw indexed, non-instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="58158-183">**ID3D11DeviceContext::DrawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="58158-183">**ID3D11DeviceContext::DrawIndexedInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | <span data-ttu-id="58158-184">Desenhe primitivos indexados e com instância.</span><span class="sxs-lookup"><span data-stu-id="58158-184">Draw indexed, instanced primitives.</span></span>                                                                    |
| [<span data-ttu-id="58158-185">**ID3D11DeviceContext::DrawAuto**</span><span class="sxs-lookup"><span data-stu-id="58158-185">**ID3D11DeviceContext::DrawAuto**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | <span data-ttu-id="58158-186">Desenhe primitivos não indexados e não-instância de dados de entrada provenientes do estágio streaming-output.</span><span class="sxs-lookup"><span data-stu-id="58158-186">Draw non-indexed, non-instanced primitives from input data that comes from the streaming-output stage.</span></span> |



 

<span data-ttu-id="58158-187">Cada método Draw renderiza um único tipo de topologia.</span><span class="sxs-lookup"><span data-stu-id="58158-187">Each draw method renders a single topology type.</span></span> <span data-ttu-id="58158-188">Durante a renderização, os primitivos incompletos (aqueles sem vértices suficientes, não há índices, primitivos parciais e assim por diante) são silenciosamente descartados.</span><span class="sxs-lookup"><span data-stu-id="58158-188">During rendering, incomplete primitives (those without enough vertices, lacking indices, partial primitives, and so on) are silently discarded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58158-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="58158-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58158-190">Estágio de Assembler de entrada</span><span class="sxs-lookup"><span data-stu-id="58158-190">Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 