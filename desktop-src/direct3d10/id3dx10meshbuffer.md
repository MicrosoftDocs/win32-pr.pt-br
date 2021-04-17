---
description: Um buffer de malha é um buffer que contém dados sobre uma malha.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: Interface ID3DX10MeshBuffer (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 42076393c3be5443688ec4db954131935b62f696
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105752817"
---
# <a name="id3dx10meshbuffer-interface"></a><span data-ttu-id="793e0-103">Interface ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="793e0-103">ID3DX10MeshBuffer interface</span></span>

<span data-ttu-id="793e0-104">Um buffer de malha é um buffer que contém dados sobre uma malha.</span><span class="sxs-lookup"><span data-stu-id="793e0-104">A mesh buffer is a buffer that contains data about a mesh.</span></span> <span data-ttu-id="793e0-105">Ele pode conter um dos cinco tipos diferentes de dados: dados de vértice, dados de índice, dados de adjacência, dados de atributo ou dados de representante de ponto.</span><span class="sxs-lookup"><span data-stu-id="793e0-105">It can contain one of five different types of data: vertex data, index data, adjacency data, attribute data, or point rep data.</span></span> <span data-ttu-id="793e0-106">A estrutura é usada para acessar esses cinco tipos de dados por meio das cinco APIs a seguir: [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh:: GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh:: GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md)ou [**ID3DX10Mesh:: GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="793e0-106">The structure is used to access these five pieces of data through the following five APIs: [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh::GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh::GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md), or [**ID3DX10Mesh::GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).</span></span>

## <a name="members"></a><span data-ttu-id="793e0-107">Membros</span><span class="sxs-lookup"><span data-stu-id="793e0-107">Members</span></span>

<span data-ttu-id="793e0-108">A interface **ID3DX10MeshBuffer** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="793e0-108">The **ID3DX10MeshBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="793e0-109">**ID3DX10MeshBuffer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="793e0-109">**ID3DX10MeshBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="793e0-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="793e0-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="793e0-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="793e0-111">Methods</span></span>

<span data-ttu-id="793e0-112">A interface **ID3DX10MeshBuffer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="793e0-112">The **ID3DX10MeshBuffer** interface has these methods.</span></span>



| <span data-ttu-id="793e0-113">Método</span><span class="sxs-lookup"><span data-stu-id="793e0-113">Method</span></span>                                       | <span data-ttu-id="793e0-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="793e0-114">Description</span></span>                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="793e0-115">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="793e0-115">**GetSize**</span></span>](id3dx10meshbuffer-getsize.md) | <span data-ttu-id="793e0-116">Obtenha o tamanho do buffer de malha, em bytes.</span><span class="sxs-lookup"><span data-stu-id="793e0-116">Get the size of the mesh buffer, in bytes.</span></span><br/>                      |
| [<span data-ttu-id="793e0-117">**Mapeamento**</span><span class="sxs-lookup"><span data-stu-id="793e0-117">**Map**</span></span>](id3dx10meshbuffer-map.md)         | <span data-ttu-id="793e0-118">Obtenha um ponteiro para a memória do buffer de malha para modificar seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="793e0-118">Get a pointer to the mesh buffer memory to modify its contents.</span></span><br/> |
| [<span data-ttu-id="793e0-119">**Desmapear**</span><span class="sxs-lookup"><span data-stu-id="793e0-119">**Unmap**</span></span>](id3dx10meshbuffer-unmap.md)     | <span data-ttu-id="793e0-120">Cancelar o mapeamento de um buffer.</span><span class="sxs-lookup"><span data-stu-id="793e0-120">Unmap a buffer.</span></span><br/>                                                 |



 

## <a name="requirements"></a><span data-ttu-id="793e0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="793e0-121">Requirements</span></span>



| <span data-ttu-id="793e0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="793e0-122">Requirement</span></span> | <span data-ttu-id="793e0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="793e0-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="793e0-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="793e0-124">Header</span></span><br/>  | <dl> <span data-ttu-id="793e0-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="793e0-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="793e0-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="793e0-126">Library</span></span><br/> | <dl> <span data-ttu-id="793e0-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="793e0-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="793e0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="793e0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="793e0-129">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="793e0-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
