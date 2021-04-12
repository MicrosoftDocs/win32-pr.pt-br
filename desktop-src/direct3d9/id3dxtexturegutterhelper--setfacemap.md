---
description: Define o índice do tipo de malha ao qual cada Texel pertence.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: 'Método ID3DXTextureGutterHelper:: SetFaceMap (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ba0472052d5e2e06d759c83a404a197ecda148f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173145"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a><span data-ttu-id="b00f8-103">Método ID3DXTextureGutterHelper:: SetFaceMap</span><span class="sxs-lookup"><span data-stu-id="b00f8-103">ID3DXTextureGutterHelper::SetFaceMap method</span></span>

<span data-ttu-id="b00f8-104">Define o índice do tipo de malha ao qual cada Texel pertence.</span><span class="sxs-lookup"><span data-stu-id="b00f8-104">Sets the index of the mesh face to which each texel belongs.</span></span>

## <a name="syntax"></a><span data-ttu-id="b00f8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b00f8-105">Syntax</span></span>


```C++
HRESULT SetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a><span data-ttu-id="b00f8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b00f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b00f8-107">*pFaceData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b00f8-107">*pFaceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b00f8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b00f8-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b00f8-109">Ponteiro para o índice da face de malha à qual cada Texel pertence.</span><span class="sxs-lookup"><span data-stu-id="b00f8-109">Pointer to the index of the mesh face to which each texel belongs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b00f8-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b00f8-110">Return value</span></span>

<span data-ttu-id="b00f8-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b00f8-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b00f8-112">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b00f8-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b00f8-113">Se o método falhar, o valor a seguir será retornado. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="b00f8-113">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="b00f8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b00f8-114">Remarks</span></span>

<span data-ttu-id="b00f8-115">A entrada de dados de face de malha para esse método é válida somente para texels válidas (não classe 0).</span><span class="sxs-lookup"><span data-stu-id="b00f8-115">The mesh face data input to this method is valid only for valid (non-class 0) texels.</span></span> <span data-ttu-id="b00f8-116">[**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) retornará valores diferentes de zero para texels válidos.</span><span class="sxs-lookup"><span data-stu-id="b00f8-116">[**ID3DXTextureGutterHelper::GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) will return non-zero values for valid texels.</span></span>

## <a name="requirements"></a><span data-ttu-id="b00f8-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b00f8-117">Requirements</span></span>



| <span data-ttu-id="b00f8-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b00f8-118">Requirement</span></span> | <span data-ttu-id="b00f8-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b00f8-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b00f8-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b00f8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b00f8-121"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b00f8-121"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b00f8-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b00f8-122">Library</span></span><br/> | <dl> <span data-ttu-id="b00f8-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b00f8-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b00f8-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b00f8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b00f8-125">ID3DXTextureGutterHelper</span><span class="sxs-lookup"><span data-stu-id="b00f8-125">ID3DXTextureGutterHelper</span></span>](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
