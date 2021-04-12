---
description: Limitar o número de Bones que podem influenciar um vértice e/ou limitar a quantidade de influência que um Bone pode ter em um vértice.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'Método ID3DX10SkinInfo:: Compact (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 379343688a1fd2ffe5ebd968dc984fa09faada7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370936"
---
# <a name="id3dx10skininfocompact-method"></a><span data-ttu-id="367b5-103">Método ID3DX10SkinInfo:: Compact</span><span class="sxs-lookup"><span data-stu-id="367b5-103">ID3DX10SkinInfo::Compact method</span></span>

<span data-ttu-id="367b5-104">Limitar o número de Bones que podem influenciar um vértice e/ou limitar a quantidade de influência que um Bone pode ter em um vértice.</span><span class="sxs-lookup"><span data-stu-id="367b5-104">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span>

## <a name="syntax"></a><span data-ttu-id="367b5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="367b5-105">Syntax</span></span>


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a><span data-ttu-id="367b5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="367b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="367b5-107">*MaxPerVertexInfluences* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="367b5-107">*MaxPerVertexInfluences* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="367b5-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="367b5-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="367b5-109">O número máximo de Bones que podem influenciar qualquer vértice determinado.</span><span class="sxs-lookup"><span data-stu-id="367b5-109">The maximum number of bones that can influence any given vertex.</span></span> <span data-ttu-id="367b5-110">Esse valor será ignorado se for maior que o valor retornado por [**ID3DX10SkinInfo:: GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).</span><span class="sxs-lookup"><span data-stu-id="367b5-110">This value is ignored if it is greater than the value returned by [**ID3DX10SkinInfo::GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).</span></span>

</dd> <dt>

<span data-ttu-id="367b5-111">*ScaleMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="367b5-111">*ScaleMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="367b5-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="367b5-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="367b5-113">Um sinalizador que descreve como dimensionar os pesos restantes em um determinado vértice depois que alguns foram descortadosdos pelo MinWeight.</span><span class="sxs-lookup"><span data-stu-id="367b5-113">A flag describing how to scale the remaining weights on a given vertex after some have been chopped off by MinWeight.</span></span> <span data-ttu-id="367b5-114">Se D3DX10 \_ SKININFO \_ nenhum \_ dimensionamento for especificado, os pesos não serão dimensionados.</span><span class="sxs-lookup"><span data-stu-id="367b5-114">If D3DX10\_SKININFO\_NO\_SCALING is specified, the weights will not be scaled at all.</span></span> <span data-ttu-id="367b5-115">Se D3DX10 \_ SKININFO \_ dimensionar \_ para \_ 1 for especificado, os pesos maiores que MinWeight serão escalados verticalmente para que eles se adicionem até 1,0.</span><span class="sxs-lookup"><span data-stu-id="367b5-115">If D3DX10\_SKININFO\_SCALE\_TO\_1 is specified, the weights greater than MinWeight will be scaled up so that they add up to 1.0.</span></span> <span data-ttu-id="367b5-116">Se D3DX10 \_ SKININFO \_ dimensionar \_ para \_ total for especificado, os pesos maiores que MinWeight serão dimensionados para que eles se adicionem ao total original.</span><span class="sxs-lookup"><span data-stu-id="367b5-116">If D3DX10\_SKININFO\_SCALE\_TO\_TOTAL is specified, the weights greater than MinWeight will be scaled up so that they add up to the original total.</span></span>

</dd> <dt>

<span data-ttu-id="367b5-117">*MinWeight* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="367b5-117">*MinWeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="367b5-118">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="367b5-118">Type: **float**</span></span>

<span data-ttu-id="367b5-119">O percentual mínimo de influência, ou peso, que qualquer Bone pode ter em qualquer vértice.</span><span class="sxs-lookup"><span data-stu-id="367b5-119">The minimum percentage of influence, or weight, that any bone can have on any vertex.</span></span> <span data-ttu-id="367b5-120">Esse valor deve estar entre 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="367b5-120">This value must be between 0 and 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="367b5-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="367b5-121">Return value</span></span>

<span data-ttu-id="367b5-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="367b5-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="367b5-123">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="367b5-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="367b5-124">Se o método falhar, o valor de retorno poderá ser: E \_ OUTOFMEMORY ou E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="367b5-124">If the method fails, the return value can be: E\_OUTOFMEMORY or E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="367b5-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="367b5-125">Requirements</span></span>



| <span data-ttu-id="367b5-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="367b5-126">Requirement</span></span> | <span data-ttu-id="367b5-127">Valor</span><span class="sxs-lookup"><span data-stu-id="367b5-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="367b5-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="367b5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="367b5-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="367b5-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="367b5-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="367b5-130">Library</span></span><br/> | <dl> <span data-ttu-id="367b5-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="367b5-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="367b5-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="367b5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="367b5-133">ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="367b5-133">ID3DX10SkinInfo</span></span>](id3dx10skininfo.md)
</dt> <dt>

[<span data-ttu-id="367b5-134">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="367b5-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
