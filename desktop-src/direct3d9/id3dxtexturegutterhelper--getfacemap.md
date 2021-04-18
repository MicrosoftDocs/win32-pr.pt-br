---
description: Recupera o índice do tipo de malha ao qual cada Texel pertence.
ms.assetid: 3eb3461c-4e16-4c89-9ca9-fc9c6b5638c7
title: 'Método ID3DXTextureGutterHelper:: GetFaceMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.GetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8164ec35c3b3596914577287ecc6b9285142fca8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105786292"
---
# <a name="id3dxtexturegutterhelpergetfacemap-method"></a><span data-ttu-id="323a3-103">Método ID3DXTextureGutterHelper:: GetFaceMap</span><span class="sxs-lookup"><span data-stu-id="323a3-103">ID3DXTextureGutterHelper::GetFaceMap method</span></span>

<span data-ttu-id="323a3-104">Recupera o índice do tipo de malha ao qual cada Texel pertence.</span><span class="sxs-lookup"><span data-stu-id="323a3-104">Retrieves the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="323a3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="323a3-105">Syntax</span></span>


```C++
HRESULT GetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="323a3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="323a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="323a3-107">*pFaceData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="323a3-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="323a3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="323a3-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="323a3-109">Ponteiro para o índice da face de malha à qual cada Texel pertence.</span><span class="sxs-lookup"><span data-stu-id="323a3-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="323a3-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="323a3-110">Return value</span></span>

<span data-ttu-id="323a3-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="323a3-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="323a3-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="323a3-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="323a3-113">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="323a3-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="323a3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="323a3-114">Remarks</span></span>

<span data-ttu-id="323a3-115">Os dados de face de malha retornados por esse método são válidos somente para texels válidos (não classe 0).</span><span class="sxs-lookup"><span data-stu-id="323a3-115">The mesh face data returned by this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="323a3-116">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retornará valores diferentes de zero para texels válidos (não classe 0).</span><span class="sxs-lookup"><span data-stu-id="323a3-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return nonzero values for valid (non-class 0) texels.</span></span>

<span data-ttu-id="323a3-117">Para a [**classe 2 texels**](id3dxtexturegutterhelper.md), esse método recupera a face mais próxima.</span><span class="sxs-lookup"><span data-stu-id="323a3-117">For [**class 2 texels**](id3dxtexturegutterhelper.md), this method retrieves the closest face.</span></span>

<span data-ttu-id="323a3-118">O aplicativo deve alocar e gerenciar pFaceData.</span><span class="sxs-lookup"><span data-stu-id="323a3-118">The application must allocate and manage pFaceData.</span></span>

## <a name="requirements"></a><span data-ttu-id="323a3-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="323a3-119">Requirements</span></span>



| <span data-ttu-id="323a3-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="323a3-120">Requirement</span></span> | <span data-ttu-id="323a3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="323a3-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="323a3-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="323a3-122">Header</span></span><br/>  | <dl> <span data-ttu-id="323a3-123"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="323a3-123"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="323a3-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="323a3-124">Library</span></span><br/> | <dl> <span data-ttu-id="323a3-125"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="323a3-125"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="323a3-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="323a3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="323a3-127">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="323a3-127">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
