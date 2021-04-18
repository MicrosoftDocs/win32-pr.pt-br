---
description: Cancelar o mapeamento de um buffer.
ms.assetid: 47f125cd-5c0a-4814-93c5-f2f11ce33ea6
title: 'Método ID3DX10MeshBuffer:: inmapeamento (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer.Unmap
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0c3b382e0cfd01a51d89ddacb51ad390446315a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813517"
---
# <a name="id3dx10meshbufferunmap-method"></a><span data-ttu-id="79943-103">Método ID3DX10MeshBuffer:: remapeamento</span><span class="sxs-lookup"><span data-stu-id="79943-103">ID3DX10MeshBuffer::Unmap method</span></span>

<span data-ttu-id="79943-104">Cancelar o mapeamento de um buffer.</span><span class="sxs-lookup"><span data-stu-id="79943-104">Unmap a buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="79943-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79943-105">Syntax</span></span>


```C++
HRESULT Unmap();
```



## <a name="parameters"></a><span data-ttu-id="79943-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="79943-106">Parameters</span></span>

<span data-ttu-id="79943-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="79943-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79943-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="79943-108">Return value</span></span>

<span data-ttu-id="79943-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="79943-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="79943-110">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="79943-110">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="79943-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="79943-111">Remarks</span></span>



|                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79943-112">Diferenças entre o Direct3D 9 e o Direct3D 10:</span><span class="sxs-lookup"><span data-stu-id="79943-112">Differences between Direct3D 9 and Direct3D 10:</span></span><br/> <span data-ttu-id="79943-113">O desmapeamento () no Direct3D 10 é análogo ao desbloqueio de recurso () no Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="79943-113">Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="79943-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79943-114">Requirements</span></span>



| <span data-ttu-id="79943-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="79943-115">Requirement</span></span> | <span data-ttu-id="79943-116">Valor</span><span class="sxs-lookup"><span data-stu-id="79943-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79943-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79943-117">Header</span></span><br/>  | <dl> <span data-ttu-id="79943-118"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="79943-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="79943-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="79943-119">Library</span></span><br/> | <dl> <span data-ttu-id="79943-120"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79943-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79943-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="79943-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79943-122">ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="79943-122">ID3DX10MeshBuffer</span></span>](id3dx10meshbuffer.md)
</dt> <dt>

[<span data-ttu-id="79943-123">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="79943-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




