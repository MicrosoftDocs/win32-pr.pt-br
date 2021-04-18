---
description: Extrai as IDs de cluster por amostra de um buffer de dados compactado ID3DXPRTCompBuffer.
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'Método ID3DXPRTCompBuffer:: ExtractClusterIDs (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef68a972109e89e318adb83ab388c653c6a3deed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771393"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a><span data-ttu-id="53ee8-103">Método ID3DXPRTCompBuffer:: ExtractClusterIDs</span><span class="sxs-lookup"><span data-stu-id="53ee8-103">ID3DXPRTCompBuffer::ExtractClusterIDs method</span></span>

<span data-ttu-id="53ee8-104">Extrai as IDs de cluster por amostra de um buffer de dados compactado [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="53ee8-104">Extracts the per-sample cluster IDs from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="53ee8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="53ee8-105">Syntax</span></span>


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a><span data-ttu-id="53ee8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="53ee8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53ee8-107">*pClusterIDs* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="53ee8-107">*pClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53ee8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="53ee8-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="53ee8-109">Ponteiro para o local na memória em que as IDs são gravadas.</span><span class="sxs-lookup"><span data-stu-id="53ee8-109">Pointer to the location in memory where IDs are written.</span></span> <span data-ttu-id="53ee8-110">O tamanho da memória necessária é o valor retornado por [**ID3DXPRTCompBuffer:: GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).</span><span class="sxs-lookup"><span data-stu-id="53ee8-110">The length of memory required is the value returned by [**ID3DXPRTCompBuffer::GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53ee8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="53ee8-111">Return value</span></span>

<span data-ttu-id="53ee8-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="53ee8-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="53ee8-113">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="53ee8-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="53ee8-114">Se o método falhar, o valor a seguir será retornado.</span><span class="sxs-lookup"><span data-stu-id="53ee8-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="53ee8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53ee8-115">Requirements</span></span>



| <span data-ttu-id="53ee8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="53ee8-116">Requirement</span></span> | <span data-ttu-id="53ee8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="53ee8-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53ee8-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="53ee8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="53ee8-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="53ee8-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="53ee8-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="53ee8-120">Library</span></span><br/> | <dl> <span data-ttu-id="53ee8-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53ee8-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="53ee8-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="53ee8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53ee8-123">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="53ee8-123">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
