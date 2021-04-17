---
description: A interface ID3DXBuffer é usada como um buffer de dados, armazenando vértices, adjacências e informações materiais durante a otimização da malha e operações de carregamento.
ms.assetid: 63ee3b2d-c0e6-4ad4-9274-2b1dfd77f89d
title: Interface ID3DXBuffer (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5fff273d2e38daeb003fb360f099e7a7b4985504
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105753512"
---
# <a name="id3dxbuffer-interface"></a><span data-ttu-id="dfa5d-103">Interface ID3DXBuffer</span><span class="sxs-lookup"><span data-stu-id="dfa5d-103">ID3DXBuffer interface</span></span>

<span data-ttu-id="dfa5d-104">A interface ID3DXBuffer é usada como um buffer de dados, armazenando vértices, adjacências e informações materiais durante a otimização da malha e operações de carregamento.</span><span class="sxs-lookup"><span data-stu-id="dfa5d-104">The ID3DXBuffer interface is used as a data buffer, storing vertex, adjacency, and material information during mesh optimization and loading operations.</span></span> <span data-ttu-id="dfa5d-105">O objeto buffer é usado para retornar dados de comprimento arbitrário.</span><span class="sxs-lookup"><span data-stu-id="dfa5d-105">The buffer object is used to return arbitrary length data.</span></span> <span data-ttu-id="dfa5d-106">Além disso, os objetos buffer são usados para retornar código de objeto e mensagens de erro em métodos que montam os sombreadores de vértices e de pixel.</span><span class="sxs-lookup"><span data-stu-id="dfa5d-106">Also, buffer objects are used to return object code and error messages in methods that assemble vertex and pixel shaders.</span></span>

## <a name="members"></a><span data-ttu-id="dfa5d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="dfa5d-107">Members</span></span>

<span data-ttu-id="dfa5d-108">A interface **ID3DXBuffer** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dfa5d-108">The **ID3DXBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dfa5d-109">**ID3DXBuffer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="dfa5d-109">**ID3DXBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="dfa5d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="dfa5d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dfa5d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="dfa5d-111">Methods</span></span>

<span data-ttu-id="dfa5d-112">A interface **ID3DXBuffer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="dfa5d-112">The **ID3DXBuffer** interface has these methods.</span></span>



| <span data-ttu-id="dfa5d-113">Método</span><span class="sxs-lookup"><span data-stu-id="dfa5d-113">Method</span></span>                                                    | <span data-ttu-id="dfa5d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="dfa5d-114">Description</span></span>                                                    |
|:----------------------------------------------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="dfa5d-115">**GetBufferPointer**</span><span class="sxs-lookup"><span data-stu-id="dfa5d-115">**GetBufferPointer**</span></span>](id3dxbuffer--getbufferpointer.md) | <span data-ttu-id="dfa5d-116">Recupera um ponteiro para os dados no buffer.</span><span class="sxs-lookup"><span data-stu-id="dfa5d-116">Retrieves a pointer to the data in the buffer.</span></span><br/>      |
| [<span data-ttu-id="dfa5d-117">**Getbuffersize**</span><span class="sxs-lookup"><span data-stu-id="dfa5d-117">**GetBufferSize**</span></span>](id3dxbuffer--getbuffersize.md)       | <span data-ttu-id="dfa5d-118">Recupera o tamanho total dos dados no buffer.</span><span class="sxs-lookup"><span data-stu-id="dfa5d-118">Retrieves the total size of the data in the buffer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dfa5d-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfa5d-119">Remarks</span></span>

<span data-ttu-id="dfa5d-120">A interface **ID3DXBuffer** é obtida chamando a função [**D3DXCreateBuffer**](d3dxcreatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="dfa5d-120">The **ID3DXBuffer** interface is obtained by calling the [**D3DXCreateBuffer**](d3dxcreatebuffer.md) function.</span></span>

<span data-ttu-id="dfa5d-121">O tipo LPD3DXBUFFER é definido como um ponteiro para a interface **ID3DXBuffer** .</span><span class="sxs-lookup"><span data-stu-id="dfa5d-121">The LPD3DXBUFFER type is defined as a pointer to the **ID3DXBuffer** interface.</span></span>


```
typedef interface ID3DXBuffer ID3DXBuffer;
typedef interface ID3DXBuffer *LPD3DXBUFFER;
```



## <a name="requirements"></a><span data-ttu-id="dfa5d-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfa5d-122">Requirements</span></span>



| <span data-ttu-id="dfa5d-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfa5d-123">Requirement</span></span> | <span data-ttu-id="dfa5d-124">Valor</span><span class="sxs-lookup"><span data-stu-id="dfa5d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa5d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfa5d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="dfa5d-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa5d-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="dfa5d-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="dfa5d-127">Library</span></span><br/> | <dl> <span data-ttu-id="dfa5d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfa5d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dfa5d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfa5d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa5d-130">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="dfa5d-130">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
