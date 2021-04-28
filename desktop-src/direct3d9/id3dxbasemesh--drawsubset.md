---
description: 'ID3DXBaseMesh: método rawSubset:D-desenha um subconjunto de uma malha.'
ms.assetid: 99eaa185-b681-47f2-aed8-5ca1697ff73c
title: 'ID3DXBaseMesh: método rawSubset de:D (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.DrawSubset
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 252c9b9921c7eafd8f0c2a54cfa14a85e91b8f7d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115464"
---
# <a name="id3dxbasemeshdrawsubset-method"></a><span data-ttu-id="797ca-103">ID3DXBaseMesh: método rawSubset de:D</span><span class="sxs-lookup"><span data-stu-id="797ca-103">ID3DXBaseMesh::DrawSubset method</span></span>

<span data-ttu-id="797ca-104">Desenha um subconjunto de uma malha.</span><span class="sxs-lookup"><span data-stu-id="797ca-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="797ca-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="797ca-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] DWORD AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="797ca-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="797ca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="797ca-107">*Atribid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="797ca-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="797ca-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="797ca-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="797ca-109">DWORD que especifica qual subconjunto da malha deve ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="797ca-109">DWORD that specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="797ca-110">Esse valor é usado para diferenciar faces em uma malha como pertencente a um ou mais grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="797ca-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="797ca-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="797ca-111">Return value</span></span>

<span data-ttu-id="797ca-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="797ca-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="797ca-113">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="797ca-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="797ca-114">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="797ca-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="797ca-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="797ca-115">Remarks</span></span>

<span data-ttu-id="797ca-116">O subconjunto especificado por AttribId será renderizado pelo método [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) , usando o \_ tipo primitivo triângulolist D3DPT, portanto, um buffer de índice deve ser inicializado corretamente.</span><span class="sxs-lookup"><span data-stu-id="797ca-116">The subset that is specified by AttribId will be rendered by the [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) method, using the D3DPT\_TRIANGLELIST primitive type, so an index buffer must be properly initialized.</span></span>

<span data-ttu-id="797ca-117">Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="797ca-117">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="797ca-118">Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha por não desenhar um determinado identificador de atributo (*attrib*) ao desenhar o quadro.</span><span class="sxs-lookup"><span data-stu-id="797ca-118">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (*AttribId*) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="797ca-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="797ca-119">Requirements</span></span>



| <span data-ttu-id="797ca-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="797ca-120">Requirement</span></span> | <span data-ttu-id="797ca-121">Valor</span><span class="sxs-lookup"><span data-stu-id="797ca-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="797ca-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="797ca-122">Header</span></span><br/>  | <dl> <span data-ttu-id="797ca-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="797ca-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="797ca-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="797ca-124">Library</span></span><br/> | <dl> <span data-ttu-id="797ca-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="797ca-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="797ca-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="797ca-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="797ca-127">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="797ca-127">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> </dl>

 

 
