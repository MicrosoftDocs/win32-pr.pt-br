---
description: Transforma animações em uma animação definida em um formato compactado e retorna um ponteiro para o buffer que armazena os dados compactados.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'Método ID3DXKeyframedAnimationSet:: compress (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cd3a278760f2598df52d251a9e3558a72f954ceb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105763005"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a><span data-ttu-id="9898b-103">Método ID3DXKeyframedAnimationSet:: compress</span><span class="sxs-lookup"><span data-stu-id="9898b-103">ID3DXKeyframedAnimationSet::Compress method</span></span>

<span data-ttu-id="9898b-104">Transforma animações em uma animação definida em um formato compactado e retorna um ponteiro para o buffer que armazena os dados compactados.</span><span class="sxs-lookup"><span data-stu-id="9898b-104">Transforms animations in an animation set into a compressed format and returns a pointer to the buffer that stores the compressed data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9898b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9898b-105">Syntax</span></span>


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a><span data-ttu-id="9898b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9898b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9898b-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="9898b-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9898b-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9898b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9898b-109">Um dos valores [**de \_ sinalizadores D3DXCOMPRESSION**](./d3dxcompression-flags.md) que definem o modo de compactação usado para armazenar dados de conjunto de animação compactados.</span><span class="sxs-lookup"><span data-stu-id="9898b-109">One of the [**D3DXCOMPRESSION\_FLAGS**](./d3dxcompression-flags.md) values that define the compression mode used for storing compressed animation set data.</span></span> <span data-ttu-id="9898b-110">D3DXCOMPRESS \_ default é o único valor com suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="9898b-110">D3DXCOMPRESS\_DEFAULT is the only value currently supported.</span></span>

</dd> <dt>

<span data-ttu-id="9898b-111">*Perda* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9898b-111">*Lossiness* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9898b-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9898b-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9898b-113">Taxa de perda de compactação desejada, no intervalo de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="9898b-113">Desired compression loss ratio, in the range from 0 to 1.</span></span>

</dd> <dt>

<span data-ttu-id="9898b-114">*pHierarchy* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9898b-114">*pHierarchy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9898b-115">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)**</span><span class="sxs-lookup"><span data-stu-id="9898b-115">Type: **[**LPD3DXFRAME**](d3dxframe.md)**</span></span>

<span data-ttu-id="9898b-116">Ponteiro para uma hierarquia de quadros de transformação [**D3DXFRAME**](d3dxframe.md) .</span><span class="sxs-lookup"><span data-stu-id="9898b-116">Pointer to a [**D3DXFRAME**](d3dxframe.md) transformation frame hierarchy.</span></span> <span data-ttu-id="9898b-117">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="9898b-117">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="9898b-118">*ppCompressedData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9898b-118">*ppCompressedData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9898b-119">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9898b-119">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="9898b-120">Endereço de um ponteiro para o conjunto de animações compactadas [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="9898b-120">Address of a pointer to the [**ID3DXBuffer**](id3dxbuffer.md) compressed animation set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9898b-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9898b-121">Return value</span></span>

<span data-ttu-id="9898b-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9898b-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9898b-123">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9898b-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="9898b-124">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="9898b-124">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="9898b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9898b-125">Requirements</span></span>



| <span data-ttu-id="9898b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9898b-126">Requirement</span></span> | <span data-ttu-id="9898b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="9898b-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9898b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9898b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9898b-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9898b-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9898b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9898b-130">Library</span></span><br/> | <dl> <span data-ttu-id="9898b-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9898b-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9898b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="9898b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9898b-133">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="9898b-133">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
