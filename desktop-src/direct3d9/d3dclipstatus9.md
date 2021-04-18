---
description: Descreve o status atual do clipe.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: Estrutura D3DCLIPSTATUS9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3b22fdfcc136c05ec8fe03ae491612606b2df62f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105808325"
---
# <a name="d3dclipstatus9-structure"></a><span data-ttu-id="4b7b3-103">Estrutura D3DCLIPSTATUS9</span><span class="sxs-lookup"><span data-stu-id="4b7b3-103">D3DCLIPSTATUS9 structure</span></span>

<span data-ttu-id="4b7b3-104">Descreve o status atual do clipe.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-104">Describes the current clip status.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b7b3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4b7b3-105">Syntax</span></span>


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a><span data-ttu-id="4b7b3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="4b7b3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4b7b3-107">**ClipUnion**</span><span class="sxs-lookup"><span data-stu-id="4b7b3-107">**ClipUnion**</span></span>
</dt> <dd>

<span data-ttu-id="4b7b3-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b7b3-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4b7b3-109">Sinalizadores de União de clipe que descrevem o status atual do clipe.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-109">Clip union flags that describe the current clip status.</span></span> <span data-ttu-id="4b7b3-110">Esse membro pode ser um ou mais dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="4b7b3-110">This member can be one or more of the following flags:</span></span>



| <span data-ttu-id="4b7b3-111">Valor</span><span class="sxs-lookup"><span data-stu-id="4b7b3-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="4b7b3-112">Significado</span><span class="sxs-lookup"><span data-stu-id="4b7b3-112">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <span data-ttu-id="4b7b3-113"><dt>**D3DCS \_ tudo**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-113"><dt>**D3DCS\_ALL**</dt></span></span> </dl>          | <span data-ttu-id="4b7b3-114">Combinação de todos os sinalizadores de clipe.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-114">Combination of all clip flags.</span></span><br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <span data-ttu-id="4b7b3-115"><dt>**D3DCS \_ à esquerda**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-115"><dt>**D3DCS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="4b7b3-116">Todos os vértices são recortados pelo plano à esquerda do frustum de exibição.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-116">All vertices are clipped by the left plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <span data-ttu-id="4b7b3-117"><dt>**D3DCS \_ à direita**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-117"><dt>**D3DCS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="4b7b3-118">Todos os vértices são recortados pelo plano certo do frustum de exibição.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-118">All vertices are clipped by the right plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <span data-ttu-id="4b7b3-119"><dt>**D3DCS \_ superior**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-119"><dt>**D3DCS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="4b7b3-120">Todos os vértices são recortados pelo plano superior do frustum de exibição.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-120">All vertices are clipped by the top plane of the viewing frustum.</span></span><br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <span data-ttu-id="4b7b3-121"><dt>**D3DCS \_ inferior**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-121"><dt>**D3DCS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="4b7b3-122">Todos os vértices são recortados pelo plano inferior do frustum de exibição.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-122">All vertices are clipped by the bottom plane of the viewing frustum.</span></span><br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <span data-ttu-id="4b7b3-123"><dt>**D3DCS \_ frontal**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-123"><dt>**D3DCS\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="4b7b3-124">Todos os vértices são recortados pelo plano frontal do frustum de exibição.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-124">All vertices are clipped by the front plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <span data-ttu-id="4b7b3-125"><dt>**D3DCS \_ voltar**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-125"><dt>**D3DCS\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="4b7b3-126">Todos os vértices são recortados pelo plano de fundo do frustum de exibição.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-126">All vertices are clipped by the back plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <span data-ttu-id="4b7b3-127"><dt>**D3DCS \_ PLANE0**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-127"><dt>**D3DCS\_PLANE0**</dt></span></span> </dl> | <span data-ttu-id="4b7b3-128">Planos de recorte definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-128">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <span data-ttu-id="4b7b3-129"><dt>**D3DCS \_ PLANE1**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-129"><dt>**D3DCS\_PLANE1**</dt></span></span> </dl> | <span data-ttu-id="4b7b3-130">Planos de recorte definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-130">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <span data-ttu-id="4b7b3-131"><dt>**D3DCS \_ PLANE2**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-131"><dt>**D3DCS\_PLANE2**</dt></span></span> </dl> | <span data-ttu-id="4b7b3-132">Planos de recorte definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-132">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <span data-ttu-id="4b7b3-133"><dt>**D3DCS \_ PLANE3**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-133"><dt>**D3DCS\_PLANE3**</dt></span></span> </dl> | <span data-ttu-id="4b7b3-134">Planos de recorte definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-134">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <span data-ttu-id="4b7b3-135"><dt>**D3DCS \_ PLANE4**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-135"><dt>**D3DCS\_PLANE4**</dt></span></span> </dl> | <span data-ttu-id="4b7b3-136">Planos de recorte definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-136">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <span data-ttu-id="4b7b3-137"><dt>**D3DCS \_ PLANE5**</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-137"><dt>**D3DCS\_PLANE5**</dt></span></span> </dl> | <span data-ttu-id="4b7b3-138">Planos de recorte definidos pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-138">Application-defined clipping planes.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="4b7b3-139">**ClipIntersection**</span><span class="sxs-lookup"><span data-stu-id="4b7b3-139">**ClipIntersection**</span></span>
</dt> <dd>

