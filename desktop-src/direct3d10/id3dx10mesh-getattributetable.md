---
description: 'Método ID3DX10Mesh:: getattributetable – recupera uma tabela de atributos para uma malha ou o número de entradas armazenadas em uma tabela de atributos para uma malha.'
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'Método ID3DX10Mesh:: getattributetable (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e7fc503af1a290b27fea81d0c2aba6b84393323b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083984"
---
# <a name="id3dx10meshgetattributetable-method"></a><span data-ttu-id="ef9d5-103">Método ID3DX10Mesh:: getattributetable</span><span class="sxs-lookup"><span data-stu-id="ef9d5-103">ID3DX10Mesh::GetAttributeTable method</span></span>

<span data-ttu-id="ef9d5-104">Recupera uma tabela de atributos para uma malha ou o número de entradas armazenadas em uma tabela de atributos para uma malha.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-104">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef9d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ef9d5-105">Syntax</span></span>


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="ef9d5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef9d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef9d5-107">*pAttribTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ef9d5-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef9d5-108">Tipo: **[ **\_ \_ intervalo de atributos D3DX10**](d3dx10-attribute-range.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef9d5-108">Type: **[**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="ef9d5-109">Ponteiro para uma matriz de \_ estruturas de intervalo de atributos D3DX10 \_ , representando as entradas na tabela de atributos da malha.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh's attribute table.</span></span> <span data-ttu-id="ef9d5-110">Especifique **NULL** para recuperar o valor de pAttribTableSize.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-110">Specify **NULL** to retrieve the value for pAttribTableSize.</span></span>

</dd> <dt>

<span data-ttu-id="ef9d5-111">*pAttribTableSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ef9d5-111">*pAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef9d5-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ef9d5-112">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ef9d5-113">Ponteiro para o número de entradas armazenadas em pAttribTable ou um valor a ser preenchido com o número de entradas armazenadas na tabela de atributos para a malha.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-113">Pointer to either the number of entries stored in pAttribTable or a value to be filled in with the number of entries stored in the attribute table for the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef9d5-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ef9d5-114">Return value</span></span>

<span data-ttu-id="ef9d5-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef9d5-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef9d5-116">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ef9d5-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ef9d5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef9d5-117">Remarks</span></span>

<span data-ttu-id="ef9d5-118">Uma tabela de atributos é usada para identificar áreas da malha que precisam ser desenhadas com texturas diferentes, Estados de renderização, materiais e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-118">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="ef9d5-119">Além disso, o aplicativo pode usar a tabela de atributos para ocultar partes de uma malha não desenhando um determinado identificador de atributo ao desenhar o quadro.</span><span class="sxs-lookup"><span data-stu-id="ef9d5-119">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier when drawing the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef9d5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef9d5-120">Requirements</span></span>



| <span data-ttu-id="ef9d5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef9d5-121">Requirement</span></span> | <span data-ttu-id="ef9d5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ef9d5-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef9d5-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ef9d5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ef9d5-124"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef9d5-124"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef9d5-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ef9d5-125">Library</span></span><br/> | <dl> <span data-ttu-id="ef9d5-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef9d5-126"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef9d5-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="ef9d5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef9d5-128">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="ef9d5-128">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="ef9d5-129">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="ef9d5-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
