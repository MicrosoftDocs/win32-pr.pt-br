---
description: Função D3DX10CreateSkinInfo – cria um objeto de malha de capa vazio usando um Declarador.
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Função D3DX10CreateSkinInfo (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 17d6ec99d3f43c41d56deebef81a021c81ec1d69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103594"
---
# <a name="d3dx10createskininfo-function"></a><span data-ttu-id="bb59b-103">Função D3DX10CreateSkinInfo</span><span class="sxs-lookup"><span data-stu-id="bb59b-103">D3DX10CreateSkinInfo function</span></span>

<span data-ttu-id="bb59b-104">Cria um objeto de malha de capa vazio usando um Declarador.</span><span class="sxs-lookup"><span data-stu-id="bb59b-104">Creates an empty skin mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb59b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bb59b-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a><span data-ttu-id="bb59b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bb59b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb59b-107">*ppSkinInfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bb59b-107">*ppSkinInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb59b-108">Tipo: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span><span class="sxs-lookup"><span data-stu-id="bb59b-108">Type: **[**LPD3DX10SKININFO**](id3dx10skininfo.md)\***</span></span>

<span data-ttu-id="bb59b-109">Endereço de um ponteiro para uma [**interface ID3DX10SkinInfo**](id3dx10skininfo.md), que representa o objeto de malha de capa criado.</span><span class="sxs-lookup"><span data-stu-id="bb59b-109">Address of a pointer to an [**ID3DX10SkinInfo Interface**](id3dx10skininfo.md), representing the created skin mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb59b-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bb59b-110">Return value</span></span>

<span data-ttu-id="bb59b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="bb59b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="bb59b-112">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bb59b-112">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="bb59b-113">Se a função falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="bb59b-113">If the function fails, the return value can be: E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb59b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb59b-114">Remarks</span></span>

<span data-ttu-id="bb59b-115">Use o [**ID3DX10SkinInfo:: SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) para preencher o objeto de malha de capa vazio retornado por esse método.</span><span class="sxs-lookup"><span data-stu-id="bb59b-115">Use the [**ID3DX10SkinInfo::SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) to populate the empty skin mesh object returned by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb59b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb59b-116">Requirements</span></span>



| <span data-ttu-id="bb59b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb59b-117">Requirement</span></span> | <span data-ttu-id="bb59b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bb59b-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb59b-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb59b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bb59b-120"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb59b-120"><dt>D3DX10Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bb59b-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bb59b-121">Library</span></span><br/> | <dl> <span data-ttu-id="bb59b-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb59b-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb59b-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bb59b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb59b-124">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="bb59b-124">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="bb59b-125">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="bb59b-125">D3DX Functions</span></span>](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




