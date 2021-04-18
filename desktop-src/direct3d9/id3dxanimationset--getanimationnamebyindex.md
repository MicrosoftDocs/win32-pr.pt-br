---
description: Obtém o nome de uma animação, dado seu índice.
ms.assetid: vs|directx_sdk|~\id3dxanimationset__getanimationnamebyindex.htm
title: 'Método ID3DXAnimationSet:: GetAnimationNameByIndex (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationNameByIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 820b21fa69fd7007bdd1971e83ea44368dce5cc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105789301"
---
# <a name="id3dxanimationsetgetanimationnamebyindex-method"></a><span data-ttu-id="5202d-103">Método ID3DXAnimationSet:: GetAnimationNameByIndex</span><span class="sxs-lookup"><span data-stu-id="5202d-103">ID3DXAnimationSet::GetAnimationNameByIndex method</span></span>

<span data-ttu-id="5202d-104">Obtém o nome de uma animação, dado seu índice.</span><span class="sxs-lookup"><span data-stu-id="5202d-104">Gets the name of an animation, given its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5202d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5202d-105">Syntax</span></span>


```C++
HRESULT GetAnimationNameByIndex(
  [in]  UINT   Index,
  [out] LPCSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="5202d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5202d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5202d-107">*Índice* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="5202d-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5202d-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5202d-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5202d-109">Índice da animação.</span><span class="sxs-lookup"><span data-stu-id="5202d-109">Index of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="5202d-110">*ppName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="5202d-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5202d-111">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5202d-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5202d-112">Endereço de um ponteiro para uma cadeia de caracteres que recebe o nome da animação.</span><span class="sxs-lookup"><span data-stu-id="5202d-112">Address of a pointer to a string that receives the animation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5202d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5202d-113">Return value</span></span>

<span data-ttu-id="5202d-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5202d-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5202d-115">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="5202d-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="5202d-116">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5202d-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="5202d-117">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de [D3DERR](d3derr.md) ou [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="5202d-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5202d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5202d-118">Requirements</span></span>



| <span data-ttu-id="5202d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5202d-119">Requirement</span></span> | <span data-ttu-id="5202d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="5202d-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5202d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5202d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5202d-122"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="5202d-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="5202d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5202d-123">Library</span></span><br/> | <dl> <span data-ttu-id="5202d-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5202d-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="5202d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="5202d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5202d-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="5202d-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
