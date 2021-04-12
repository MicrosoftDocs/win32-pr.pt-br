---
description: Os aplicativos usam a interface ID3DXEffectPool para identificar os parâmetros que serão compartilhados entre os efeitos. Consulte compartilhamento de parâmetro em clonagem e compartilhamento (Direct3D 9). Esta interface não tem métodos.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Interface ID3DXEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104370926"
---
# <a name="id3dxeffectpool-interface"></a><span data-ttu-id="2d2f3-105">Interface ID3DXEffectPool</span><span class="sxs-lookup"><span data-stu-id="2d2f3-105">ID3DXEffectPool interface</span></span>

<span data-ttu-id="2d2f3-106">Os aplicativos usam a interface **ID3DXEffectPool** para identificar os parâmetros que serão compartilhados entre os efeitos.</span><span class="sxs-lookup"><span data-stu-id="2d2f3-106">Applications use the **ID3DXEffectPool** interface to identify parameters that are going to be shared across effects.</span></span> <span data-ttu-id="2d2f3-107">Consulte compartilhamento de parâmetro em [clonagem e compartilhamento (Direct3D 9)](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="2d2f3-107">See parameter sharing in [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span> <span data-ttu-id="2d2f3-108">Esta interface não tem métodos.</span><span class="sxs-lookup"><span data-stu-id="2d2f3-108">This interface has no methods.</span></span>

## <a name="members"></a><span data-ttu-id="2d2f3-109">Membros</span><span class="sxs-lookup"><span data-stu-id="2d2f3-109">Members</span></span>

<span data-ttu-id="2d2f3-110">A interface **ID3DXEffectPool** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="2d2f3-110">The **ID3DXEffectPool** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d2f3-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d2f3-111">Remarks</span></span>

<span data-ttu-id="2d2f3-112">A interface ID3DXEffectPool é obtida chamando [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span><span class="sxs-lookup"><span data-stu-id="2d2f3-112">The ID3DXEffectPool interface is obtained by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span></span>

<span data-ttu-id="2d2f3-113">O tipo LPD3DXEFFECTPOOL é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="2d2f3-113">The LPD3DXEFFECTPOOL type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a><span data-ttu-id="2d2f3-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d2f3-114">Requirements</span></span>



| <span data-ttu-id="2d2f3-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d2f3-115">Requirement</span></span> | <span data-ttu-id="2d2f3-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2d2f3-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d2f3-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2d2f3-117">Header</span></span><br/>  | <dl> <span data-ttu-id="2d2f3-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d2f3-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2d2f3-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2d2f3-119">Library</span></span><br/> | <dl> <span data-ttu-id="2d2f3-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d2f3-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2d2f3-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d2f3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d2f3-122">Interfaces de efeito</span><span class="sxs-lookup"><span data-stu-id="2d2f3-122">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
