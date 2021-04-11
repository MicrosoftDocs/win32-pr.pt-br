---
description: Define um conjunto de propriedades de iluminação.
ms.assetid: 25ce9d72-949c-41fc-8e3b-146d6a2de0dc
title: Estrutura D3DLIGHT9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHT9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 90e72fbb2bf4f1d74a74dc177346387b36eb25e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173057"
---
# <a name="d3dlight9-structure"></a><span data-ttu-id="6795b-103">Estrutura D3DLIGHT9</span><span class="sxs-lookup"><span data-stu-id="6795b-103">D3DLIGHT9 structure</span></span>

<span data-ttu-id="6795b-104">Define um conjunto de propriedades de iluminação.</span><span class="sxs-lookup"><span data-stu-id="6795b-104">Defines a set of lighting properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6795b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6795b-105">Syntax</span></span>


```C++
typedef struct D3DLIGHT9 {
  D3DLIGHTTYPE  Type;
  D3DCOLORVALUE Diffuse;
  D3DCOLORVALUE Specular;
  D3DCOLORVALUE Ambient;
  D3DVECTOR     Position;
  D3DVECTOR     Direction;
  float         Range;
  float         Falloff;
  float         Attenuation0;
  float         Attenuation1;
  float         Attenuation2;
  float         Theta;
  float         Phi;
} D3DLIGHT9, *LPD3DLIGHT;
```



## <a name="members"></a><span data-ttu-id="6795b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6795b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="6795b-107">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="6795b-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-108">Tipo: **[ **D3DLIGHTTYPE**](./d3dlighttype.md)**</span><span class="sxs-lookup"><span data-stu-id="6795b-108">Type: **[**D3DLIGHTTYPE**](./d3dlighttype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-109">Tipo da fonte de luz.</span><span class="sxs-lookup"><span data-stu-id="6795b-109">Type of the light source.</span></span> <span data-ttu-id="6795b-110">Esse valor é um dos membros do tipo enumerado [**D3DLIGHTTYPE**](./d3dlighttype.md) .</span><span class="sxs-lookup"><span data-stu-id="6795b-110">This value is one of the members of the [**D3DLIGHTTYPE**](./d3dlighttype.md) enumerated type.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-111">**Difusa**</span><span class="sxs-lookup"><span data-stu-id="6795b-111">**Diffuse**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-112">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="6795b-112">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-113">Cor difusa emitida pela luz.</span><span class="sxs-lookup"><span data-stu-id="6795b-113">Diffuse color emitted by the light.</span></span> <span data-ttu-id="6795b-114">Esse membro é uma estrutura [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="6795b-114">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-115">**Especular**</span><span class="sxs-lookup"><span data-stu-id="6795b-115">**Specular**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-116">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="6795b-116">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-117">Cor especulada emitida pela luz.</span><span class="sxs-lookup"><span data-stu-id="6795b-117">Specular color emitted by the light.</span></span> <span data-ttu-id="6795b-118">Esse membro é uma estrutura [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="6795b-118">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-119">**Ambiente**</span><span class="sxs-lookup"><span data-stu-id="6795b-119">**Ambient**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-120">Tipo: **[ **D3DCOLORVALUE**](d3dcolorvalue.md)**</span><span class="sxs-lookup"><span data-stu-id="6795b-120">Type: **[**D3DCOLORVALUE**](d3dcolorvalue.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-121">Cor de ambiente emitida pela luz.</span><span class="sxs-lookup"><span data-stu-id="6795b-121">Ambient color emitted by the light.</span></span> <span data-ttu-id="6795b-122">Esse membro é uma estrutura [**D3DCOLORVALUE**](d3dcolorvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="6795b-122">This member is a [**D3DCOLORVALUE**](d3dcolorvalue.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-123">**Posição**</span><span class="sxs-lookup"><span data-stu-id="6795b-123">**Position**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-124">Tipo: **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="6795b-124">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-125">Posição da luz no espaço do mundo, especificada por uma estrutura [**D3DVECTOR**](d3dvector.md) .</span><span class="sxs-lookup"><span data-stu-id="6795b-125">Position of the light in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="6795b-126">Esse membro não tem significado para luzes direcionais e é ignorado nesse caso.</span><span class="sxs-lookup"><span data-stu-id="6795b-126">This member has no meaning for directional lights and is ignored in that case.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-127">**Direção**</span><span class="sxs-lookup"><span data-stu-id="6795b-127">**Direction**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-128">Tipo: **[ **D3DVECTOR**](d3dvector.md)**</span><span class="sxs-lookup"><span data-stu-id="6795b-128">Type: **[**D3DVECTOR**](d3dvector.md)**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-129">Direção em que a luz está apontando no espaço do mundo, especificada por uma estrutura [**D3DVECTOR**](d3dvector.md) .</span><span class="sxs-lookup"><span data-stu-id="6795b-129">Direction that the light is pointing in world space, specified by a [**D3DVECTOR**](d3dvector.md) structure.</span></span> <span data-ttu-id="6795b-130">Esse membro tem significado apenas para rotas direcionais e Spotlights.</span><span class="sxs-lookup"><span data-stu-id="6795b-130">This member has meaning only for directional and spotlights.</span></span> <span data-ttu-id="6795b-131">Este vetor não precisa ser normalizado, mas deve ter um comprimento diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="6795b-131">This vector need not be normalized, but it should have a nonzero length.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-132">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="6795b-132">**Range**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-133">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6795b-133">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-134">Distância além da qual a luz não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="6795b-134">Distance beyond which the light has no effect.</span></span> <span data-ttu-id="6795b-135">O valor máximo permitido para esse membro é a raiz quadrada de FLT \_ Max.</span><span class="sxs-lookup"><span data-stu-id="6795b-135">The maximum allowable value for this member is the square root of FLT\_MAX.</span></span> <span data-ttu-id="6795b-136">Esse membro não afeta as luzes direcionais.</span><span class="sxs-lookup"><span data-stu-id="6795b-136">This member does not affect directional lights.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-137">**Queda**</span><span class="sxs-lookup"><span data-stu-id="6795b-137">**Falloff**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-138">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6795b-138">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-139">Diminuir a iluminação entre o cone interno de um Spotlight (o ângulo especificado por teta) e a borda externa do cone externo (o ângulo especificado por Phi).</span><span class="sxs-lookup"><span data-stu-id="6795b-139">Decrease in illumination between a spotlight's inner cone (the angle specified by Theta) and the outer edge of the outer cone (the angle specified by Phi).</span></span>

