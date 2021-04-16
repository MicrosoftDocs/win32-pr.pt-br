---
description: Multiplica cada valor no buffer por um valor constante.
ms.assetid: 3d7ef530-b83a-4123-a2ed-fff2b21378ee
title: 'Método ID3DXPRTBuffer:: ScaleBuffer (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ScaleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 05bdd066f4b7c33ad06f089551f16f0489608c83
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772906"
---
# <a name="id3dxprtbufferscalebuffer-method"></a><span data-ttu-id="eea60-103">Método ID3DXPRTBuffer:: ScaleBuffer</span><span class="sxs-lookup"><span data-stu-id="eea60-103">ID3DXPRTBuffer::ScaleBuffer method</span></span>

<span data-ttu-id="eea60-104">Multiplica cada valor no buffer por um valor constante.</span><span class="sxs-lookup"><span data-stu-id="eea60-104">Multiplies every value in the buffer by a constant value.</span></span>

## <a name="syntax"></a><span data-ttu-id="eea60-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eea60-105">Syntax</span></span>


```C++
HRESULT ScaleBuffer(
  [in] FLOAT Scale
);
```



## <a name="parameters"></a><span data-ttu-id="eea60-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eea60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eea60-107">*Escala* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="eea60-107">*Scale* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eea60-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eea60-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="eea60-109">Valor constante usado para dimensionar o buffer.</span><span class="sxs-lookup"><span data-stu-id="eea60-109">Constant value used to scale the buffer.</span></span> <span data-ttu-id="eea60-110">Cada valor no buffer é substituído pelo produto desse valor e pelo valor do buffer original.</span><span class="sxs-lookup"><span data-stu-id="eea60-110">Every value in the buffer is replaced by the product of this value and the original buffer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eea60-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eea60-111">Return value</span></span>

<span data-ttu-id="eea60-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eea60-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eea60-113">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eea60-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="eea60-114">Se o método falhar, o valor a seguir será retornado.</span><span class="sxs-lookup"><span data-stu-id="eea60-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="eea60-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eea60-115">Requirements</span></span>



| <span data-ttu-id="eea60-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="eea60-116">Requirement</span></span> | <span data-ttu-id="eea60-117">Valor</span><span class="sxs-lookup"><span data-stu-id="eea60-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eea60-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eea60-118">Header</span></span><br/>  | <dl> <span data-ttu-id="eea60-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="eea60-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="eea60-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eea60-120">Library</span></span><br/> | <dl> <span data-ttu-id="eea60-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eea60-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eea60-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="eea60-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eea60-123">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="eea60-123">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
