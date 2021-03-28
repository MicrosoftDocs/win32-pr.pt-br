---
title: RWByteAddressBuffer
description: Um buffer de leitura/gravação que indexa em bytes.
ms.assetid: 8370c14c-5822-4240-942d-565aa223d48c
keywords:
- RWByteAddressBuffer HLSL
topic_type:
- apiref
api_name:
- RWByteAddressBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d065926b0769e15284cbe705783be012d82554b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366042"
---
# <a name="rwbyteaddressbuffer"></a><span data-ttu-id="c60ed-104">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="c60ed-104">RWByteAddressBuffer</span></span>

<span data-ttu-id="c60ed-105">Um buffer de leitura/gravação que indexa em bytes.</span><span class="sxs-lookup"><span data-stu-id="c60ed-105">A read/write buffer that indexes in bytes.</span></span>



| <span data-ttu-id="c60ed-106">Método</span><span class="sxs-lookup"><span data-stu-id="c60ed-106">Method</span></span>                                                                                          | <span data-ttu-id="c60ed-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c60ed-107">Description</span></span>                         |
|-------------------------------------------------------------------------------------------------|-------------------------------------|
| [<span data-ttu-id="c60ed-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="c60ed-108">**GetDimensions**</span></span>](sm5-object-rwbyteaddressbuffer-getdimensions.md)                           | <span data-ttu-id="c60ed-109">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="c60ed-109">Gets the resource dimensions.</span></span>       |
| [<span data-ttu-id="c60ed-110">**InterlockedAdd**</span><span class="sxs-lookup"><span data-stu-id="c60ed-110">**InterlockedAdd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedadd.md)                         | <span data-ttu-id="c60ed-111">Adiciona, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="c60ed-111">Adds, atomically.</span></span>                   |
| [<span data-ttu-id="c60ed-112">**InterlockedAnd**</span><span class="sxs-lookup"><span data-stu-id="c60ed-112">**InterlockedAnd**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedand.md)                         | <span data-ttu-id="c60ed-113">ANDs, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="c60ed-113">ANDs, atomically.</span></span>                   |
| [<span data-ttu-id="c60ed-114">**InterlockedCompareExchange**</span><span class="sxs-lookup"><span data-stu-id="c60ed-114">**InterlockedCompareExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcompareexchange.md) | <span data-ttu-id="c60ed-115">Compara e troca, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="c60ed-115">Compares and exchanges, atomically.</span></span> |
| [<span data-ttu-id="c60ed-116">**InterlockedCompareStore**</span><span class="sxs-lookup"><span data-stu-id="c60ed-116">**InterlockedCompareStore**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedcomparestore.md)       | <span data-ttu-id="c60ed-117">Compara e armazena, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="c60ed-117">Compares and stores, atomically.</span></span>    |
| [<span data-ttu-id="c60ed-118">**InterlockedExchange**</span><span class="sxs-lookup"><span data-stu-id="c60ed-118">**InterlockedExchange**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedexchange.md)               | <span data-ttu-id="c60ed-119">Troca, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="c60ed-119">Exchanges, atomically.</span></span>              |
| [<span data-ttu-id="c60ed-120">**InterlockedMax**</span><span class="sxs-lookup"><span data-stu-id="c60ed-120">**InterlockedMax**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmax.md)                         | <span data-ttu-id="c60ed-121">Localiza o máximo, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="c60ed-121">Finds the max, atomically.</span></span>          |
| [<span data-ttu-id="c60ed-122">**InterlockedMin**</span><span class="sxs-lookup"><span data-stu-id="c60ed-122">**InterlockedMin**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedmin.md)                         | <span data-ttu-id="c60ed-123">Localize o mínimo, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="c60ed-123">Find the min, atomically.</span></span>           |
| [<span data-ttu-id="c60ed-124">**Interbloqueador**</span><span class="sxs-lookup"><span data-stu-id="c60ed-124">**InterlockedOr**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedor.md)                           | <span data-ttu-id="c60ed-125">ORs, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="c60ed-125">ORs, atomically.</span></span>                    |
| [<span data-ttu-id="c60ed-126">**InterlockedXor**</span><span class="sxs-lookup"><span data-stu-id="c60ed-126">**InterlockedXor**</span></span>](sm5-object-rwbyteaddressbuffer-interlockedxor.md)                         | <span data-ttu-id="c60ed-127">XOR, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="c60ed-127">XORs, atomically.</span></span>                   |
| [<span data-ttu-id="c60ed-128">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="c60ed-128">**Load**</span></span>](rwbyteaddressbuffer-load.md)                                                        | <span data-ttu-id="c60ed-129">Obtém um valor.</span><span class="sxs-lookup"><span data-stu-id="c60ed-129">Gets one value.</span></span>                     |
| [<span data-ttu-id="c60ed-130">**Load2**</span><span class="sxs-lookup"><span data-stu-id="c60ed-130">**Load2**</span></span>](rwbyteaddressbuffer-load2.md)                                                      | <span data-ttu-id="c60ed-131">Obtém dois valores.</span><span class="sxs-lookup"><span data-stu-id="c60ed-131">Gets two values.</span></span>                    |
| [<span data-ttu-id="c60ed-132">**Load3**</span><span class="sxs-lookup"><span data-stu-id="c60ed-132">**Load3**</span></span>](rwbyteaddressbuffer-load3.md)                                                      | <span data-ttu-id="c60ed-133">Obtém três valores.</span><span class="sxs-lookup"><span data-stu-id="c60ed-133">Gets three values.</span></span>                  |
| [<span data-ttu-id="c60ed-134">**Load4**</span><span class="sxs-lookup"><span data-stu-id="c60ed-134">**Load4**</span></span>](rwbyteaddressbuffer-load4.md)                                                      | <span data-ttu-id="c60ed-135">Obtém quatro valores.</span><span class="sxs-lookup"><span data-stu-id="c60ed-135">Gets four values.</span></span>                   |
| [<span data-ttu-id="c60ed-136">**Store**</span><span class="sxs-lookup"><span data-stu-id="c60ed-136">**Store**</span></span>](sm5-object-rwbyteaddressbuffer-store.md)                                           | <span data-ttu-id="c60ed-137">Define um valor.</span><span class="sxs-lookup"><span data-stu-id="c60ed-137">Sets one value.</span></span>                     |
| [<span data-ttu-id="c60ed-138">**Store2**</span><span class="sxs-lookup"><span data-stu-id="c60ed-138">**Store2**</span></span>](sm5-object-rwbyteaddressbuffer-store2.md)                                         | <span data-ttu-id="c60ed-139">Define dois valores.</span><span class="sxs-lookup"><span data-stu-id="c60ed-139">Sets two values.</span></span>                    |
| [<span data-ttu-id="c60ed-140">**Store3**</span><span class="sxs-lookup"><span data-stu-id="c60ed-140">**Store3**</span></span>](sm5-object-rwbyteaddressbuffer-store3.md)                                         | <span data-ttu-id="c60ed-141">Define três valores.</span><span class="sxs-lookup"><span data-stu-id="c60ed-141">Sets three values.</span></span>                  |
| [<span data-ttu-id="c60ed-142">**Store4**</span><span class="sxs-lookup"><span data-stu-id="c60ed-142">**Store4**</span></span>](sm5-object-rwbyteaddressbuffer-store4.md)                                         | <span data-ttu-id="c60ed-143">Define quatro valores.</span><span class="sxs-lookup"><span data-stu-id="c60ed-143">Sets four values.</span></span>                   |



 

<span data-ttu-id="c60ed-144">Os objetos RWByteAddressBuffer podem ser prefixados com a classe de armazenamento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="c60ed-144">RWByteAddressBuffer objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="c60ed-145">Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações.</span><span class="sxs-lookup"><span data-stu-id="c60ed-145">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="c60ed-146">Sem esse especificador, uma barreira de memória ou sincronização liberará um UAV somente dentro do grupo atual.</span><span class="sxs-lookup"><span data-stu-id="c60ed-146">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

<span data-ttu-id="c60ed-147">O formato UAV associado a esse recurso precisa ser criado com o formato DXGI \_ \_ R32 \_ formato sem tipo.</span><span class="sxs-lookup"><span data-stu-id="c60ed-147">The UAV format bound to this resource needs to be created with the DXGI\_FORMAT\_R32\_TYPELESS format.</span></span>

<span data-ttu-id="c60ed-148">O UAV associado a esse recurso deve ter sido criado com o [**\_ sinalizador de UAV de buffer D3D11 \_ \_ \_ bruto**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span><span class="sxs-lookup"><span data-stu-id="c60ed-148">The UAV bound to this resource must have been created with the [**D3D11\_BUFFER\_UAV\_FLAG\_RAW**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_buffer_uav_flag).</span></span>

<span data-ttu-id="c60ed-149">Você pode usar o tipo de objeto **RWByteAddressBuffer** ao trabalhar com buffers brutos.</span><span class="sxs-lookup"><span data-stu-id="c60ed-149">You can use the **RWByteAddressBuffer** object type when you work with raw buffers.</span></span> <span data-ttu-id="c60ed-150">Para obter mais informações sobre a exibição bruta de buffers, consulte [exibições brutas de buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span><span class="sxs-lookup"><span data-stu-id="c60ed-150">For more info about raw viewing of buffers, see [Raw Views of Buffers](/windows/desktop/direct3d11/overviews-direct3d-11-resources-intro).</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c60ed-151">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c60ed-151">Minimum Shader Model</span></span>

<span data-ttu-id="c60ed-152">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c60ed-152">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="c60ed-153">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c60ed-153">Shader Model</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="c60ed-154">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c60ed-154">Supported</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c60ed-155">O [Shader Model 5](d3d11-graphics-reference-sm5.md) e os modelos de sombreador superiores modelo de sombreador [4](dx-graphics-hlsl-sm4.md) (disponível por meio da API do Direct3D 11 usando o nível de recurso 10,0 ou 10,1 ([**\_ \_ nível**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)de recurso do D3D \_ 10 \_ X) em dispositivos que dão suporte a sombreadores de computação.</span><span class="sxs-lookup"><span data-stu-id="c60ed-155">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models [Shader Model 4](dx-graphics-hlsl-sm4.md) (Available through the Direct3D 11 API by using 10.0 or 10.1 feature level ([**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level)\_10\_X) on devices that support compute shaders.</span></span> <span data-ttu-id="c60ed-156">Para obter mais informações sobre o suporte de sombreador de computação em hardware de nível inferior, consulte [sombreadores de computação em hardware de nível inferior](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span><span class="sxs-lookup"><span data-stu-id="c60ed-156">For more information about compute shader support on downlevel hardware, see [Compute Shaders on Downlevel Hardware](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-compute-shaders).)</span></span><br/> | <span data-ttu-id="c60ed-157">sim</span><span class="sxs-lookup"><span data-stu-id="c60ed-157">yes</span></span>       |



 

<span data-ttu-id="c60ed-158">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c60ed-158">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c60ed-159">Vértice</span><span class="sxs-lookup"><span data-stu-id="c60ed-159">Vertex</span></span> | <span data-ttu-id="c60ed-160">Envoltória</span><span class="sxs-lookup"><span data-stu-id="c60ed-160">Hull</span></span> | <span data-ttu-id="c60ed-161">Domínio</span><span class="sxs-lookup"><span data-stu-id="c60ed-161">Domain</span></span> | <span data-ttu-id="c60ed-162">Geometria</span><span class="sxs-lookup"><span data-stu-id="c60ed-162">Geometry</span></span> | <span data-ttu-id="c60ed-163">16x16</span><span class="sxs-lookup"><span data-stu-id="c60ed-163">Pixel</span></span> | <span data-ttu-id="c60ed-164">Computação</span><span class="sxs-lookup"><span data-stu-id="c60ed-164">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c60ed-165">x</span><span class="sxs-lookup"><span data-stu-id="c60ed-165">x</span></span>     | <span data-ttu-id="c60ed-166">x</span><span class="sxs-lookup"><span data-stu-id="c60ed-166">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c60ed-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="c60ed-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c60ed-168">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="c60ed-168">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