<span data-ttu-id="4b7b3-140">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4b7b3-140">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="4b7b3-141">Sinalizadores de interseção de clipe que descrevem o status atual do clipe.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-141">Clip intersection flags that describe the current clip status.</span></span> <span data-ttu-id="4b7b3-142">Esse membro pode usar os mesmos sinalizadores que ClipUnion.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-142">This member can take the same flags as ClipUnion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4b7b3-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b7b3-143">Remarks</span></span>

<span data-ttu-id="4b7b3-144">Quando o recorte é habilitado durante o processamento de vértice (por [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)ou outras funções de desenho), o Direct3D computa um código de clipe para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-144">When clipping is enabled during vertex processing (by [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), or other drawing functions), Direct3D computes a clip code for every vertex.</span></span> <span data-ttu-id="4b7b3-145">O código do clipe é uma combinação de \_ \* bits D3DCS.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-145">The clip code is a combination of D3DCS\_\* bits.</span></span> <span data-ttu-id="4b7b3-146">Quando um vértice está fora de um plano de recorte específico, o bit correspondente é definido no código de recorte.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-146">When a vertex is outside a particular clipping plane, the corresponding bit is set in the clipping code.</span></span> <span data-ttu-id="4b7b3-147">O Direct3D mantém o status do clipe usando **D3DCLIPSTATUS9**, que tem membros ClipUnion e ClipIntersection.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-147">Direct3D maintains the clip status using **D3DCLIPSTATUS9**, which has ClipUnion and ClipIntersection members.</span></span> <span data-ttu-id="4b7b3-148">ClipUnion é uma ou bit a bit de todos os códigos de clipe de vértice, e ClipIntersection é um bit e de todos os códigos de clipes de vértice.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-148">ClipUnion is a bitwise OR of all vertex clip codes and ClipIntersection is a bitwise AND of all vertex clip codes.</span></span> <span data-ttu-id="4b7b3-149">Os valores iniciais são zero para ClipUnion e 0xFFFFFFFF para ClipIntersection.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-149">Initial values are zero for ClipUnion and 0xFFFFFFFF for ClipIntersection.</span></span> <span data-ttu-id="4b7b3-150">Quando o \_ recorte de D3DRS é definido como **false**, ClipUnion e ClipIntersection são definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-150">When D3DRS\_CLIPPING is set to **FALSE**, ClipUnion and ClipIntersection are set to zero.</span></span> <span data-ttu-id="4b7b3-151">O Direct3D atualiza o status do clipe durante chamadas de desenho.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-151">Direct3D updates the clip status during drawing calls.</span></span> <span data-ttu-id="4b7b3-152">Para calcular o status do clipe de um objeto específico, defina ClipUnion e ClipIntersection como seu valor inicial e continue o desenho.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-152">To compute clip status for a particular object, set ClipUnion and ClipIntersection to their initial value and continue drawing.</span></span>

<span data-ttu-id="4b7b3-153">O status do clipe não é atualizado por [**DrawRectPatch**](/windows/desktop/api) e [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) porque não há emulação de software para eles.</span><span class="sxs-lookup"><span data-stu-id="4b7b3-153">Clip status is not updated by [**DrawRectPatch**](/windows/desktop/api) and [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) because there is no software emulation for them.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b7b3-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4b7b3-154">Requirements</span></span>



| <span data-ttu-id="4b7b3-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="4b7b3-155">Requirement</span></span> | <span data-ttu-id="4b7b3-156">Valor</span><span class="sxs-lookup"><span data-stu-id="4b7b3-156">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b7b3-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4b7b3-157">Header</span></span><br/> | <dl> <span data-ttu-id="4b7b3-158"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b3-158"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b7b3-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="4b7b3-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b7b3-160">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="4b7b3-160">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="4b7b3-161">**GetClipStatus**</span><span class="sxs-lookup"><span data-stu-id="4b7b3-161">**GetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[<span data-ttu-id="4b7b3-162">**SetClipStatus**</span><span class="sxs-lookup"><span data-stu-id="4b7b3-162">**SetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
