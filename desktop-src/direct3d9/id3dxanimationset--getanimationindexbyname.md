---
description: Obtém o índice de uma animação, dado seu nome.
ms.assetid: 6e91a4fe-3202-447b-b486-d29e8da64af2
title: 'Método ID3DXAnimationSet:: GetAnimationIndexByName (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationIndexByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4d3e5fb39ebcfa5ce906d1f90c2c5c10bdd4b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813671"
---
# <a name="id3dxanimationsetgetanimationindexbyname-method"></a><span data-ttu-id="1fc39-103">Método ID3DXAnimationSet:: GetAnimationIndexByName</span><span class="sxs-lookup"><span data-stu-id="1fc39-103">ID3DXAnimationSet::GetAnimationIndexByName method</span></span>

<span data-ttu-id="1fc39-104">Obtém o índice de uma animação, dado seu nome.</span><span class="sxs-lookup"><span data-stu-id="1fc39-104">Gets the index of an animation, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc39-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fc39-105">Syntax</span></span>


```C++
HRESULT GetAnimationIndexByName(
  [in]  LPCSTR pName,
  [out] UINT   *pIndex
);
```



## <a name="parameters"></a><span data-ttu-id="1fc39-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fc39-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fc39-107">*pname* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1fc39-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc39-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fc39-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fc39-109">Nome da animação.</span><span class="sxs-lookup"><span data-stu-id="1fc39-109">Name of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="1fc39-110">*pIndex* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1fc39-110">*pIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fc39-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1fc39-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1fc39-112">Ponteiro para o índice de animação.</span><span class="sxs-lookup"><span data-stu-id="1fc39-112">Pointer to the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fc39-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fc39-113">Return value</span></span>

<span data-ttu-id="1fc39-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fc39-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fc39-115">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1fc39-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="1fc39-116">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1fc39-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="1fc39-117">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="1fc39-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fc39-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc39-118">Requirements</span></span>



| <span data-ttu-id="1fc39-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc39-119">Requirement</span></span> | <span data-ttu-id="1fc39-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1fc39-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc39-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fc39-121">Header</span></span><br/>  | <dl> <span data-ttu-id="1fc39-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fc39-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1fc39-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1fc39-123">Library</span></span><br/> | <dl> <span data-ttu-id="1fc39-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fc39-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1fc39-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fc39-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fc39-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="1fc39-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
