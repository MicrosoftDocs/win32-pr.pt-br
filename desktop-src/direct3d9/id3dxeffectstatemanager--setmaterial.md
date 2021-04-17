---
description: Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do material.
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'Método ID3DXEffectStateManager:: SetMaterial (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b503bd195468fb323e7e655c0bdd201e25dfdce2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105764061"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a><span data-ttu-id="47316-103">Método ID3DXEffectStateManager:: SetMaterial</span><span class="sxs-lookup"><span data-stu-id="47316-103">ID3DXEffectStateManager::SetMaterial method</span></span>

<span data-ttu-id="47316-104">Uma função de retorno de chamada que deve ser implementada por um usuário para definir o estado do material.</span><span class="sxs-lookup"><span data-stu-id="47316-104">A callback function that must be implemented by a user to set material state.</span></span>

## <a name="syntax"></a><span data-ttu-id="47316-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47316-105">Syntax</span></span>


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a><span data-ttu-id="47316-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47316-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47316-107">*pMaterial* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="47316-107">*pMaterial* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47316-108">Tipo: **const [**D3DMATERIAL9**](d3dmaterial9.md) \***</span><span class="sxs-lookup"><span data-stu-id="47316-108">Type: **const [**D3DMATERIAL9**](d3dmaterial9.md)\***</span></span>

<span data-ttu-id="47316-109">Um ponteiro para o estado do material.</span><span class="sxs-lookup"><span data-stu-id="47316-109">A pointer to the material state.</span></span> <span data-ttu-id="47316-110">Consulte [**D3DMATERIAL9**](d3dmaterial9.md).</span><span class="sxs-lookup"><span data-stu-id="47316-110">See [**D3DMATERIAL9**](d3dmaterial9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47316-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="47316-111">Return value</span></span>

<span data-ttu-id="47316-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47316-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47316-113">O método implementado pelo usuário deve retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="47316-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="47316-114">Se o retorno de chamada falhar ao definir o estado do dispositivo, ocorrerá uma das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="47316-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="47316-115">O efeito falhará durante [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md).</span><span class="sxs-lookup"><span data-stu-id="47316-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="47316-116">A chamada de estado de efeito dinâmico (como [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) falhará.</span><span class="sxs-lookup"><span data-stu-id="47316-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="47316-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47316-117">Requirements</span></span>



| <span data-ttu-id="47316-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="47316-118">Requirement</span></span> | <span data-ttu-id="47316-119">Valor</span><span class="sxs-lookup"><span data-stu-id="47316-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="47316-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="47316-120">Header</span></span><br/>  | <dl> <span data-ttu-id="47316-121"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="47316-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="47316-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="47316-122">Library</span></span><br/> | <dl> <span data-ttu-id="47316-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47316-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="47316-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="47316-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47316-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="47316-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
