---
description: Define a classe de memória que mantém os buffers de um recurso.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: Enumeração D3DPOOL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105747256"
---
# <a name="d3dpool-enumeration"></a><span data-ttu-id="57161-103">Enumeração D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="57161-103">D3DPOOL enumeration</span></span>

<span data-ttu-id="57161-104">Define a classe de memória que mantém os buffers de um recurso.</span><span class="sxs-lookup"><span data-stu-id="57161-104">Defines the memory class that holds the buffers for a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="57161-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57161-105">Syntax</span></span>


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a><span data-ttu-id="57161-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="57161-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="57161-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL \_ padrão**</span><span class="sxs-lookup"><span data-stu-id="57161-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="57161-108">Os recursos são colocados no pool de memória mais apropriado para o conjunto de usos solicitados para o recurso fornecido.</span><span class="sxs-lookup"><span data-stu-id="57161-108">Resources are placed in the memory pool most appropriate for the set of usages requested for the given resource.</span></span> <span data-ttu-id="57161-109">Normalmente, essa é a memória de vídeo, incluindo a memória de vídeo local e a memória AGP.</span><span class="sxs-lookup"><span data-stu-id="57161-109">This is usually video memory, including both local video memory and AGP memory.</span></span> <span data-ttu-id="57161-110">O \_ pool padrão D3DPOOL é separado de D3DPOOL \_ gerenciados e D3DPOOL \_ SYSTEMMEM e especifica que o recurso é colocado na memória preferencial para acesso ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57161-110">The D3DPOOL\_DEFAULT pool is separate from D3DPOOL\_MANAGED and D3DPOOL\_SYSTEMMEM, and it specifies that the resource is placed in the preferred memory for device access.</span></span> <span data-ttu-id="57161-111">Observe que D3DPOOL \_ Default nunca indica que D3DPOOL \_ gerenciado ou D3DPOOL \_ SYSTEMMEM devem ser escolhidos como o tipo de pool de memória para esse recurso.</span><span class="sxs-lookup"><span data-stu-id="57161-111">Note that D3DPOOL\_DEFAULT never indicates that either D3DPOOL\_MANAGED or D3DPOOL\_SYSTEMMEM should be chosen as the memory pool type for this resource.</span></span> <span data-ttu-id="57161-112">As texturas colocadas no \_ pool padrão D3DPOOL não podem ser bloqueadas a menos que sejam texturas dinâmicas ou sejam formatos de driver privados, FOURCC.</span><span class="sxs-lookup"><span data-stu-id="57161-112">Textures placed in the D3DPOOL\_DEFAULT pool cannot be locked unless they are dynamic textures or they are private, FOURCC, driver formats.</span></span> <span data-ttu-id="57161-113">Para acessar texturas inbloqueadas, você deve usar funções como [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9:: GetFrontBufferData**](/windows/desktop/api)e [**IDirect3DDevice9:: GetRenderTargetData**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="57161-113">To access unlockable textures, you must use functions such as [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9::GetFrontBufferData**](/windows/desktop/api), and [**IDirect3DDevice9::GetRenderTargetData**](/windows/desktop/api).</span></span> <span data-ttu-id="57161-114">\_O D3DPOOL gerenciado provavelmente é uma opção melhor do que o \_ padrão D3DPOOL para a maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="57161-114">D3DPOOL\_MANAGED is probably a better choice than D3DPOOL\_DEFAULT for most applications.</span></span> <span data-ttu-id="57161-115">Observe que algumas texturas criadas nos formatos de pixel proprietários do driver, desconhecidos para o tempo de execução do Direct3D, podem ser bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="57161-115">Note that some textures created in driver-proprietary pixel formats, unknown to the Direct3D runtime, can be locked.</span></span> <span data-ttu-id="57161-116">Observe também que-ao contrário de texturas – buffers de fundo de cadeia de troca, destinos de renderização, buffers de vértice e buffers de índice podem ser bloqueados.</span><span class="sxs-lookup"><span data-stu-id="57161-116">Also note that - unlike textures - swap chain back buffers, render targets, vertex buffers, and index buffers can be locked.</span></span> <span data-ttu-id="57161-117">Quando um dispositivo é perdido, os recursos criados usando D3DPOOL \_ padrão devem ser liberados antes de chamar [**IDirect3DDevice9:: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="57161-117">When a device is lost, resources created using D3DPOOL\_DEFAULT must be released before calling [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="57161-118">Para obter mais informações, consulte [dispositivos perdidos (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="57161-118">For more information, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="57161-119">Ao criar recursos com D3DPOOL \_ padrão, se a memória da placa de vídeo já estiver confirmada, os recursos gerenciados serão removidos para liberar memória suficiente para atender à solicitação.</span><span class="sxs-lookup"><span data-stu-id="57161-119">When creating resources with D3DPOOL\_DEFAULT, if video card memory is already committed, managed resources will be evicted to free enough memory to satisfy the request.</span></span>

