---
description: Obtenha um ponteiro para a memória do buffer de malha para modificar seu conteúdo.
ms.assetid: d15ed47a-450e-404a-bcc2-a641abc2d02e
title: 'Método ID3DX10MeshBuffer:: Map (D3DX10. h)'
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
ms.openlocfilehash: 1b8cb03e128a6673963ce2d3cde993babb03da5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298638"
---
# <a name="id3dx10meshbuffermap-method"></a><span data-ttu-id="d89b1-103">Método ID3DX10MeshBuffer:: map</span><span class="sxs-lookup"><span data-stu-id="d89b1-103">ID3DX10MeshBuffer::Map method</span></span>

<span data-ttu-id="d89b1-104">Obtenha um ponteiro para a memória do buffer de malha para modificar seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="d89b1-104">Get a pointer to the mesh buffer memory to modify its contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="d89b1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d89b1-105">Syntax</span></span>


```C++
HRESULT Map(
  [out] void   **ppData,
  [out] SIZE_T *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="d89b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d89b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d89b1-107">*ppData* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d89b1-107">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d89b1-108">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="d89b1-108">Type: **void\*\***</span></span>

<span data-ttu-id="d89b1-109">Ponteiro para os dados do buffer.</span><span class="sxs-lookup"><span data-stu-id="d89b1-109">Pointer to the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="d89b1-110">*psize* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d89b1-110">*pSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d89b1-111">Tipo: **[ **tamanho \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d89b1-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d89b1-112">O tamanho do buffer em bytes.</span><span class="sxs-lookup"><span data-stu-id="d89b1-112">Size of the buffer in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d89b1-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d89b1-113">Return value</span></span>

<span data-ttu-id="d89b1-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d89b1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d89b1-115">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d89b1-115">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d89b1-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="d89b1-116">Remarks</span></span>



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d89b1-117">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="d89b1-117">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="d89b1-118">O MAP () no Direct3D 10 é análogo ao mapa de recursos () no Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="d89b1-118">Map() in Direct3D 10 is analogous to resource Map() in Direct3D 9.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d89b1-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d89b1-119">Requirements</span></span>



| <span data-ttu-id="d89b1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d89b1-120">Requirement</span></span> | <span data-ttu-id="d89b1-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d89b1-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d89b1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d89b1-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d89b1-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="d89b1-123"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d89b1-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d89b1-124">Library</span></span><br/> | <dl> <span data-ttu-id="d89b1-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d89b1-125"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d89b1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d89b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d89b1-127">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="d89b1-127">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="d89b1-128">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="d89b1-128">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
