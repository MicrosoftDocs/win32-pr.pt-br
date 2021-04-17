---
description: Define a descrição da faixa.
ms.assetid: bc3324b3-ca23-4035-958d-9763a70071f2
title: 'Método ID3DXAnimationController:: SetTrackDesc (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1aca9385f1e9bc9439b9fe4b3dc1acddda94e395
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791264"
---
# <a name="id3dxanimationcontrollersettrackdesc-method"></a><span data-ttu-id="ff5b3-103">Método ID3DXAnimationController:: SetTrackDesc</span><span class="sxs-lookup"><span data-stu-id="ff5b3-103">ID3DXAnimationController::SetTrackDesc method</span></span>

<span data-ttu-id="ff5b3-104">Define a descrição da faixa.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-104">Sets the track description.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff5b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff5b3-105">Syntax</span></span>


```C++
HRESULT SetTrackDesc(
  [in] UINT             Track,
  [in] LPD3DXTRACK_DESC pDesc
);
```



## <a name="parameters"></a><span data-ttu-id="ff5b3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ff5b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff5b3-107">*Acompanhar* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff5b3-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5b3-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ff5b3-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ff5b3-109">Identificador da faixa a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-109">Identifier of the track to modify.</span></span>

</dd> <dt>

<span data-ttu-id="ff5b3-110">*pDesc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ff5b3-110">*pDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff5b3-111">Tipo: **[ **LPD3DXTRACK \_ desc**](d3dxtrack-desc.md)**</span><span class="sxs-lookup"><span data-stu-id="ff5b3-111">Type: **[**LPD3DXTRACK\_DESC**](d3dxtrack-desc.md)**</span></span>

<span data-ttu-id="ff5b3-112">Descrição da faixa.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-112">Description of the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff5b3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ff5b3-113">Return value</span></span>

<span data-ttu-id="ff5b3-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ff5b3-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ff5b3-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ff5b3-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ff5b3-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff5b3-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff5b3-117">Requirements</span></span>



| <span data-ttu-id="ff5b3-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff5b3-118">Requirement</span></span> | <span data-ttu-id="ff5b3-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ff5b3-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff5b3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff5b3-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ff5b3-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff5b3-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ff5b3-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ff5b3-122">Library</span></span><br/> | <dl> <span data-ttu-id="ff5b3-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff5b3-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ff5b3-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff5b3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff5b3-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="ff5b3-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
