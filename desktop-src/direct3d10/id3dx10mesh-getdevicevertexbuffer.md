---
description: 'Acesse o buffer de vértice da malha depois que ele tiver sido confirmado no dispositivo com ID3DX10Mesh:: CommitToDevice. Isso é diferente de ID3DX10Mesh:: GetVertexBuffer, que retorna o buffer de vértice antes de ser confirmado no dispositivo.'
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'Método ID3DX10Mesh:: GetDeviceVertexBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9943050d174acb4e8f8e676f56a95cfdcde88f5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105787595"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a><span data-ttu-id="222c6-104">Método ID3DX10Mesh:: GetDeviceVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="222c6-104">ID3DX10Mesh::GetDeviceVertexBuffer method</span></span>

<span data-ttu-id="222c6-105">Acesse o buffer de vértice da malha depois que ele tiver sido confirmado no dispositivo com [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md).</span><span class="sxs-lookup"><span data-stu-id="222c6-105">Access the mesh's vertex buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="222c6-106">Isso é diferente de [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), que retorna o buffer de vértice antes de ser confirmado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="222c6-106">This is different from [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), which returns the vertex buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="222c6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="222c6-107">Syntax</span></span>


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="222c6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="222c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="222c6-109">*iBuffer* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="222c6-109">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="222c6-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="222c6-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="222c6-111">Um índice que identifica qual buffer de vértice deve ser acessado.</span><span class="sxs-lookup"><span data-stu-id="222c6-111">An index identifying which vertex buffer to access.</span></span>

</dd> <dt>

<span data-ttu-id="222c6-112">*ppVertexBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="222c6-112">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="222c6-113">Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="222c6-113">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="222c6-114">O buffer de vértice após ter sido confirmado no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="222c6-114">The vertex buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="222c6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="222c6-115">Return value</span></span>

<span data-ttu-id="222c6-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="222c6-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="222c6-117">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="222c6-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="222c6-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="222c6-118">Requirements</span></span>



| <span data-ttu-id="222c6-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="222c6-119">Requirement</span></span> | <span data-ttu-id="222c6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="222c6-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="222c6-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="222c6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="222c6-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="222c6-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="222c6-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="222c6-123">Library</span></span><br/> | <dl> <span data-ttu-id="222c6-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="222c6-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="222c6-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="222c6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="222c6-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="222c6-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="222c6-127">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="222c6-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