<span data-ttu-id="6795b-140">O efeito de queda na iluminação é sutil.</span><span class="sxs-lookup"><span data-stu-id="6795b-140">The effect of falloff on the lighting is subtle.</span></span> <span data-ttu-id="6795b-141">Além disso, uma pequena penalidade de desempenho é incorrida com a formação da curva de queda.</span><span class="sxs-lookup"><span data-stu-id="6795b-141">Furthermore, a small performance penalty is incurred by shaping the falloff curve.</span></span> <span data-ttu-id="6795b-142">Por esses motivos, a maioria dos desenvolvedores define esse valor como 1,0.</span><span class="sxs-lookup"><span data-stu-id="6795b-142">For these reasons, most developers set this value to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-143">**Attenuation0**</span><span class="sxs-lookup"><span data-stu-id="6795b-143">**Attenuation0**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-144">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6795b-144">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-145">Valor que especifica como a intensidade de luz é alterada à distância.</span><span class="sxs-lookup"><span data-stu-id="6795b-145">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="6795b-146">Os valores de atenuação são ignorados para luzes direcionais.</span><span class="sxs-lookup"><span data-stu-id="6795b-146">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="6795b-147">Esse membro representa uma constante de atenuação.</span><span class="sxs-lookup"><span data-stu-id="6795b-147">This member represents an attenuation constant.</span></span> <span data-ttu-id="6795b-148">Para obter informações sobre atenuação, consulte [Propriedades claras (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="6795b-148">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="6795b-149">Os valores válidos para esse membro variam de 0,0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="6795b-149">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="6795b-150">Para luzes não-direcionais, os três valores de atenuação não devem ser definidos como 0,0 ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6795b-150">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-151">**Attenuation1**</span><span class="sxs-lookup"><span data-stu-id="6795b-151">**Attenuation1**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-152">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6795b-152">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-153">Valor que especifica como a intensidade de luz é alterada à distância.</span><span class="sxs-lookup"><span data-stu-id="6795b-153">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="6795b-154">Os valores de atenuação são ignorados para luzes direcionais.</span><span class="sxs-lookup"><span data-stu-id="6795b-154">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="6795b-155">Esse membro representa uma constante de atenuação.</span><span class="sxs-lookup"><span data-stu-id="6795b-155">This member represents an attenuation constant.</span></span> <span data-ttu-id="6795b-156">Para obter informações sobre atenuação, consulte [Propriedades claras (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="6795b-156">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="6795b-157">Os valores válidos para esse membro variam de 0,0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="6795b-157">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="6795b-158">Para luzes não-direcionais, os três valores de atenuação não devem ser definidos como 0,0 ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6795b-158">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-159">**Attenuation2**</span><span class="sxs-lookup"><span data-stu-id="6795b-159">**Attenuation2**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-160">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6795b-160">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-161">Valor que especifica como a intensidade de luz é alterada à distância.</span><span class="sxs-lookup"><span data-stu-id="6795b-161">Value specifying how the light intensity changes over distance.</span></span> <span data-ttu-id="6795b-162">Os valores de atenuação são ignorados para luzes direcionais.</span><span class="sxs-lookup"><span data-stu-id="6795b-162">Attenuation values are ignored for directional lights.</span></span> <span data-ttu-id="6795b-163">Esse membro representa uma constante de atenuação.</span><span class="sxs-lookup"><span data-stu-id="6795b-163">This member represents an attenuation constant.</span></span> <span data-ttu-id="6795b-164">Para obter informações sobre atenuação, consulte [Propriedades claras (Direct3D 9)](light-properties.md).</span><span class="sxs-lookup"><span data-stu-id="6795b-164">For information about attenuation, see [Light Properties (Direct3D 9)](light-properties.md).</span></span> <span data-ttu-id="6795b-165">Os valores válidos para esse membro variam de 0,0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="6795b-165">Valid values for this member range from 0.0 to infinity.</span></span> <span data-ttu-id="6795b-166">Para luzes não-direcionais, os três valores de atenuação não devem ser definidos como 0,0 ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="6795b-166">For non-directional lights, all three attenuation values should not be set to 0.0 at the same time.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-167">**Teta**</span><span class="sxs-lookup"><span data-stu-id="6795b-167">**Theta**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-168">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6795b-168">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-169">Ângulo, em radianos, do cone interno de um Spotlight-ou seja, o cone de destaque totalmente iluminado.</span><span class="sxs-lookup"><span data-stu-id="6795b-169">Angle, in radians, of a spotlight's inner cone - that is, the fully illuminated spotlight cone.</span></span> <span data-ttu-id="6795b-170">Esse valor deve estar no intervalo de 0 até o valor especificado por Phi.</span><span class="sxs-lookup"><span data-stu-id="6795b-170">This value must be in the range from 0 through the value specified by Phi.</span></span>

</dd> <dt>

<span data-ttu-id="6795b-171">**PI**</span><span class="sxs-lookup"><span data-stu-id="6795b-171">**Phi**</span></span>
</dt> <dd>

<span data-ttu-id="6795b-172">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="6795b-172">Type: **float**</span></span>

</dd> <dd>

<span data-ttu-id="6795b-173">Ângulo, em radianos, definindo a borda externa do cone externo do Spotlight.</span><span class="sxs-lookup"><span data-stu-id="6795b-173">Angle, in radians, defining the outer edge of the spotlight's outer cone.</span></span> <span data-ttu-id="6795b-174">Pontos fora deste cone não estão acesos pelo Spotlight.</span><span class="sxs-lookup"><span data-stu-id="6795b-174">Points outside this cone are not lit by the spotlight.</span></span> <span data-ttu-id="6795b-175">Esse valor deve estar entre 0 e PI.</span><span class="sxs-lookup"><span data-stu-id="6795b-175">This value must be between 0 and pi.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6795b-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6795b-176">Requirements</span></span>



| <span data-ttu-id="6795b-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="6795b-177">Requirement</span></span> | <span data-ttu-id="6795b-178">Valor</span><span class="sxs-lookup"><span data-stu-id="6795b-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6795b-179">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6795b-179">Header</span></span><br/> | <dl> <span data-ttu-id="6795b-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6795b-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6795b-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="6795b-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6795b-182">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="6795b-182">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="6795b-183">**Getleve**</span><span class="sxs-lookup"><span data-stu-id="6795b-183">**GetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getlight)
</dt> <dt>

[<span data-ttu-id="6795b-184">**SetLight**</span><span class="sxs-lookup"><span data-stu-id="6795b-184">**SetLight**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)
</dt> </dl>

 

 
