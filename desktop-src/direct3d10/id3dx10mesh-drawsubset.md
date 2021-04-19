---
description: Desenha um subconjunto de uma malha.
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
ms.openlocfilehash: 80beceebeead84a782cc7852ac0d2fe15ad61ff3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105756958"
---
# <a name="id3dx10meshdrawsubset-method"></a><span data-ttu-id="8e105-103">ID3DX10Mesh: método rawSubset de:D</span><span class="sxs-lookup"><span data-stu-id="8e105-103">ID3DX10Mesh::DrawSubset method</span></span>

<span data-ttu-id="8e105-104">Desenha um subconjunto de uma malha.</span><span class="sxs-lookup"><span data-stu-id="8e105-104">Draws a subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e105-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8e105-105">Syntax</span></span>


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a><span data-ttu-id="8e105-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8e105-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e105-107">*Atribid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8e105-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e105-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8e105-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8e105-109">Especifica qual subconjunto da malha deve ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="8e105-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="8e105-110">Esse valor é usado para diferenciar faces em uma malha como pertencente a um ou mais grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="8e105-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e105-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8e105-111">Return value</span></span>

<span data-ttu-id="8e105-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8e105-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8e105-113">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="8e105-113">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8e105-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e105-114">Remarks</span></span>

<span data-ttu-id="8e105-115">Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8e105-115">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="8e105-116">Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha por não desenhar um determinado identificador de atributo (attrib) ao desenhar o quadro.</span><span class="sxs-lookup"><span data-stu-id="8e105-116">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e105-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e105-117">Requirements</span></span>



| <span data-ttu-id="8e105-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e105-118">Requirement</span></span> | <span data-ttu-id="8e105-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8e105-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e105-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e105-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8e105-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e105-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e105-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8e105-122">Library</span></span><br/> | <dl> <span data-ttu-id="8e105-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e105-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e105-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e105-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e105-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="8e105-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="8e105-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="8e105-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
