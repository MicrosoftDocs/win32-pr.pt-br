---
description: Sinalizadores passados para a função TraceRay para substituir transparência, remoção e comportamento de início.
ms.assetid: ''
title: Enumeração de RAY_FLAG
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RAY_FLAG
api_type:
- NA
ms.openlocfilehash: 31d6a002e5f3f4eeb5f86e671be0904d61cb916d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762981"
---
# <a name="ray_flag-enumeration"></a><span data-ttu-id="db7d3-103">Enumeração de sinalizador de RAY \_</span><span class="sxs-lookup"><span data-stu-id="db7d3-103">RAY\_FLAG enumeration</span></span>

<span data-ttu-id="db7d3-104">Sinalizadores passados para a função [**TraceRay**](traceray-function.md) para substituir transparência, remoção e comportamento de início.</span><span class="sxs-lookup"><span data-stu-id="db7d3-104">Flags passed to the [**TraceRay**](traceray-function.md) function to override transparency, culling, and early-out behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="db7d3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="db7d3-105">Syntax</span></span>


```
enum RAY_FLAG : uint
{
    RAY_FLAG_NONE                            = 0x00,
    RAY_FLAG_FORCE_OPAQUE                    = 0x01,
    RAY_FLAG_FORCE_NON_OPAQUE                = 0x02,
    RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH = 0x04,
    RAY_FLAG_SKIP_CLOSEST_HIT_SHADER         = 0x08,
    RAY_FLAG_CULL_BACK_FACING_TRIANGLES      = 0x10,
    RAY_FLAG_CULL_FRONT_FACING_TRIANGLES     = 0x20,
    RAY_FLAG_CULL_OPAQUE                     = 0x40,
    RAY_FLAG_CULL_NON_OPAQUE                 = 0x80,
}; 
```



## <a name="constants"></a><span data-ttu-id="db7d3-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="db7d3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="db7d3-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**sinalizador de RAY \_ \_ None**</span><span class="sxs-lookup"><span data-stu-id="db7d3-107"><span id="RAY_FLAG_NONE"></span><span id="ray_flag_none"></span>**RAY\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="db7d3-108">Nenhuma opção selecionada.</span><span class="sxs-lookup"><span data-stu-id="db7d3-108">No options selected.</span></span>

</dd> <dt>

<span data-ttu-id="db7d3-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**sinalizador de RAY \_ \_ Force \_ opaco**</span><span class="sxs-lookup"><span data-stu-id="db7d3-109"><span id="RAY_FLAG_FORCE_OPAQUE"></span><span id="ray_flag_force_opaque"></span>**RAY\_FLAG\_FORCE\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="db7d3-110">Todas as interseções de Ray-Primitive encontradas em um raytrace são tratadas como opacas.</span><span class="sxs-lookup"><span data-stu-id="db7d3-110">All ray-primitive intersections encountered in a raytrace are treated as opaque.</span></span>  <span data-ttu-id="db7d3-111">Portanto, nenhum sombreador de ocorrência será executado, independentemente de a geometria de ocorrência ou não especificar o \_ sinalizador de geometria D3D12 RAYTRACING \_ \_ \_ opaco e, independentemente dos sinalizadores de instância na instância que foi atingido.</span><span class="sxs-lookup"><span data-stu-id="db7d3-111">So no any hit shaders will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>

