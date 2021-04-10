---
description: Obtém a transformação de Sprite.
ms.assetid: d91f2776-ee87-42b3-998b-fccea178cee2
title: 'Método ID3DXSprite:: GetTransform (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.GetTransform
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 646fa3574c3b9be788ad32ef402a7ca2051d04de
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012116"
---
# <a name="id3dxspritegettransform-method"></a><span data-ttu-id="2586c-103">Método ID3DXSprite:: GetTransform</span><span class="sxs-lookup"><span data-stu-id="2586c-103">ID3DXSprite::GetTransform method</span></span>

<span data-ttu-id="2586c-104">Obtém a transformação de Sprite.</span><span class="sxs-lookup"><span data-stu-id="2586c-104">Gets the sprite transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="2586c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2586c-105">Syntax</span></span>


```C++
HRESULT GetTransform(
  [in] D3DXMATRIX *pTransform
);
```



## <a name="parameters"></a><span data-ttu-id="2586c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2586c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2586c-107">*pTransform* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2586c-107">*pTransform* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2586c-108">Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2586c-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2586c-109">Ponteiro para um [**D3DXMATRIX**](d3dxmatrix.md) que contém uma transformação do sprite do espaço do mundo original.</span><span class="sxs-lookup"><span data-stu-id="2586c-109">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a transform of the sprite from the original world space.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2586c-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2586c-110">Return value</span></span>

<span data-ttu-id="2586c-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2586c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2586c-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2586c-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2586c-113">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="2586c-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="2586c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2586c-114">Requirements</span></span>



| <span data-ttu-id="2586c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2586c-115">Requirement</span></span> | <span data-ttu-id="2586c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2586c-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2586c-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2586c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2586c-118"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="2586c-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="2586c-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2586c-119">Library</span></span><br/> | <dl> <span data-ttu-id="2586c-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2586c-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2586c-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2586c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2586c-122">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="2586c-122">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




