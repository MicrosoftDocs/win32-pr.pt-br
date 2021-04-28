---
description: 'Método ID3DX10Mesh:: SetAttributeTable – define a tabela de atributos para uma malha e o número de entradas armazenadas na tabela.'
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: 'Método ID3DX10Mesh:: SetAttributeTable (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4e06b181bb512e16e9caaa0d233ebbd3472bfcf8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084004"
---
# <a name="id3dx10meshsetattributetable-method"></a><span data-ttu-id="a5992-103">Método ID3DX10Mesh:: SetAttributeTable</span><span class="sxs-lookup"><span data-stu-id="a5992-103">ID3DX10Mesh::SetAttributeTable method</span></span>

<span data-ttu-id="a5992-104">Define a tabela de atributos para uma malha e o número de entradas armazenadas na tabela.</span><span class="sxs-lookup"><span data-stu-id="a5992-104">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5992-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a5992-105">Syntax</span></span>


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a><span data-ttu-id="a5992-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5992-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5992-107">*pAttribTable* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5992-107">*pAttribTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5992-108">Tipo: **\* [**intervalo de \_ atributos \_ const D3DX10**](d3dx10-attribute-range.md)**</span><span class="sxs-lookup"><span data-stu-id="a5992-108">Type: **const [**D3DX10\_ATTRIBUTE\_RANGE**](d3dx10-attribute-range.md)\***</span></span>

<span data-ttu-id="a5992-109">Ponteiro para uma matriz de \_ estruturas de intervalo de atributos D3DX10 \_ , representando as entradas na tabela de atributos de malha.</span><span class="sxs-lookup"><span data-stu-id="a5992-109">Pointer to an array of D3DX10\_ATTRIBUTE\_RANGE structures, representing the entries in the mesh attribute table.</span></span>

</dd> <dt>

<span data-ttu-id="a5992-110">*cAttribTableSize* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a5992-110">*cAttribTableSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5992-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a5992-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a5992-112">Número de atributos na tabela de atributos de malha.</span><span class="sxs-lookup"><span data-stu-id="a5992-112">Number of attributes in the mesh attribute table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5992-113">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a5992-113">Return value</span></span>

<span data-ttu-id="a5992-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5992-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5992-115">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="a5992-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5992-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5992-116">Remarks</span></span>

<span data-ttu-id="a5992-117">Se um aplicativo acompanhar as informações em uma tabela de atributos e reorganizar a tabela como resultado de alterações em atributos ou rostos, esse método permitirá que o aplicativo atualize as tabelas de atributos em vez de chamar ID3DX10Mesh:: Optimize novamente.</span><span class="sxs-lookup"><span data-stu-id="a5992-117">If an application keeps track of the information in an attribute table, and rearranges the table as a result of changes to attributes or faces, this method allows the application to update the attribute tables instead of calling ID3DX10Mesh::Optimize again.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5992-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5992-118">Requirements</span></span>



| <span data-ttu-id="a5992-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5992-119">Requirement</span></span> | <span data-ttu-id="a5992-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a5992-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5992-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a5992-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a5992-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5992-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5992-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a5992-123">Library</span></span><br/> | <dl> <span data-ttu-id="a5992-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5992-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5992-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="a5992-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5992-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="a5992-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="a5992-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="a5992-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
