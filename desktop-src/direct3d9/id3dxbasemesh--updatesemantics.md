---
description: Esse método permite que o usuário altere a declaração de malha sem alterar o layout de dados do buffer de vértice. A chamada será válida somente se os formatos de declaração antigo e novo tiverem o mesmo tamanho de vértice.
ms.assetid: ed2ad479-e0f7-4580-a20a-d3649759876a
title: 'Método ID3DXBaseMesh:: UpdateSemantics (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.UpdateSemantics
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e31a6fe424d085467bfa795c7ce7b2d445a1f69
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012109"
---
# <a name="id3dxbasemeshupdatesemantics-method"></a><span data-ttu-id="02077-104">Método ID3DXBaseMesh:: UpdateSemantics</span><span class="sxs-lookup"><span data-stu-id="02077-104">ID3DXBaseMesh::UpdateSemantics method</span></span>

<span data-ttu-id="02077-105">Esse método permite que o usuário altere a declaração de malha sem alterar o layout de dados do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="02077-105">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="02077-106">A chamada será válida somente se os formatos de declaração antigo e novo tiverem o mesmo tamanho de vértice.</span><span class="sxs-lookup"><span data-stu-id="02077-106">The call is valid only if the old and new declaration formats have the same vertex size.</span></span>

## <a name="syntax"></a><span data-ttu-id="02077-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02077-107">Syntax</span></span>


```C++
HRESULT UpdateSemantics(
  [in, out] D3DVERTEXELEMENT9 Declaration
);
```



## <a name="parameters"></a><span data-ttu-id="02077-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="02077-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02077-109">*Declaração* \[ de entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="02077-109">*Declaration* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="02077-110">Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span><span class="sxs-lookup"><span data-stu-id="02077-110">Type: **[**D3DVERTEXELEMENT9**](d3dvertexelement9.md)**</span></span>

<span data-ttu-id="02077-111">Uma matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que descreve o formato de vértice dos vértices de malha.</span><span class="sxs-lookup"><span data-stu-id="02077-111">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format of the mesh vertices.</span></span> <span data-ttu-id="02077-112">O limite superior dessa matriz de Declarador é o [**tamanho máximo de \_ \_ DECL \_ FVF**](./max-fvf-decl-size.md).</span><span class="sxs-lookup"><span data-stu-id="02077-112">The upper limit of this declarator array is [**MAX\_FVF\_DECL\_SIZE**](./max-fvf-decl-size.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02077-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="02077-113">Return value</span></span>

<span data-ttu-id="02077-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="02077-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="02077-115">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="02077-115">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="02077-116">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="02077-116">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="02077-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="02077-117">Remarks</span></span>

<span data-ttu-id="02077-118">[**ID3DXBaseMesh:: CloneMesh**](id3dxbasemesh--clonemesh.md) é usado para reformatar e alterar o layout de dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="02077-118">[**ID3DXBaseMesh::CloneMesh**](id3dxbasemesh--clonemesh.md) is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="02077-119">Por exemplo, use-o para adicionar espaço para Normals, coordenadas de textura, cores, pesos, etc. que não estavam presentes antes.</span><span class="sxs-lookup"><span data-stu-id="02077-119">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="02077-120">**ID3DXBaseMesh:: UpdateSemantics** é um método para atualizar a declaração de vértice com informações semânticas diferentes, sem alterar o layout do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="02077-120">**ID3DXBaseMesh::UpdateSemantics** is a method for updating the vertex declaration with different semantic information, without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="02077-121">Por exemplo, use-o para rerotular uma coordenada de textura 3D como uma binormal ou uma tangente, ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="02077-121">For example, use it to relabel a 3D texture coordinate as a binormal or tangent, or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="02077-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="02077-122">Requirements</span></span>



| <span data-ttu-id="02077-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="02077-123">Requirement</span></span> | <span data-ttu-id="02077-124">Valor</span><span class="sxs-lookup"><span data-stu-id="02077-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="02077-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="02077-125">Header</span></span><br/>  | <dl> <span data-ttu-id="02077-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="02077-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="02077-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="02077-127">Library</span></span><br/> | <dl> <span data-ttu-id="02077-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02077-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="02077-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="02077-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02077-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="02077-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="02077-131">**ID3DXBaseMesh::CloneMeshFVF**</span><span class="sxs-lookup"><span data-stu-id="02077-131">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="02077-132">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="02077-132">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