<span data-ttu-id="db7d3-112">Esse sinalizador é mutuamente exclusivo com o sinalizador de RAY \_ \_ Force \_ não \_ opaco, Ray \_ flag de \_ seleção \_ opaca e Ray \_ Flag \_ \_ não \_ opaco.</span><span class="sxs-lookup"><span data-stu-id="db7d3-112">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_NON\_OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="db7d3-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**sinalizador de RAY \_ \_ Force \_ não \_ opaco**</span><span class="sxs-lookup"><span data-stu-id="db7d3-113"><span id="RAY_FLAG_FORCE_NON_OPAQUE"></span><span id="ray_flag_force_non_opaque"></span>**RAY\_FLAG\_FORCE\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="db7d3-114">Todas as interseções de Ray-Primitive encontradas em um raytrace são tratadas como não opacas.</span><span class="sxs-lookup"><span data-stu-id="db7d3-114">All ray-primitive intersections encountered in a raytrace are treated as non-opaque.</span></span>  <span data-ttu-id="db7d3-115">Portanto, qualquer sombreador de ocorrências, se presente, será executado, independentemente de a geometria de ocorrência especificar ou não o \_ sinalizador de geometria D3D12 RAYTRACING \_ \_ \_ opaco e, independentemente dos sinalizadores de instância na instância que foi atingido.</span><span class="sxs-lookup"><span data-stu-id="db7d3-115">So any hit shaders, if present, will be executed regardless of whether or not the hit geometry specifies D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE, and regardless of the instance flags on the instance that was hit.</span></span>
<span data-ttu-id="db7d3-116">Esse sinalizador é mutuamente exclusivo com o sinalizador de RAY \_ \_ FORCE_ \OPAQUE, Ray \_ flag de \_ seleção \_ opaca e Ray \_ flag de \_ seleção \_ não \_ opaco.</span><span class="sxs-lookup"><span data-stu-id="db7d3-116">This flag is mutually exclusive with RAY\_FLAG\_FORCE_\OPAQUE, RAY\_FLAG\_CULL\_OPAQUE and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="db7d3-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**o \_ sinalizador \_ de Ray aceita \_ primeira \_ jogada \_ e \_ finalizar \_ pesquisa**</span><span class="sxs-lookup"><span data-stu-id="db7d3-117"><span id="RAY_FLAG_ACCEPT_FIRST_HIT_AND_END_SEARCH"></span><span id="ray_flag_accept_first_hit_and_end_search"></span>**RAY\_FLAG\_ACCEPT\_FIRST\_HIT\_AND\_END\_SEARCH**</span></span>
</dt> <dd>

<span data-ttu-id="db7d3-118">A primeira interseção Ray-Primitive encontrada em um raytrace faz com que **AcceptHitAndEndSearch** seja chamado imediatamente após o sombreador de qualquer clique, incluindo se não houver nenhum sombreador de clique.</span><span class="sxs-lookup"><span data-stu-id="db7d3-118">The first ray-primitive intersection encountered in a raytrace automatically causes **AcceptHitAndEndSearch** to be called immediately after the any hit shader, including if there is no any hit shader.</span></span> 
 
<span data-ttu-id="db7d3-119">A única exceção é quando o sombreador de ocorrências anterior chama **IgnoreHit**; nesse caso, o raio continua inalterado, de modo que o próximo clique se torna outro candidato a ser a primeira ocorrência.</span><span class="sxs-lookup"><span data-stu-id="db7d3-119">The only exception is when the preceding any hit shader calls **IgnoreHit**, in which case the ray continues unaffected such that the next hit becomes another candidate to be the first hit.</span></span>  <span data-ttu-id="db7d3-120">Para que essa exceção seja aplicada, o sombreador de qualquer clique tem que ser realmente executado.</span><span class="sxs-lookup"><span data-stu-id="db7d3-120">For this exception to apply, the any hit shader has to actually be executed.</span></span>  <span data-ttu-id="db7d3-121">Portanto, se o sombreador any for ignorado porque o pressionamento é tratado como opaco (por exemplo, devido ao sinalizador de RAY \_ \_ Force \_ opaco ou D3D12 RAYTRACING do sinalizador de \_ geometria opaco \_ \_ \_ ou D3D12 \_ RAYTRACING \_ \_ de instância \_ opaco que está sendo definido), então **AcceptHitAndEndSearch** é chamado.</span><span class="sxs-lookup"><span data-stu-id="db7d3-121">So if the any hit shader is skipped because the hit is treated as opaque (e.g. due to RAY\_FLAG\_FORCE\_OPAQUE or D3D12\_RAYTRACING\_GEOMETRY\_FLAG\_OPAQUE or D3D12\_RAYTRACING\_INSTANCE\_FLAG\_OPAQUE being set), then **AcceptHitAndEndSearch** is called.</span></span>

