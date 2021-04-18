---
description: Cria uma cópia de um efeito.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: 'Método ID3DXEffect:: CloneEffect (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: eba2f6248bd1373ebf0aae55cf94103e2c269be7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771441"
---
# <a name="id3dxeffectcloneeffect-method"></a><span data-ttu-id="30373-103">Método ID3DXEffect:: CloneEffect</span><span class="sxs-lookup"><span data-stu-id="30373-103">ID3DXEffect::CloneEffect method</span></span>

<span data-ttu-id="30373-104">Cria uma cópia de um efeito.</span><span class="sxs-lookup"><span data-stu-id="30373-104">Creates a copy of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="30373-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30373-105">Syntax</span></span>


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="30373-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30373-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30373-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="30373-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30373-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="30373-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="30373-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado ao efeito.</span><span class="sxs-lookup"><span data-stu-id="30373-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> <dt>

<span data-ttu-id="30373-110">*ppEffect* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="30373-110">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30373-111">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="30373-111">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="30373-112">Ponteiro para uma interface [**ID3DXEffect**](id3dxeffect.md) , que contém o efeito clonado.</span><span class="sxs-lookup"><span data-stu-id="30373-112">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface, containing the cloned effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30373-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="30373-113">Return value</span></span>

<span data-ttu-id="30373-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="30373-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="30373-115">Se o método for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="30373-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="30373-116">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="30373-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="30373-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="30373-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30373-118">Essa função não clonará um efeito se o usuário especificar [D3DXFX \_ não \_ clonável](d3dxfx.md) durante a criação do efeito.</span><span class="sxs-lookup"><span data-stu-id="30373-118">This function will not clone an effect if the user specifies [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md) during effect creation.</span></span>

 

<span data-ttu-id="30373-119">Para atualizar parâmetros compartilhados e não compartilhados em uma técnica ativa de um efeito clonado, consulte [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md).</span><span class="sxs-lookup"><span data-stu-id="30373-119">To update shared and non-shared parameters in an active technique of a cloned effect, see [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30373-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30373-120">Requirements</span></span>



| <span data-ttu-id="30373-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="30373-121">Requirement</span></span> | <span data-ttu-id="30373-122">Valor</span><span class="sxs-lookup"><span data-stu-id="30373-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="30373-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30373-123">Header</span></span><br/>  | <dl> <span data-ttu-id="30373-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="30373-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="30373-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30373-125">Library</span></span><br/> | <dl> <span data-ttu-id="30373-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30373-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="30373-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="30373-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30373-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="30373-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
