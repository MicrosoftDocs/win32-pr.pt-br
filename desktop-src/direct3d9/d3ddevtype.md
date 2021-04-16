---
description: Define os tipos de dispositivo.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Enumeração D3DDEVTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761182"
---
# <a name="d3ddevtype-enumeration"></a><span data-ttu-id="1031f-103">Enumeração D3DDEVTYPE</span><span class="sxs-lookup"><span data-stu-id="1031f-103">D3DDEVTYPE enumeration</span></span>

<span data-ttu-id="1031f-104">Define os tipos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1031f-104">Defines device types.</span></span>

## <a name="syntax"></a><span data-ttu-id="1031f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1031f-105">Syntax</span></span>


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a><span data-ttu-id="1031f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1031f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1031f-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**\_Hal D3DDEVTYPE**</span><span class="sxs-lookup"><span data-stu-id="1031f-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE\_HAL**</span></span>
</dt> <dd>

<span data-ttu-id="1031f-108">Rasterização de hardware.</span><span class="sxs-lookup"><span data-stu-id="1031f-108">Hardware rasterization.</span></span> <span data-ttu-id="1031f-109">O sombreamento é feito com software, hardware ou transformação mista e iluminação.</span><span class="sxs-lookup"><span data-stu-id="1031f-109">Shading is done with software, hardware, or mixed transform and lighting.</span></span>

</dd> <dt>

<span data-ttu-id="1031f-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NULLREF**</span><span class="sxs-lookup"><span data-stu-id="1031f-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE\_NULLREF**</span></span>
</dt> <dd>

<span data-ttu-id="1031f-111">Inicialize o Direct3D em um computador que não tenha hardware nem que a rasterização de referência esteja disponível e habilite recursos para a criação de conteúdo 3D.</span><span class="sxs-lookup"><span data-stu-id="1031f-111">Initialize Direct3D on a computer that has neither hardware nor reference rasterization available, and enable resources for 3D content creation.</span></span> <span data-ttu-id="1031f-112">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="1031f-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1031f-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ ref**</span><span class="sxs-lookup"><span data-stu-id="1031f-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE\_REF**</span></span>
</dt> <dd>

<span data-ttu-id="1031f-114">Os recursos do Direct3D são implementados no software; no entanto, o rasterizador de referência faz uso de instruções de CPU especiais sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="1031f-114">Direct3D features are implemented in software; however, the reference rasterizer does make use of special CPU instructions whenever it can.</span></span>

<span data-ttu-id="1031f-115">O dispositivo de referência é instalado pelo SDK do Windows 8,0 ou posterior e destina-se como uma ajuda na depuração apenas para desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="1031f-115">The reference device is installed by the Windows SDK 8.0 or later and is intended as an aid in debugging for development only.</span></span>

</dd> <dt>

<span data-ttu-id="1031f-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**</span><span class="sxs-lookup"><span data-stu-id="1031f-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE\_SW**</span></span>
</dt> <dd>

<span data-ttu-id="1031f-117">Um dispositivo de software conectável que foi registrado com [**IDirect3D9:: RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span><span class="sxs-lookup"><span data-stu-id="1031f-117">A pluggable software device that has been registered with [**IDirect3D9::RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span></span>

</dd> <dt>

<span data-ttu-id="1031f-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="1031f-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="1031f-119">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="1031f-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="1031f-120">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="1031f-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="1031f-121">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="1031f-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1031f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="1031f-122">Remarks</span></span>

<span data-ttu-id="1031f-123">Todos os métodos da interface [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) que usam um tipo de dispositivo **D3DDEVTYPE** falharão se D3DDEVTYPE \_ NULLREF for especificado.</span><span class="sxs-lookup"><span data-stu-id="1031f-123">All methods of the [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) interface that take a **D3DDEVTYPE** device type will fail if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="1031f-124">Para usar esses métodos, substitua D3DDEVTYPE \_ ref na chamada do método.</span><span class="sxs-lookup"><span data-stu-id="1031f-124">To use these methods, substitute D3DDEVTYPE\_REF in the method call.</span></span>

<span data-ttu-id="1031f-125">Um dispositivo de referência de D3DDEVTYPE \_ deve ser criado na memória de rascunho do D3DPOOL \_ , a menos que os buffers de vértice e de índice sejam necessários.</span><span class="sxs-lookup"><span data-stu-id="1031f-125">A D3DDEVTYPE\_REF device should be created in D3DPOOL\_SCRATCH memory, unless vertex and index buffers are required.</span></span> <span data-ttu-id="1031f-126">Para dar suporte a buffers de vértice e de índice, crie o dispositivo no D3DPOOL \_ SYSTEMMEM Memory.</span><span class="sxs-lookup"><span data-stu-id="1031f-126">To support vertex and index buffers, create the device in D3DPOOL\_SYSTEMMEM memory.</span></span>

<span data-ttu-id="1031f-127">Se D3dref9.dll estiver instalado, o Direct3D usará o rasterizador de referência para criar um \_ tipo de dispositivo D3DDEVTYPE ref, mesmo se D3DDEVTYPE \_ NULLREF for especificado.</span><span class="sxs-lookup"><span data-stu-id="1031f-127">If D3dref9.dll is installed, Direct3D will use the reference rasterizer to create a D3DDEVTYPE\_REF device type, even if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="1031f-128">Se D3dref9.dll não estiver disponível e D3DDEVTYPE \_ NULLREF for especificado, o Direct3D não será renderizado nem apresentará a cena.</span><span class="sxs-lookup"><span data-stu-id="1031f-128">If D3dref9.dll is not available and D3DDEVTYPE\_NULLREF is specified, Direct3D will neither render nor present the scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="1031f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1031f-129">Requirements</span></span>



| <span data-ttu-id="1031f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1031f-130">Requirement</span></span> | <span data-ttu-id="1031f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="1031f-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1031f-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1031f-132">Header</span></span><br/> | <dl> <span data-ttu-id="1031f-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1031f-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1031f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1031f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1031f-135">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="1031f-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="1031f-136">**IDirect3D9::CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="1031f-136">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[<span data-ttu-id="1031f-137">**IDirect3D9::CheckDeviceMultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="1031f-137">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[<span data-ttu-id="1031f-138">**IDirect3D9::CheckDeviceType**</span><span class="sxs-lookup"><span data-stu-id="1031f-138">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[<span data-ttu-id="1031f-139">**IDirect3D9:: CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="1031f-139">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="1031f-140">**IDirect3D9::GetDeviceCaps**</span><span class="sxs-lookup"><span data-stu-id="1031f-140">**IDirect3D9::GetDeviceCaps**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[<span data-ttu-id="1031f-141">**\_Parâmetros de criação de D3DDEVICE \_**</span><span class="sxs-lookup"><span data-stu-id="1031f-141">**D3DDEVICE\_CREATION\_PARAMETERS**</span></span>](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