<span data-ttu-id="db7d3-122">Se um sombreador de clique mais próximo estiver presente no primeiro acesso, ele será invocado, a menos que o \_ \_ sombreador de clique de raio \_ mais próximo \_ \_ também esteja presente.</span><span class="sxs-lookup"><span data-stu-id="db7d3-122">If a closest hit shader is present at the first hit, it gets invoked unless RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER is also present.</span></span>  <span data-ttu-id="db7d3-123">O único clique que foi encontrado é considerado "mais próximo", mesmo que outras ocorrências em potencial que possam estar mais próximas do raio possam não ter sido visitadas.</span><span class="sxs-lookup"><span data-stu-id="db7d3-123">The one hit that was found is considered “closest”, even though other potential hits that might be closer on the ray may not have been visited.</span></span>

<span data-ttu-id="db7d3-124">Um uso típico para esse sinalizador é para sombras, em que apenas um único pressionamento precisa ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="db7d3-124">A typical use for this flag is for shadows, where only a single hit needs to be found.</span></span>


</dd> <dt>

<span data-ttu-id="db7d3-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**\_ \_ \_ sombreador de fechamento de omissão de \_ sinal de \_ Ray**</span><span class="sxs-lookup"><span data-stu-id="db7d3-125"><span id="RAY_FLAG_SKIP_CLOSEST_HIT_SHADER"></span><span id="ray_flag_skip_closest_hit_shader"></span>**RAY\_FLAG\_SKIP\_CLOSEST\_HIT\_SHADER**</span></span>
</dt> <dd>

<span data-ttu-id="db7d3-126">Mesmo que pelo menos um clique tenha sido confirmado e o grupo de acesso para a visita mais próxima contenha um sombreador de clique mais próximo, ignore a execução desse sombreador.</span><span class="sxs-lookup"><span data-stu-id="db7d3-126">Even if at least one hit has been committed, and the hit group for the closest hit contains a closest hit shader, skip execution of that shader.</span></span> 

</dd> <dt>

<span data-ttu-id="db7d3-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**triângulos voltados para a remoção do sinalizador de RAY \_ \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="db7d3-127"><span id="RAY_FLAG_CULL_BACK_FACING_TRIANGLES"></span><span id="ray_flag_cull_back_facing_triangles"></span>**RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="db7d3-128">Permite a remoção de triângulos voltados.</span><span class="sxs-lookup"><span data-stu-id="db7d3-128">Enables culling of back facing triangles.</span></span> <span data-ttu-id="db7d3-129">Consulte **\_ sinalizadores de \_ instância \_ do D3D12 RAYTRACING** para selecionar quais triângulos são voltados, por instância.</span><span class="sxs-lookup"><span data-stu-id="db7d3-129">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="db7d3-130">Em instâncias que especificam \_ \_ o sinalizador de instância D3D12 RAYTRACING \_ \_ \_ \_ , desabilite o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="db7d3-130">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="db7d3-131">Em tipos de geometria diferentes dos \_ \_ triângulos de tipo de geometria D3D12 RAYTRACING \_ \_ , esse sinalizador não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="db7d3-131">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="db7d3-132">Esse sinalizador é mutuamente exclusivo com \_ \_ \_ \_ triângulos frontais de seleção de sinalizador de raio \_ .</span><span class="sxs-lookup"><span data-stu-id="db7d3-132">This flag is mutually exclusive with RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="db7d3-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**triângulos de seleção de sinalizador de RAY \_ \_ \_ - \_ face \_**</span><span class="sxs-lookup"><span data-stu-id="db7d3-133"><span id="RAY_FLAG_CULL_FRONT_FACING_TRIANGLES"></span><span id="ray_flag_cull_front_facing_trianglesag_none"></span>**RAY\_FLAG\_CULL\_FRONT\_FACING\_TRIANGLES**</span></span>
</dt> <dd>

<span data-ttu-id="db7d3-134">Permite a remoção de triângulos frontais.</span><span class="sxs-lookup"><span data-stu-id="db7d3-134">Enables culling of front facing triangles.</span></span> <span data-ttu-id="db7d3-135">Consulte **\_ sinalizadores de \_ instância \_ do D3D12 RAYTRACING** para selecionar quais triângulos são voltados, por instância.</span><span class="sxs-lookup"><span data-stu-id="db7d3-135">See **D3D12\_RAYTRACING\_INSTANCE\_FLAGS** for selecting which triangles are back facing, per-instance.</span></span>

