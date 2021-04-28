---
description: 'ID3DX10Mesh: método rawSubset:D-desenha um subconjunto de uma malha.'
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: 'ID3DX10Mesh: método rawSubset de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8441bfe4c5d965733a40816ff2def1015f3eb79c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084034"
---
# <a name="id3dx10meshdrawsubset-method"></a><span data-ttu-id="2fffe-103">ID3DX10Mesh: método rawSubset de:D</span><span class="sxs-lookup"><span data-stu-id="2fffe-103">ID3DX10Mesh::DrawSubset method</span></span>

<span data-ttu-id="2fffe-104">Desenha um subconjunto de uma malha.</span><span class="sxs-lookup"><span data-stu-id="2fffe-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fffe-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2fffe-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="2fffe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fffe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fffe-107">*Atribid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2fffe-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fffe-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fffe-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fffe-109">Especifica qual subconjunto da malha deve ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="2fffe-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="2fffe-110">Esse valor é usado para diferenciar faces em uma malha como pertencente a um ou mais grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="2fffe-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fffe-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2fffe-111">Return value</span></span>

<span data-ttu-id="2fffe-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2fffe-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2fffe-113">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="2fffe-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="2fffe-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fffe-114">Remarks</span></span>

<span data-ttu-id="2fffe-115">Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="2fffe-115">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="2fffe-116">Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha por não desenhar um determinado identificador de atributo (attrib) ao desenhar o quadro.</span><span class="sxs-lookup"><span data-stu-id="2fffe-116">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fffe-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fffe-117">Requirements</span></span>



| <span data-ttu-id="2fffe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fffe-118">Requirement</span></span> | <span data-ttu-id="2fffe-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2fffe-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2fffe-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2fffe-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2fffe-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fffe-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fffe-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fffe-122">Library</span></span><br/> | <dl> <span data-ttu-id="2fffe-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fffe-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fffe-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2fffe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fffe-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="2fffe-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="2fffe-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="2fffe-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
