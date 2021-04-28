---
description: 'Método ID3DXBaseMesh:: getattributetable – recupera uma tabela de atributos para uma malha ou o número de entradas armazenadas em uma tabela de atributos para uma malha.'
ms.assetid: 15b24137-0ff9-4299-971b-90fa4ef2686d
title: 'Método ID3DXBaseMesh:: getattributetable (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetAttributeTable
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7f5d27de884f72b46db900487e26f1099bf30949
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115444"
---
# <a name="id3dxbasemeshgetattributetable-method"></a><span data-ttu-id="d8e86-103">Método ID3DXBaseMesh:: getattributetable</span><span class="sxs-lookup"><span data-stu-id="d8e86-103">ID3DXBaseMesh::GetAttributeTable method</span></span>

<span data-ttu-id="d8e86-104">Recupera uma tabela de atributos para uma malha ou o número de entradas armazenadas em uma tabela de atributos para uma malha.</span><span class="sxs-lookup"><span data-stu-id="d8e86-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8e86-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8e86-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in, out] D3DXATTRIBUTERANGE *pAttribTable,
  [in, out] DWORD              *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="d8e86-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8e86-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8e86-107">*pAttribTable* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d8e86-107">*pAttribTable* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e86-108">Tipo: **[ **D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8e86-108">Type: **[**D3DXATTRIBUTERANGE**](d3dxattributerange.md)\***</span></span>

<span data-ttu-id="d8e86-109">Ponteiro para uma matriz de estruturas [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) , representando as entradas na tabela de atributos da malha.</span><span class="sxs-lookup"><span data-stu-id="d8e86-109">Pointer to an array of [**D3DXATTRIBUTERANGE**](d3dxattributerange.md) structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="d8e86-110">Especifique **NULL** para recuperar o valor de pAttribTableSize.</span><span class="sxs-lookup"><span data-stu-id="d8e86-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="d8e86-111">*pAttribTableSize* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="d8e86-111">*pAttribTableSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8e86-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d8e86-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d8e86-113">Ponteiro para o número de entradas armazenadas em pAttribTable ou um valor a ser preenchido com o número de entradas armazenadas na tabela de atributos para a malha.</span><span class="sxs-lookup"><span data-stu-id="d8e86-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8e86-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="d8e86-114">Return value</span></span>

<span data-ttu-id="d8e86-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d8e86-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d8e86-116">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d8e86-116">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d8e86-117">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="d8e86-117">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8e86-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8e86-118">Remarks</span></span>

<span data-ttu-id="d8e86-119">Uma tabela de atributos é criada por [**ID3DXMesh:: Optimize**](id3dxmesh--optimize.md) e passando D3DXMESHOPT \_ ATTRSORT para o parâmetro flags.</span><span class="sxs-lookup"><span data-stu-id="d8e86-119">An attribute table is created by [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) and passing D3DXMESHOPT\_ATTRSORT for the Flags parameter.</span></span>

<span data-ttu-id="d8e86-120">Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d8e86-120">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="d8e86-121">Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha não desenhando um determinado identificador de atributo ao desenhar o quadro.</span><span class="sxs-lookup"><span data-stu-id="d8e86-121">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8e86-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8e86-122">Requirements</span></span>



| <span data-ttu-id="d8e86-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8e86-123">Requirement</span></span> | <span data-ttu-id="d8e86-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d8e86-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8e86-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8e86-125">Header</span></span><br/>  | <dl> <span data-ttu-id="d8e86-126"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8e86-126"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="d8e86-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8e86-127">Library</span></span><br/> | <dl> <span data-ttu-id="d8e86-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8e86-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d8e86-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="d8e86-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8e86-130">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="d8e86-130">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
