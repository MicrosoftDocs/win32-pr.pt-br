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
# <a name="how-to-create-a-constant-buffer"></a><span data-ttu-id="946af-104">Como: criar um buffer de constantes</span><span class="sxs-lookup"><span data-stu-id="946af-104">How to: Create a Constant Buffer</span></span>

<span data-ttu-id="946af-105">[Buffers de constantes](overviews-direct3d-11-resources-buffers-intro.md) contêm dados de constante de sombreador.</span><span class="sxs-lookup"><span data-stu-id="946af-105">[Constant buffers](overviews-direct3d-11-resources-buffers-intro.md) contain shader constant data.</span></span> <span data-ttu-id="946af-106">Este tópico mostra como inicializar um [buffer de constantes](overviews-direct3d-11-resources-buffers-intro.md) na preparação para renderização.</span><span class="sxs-lookup"><span data-stu-id="946af-106">This topic shows how to initialize a [constant buffer](overviews-direct3d-11-resources-buffers-intro.md) in preparation for rendering.</span></span>

<span data-ttu-id="946af-107">**Para inicializar um buffer de constantes**</span><span class="sxs-lookup"><span data-stu-id="946af-107">**To initialize a constant buffer**</span></span>

1.  <span data-ttu-id="946af-108">Defina uma estrutura que descreve os dados constantes do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="946af-108">Define a structure that describes the vertex shader constant data.</span></span>
2.  <span data-ttu-id="946af-109">Aloque memória para a estrutura que você definiu na etapa um.</span><span class="sxs-lookup"><span data-stu-id="946af-109">Allocate memory for the structure that you defined in step one.</span></span> <span data-ttu-id="946af-110">Preencha esse buffer com dados constantes de sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="946af-110">Fill this buffer with vertex shader constant data.</span></span> <span data-ttu-id="946af-111">Você pode usar **malloc** ou **New** para alocar a memória ou pode alocar memória para a estrutura da pilha.</span><span class="sxs-lookup"><span data-stu-id="946af-111">You can use **malloc** or **new** to allocate the memory, or you can allocate memory for the structure from the stack.</span></span>
3.  <span data-ttu-id="946af-112">Crie uma descrição de buffer preenchendo uma estrutura [**\_ \_ desc de buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) .</span><span class="sxs-lookup"><span data-stu-id="946af-112">Create a buffer description by filling in a [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure.</span></span> <span data-ttu-id="946af-113">Passe o \_ sinalizador de \_ buffer constante de ligação D3D11 \_ para o membro **BindFlags** e passe o tamanho da estrutura de descrição de buffer constante em bytes para o membro **ByteWidth** .</span><span class="sxs-lookup"><span data-stu-id="946af-113">Pass the D3D11\_BIND\_CONSTANT\_BUFFER flag to the **BindFlags** member and pass the size of the constant buffer description structure in bytes to the **ByteWidth** member.</span></span>

    > [!Note]  
    > <span data-ttu-id="946af-114">O \_ sinalizador de \_ buffer constante de ligação D3D11 \_ não pode ser combinado com nenhum outro sinalizador.</span><span class="sxs-lookup"><span data-stu-id="946af-114">The D3D11\_BIND\_CONSTANT\_BUFFER flag cannot be combined with any other flags.</span></span>

     

4.  <span data-ttu-id="946af-115">Crie uma descrição de dados de subrecurso preenchendo uma estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) .</span><span class="sxs-lookup"><span data-stu-id="946af-115">Create a subresource data description by filling in a [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure.</span></span> <span data-ttu-id="946af-116">O membro **pSysMem** da estrutura **de \_ \_ dados do subrecurso D3D11** deve apontar diretamente para os dados constantes de sombreador de vértice que você criou na etapa dois.</span><span class="sxs-lookup"><span data-stu-id="946af-116">The **pSysMem** member of the **D3D11\_SUBRESOURCE\_DATA** structure must point directly to the vertex shader constant data that you created in step two.</span></span>
5.  <span data-ttu-id="946af-117">Chame [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) enquanto passa a [**estrutura \_ \_ Desc do buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) , a estrutura de [**\_ \_ dados de subrecurso do D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) e o endereço de um ponteiro para a interface [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) para inicializar.</span><span class="sxs-lookup"><span data-stu-id="946af-117">Call [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) while passing the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure, the [**D3D11\_SUBRESOURCE\_DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data) structure, and the address of a pointer to the [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer) interface to initialize.</span></span>

<span data-ttu-id="946af-118">Esses exemplos de código demonstram como criar um buffer constante.</span><span class="sxs-lookup"><span data-stu-id="946af-118">These code examples demonstrate how to create a constant buffer.</span></span>

<span data-ttu-id="946af-119">Este exemplo pressupõe que **g \_ pd3dDevice** é um objeto [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) válido e que **g \_ pd3dContext** é um objeto [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) válido.</span><span class="sxs-lookup"><span data-stu-id="946af-119">This example assumes that **g\_pd3dDevice** is a valid [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) object and that **g\_pd3dContext** is a valid [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) object.</span></span>


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



<span data-ttu-id="946af-120">Este exemplo mostra a definição HLSL CBuffer associada.</span><span class="sxs-lookup"><span data-stu-id="946af-120">This example shows the associated HLSL cbuffer definition.</span></span>

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
> <span data-ttu-id="946af-121">Certifique-se de corresponder o \_ layout de memória de buffer de constante vs \_ em C++ com o layout HLSL.</span><span class="sxs-lookup"><span data-stu-id="946af-121">Make sure to match the VS\_CONSTANT\_BUFFER memory layout in C++ with the HLSL layout.</span></span> <span data-ttu-id="946af-122">Para obter informações sobre como o HLSL manipula o layout na memória, consulte [regras de empacotamento para variáveis constantes](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span><span class="sxs-lookup"><span data-stu-id="946af-122">For info about how HLSL handles layout in memory, see [Packing Rules for Constant Variables](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="946af-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="946af-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="946af-124">Buffers</span><span class="sxs-lookup"><span data-stu-id="946af-124">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)
</dt> <dt>

[<span data-ttu-id="946af-125">Como usar o Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="946af-125">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 