<span data-ttu-id="db7d3-136">Em instâncias que especificam \_ \_ o sinalizador de instância D3D12 RAYTRACING \_ \_ \_ \_ , desabilite o sinalizador.</span><span class="sxs-lookup"><span data-stu-id="db7d3-136">On instances that specify D3D12\_RAYTRACING\_INSTANCE\_FLAG\_TRIANGLE\_CULL\_DISABLE, this flag has no effect.</span></span>

<span data-ttu-id="db7d3-137">Em tipos de geometria diferentes dos \_ \_ triângulos de tipo de geometria D3D12 RAYTRACING \_ \_ , esse sinalizador não tem nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="db7d3-137">On geometry types other than D3D12\_RAYTRACING\_GEOMETRY\_TYPE\_TRIANGLES, this flag has no effect.</span></span>

<span data-ttu-id="db7d3-138">Esse sinalizador é mutuamente exclusivo com \_ \_ \_ \_ \_ triângulos voltados para a seleção de sinalizador de raio.</span><span class="sxs-lookup"><span data-stu-id="db7d3-138">This flag is mutually exclusive with RAY\_FLAG\_CULL\_BACK\_FACING\_TRIANGLES.</span></span>


</dd> <dt>

<span data-ttu-id="db7d3-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**sinalizador de raio de \_ \_ seleção \_ opaco**</span><span class="sxs-lookup"><span data-stu-id="db7d3-139"><span id="RAY_FLAG_CULL_OPAQUE"></span><span id="ray_flag_cull_opaque"></span>**RAY\_FLAG\_CULL\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="db7d3-140">Escolhe todos os primitivos que são considerados opacos com base em seus sinalizadores de geometria e de instância.</span><span class="sxs-lookup"><span data-stu-id="db7d3-140">Culls all primitives that are considered opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="db7d3-141">Esse sinalizador é mutuamente exclusivo com RAY \_ Flag \_ Force \_ opaco, Ray \_ Flag \_ Force \_ não \_ opaco e Ray \_ Flag \_ \_ não \_ opaco.</span><span class="sxs-lookup"><span data-stu-id="db7d3-141">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_NON\_OPAQUE.</span></span>


</dd> <dt>

<span data-ttu-id="db7d3-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**\_seleção de sinalizador Ray \_ \_ não \_ opaco**</span><span class="sxs-lookup"><span data-stu-id="db7d3-142"><span id="RAY_FLAG_CULL_NON_OPAQUE"></span><span id="ray_flag_cull_non_opaque"></span>**RAY\_FLAG\_CULL\_NON\_OPAQUE**</span></span>
</dt> <dd>

<span data-ttu-id="db7d3-143">Escolhe todos os primitivos que são considerados não opacos com base em seus sinalizadores de geometria e de instância.</span><span class="sxs-lookup"><span data-stu-id="db7d3-143">Culls all primitives that are considered non-opaque based on their geometry and instance flags.</span></span>

<span data-ttu-id="db7d3-144">Esse sinalizador é mutuamente exclusivo com RAY \_ Flag \_ Force \_ opaco, Ray \_ Flag \_ Force \_ não \_ opaco e Ray flag de \_ \_ seleção \_ opaca.</span><span class="sxs-lookup"><span data-stu-id="db7d3-144">This flag is mutually exclusive with RAY\_FLAG\_FORCE\_OPAQUE, RAY\_FLAG\_FORCE\_NON\_OPAQUE, and RAY\_FLAG\_CULL\_OPAQUE.</span></span>


</dd>

## <a name="requirements"></a><span data-ttu-id="db7d3-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db7d3-145">Requirements</span></span>



## <a name="see-also"></a><span data-ttu-id="db7d3-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="db7d3-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db7d3-147">Referência HLSL de raytracing do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="db7d3-147">Direct3D 12 Raytracing HLSL Reference</span></span>](direct3d-12-raytracing-hlsl-reference.md)
</dt> </dl>

 

 




