---
description: 'Acesse o buffer de índice da malha depois que ele tiver sido confirmado no dispositivo com ID3DX10Mesh:: CommitToDevice. Isso é diferente de ID3DX10Mesh:: GetIndexBuffer, que retorna o buffer de índice antes de ser confirmado no dispositivo.'
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'Método ID3DX10Mesh:: GetDeviceIndexBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105813309"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a><span data-ttu-id="cda2a-104">Método ID3DX10Mesh:: GetDeviceIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="cda2a-104">ID3DX10Mesh::GetDeviceIndexBuffer method</span></span>

<span data-ttu-id="cda2a-105">Acesse o buffer de índice da malha depois que ele tiver sido confirmado no dispositivo com [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md).</span><span class="sxs-lookup"><span data-stu-id="cda2a-105">Access the mesh's index buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="cda2a-106">Isso é diferente de [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), que retorna o buffer de índice antes de ser confirmado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cda2a-106">This is different from [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), which returns the index buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda2a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cda2a-107">Syntax</span></span>


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="cda2a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cda2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cda2a-109">*ppIndexBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cda2a-109">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cda2a-110">Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="cda2a-110">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="cda2a-111">O buffer de índice depois de ter sido confirmado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cda2a-111">The index buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cda2a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cda2a-112">Return value</span></span>

<span data-ttu-id="cda2a-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cda2a-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cda2a-114">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="cda2a-114">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cda2a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cda2a-115">Remarks</span></span>

<span data-ttu-id="cda2a-116">Se o buffer de índice da malha ainda não tiver sido confirmado no dispositivo, essa API confirmará automaticamente o buffer de índice antes de retornar um ponteiro para o buffer.</span><span class="sxs-lookup"><span data-stu-id="cda2a-116">If the mesh's index buffer has not already been committed to the device, this API will automatically commit the index buffer before it returns a pointer to the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="cda2a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cda2a-117">Requirements</span></span>



| <span data-ttu-id="cda2a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cda2a-118">Requirement</span></span> | <span data-ttu-id="cda2a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cda2a-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cda2a-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cda2a-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cda2a-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="cda2a-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cda2a-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cda2a-122">Library</span></span><br/> | <dl> <span data-ttu-id="cda2a-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cda2a-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda2a-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="cda2a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda2a-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="cda2a-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="cda2a-126">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="cda2a-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