</dd> <dt>

<span data-ttu-id="57161-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**\_Gerenciado D3DPOOL**</span><span class="sxs-lookup"><span data-stu-id="57161-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="57161-121">Os recursos são copiados automaticamente para a memória acessível pelo dispositivo, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="57161-121">Resources are copied automatically to device-accessible memory as needed.</span></span> <span data-ttu-id="57161-122">Os recursos gerenciados são apoiados pela memória do sistema e não precisam ser recriados quando um dispositivo é perdido.</span><span class="sxs-lookup"><span data-stu-id="57161-122">Managed resources are backed by system memory and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="57161-123">Consulte [Gerenciando recursos (Direct3D 9)](managing-resources.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="57161-123">See [Managing Resources (Direct3D 9)](managing-resources.md) for more information.</span></span> <span data-ttu-id="57161-124">Os recursos gerenciados podem ser bloqueados.</span><span class="sxs-lookup"><span data-stu-id="57161-124">Managed resources can be locked.</span></span> <span data-ttu-id="57161-125">Somente a cópia da memória do sistema é modificada diretamente.</span><span class="sxs-lookup"><span data-stu-id="57161-125">Only the system-memory copy is directly modified.</span></span> <span data-ttu-id="57161-126">O Direct3D copia suas alterações para a memória acessível por Driver, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="57161-126">Direct3D copies your changes to driver-accessible memory as needed.</span></span>



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57161-127">Diferenças entre o Direct3D 9 e o Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="57161-127">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="57161-128">D3DPOOL \_ gerenciado é válido com [**IDirect3DDevice9**](/windows/desktop/api); no entanto, ele não é válido com [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span><span class="sxs-lookup"><span data-stu-id="57161-128">D3DPOOL\_MANAGED is valid with [**IDirect3DDevice9**](/windows/desktop/api); however, it is not valid with [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="57161-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL \_ SYSTEMMEM**</span><span class="sxs-lookup"><span data-stu-id="57161-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="57161-130">Os recursos são colocados na memória que normalmente não é acessível pelo dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="57161-130">Resources are placed in memory that is not typically accessible by the Direct3D device.</span></span> <span data-ttu-id="57161-131">Essa alocação de memória consome RAM do sistema, mas não reduz a RAM paginável.</span><span class="sxs-lookup"><span data-stu-id="57161-131">This memory allocation consumes system RAM but does not reduce pageable RAM.</span></span> <span data-ttu-id="57161-132">Esses recursos não precisam ser recriados quando um dispositivo é perdido.</span><span class="sxs-lookup"><span data-stu-id="57161-132">These resources do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="57161-133">Os recursos neste pool podem ser bloqueados e podem ser usados como a origem de uma operação [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api) ou [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) para um recurso de memória criado com D3DPOOL \_ padrão.</span><span class="sxs-lookup"><span data-stu-id="57161-133">Resources in this pool can be locked and can be used as the source for a [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api) or [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) operation to a memory resource created with D3DPOOL\_DEFAULT.</span></span>

</dd> <dt>

<span data-ttu-id="57161-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_ rascunho**</span><span class="sxs-lookup"><span data-stu-id="57161-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL\_SCRATCH**</span></span>
</dt> <dd>

<span data-ttu-id="57161-135">Os recursos são colocados na RAM do sistema e não precisam ser recriados quando um dispositivo é perdido.</span><span class="sxs-lookup"><span data-stu-id="57161-135">Resources are placed in system RAM and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="57161-136">Esses recursos não são associados por restrições de formato ou tamanho do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57161-136">These resources are not bound by device size or format restrictions.</span></span> <span data-ttu-id="57161-137">Por isso, esses recursos não podem ser acessados pelo dispositivo Direct3D nem definidos como texturas ou destinos de renderização.</span><span class="sxs-lookup"><span data-stu-id="57161-137">Because of this, these resources cannot be accessed by the Direct3D device nor set as textures or render targets.</span></span> <span data-ttu-id="57161-138">No entanto, esses recursos sempre podem ser criados, bloqueados e copiados.</span><span class="sxs-lookup"><span data-stu-id="57161-138">However, these resources can always be created, locked, and copied.</span></span>

</dd> <dt>

<span data-ttu-id="57161-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="57161-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="57161-140">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="57161-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="57161-141">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="57161-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="57161-142">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="57161-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57161-143">Comentários</span><span class="sxs-lookup"><span data-stu-id="57161-143">Remarks</span></span>

<span data-ttu-id="57161-144">Todos os tipos de pool são válidos com todos os recursos, incluindo: buffers de vértice, buffers de índice, texturas e superfícies.</span><span class="sxs-lookup"><span data-stu-id="57161-144">All pool types are valid with all resources including: vertex buffers, index buffers, textures, and surfaces.</span></span>

<span data-ttu-id="57161-145">As tabelas a seguir indicam restrições em tipos de pool para destinos de renderização, estênceis de profundidade e usos dinâmico e mipmap.</span><span class="sxs-lookup"><span data-stu-id="57161-145">The following tables indicate restrictions on pool types for render targets, depth stencils, and dynamic and mipmap usages.</span></span> <span data-ttu-id="57161-146">Um x indica uma combinação compatível; a falta de um x indica incompatibilidade.</span><span class="sxs-lookup"><span data-stu-id="57161-146">An x indicates a compatible combination; lack of an x indicates incompatibility.</span></span>



| <span data-ttu-id="57161-147">pool</span><span class="sxs-lookup"><span data-stu-id="57161-147">Pool</span></span>               | <span data-ttu-id="57161-148">D3DUSAGE \_ RENDERTARGET</span><span class="sxs-lookup"><span data-stu-id="57161-148">D3DUSAGE\_RENDERTARGET</span></span> | <span data-ttu-id="57161-149">D3DUSAGE \_ DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="57161-149">D3DUSAGE\_DEPTHSTENCIL</span></span> |
|--------------------|------------------------|------------------------|
| <span data-ttu-id="57161-150">D3DPOOL \_ padrão</span><span class="sxs-lookup"><span data-stu-id="57161-150">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="57161-151">x</span><span class="sxs-lookup"><span data-stu-id="57161-151">x</span></span>                      | <span data-ttu-id="57161-152">x</span><span class="sxs-lookup"><span data-stu-id="57161-152">x</span></span>                      |
| <span data-ttu-id="57161-153">\_Gerenciado D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="57161-153">D3DPOOL\_MANAGED</span></span>   |                        |                        |
| <span data-ttu-id="57161-154">D3DPOOL \_ rascunho</span><span class="sxs-lookup"><span data-stu-id="57161-154">D3DPOOL\_SCRATCH</span></span>   |                        |                        |
| <span data-ttu-id="57161-155">D3DPOOL \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="57161-155">D3DPOOL\_SYSTEMMEM</span></span> |                        |                        |



 



| <span data-ttu-id="57161-156">pool</span><span class="sxs-lookup"><span data-stu-id="57161-156">Pool</span></span>               | <span data-ttu-id="57161-157">D3DUSAGE \_ dinâmico</span><span class="sxs-lookup"><span data-stu-id="57161-157">D3DUSAGE\_DYNAMIC</span></span> | <span data-ttu-id="57161-158">D3DUSAGE \_ AUTOGENMIPMAP</span><span class="sxs-lookup"><span data-stu-id="57161-158">D3DUSAGE\_AUTOGENMIPMAP</span></span> |
|--------------------|-------------------|-------------------------|
| <span data-ttu-id="57161-159">D3DPOOL \_ padrão</span><span class="sxs-lookup"><span data-stu-id="57161-159">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="57161-160">x</span><span class="sxs-lookup"><span data-stu-id="57161-160">x</span></span>                 | <span data-ttu-id="57161-161">x</span><span class="sxs-lookup"><span data-stu-id="57161-161">x</span></span>                       |
| <span data-ttu-id="57161-162">\_Gerenciado D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="57161-162">D3DPOOL\_MANAGED</span></span>   |                   | <span data-ttu-id="57161-163">x</span><span class="sxs-lookup"><span data-stu-id="57161-163">x</span></span>                       |
| <span data-ttu-id="57161-164">D3DPOOL \_ rascunho</span><span class="sxs-lookup"><span data-stu-id="57161-164">D3DPOOL\_SCRATCH</span></span>   |                   |                         |
| <span data-ttu-id="57161-165">D3DPOOL \_ SYSTEMMEM</span><span class="sxs-lookup"><span data-stu-id="57161-165">D3DPOOL\_SYSTEMMEM</span></span> | <span data-ttu-id="57161-166">x</span><span class="sxs-lookup"><span data-stu-id="57161-166">x</span></span>                 |                         |



 

<span data-ttu-id="57161-167">Para obter mais informações sobre tipos de uso, consulte [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="57161-167">For more information about usage types, see [**D3DUSAGE**](d3dusage.md).</span></span>

<span data-ttu-id="57161-168">Os pools não podem ser misturados para objetos diferentes contidos em um recurso (níveis de MIP em um mipmap) e, quando um pool é escolhido, ele não pode ser alterado.</span><span class="sxs-lookup"><span data-stu-id="57161-168">Pools cannot be mixed for different objects contained within one resource (mip levels in a mipmap) and, when a pool is chosen, it cannot be changed.</span></span>

<span data-ttu-id="57161-169">Os aplicativos devem usar \_ o D3DPOOL gerenciado para a maioria dos recursos estáticos, pois isso evita que o aplicativo tenha que lidar com dispositivos perdidos.</span><span class="sxs-lookup"><span data-stu-id="57161-169">Applications should use D3DPOOL\_MANAGED for most static resources because this saves the application from having to deal with lost devices.</span></span> <span data-ttu-id="57161-170">(Os recursos gerenciados são restaurados pelo tempo de execução.) Isso é especialmente benéfico para sistemas de uma (arquitetura de memória unificada).</span><span class="sxs-lookup"><span data-stu-id="57161-170">(Managed resources are restored by the runtime.) This is especially beneficial for unified memory architecture (UMA) systems.</span></span> <span data-ttu-id="57161-171">Outros recursos dinâmicos não são uma boa correspondência para D3DPOOL \_ gerenciados.</span><span class="sxs-lookup"><span data-stu-id="57161-171">Other dynamic resources are not a good match for D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="57161-172">Na verdade, os buffers de índice e os buffers de vértice não podem ser criados usando D3DPOOL \_ gerenciados junto com o D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="57161-172">In fact, index buffers and vertex buffers cannot be created using D3DPOOL\_MANAGED together with D3DUSAGE\_DYNAMIC.</span></span>

<span data-ttu-id="57161-173">Para texturas dinâmicas, às vezes é desejável usar um par de texturas de memória de vídeo e de memória do sistema, alocando a memória de vídeo usando D3DPOOL \_ padrão e a memória do sistema usando o D3DPOOL \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="57161-173">For dynamic textures, it is sometimes desirable to use a pair of video memory and system memory textures, allocating the video memory using D3DPOOL\_DEFAULT and the system memory using D3DPOOL\_SYSTEMMEM.</span></span> <span data-ttu-id="57161-174">Você pode bloquear e modificar os bits da textura de memória do sistema usando um método de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="57161-174">You can lock and modify the bits of the system memory texture using a locking method.</span></span> <span data-ttu-id="57161-175">Em seguida, você pode atualizar a textura da memória de vídeo usando [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span><span class="sxs-lookup"><span data-stu-id="57161-175">Then you can update the video memory texture using [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

## <a name="requirements"></a><span data-ttu-id="57161-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57161-176">Requirements</span></span>



| <span data-ttu-id="57161-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="57161-177">Requirement</span></span> | <span data-ttu-id="57161-178">Valor</span><span class="sxs-lookup"><span data-stu-id="57161-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57161-179">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57161-179">Header</span></span><br/> | <dl> <span data-ttu-id="57161-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="57161-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57161-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="57161-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57161-182">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="57161-182">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="57161-183">**D3DUSAGE**</span><span class="sxs-lookup"><span data-stu-id="57161-183">**D3DUSAGE**</span></span>](d3dusage.md)
</dt> <dt>

[<span data-ttu-id="57161-184">**IDirect3DDevice9::CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="57161-184">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[<span data-ttu-id="57161-185">**IDirect3DDevice9::CreateIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="57161-185">**IDirect3DDevice9::CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[<span data-ttu-id="57161-186">**IDirect3DDevice9:: CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="57161-186">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[<span data-ttu-id="57161-187">**IDirect3DDevice9::CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="57161-187">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[<span data-ttu-id="57161-188">**IDirect3DDevice9::CreateVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="57161-188">**IDirect3DDevice9::CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[<span data-ttu-id="57161-189">**D3DINDEXBUFFER \_ desc**</span><span class="sxs-lookup"><span data-stu-id="57161-189">**D3DINDEXBUFFER\_DESC**</span></span>](d3dindexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="57161-190">**D3DSURFACE \_ desc**</span><span class="sxs-lookup"><span data-stu-id="57161-190">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> <dt>

[<span data-ttu-id="57161-191">**D3DVERTEXBUFFER \_ desc**</span><span class="sxs-lookup"><span data-stu-id="57161-191">**D3DVERTEXBUFFER\_DESC**</span></span>](d3dvertexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="57161-192">**D3DVOLUME \_ desc**</span><span class="sxs-lookup"><span data-stu-id="57161-192">**D3DVOLUME\_DESC**</span></span>](d3dvolume-desc.md)
</dt> </dl>

 

 
