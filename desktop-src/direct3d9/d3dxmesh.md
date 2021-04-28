---
description: Enumeração D3DXMESH – sinalizadores usados para especificar as opções de criação para uma malha.
ms.assetid: c94e19ab-8024-4a28-9d1a-6d57707c3a52
title: Enumeração D3DXMESH (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESH
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a312c2618960691184182039afe38acc8947eb6a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098094"
---
# <a name="d3dxmesh-enumeration"></a><span data-ttu-id="16807-103">Enumeração D3DXMESH</span><span class="sxs-lookup"><span data-stu-id="16807-103">D3DXMESH enumeration</span></span>

<span data-ttu-id="16807-104">Sinalizadores usados para especificar as opções de criação para uma malha.</span><span class="sxs-lookup"><span data-stu-id="16807-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="16807-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16807-105">Syntax</span></span>


```C++
typedef enum D3DXMESH { 
  D3DXMESH_32BIT                  = 0x001,
  D3DXMESH_DONOTCLIP              = 0x002,
  D3DXMESH_POINTS                 = 0x004,
  D3DXMESH_RTPATCHES              = 0x008,
  D3DXMESH_NPATCHES               = 0x4000,
  D3DXMESH_VB_SYSTEMMEM           = 0x010,
  D3DXMESH_VB_MANAGED             = 0x020,
  D3DXMESH_VB_WRITEONLY           = 0x040,
  D3DXMESH_VB_DYNAMIC             = 0x080,
  D3DXMESH_VB_SOFTWAREPROCESSING  = 0x8000,
  D3DXMESH_IB_SYSTEMMEM           = 0x100,
  D3DXMESH_IB_MANAGED             = 0x200,
  D3DXMESH_IB_WRITEONLY           = 0x400,
  D3DXMESH_IB_DYNAMIC             = 0x800,
  D3DXMESH_IB_SOFTWAREPROCESSING  = 0x10000,
  D3DXMESH_VB_SHARE               = 0x1000,
  D3DXMESH_USEHWONLY              = 0x2000,
  D3DXMESH_SYSTEMMEM              = 0x110,
  D3DXMESH_MANAGED                = 0x220,
  D3DXMESH_WRITEONLY              = 0x440,
  D3DXMESH_DYNAMIC                = 0x880,
  D3DXMESH_SOFTWAREPROCESSING     = 0x18000
} D3DXMESH, *LPD3DXMESH;
```



## <a name="constants"></a><span data-ttu-id="16807-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="16807-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="16807-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH \_ 32 bits**</span><span class="sxs-lookup"><span data-stu-id="16807-107"><span id="D3DXMESH_32BIT"></span><span id="d3dxmesh_32bit"></span>**D3DXMESH\_32BIT**</span></span>
</dt> <dd>

<span data-ttu-id="16807-108">A malha tem índices de 32 bits em vez de índices de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="16807-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="16807-109">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="16807-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="16807-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH \_ DONOTCLIP**</span><span class="sxs-lookup"><span data-stu-id="16807-110"><span id="D3DXMESH_DONOTCLIP"></span><span id="d3dxmesh_donotclip"></span>**D3DXMESH\_DONOTCLIP**</span></span>
</dt> <dd>

<span data-ttu-id="16807-111">Use o sinalizador de uso [**D3DUSAGE \_ DONOTCLIP**](d3dusage.md) para os buffers de vértice e de índice.</span><span class="sxs-lookup"><span data-stu-id="16807-111">Use the [**D3DUSAGE\_DONOTCLIP**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**Pontos de D3DXMESH \_**</span><span class="sxs-lookup"><span data-stu-id="16807-112"><span id="D3DXMESH_POINTS"></span><span id="d3dxmesh_points"></span>**D3DXMESH\_POINTS**</span></span>
</dt> <dd>

<span data-ttu-id="16807-113">Use o sinalizador de uso de [**\_ pontos D3DUSAGE**](d3dusage.md) para os buffers de vértice e de índice.</span><span class="sxs-lookup"><span data-stu-id="16807-113">Use the [**D3DUSAGE\_POINTS**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH \_ RTPATCHES**</span><span class="sxs-lookup"><span data-stu-id="16807-114"><span id="D3DXMESH_RTPATCHES"></span><span id="d3dxmesh_rtpatches"></span>**D3DXMESH\_RTPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="16807-115">Use o sinalizador de uso [**D3DUSAGE \_ RTPATCHES**](d3dusage.md) para os buffers de vértice e de índice.</span><span class="sxs-lookup"><span data-stu-id="16807-115">Use the [**D3DUSAGE\_RTPATCHES**](d3dusage.md) usage flag for vertex and index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH \_ NPATCHES**</span><span class="sxs-lookup"><span data-stu-id="16807-116"><span id="D3DXMESH_NPATCHES"></span><span id="d3dxmesh_npatches"></span>**D3DXMESH\_NPATCHES**</span></span>
</dt> <dd>

<span data-ttu-id="16807-117">A especificação desse sinalizador faz com que o vértice e o buffer do índice da malha sejam criados com o sinalizador [**D3DUSAGE \_ NPATCHES**](d3dusage.md) .</span><span class="sxs-lookup"><span data-stu-id="16807-117">Specifying this flag causes the vertex and index buffer of the mesh to be created with [**D3DUSAGE\_NPATCHES**](d3dusage.md) flag.</span></span> <span data-ttu-id="16807-118">Isso será necessário se o objeto de malha for renderizado usando o aprimoramento de N-patch usando o Direct3D.</span><span class="sxs-lookup"><span data-stu-id="16807-118">This is required if the mesh object is to be rendered using N-patch enhancement using Direct3D.</span></span>

</dd> <dt>

<span data-ttu-id="16807-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH \_ VB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="16807-119"><span id="D3DXMESH_VB_SYSTEMMEM"></span><span id="d3dxmesh_vb_systemmem"></span>**D3DXMESH\_VB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="16807-120">Use o sinalizador de uso [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) para os buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="16807-120">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**Gerenciado por D3DXMESH \_ VB \_**</span><span class="sxs-lookup"><span data-stu-id="16807-121"><span id="D3DXMESH_VB_MANAGED"></span><span id="d3dxmesh_vb_managed"></span>**D3DXMESH\_VB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="16807-122">Use o sinalizador de uso [**\_ gerenciado D3DPOOL**](./d3dpool.md) para buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="16807-122">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH \_ VB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="16807-123"><span id="D3DXMESH_VB_WRITEONLY"></span><span id="d3dxmesh_vb_writeonly"></span>**D3DXMESH\_VB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="16807-124">Use o sinalizador de uso de [**\_ WRITEONLY D3DUSAGE**](d3dusage.md) para buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="16807-124">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH \_ VB \_ Dynamic**</span><span class="sxs-lookup"><span data-stu-id="16807-125"><span id="D3DXMESH_VB_DYNAMIC"></span><span id="d3dxmesh_vb_dynamic"></span>**D3DXMESH\_VB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="16807-126">Use o sinalizador de uso [**\_ dinâmico D3DUSAGE**](d3dusage.md) para buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="16807-126">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH \_ VB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="16807-127"><span id="D3DXMESH_VB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_vb_softwareprocessing"></span>**D3DXMESH\_VB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="16807-128">Use o sinalizador de uso [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) para os buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="16807-128">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH \_ IB \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="16807-129"><span id="D3DXMESH_IB_SYSTEMMEM"></span><span id="d3dxmesh_ib_systemmem"></span>**D3DXMESH\_IB\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="16807-130">Use o sinalizador de uso [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) para buffers de índice.</span><span class="sxs-lookup"><span data-stu-id="16807-130">Use the [**D3DPOOL\_SYSTEMMEM**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH \_ IB \_ gerenciado**</span><span class="sxs-lookup"><span data-stu-id="16807-131"><span id="D3DXMESH_IB_MANAGED"></span><span id="d3dxmesh_ib_managed"></span>**D3DXMESH\_IB\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="16807-132">Use o sinalizador de uso [**\_ gerenciado D3DPOOL**](./d3dpool.md) para buffers de índice.</span><span class="sxs-lookup"><span data-stu-id="16807-132">Use the [**D3DPOOL\_MANAGED**](./d3dpool.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH \_ IB \_ WRITEONLY**</span><span class="sxs-lookup"><span data-stu-id="16807-133"><span id="D3DXMESH_IB_WRITEONLY"></span><span id="d3dxmesh_ib_writeonly"></span>**D3DXMESH\_IB\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="16807-134">Use o sinalizador de uso de [**\_ WRITEONLY D3DUSAGE**](d3dusage.md) para buffers de índice.</span><span class="sxs-lookup"><span data-stu-id="16807-134">Use the [**D3DUSAGE\_WRITEONLY**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH \_ IB \_ Dynamic**</span><span class="sxs-lookup"><span data-stu-id="16807-135"><span id="D3DXMESH_IB_DYNAMIC"></span><span id="d3dxmesh_ib_dynamic"></span>**D3DXMESH\_IB\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="16807-136">Use o sinalizador de uso [**\_ dinâmico D3DUSAGE**](d3dusage.md) para buffers de índice.</span><span class="sxs-lookup"><span data-stu-id="16807-136">Use the [**D3DUSAGE\_DYNAMIC**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH \_ IB \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="16807-137"><span id="D3DXMESH_IB_SOFTWAREPROCESSING"></span><span id="d3dxmesh_ib_softwareprocessing"></span>**D3DXMESH\_IB\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="16807-138">Use o sinalizador de uso [**D3DUSAGE \_ SOFTWAREPROCESSING**](d3dusage.md) para buffers de índice.</span><span class="sxs-lookup"><span data-stu-id="16807-138">Use the [**D3DUSAGE\_SOFTWAREPROCESSING**](d3dusage.md) usage flag for index buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**\_Compartilhamento D3DXMESH VB \_**</span><span class="sxs-lookup"><span data-stu-id="16807-139"><span id="D3DXMESH_VB_SHARE"></span><span id="d3dxmesh_vb_share"></span>**D3DXMESH\_VB\_SHARE**</span></span>
</dt> <dd>

<span data-ttu-id="16807-140">Força as malhas clonadas a compartilhar buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="16807-140">Forces the cloned meshes to share vertex buffers.</span></span>

</dd> <dt>

<span data-ttu-id="16807-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH \_ USEHWONLY**</span><span class="sxs-lookup"><span data-stu-id="16807-141"><span id="D3DXMESH_USEHWONLY"></span><span id="d3dxmesh_usehwonly"></span>**D3DXMESH\_USEHWONLY**</span></span>
</dt> <dd>

<span data-ttu-id="16807-142">Use somente o processamento de hardware.</span><span class="sxs-lookup"><span data-stu-id="16807-142">Use hardware processing only.</span></span> <span data-ttu-id="16807-143">Para o dispositivo de modo misto, esse sinalizador fará com que o sistema Use hardware (se houver suporte no hardware) ou usará como padrão o processamento de software.</span><span class="sxs-lookup"><span data-stu-id="16807-143">For mixed-mode device, this flag will cause the system to use hardware (if supported in hardware) or will default to software processing.</span></span>

</dd> <dt>

<span data-ttu-id="16807-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="16807-144"><span id="D3DXMESH_SYSTEMMEM"></span><span id="d3dxmesh_systemmem"></span>**D3DXMESH\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="16807-145">Equivalente a especificar D3DXMESH \_ VB \_ SYSTEMMEM e D3DXMESH \_ IB \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="16807-145">Equivalent to specifying both D3DXMESH\_VB\_SYSTEMMEM and D3DXMESH\_IB\_SYSTEMMEM.</span></span>

</dd> <dt>

<span data-ttu-id="16807-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**\_Gerenciado D3DXMESH**</span><span class="sxs-lookup"><span data-stu-id="16807-146"><span id="D3DXMESH_MANAGED"></span><span id="d3dxmesh_managed"></span>**D3DXMESH\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="16807-147">Equivalente a especificar o D3DXMESH \_ VB \_ gerenciado e o D3DXMESH \_ IB \_ gerenciados.</span><span class="sxs-lookup"><span data-stu-id="16807-147">Equivalent to specifying both D3DXMESH\_VB\_MANAGED and D3DXMESH\_IB\_MANAGED.</span></span>

</dd> <dt>

<span data-ttu-id="16807-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**\_WRITEONLY D3DXMESH**</span><span class="sxs-lookup"><span data-stu-id="16807-148"><span id="D3DXMESH_WRITEONLY"></span><span id="d3dxmesh_writeonly"></span>**D3DXMESH\_WRITEONLY**</span></span>
</dt> <dd>

<span data-ttu-id="16807-149">Equivalente a especificar ambos D3DXMESH \_ VB \_ WRITEONLY e D3DXMESH \_ IB \_ WriteOnly.</span><span class="sxs-lookup"><span data-stu-id="16807-149">Equivalent to specifying both D3DXMESH\_VB\_WRITEONLY and D3DXMESH\_IB\_WRITEONLY.</span></span>

</dd> <dt>

<span data-ttu-id="16807-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH \_ dinâmico**</span><span class="sxs-lookup"><span data-stu-id="16807-150"><span id="D3DXMESH_DYNAMIC"></span><span id="d3dxmesh_dynamic"></span>**D3DXMESH\_DYNAMIC**</span></span>
</dt> <dd>

<span data-ttu-id="16807-151">Equivalente a especificar o D3DXMESH \_ VB \_ Dynamic e D3DXMESH \_ IB \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="16807-151">Equivalent to specifying both D3DXMESH\_VB\_DYNAMIC and D3DXMESH\_IB\_DYNAMIC.</span></span>

</dd> <dt>

<span data-ttu-id="16807-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH \_ SOFTWAREPROCESSING**</span><span class="sxs-lookup"><span data-stu-id="16807-152"><span id="D3DXMESH_SOFTWAREPROCESSING"></span><span id="d3dxmesh_softwareprocessing"></span>**D3DXMESH\_SOFTWAREPROCESSING**</span></span>
</dt> <dd>

<span data-ttu-id="16807-153">Equivalente a especificar D3DXMESH \_ VB \_ SOFTWAREPROCESSING e D3DXMESH \_ IB \_ SOFTWAREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="16807-153">Equivalent to specifying both D3DXMESH\_VB\_SOFTWAREPROCESSING and D3DXMESH\_IB\_SOFTWAREPROCESSING.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16807-154">Comentários</span><span class="sxs-lookup"><span data-stu-id="16807-154">Remarks</span></span>

<span data-ttu-id="16807-155">Uma malha de 32 bits (D3DXMESH \_ 32bit) pode teoricamente dar suporte a (2 ^ 32)-1 rostos e vértices.</span><span class="sxs-lookup"><span data-stu-id="16807-155">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2^32)-1 faces and vertices.</span></span> <span data-ttu-id="16807-156">No entanto, a alocação de memória para uma malha grande em um sistema operacional de 32 bits não é prática.</span><span class="sxs-lookup"><span data-stu-id="16807-156">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="16807-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16807-157">Requirements</span></span>



| <span data-ttu-id="16807-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="16807-158">Requirement</span></span> | <span data-ttu-id="16807-159">Valor</span><span class="sxs-lookup"><span data-stu-id="16807-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16807-160">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16807-160">Header</span></span><br/> | <dl> <span data-ttu-id="16807-161"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="16807-161"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16807-162">Consulte também</span><span class="sxs-lookup"><span data-stu-id="16807-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16807-163">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="16807-163">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
