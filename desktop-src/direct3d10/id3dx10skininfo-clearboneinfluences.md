---
description: Desmarque a lista de vértices de um Bone que ele influencia.
ms.assetid: 1ba6f43a-1f85-4057-b0ed-247cc38d4932
title: 'Método ID3DX10SkinInfo:: ClearBoneInfluences (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.ClearBoneInfluences
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d6f161ba400b684b12d6b0a091abb1fa452d476b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930604"
---
# <a name="id3dx10skininfoclearboneinfluences-method"></a><span data-ttu-id="1ff20-103">Método ID3DX10SkinInfo:: ClearBoneInfluences</span><span class="sxs-lookup"><span data-stu-id="1ff20-103">ID3DX10SkinInfo::ClearBoneInfluences method</span></span>

<span data-ttu-id="1ff20-104">Desmarque a lista de vértices de um Bone que ele influencia.</span><span class="sxs-lookup"><span data-stu-id="1ff20-104">Clear a bone's list of vertices that it influences.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff20-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1ff20-105">Syntax</span></span>


```C++
HRESULT ClearBoneInfluences(
  [in] UINT BoneIndex
);
```



## <a name="parameters"></a><span data-ttu-id="1ff20-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ff20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ff20-107">*BoneIndex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1ff20-107">*BoneIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ff20-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ff20-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ff20-109">Um índice que especifica um Bone existente.</span><span class="sxs-lookup"><span data-stu-id="1ff20-109">An index that specifies an existing bone.</span></span> <span data-ttu-id="1ff20-110">Deve estar entre 0 e o valor retornado por [**ID3DX10SkinInfo:: GetNumBones**](id3dx10skininfo-getnumbones.md).</span><span class="sxs-lookup"><span data-stu-id="1ff20-110">Must be between 0 and the value returned by [**ID3DX10SkinInfo::GetNumBones**](id3dx10skininfo-getnumbones.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ff20-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1ff20-111">Return value</span></span>

<span data-ttu-id="1ff20-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ff20-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ff20-113">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ff20-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="1ff20-114">Se o método falhar, o valor de retorno poderá ser: E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="1ff20-114">If the method fails, the return value can be: E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ff20-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ff20-115">Requirements</span></span>



| <span data-ttu-id="1ff20-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ff20-116">Requirement</span></span> | <span data-ttu-id="1ff20-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1ff20-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff20-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ff20-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1ff20-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ff20-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ff20-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1ff20-120">Library</span></span><br/> | <dl> <span data-ttu-id="1ff20-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ff20-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff20-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ff20-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff20-123">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="1ff20-123">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="1ff20-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="1ff20-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
