---
description: Obter um ponteiro para a memória do buffer de malha para modificar seu conteúdo.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: Método ID3DX10MeshBuffer::Map (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Map
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c4a71aaaffe7ed11429efa67b6065f94ecd154d0
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335350"
---
# <a name="id3dx10meshbuffermap-method"></a><span data-ttu-id="c8873-103">Método ID3DX10MeshBuffer::Map</span><span class="sxs-lookup"><span data-stu-id="c8873-103">ID3DX10MeshBuffer::Map method</span></span>

<span data-ttu-id="c8873-104">Obter um ponteiro para a memória do buffer de malha para modificar seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c8873-104">Get a pointer to the mesh buffer memory to modify its contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8873-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8873-105">Syntax</span></span>


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="c8873-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8873-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8873-107">*ppData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8873-107">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8873-108">Tipo: **\* \* void**</span><span class="sxs-lookup"><span data-stu-id="c8873-108">Type: **void\*\***</span></span>

<span data-ttu-id="c8873-109">Ponteiro para os dados do buffer.</span><span class="sxs-lookup"><span data-stu-id="c8873-109">Pointer to the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="c8873-110">*pSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c8873-110">*pSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8873-111">Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c8873-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c8873-112">O tamanho do buffer em bytes.</span><span class="sxs-lookup"><span data-stu-id="c8873-112">Size of the buffer in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8873-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c8873-113">Return value</span></span>

<span data-ttu-id="c8873-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c8873-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c8873-115">O valor de retorno é um dos valores listados em Códigos de Retorno [do Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="c8873-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c8873-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8873-116">Remarks</span></span>



 <span data-ttu-id="c8873-117">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="c8873-117">Differences between Direct3D 9 and Direct3D 10:</span></span>

- <span data-ttu-id="c8873-118">Map() no Direct3D 10 é análogo ao recurso Map() no Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="c8873-118">Map() in Direct3D 10 is analogous to resource Map() in Direct3D 9.</span></span>



 

## <a name="requirements"></a><span data-ttu-id="c8873-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8873-119">Requirements</span></span>



| <span data-ttu-id="c8873-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8873-120">Requirement</span></span> | <span data-ttu-id="c8873-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c8873-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c8873-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c8873-122">Header</span></span><br/>  | <dl> <span data-ttu-id="c8873-123"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="c8873-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8873-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c8873-124">Library</span></span><br/> | <dl> <span data-ttu-id="c8873-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8873-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8873-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c8873-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8873-127">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="c8873-127">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="c8873-128">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="c8873-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
