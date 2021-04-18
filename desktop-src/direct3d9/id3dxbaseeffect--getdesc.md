---
description: Obtém a descrição do efeito.
ms.assetid: 96b53b8a-0c20-4bfd-af45-626f6e0305d2
title: 'Método ID3DXBaseEffect:: GetDesc (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 35fcb62e9461d419e6643c99c1879efa28fa78c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105796088"
---
# <a name="id3dxbaseeffectgetdesc-method"></a><span data-ttu-id="b30b9-103">Método ID3DXBaseEffect:: GetDesc</span><span class="sxs-lookup"><span data-stu-id="b30b9-103">ID3DXBaseEffect::GetDesc method</span></span>

<span data-ttu-id="b30b9-104">Obtém a descrição do efeito.</span><span class="sxs-lookup"><span data-stu-id="b30b9-104">Gets the effect description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b30b9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b30b9-105">Syntax</span></span>


```C++
HRESULT GetDesc(
  [out] D3DXEFFECT_DESC *pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="b30b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b30b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b30b9-107">*pDesc* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b30b9-107">*pDesc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b30b9-108">Tipo: **[ **D3DXEFFECT \_ desc**](d3dxeffect-desc.md)\***</span><span class="sxs-lookup"><span data-stu-id="b30b9-108">Type: **[**D3DXEFFECT\_DESC**](d3dxeffect-desc.md)\***</span></span>

<span data-ttu-id="b30b9-109">Retorna uma descrição do efeito.</span><span class="sxs-lookup"><span data-stu-id="b30b9-109">Returns a description of the effect.</span></span> <span data-ttu-id="b30b9-110">Consulte [**D3DXEFFECT \_ desc**](d3dxeffect-desc.md).</span><span class="sxs-lookup"><span data-stu-id="b30b9-110">See [**D3DXEFFECT\_DESC**](d3dxeffect-desc.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b30b9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b30b9-111">Return value</span></span>

<span data-ttu-id="b30b9-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b30b9-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b30b9-113">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b30b9-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="b30b9-114">Se o método falhar, o valor de retorno poderá ser D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="b30b9-114">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b30b9-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b30b9-115">Requirements</span></span>



| <span data-ttu-id="b30b9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b30b9-116">Requirement</span></span> | <span data-ttu-id="b30b9-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b30b9-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b30b9-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b30b9-118">Header</span></span><br/>  | <dl> <span data-ttu-id="b30b9-119"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b30b9-119"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b30b9-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b30b9-120">Library</span></span><br/> | <dl> <span data-ttu-id="b30b9-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b30b9-121"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b30b9-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b30b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b30b9-123">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="b30b9-123">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 




