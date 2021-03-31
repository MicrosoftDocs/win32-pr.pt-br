---
description: Define constantes que descrevem o tipo de buffer de fundo.
ms.assetid: f099656b-4957-40a7-a92e-2c17e5fa8df9
title: Enumeração de D3DBACKBUFFER_TYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBACKBUFFER_TYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 1641b37242339173fc5f591280d8e2beeff6a9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930561"
---
# <a name="d3dbackbuffer_type-enumeration"></a><span data-ttu-id="fbdf2-103">\_Enumeração de tipo D3DBACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="fbdf2-103">D3DBACKBUFFER\_TYPE enumeration</span></span>

<span data-ttu-id="fbdf2-104">Define constantes que descrevem o tipo de buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="fbdf2-104">Defines constants that describe the type of back buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbdf2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbdf2-105">Syntax</span></span>


```C++
typedef enum D3DBACKBUFFER_TYPE { 
  D3DBACKBUFFER_TYPE_MONO         = 0,
  D3DBACKBUFFER_TYPE_LEFT         = 1,
  D3DBACKBUFFER_TYPE_RIGHT        = 2,
  D3DBACKBUFFER_TYPE_FORCE_DWORD  = 0x7fffffff
} D3DBACKBUFFER_TYPE, *LPD3DBACKBUFFER_TYPE;
```



## <a name="constants"></a><span data-ttu-id="fbdf2-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="fbdf2-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fbdf2-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER \_ tipo \_ mono**</span><span class="sxs-lookup"><span data-stu-id="fbdf2-107"><span id="D3DBACKBUFFER_TYPE_MONO"></span><span id="d3dbackbuffer_type_mono"></span>**D3DBACKBUFFER\_TYPE\_MONO**</span></span>
</dt> <dd>

<span data-ttu-id="fbdf2-108">Especifica uma cadeia de permuta não estéreo.</span><span class="sxs-lookup"><span data-stu-id="fbdf2-108">Specifies a nonstereo swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="fbdf2-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER \_ tipo \_ esquerdo**</span><span class="sxs-lookup"><span data-stu-id="fbdf2-109"><span id="D3DBACKBUFFER_TYPE_LEFT"></span><span id="d3dbackbuffer_type_left"></span>**D3DBACKBUFFER\_TYPE\_LEFT**</span></span>
</dt> <dd>

<span data-ttu-id="fbdf2-110">Especifica o lado esquerdo de um par estéreo em uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="fbdf2-110">Specifies the left side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="fbdf2-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER \_ tipo \_ direito**</span><span class="sxs-lookup"><span data-stu-id="fbdf2-111"><span id="D3DBACKBUFFER_TYPE_RIGHT"></span><span id="d3dbackbuffer_type_right"></span>**D3DBACKBUFFER\_TYPE\_RIGHT**</span></span>
</dt> <dd>

<span data-ttu-id="fbdf2-112">Especifica o lado direito de um par estéreo em uma cadeia de permuta.</span><span class="sxs-lookup"><span data-stu-id="fbdf2-112">Specifies the right side of a stereo pair in a swap chain.</span></span>

</dd> <dt>

<span data-ttu-id="fbdf2-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER do \_ tipo \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="fbdf2-113"><span id="D3DBACKBUFFER_TYPE_FORCE_DWORD"></span><span id="d3dbackbuffer_type_force_dword"></span>**D3DBACKBUFFER\_TYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="fbdf2-114">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="fbdf2-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="fbdf2-115">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fbdf2-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="fbdf2-116">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="fbdf2-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fbdf2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="fbdf2-117">Remarks</span></span>

<span data-ttu-id="fbdf2-118">O Direct3D 9 não dá suporte à exibição de estéreo; portanto, o Direct3D não usa o \_ tipo D3DBACKBUFFER \_ Left e os \_ \_ valores de tipo Right desse tipo enumerado.</span><span class="sxs-lookup"><span data-stu-id="fbdf2-118">Direct3D 9 does not support stereo view, so Direct3D does not use the D3DBACKBUFFER\_TYPE\_LEFT and D3DBACKBUFFER\_TYPE\_RIGHT values of this enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbdf2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbdf2-119">Requirements</span></span>



| <span data-ttu-id="fbdf2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbdf2-120">Requirement</span></span> | <span data-ttu-id="fbdf2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fbdf2-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbdf2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fbdf2-122">Header</span></span><br/> | <dl> <span data-ttu-id="fbdf2-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="fbdf2-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbdf2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="fbdf2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbdf2-125">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="fbdf2-125">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="fbdf2-126">**IDirect3DDevice9::GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="fbdf2-126">**IDirect3DDevice9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getbackbuffer)
</dt> <dt>

[<span data-ttu-id="fbdf2-127">**IDirect3DSwapChain9::GetBackBuffer**</span><span class="sxs-lookup"><span data-stu-id="fbdf2-127">**IDirect3DSwapChain9::GetBackBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)
</dt> </dl>

 

 
