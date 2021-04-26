---
description: Uma combinação de zero ou mais opções de bloqueio que descrevem o tipo de bloqueio a ser executado.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adaeddbc1aff0812d3e0f67df90c2cf9b1118347
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999423"
---
# <a name="d3dlock"></a><span data-ttu-id="cd003-103">D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="cd003-103">D3DLOCK</span></span>

<span data-ttu-id="cd003-104">Uma combinação de zero ou mais opções de bloqueio que descrevem o tipo de bloqueio a ser executado.</span><span class="sxs-lookup"><span data-stu-id="cd003-104">A combination of zero or more locking options that describe the type of lock to perform.</span></span>



| <span data-ttu-id="cd003-105">\#definir</span><span class="sxs-lookup"><span data-stu-id="cd003-105">\#define</span></span>                   | <span data-ttu-id="cd003-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd003-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd003-107">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="cd003-107">D3DLOCK\_DISCARD</span></span>           | <span data-ttu-id="cd003-108">O aplicativo descarta toda a memória na região bloqueada.</span><span class="sxs-lookup"><span data-stu-id="cd003-108">The application discards all memory within the locked region.</span></span> <span data-ttu-id="cd003-109">Para os buffers de vértice e de índice, todo o buffer será Descartado.</span><span class="sxs-lookup"><span data-stu-id="cd003-109">For vertex and index buffers, the entire buffer will be discarded.</span></span> <span data-ttu-id="cd003-110">Essa opção só é válida quando o recurso é criado com uso dinâmico (consulte [D3DUSAGE](d3dusage.md)).</span><span class="sxs-lookup"><span data-stu-id="cd003-110">This option is only valid when the resource is created with dynamic usage (see [D3DUSAGE](d3dusage.md)).</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="cd003-111">D3DLOCK \_ DONOTWAIT</span><span class="sxs-lookup"><span data-stu-id="cd003-111">D3DLOCK\_DONOTWAIT</span></span>         | <span data-ttu-id="cd003-112">Permite que um aplicativo receba ciclos de CPU se o driver não puder bloquear a superfície imediatamente.</span><span class="sxs-lookup"><span data-stu-id="cd003-112">Allows an application to gain back CPU cycles if the driver cannot lock the surface immediately.</span></span> <span data-ttu-id="cd003-113">Se esse sinalizador estiver definido e o driver não puder bloquear a superfície imediatamente, a chamada de bloqueio retornará D3DERR \_ WASSTILLDRAWING.</span><span class="sxs-lookup"><span data-stu-id="cd003-113">If this flag is set and the driver cannot lock the surface immediately, the lock call will return D3DERR\_WASSTILLDRAWING.</span></span> <span data-ttu-id="cd003-114">Esse sinalizador só pode ser usado durante o bloqueio de uma superfície criada usando [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api)ou [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span><span class="sxs-lookup"><span data-stu-id="cd003-114">This flag can only be used when locking a surface created using [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api), or [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span></span> <span data-ttu-id="cd003-115">Esse sinalizador também pode ser usado com um buffer de fundo.</span><span class="sxs-lookup"><span data-stu-id="cd003-115">This flag can also be used with a back buffer.</span></span>            |
| <span data-ttu-id="cd003-116">D3DLOCK \_ nenhuma \_ \_ atualização suja</span><span class="sxs-lookup"><span data-stu-id="cd003-116">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span> | <span data-ttu-id="cd003-117">Por padrão, um bloqueio em um recurso adiciona uma região suja a esse recurso.</span><span class="sxs-lookup"><span data-stu-id="cd003-117">By default, a lock on a resource adds a dirty region to that resource.</span></span> <span data-ttu-id="cd003-118">Essa opção impede qualquer alteração no estado sujo do recurso.</span><span class="sxs-lookup"><span data-stu-id="cd003-118">This option prevents any changes to the dirty state of the resource.</span></span> <span data-ttu-id="cd003-119">Os aplicativos devem usar essa opção quando tiverem informações adicionais sobre o conjunto de regiões alteradas durante a operação de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="cd003-119">Applications should use this option when they have additional information about the set of regions changed during the lock operation.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="cd003-120">D3DLOCK \_ NOoverwrite</span><span class="sxs-lookup"><span data-stu-id="cd003-120">D3DLOCK\_NOOVERWRITE</span></span>       | <span data-ttu-id="cd003-121">Indica que a memória que foi referenciada em uma chamada de desenho desde o último bloqueio sem esse sinalizador não será modificada durante o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="cd003-121">Indicates that memory that was referred to in a drawing call since the last lock without this flag will not be modified during the lock.</span></span> <span data-ttu-id="cd003-122">Isso pode habilitar otimizações quando o aplicativo está acrescentando dados a um recurso.</span><span class="sxs-lookup"><span data-stu-id="cd003-122">This can enable optimizations when the application is appending data to a resource.</span></span> <span data-ttu-id="cd003-123">A especificação desse sinalizador permite que o driver retorne imediatamente se o recurso estiver em uso, caso contrário, o driver deverá terminar de usar o recurso antes de retornar do bloqueio.</span><span class="sxs-lookup"><span data-stu-id="cd003-123">Specifying this flag enables the driver to return immediately if the resource is in use, otherwise, the driver must finish using the resource before returning from locking.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="cd003-124">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="cd003-124">D3DLOCK\_NOSYSLOCK</span></span>         | <span data-ttu-id="cd003-125">O comportamento padrão de um bloqueio de memória de vídeo é reservar uma seção crítica em todo o sistema, garantindo que nenhuma alteração no modo de exibição ocorrerá durante o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="cd003-125">The default behavior of a video memory lock is to reserve a system-wide critical section, guaranteeing that no display mode changes will occur for the duration of the lock.</span></span> <span data-ttu-id="cd003-126">Essa opção faz com que a seção crítica em todo o sistema não seja mantida durante o bloqueio.</span><span class="sxs-lookup"><span data-stu-id="cd003-126">This option causes the system-wide critical section not to be held for the duration of the lock.</span></span><br/> <span data-ttu-id="cd003-127">A operação de bloqueio é demorada, mas pode permitir que o sistema execute outras tarefas, como mover o cursor do mouse.</span><span class="sxs-lookup"><span data-stu-id="cd003-127">The lock operation is time consuming, but can enable the system to perform other duties, such as moving the mouse cursor.</span></span> <span data-ttu-id="cd003-128">Essa opção é útil para bloqueios de longa duração, como o bloqueio do buffer de fundo para a renderização de software que, de outra forma, afetaria negativamente a capacidade de resposta do sistema.</span><span class="sxs-lookup"><span data-stu-id="cd003-128">This option is useful for long-duration locks, such as the lock of the back buffer for software rendering that would otherwise adversely affect system responsiveness.</span></span><br/> |
| <span data-ttu-id="cd003-129">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="cd003-129">D3DLOCK\_READONLY</span></span>          | <span data-ttu-id="cd003-130">O aplicativo não gravará no buffer.</span><span class="sxs-lookup"><span data-stu-id="cd003-130">The application will not write to the buffer.</span></span> <span data-ttu-id="cd003-131">Isso permite que os recursos armazenados em formatos não nativos salvem a etapa de recompactação ao desbloquear.</span><span class="sxs-lookup"><span data-stu-id="cd003-131">This enables resources stored in non-native formats to save the recompression step when unlocking.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="cd003-132">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="cd003-132">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="cd003-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd003-133">Header</span></span>                   | <span data-ttu-id="cd003-134">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="cd003-134">d3d9types.h</span></span> |
| <span data-ttu-id="cd003-135">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="cd003-135">Minimum operating system</span></span> | <span data-ttu-id="cd003-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cd003-136">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="cd003-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cd003-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd003-138">Constantes do Direct3D</span><span class="sxs-lookup"><span data-stu-id="cd003-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="cd003-139">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="cd003-139">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="cd003-140">**Bloqueio**</span><span class="sxs-lookup"><span data-stu-id="cd003-140">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="cd003-141">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="cd003-141">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="cd003-142">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="cd003-142">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="cd003-143">**Bloqueio**</span><span class="sxs-lookup"><span data-stu-id="cd003-143">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="cd003-144">**Mínima**</span><span class="sxs-lookup"><span data-stu-id="cd003-144">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="cd003-145">**Mínima**</span><span class="sxs-lookup"><span data-stu-id="cd003-145">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="cd003-146">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="cd003-146">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="cd003-147">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="cd003-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

<span data-ttu-id="cd003-148">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="cd003-148">**LockVertexBuffer**</span></span>
</dt> <dt>

[<span data-ttu-id="cd003-149">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="cd003-149">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="cd003-150">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="cd003-150">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="cd003-151">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="cd003-151">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="cd003-152">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="cd003-152">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
