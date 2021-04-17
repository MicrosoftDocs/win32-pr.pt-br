---
description: A interface IAMTimeline fornece métodos para manipular a linha do tempo, o objeto central no Microsoft DirectShow Editing Services (DES).
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: Interface IAMTimeline (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758685"
---
# <a name="iamtimeline-interface"></a><span data-ttu-id="a393d-103">Interface IAMTimeline</span><span class="sxs-lookup"><span data-stu-id="a393d-103">IAMTimeline interface</span></span>

> [!Note]  
> <span data-ttu-id="a393d-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="a393d-104">\[Deprecated.</span></span> <span data-ttu-id="a393d-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a393d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="a393d-106">A `IAMTimeline` interface fornece métodos para manipular a linha do tempo, o objeto central no [Microsoft DirectShow Editing Services](directshow-editing-services.md) (des).</span><span class="sxs-lookup"><span data-stu-id="a393d-106">The `IAMTimeline` interface provides methods for manipulating the timeline, the central object in Microsoft [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span> <span data-ttu-id="a393d-107">Uma linha do tempo é uma coleção de elementos ordenados por tempo, como clipes de vídeo, clipes de áudio, efeitos e transições entre clipes.</span><span class="sxs-lookup"><span data-stu-id="a393d-107">A timeline is a collection of time-ordered elements, such as video clips, audio clips, effects, and transitions between clips.</span></span> <span data-ttu-id="a393d-108">O mecanismo de renderização usa a linha do tempo para criar um gráfico de filtro, a partir do qual o aplicativo pode gerar a saída renderizada.</span><span class="sxs-lookup"><span data-stu-id="a393d-108">The render engine uses the timeline to create a filter graph, from which the application can generate the rendered output.</span></span>

<span data-ttu-id="a393d-109">`IAMTimeline` executa três serviços básicos.</span><span class="sxs-lookup"><span data-stu-id="a393d-109">`IAMTimeline` performs three basic services.</span></span> <span data-ttu-id="a393d-110">Ele</span><span class="sxs-lookup"><span data-stu-id="a393d-110">It</span></span>

-   <span data-ttu-id="a393d-111">Cria os objetos na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="a393d-111">Creates the objects in the timeline.</span></span>
-   <span data-ttu-id="a393d-112">Atua como um contêiner para esses objetos.</span><span class="sxs-lookup"><span data-stu-id="a393d-112">Acts as a container for those objects.</span></span>
-   <span data-ttu-id="a393d-113">Define e recupera parâmetros gerais da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="a393d-113">Sets and retrieves general parameters of the timeline.</span></span>

<span data-ttu-id="a393d-114">Para criar o objeto Timeline, chame **CoCreateInstance** com o identificador de classe CLSID \_ AMTimeline.</span><span class="sxs-lookup"><span data-stu-id="a393d-114">To create the timeline object, call **CoCreateInstance** with the class identifier CLSID\_AMTimeline.</span></span>

## <a name="members"></a><span data-ttu-id="a393d-115">Membros</span><span class="sxs-lookup"><span data-stu-id="a393d-115">Members</span></span>

<span data-ttu-id="a393d-116">A interface **IAMTimeline** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a393d-116">The **IAMTimeline** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a393d-117">**IAMTimeline** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a393d-117">**IAMTimeline** also has these types of members:</span></span>

-   [<span data-ttu-id="a393d-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="a393d-118">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a393d-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="a393d-119">Methods</span></span>

<span data-ttu-id="a393d-120">A interface **IAMTimeline** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a393d-120">The **IAMTimeline** interface has these methods.</span></span>



| <span data-ttu-id="a393d-121">Método</span><span class="sxs-lookup"><span data-stu-id="a393d-121">Method</span></span>                                                             | <span data-ttu-id="a393d-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="a393d-122">Description</span></span>                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a393d-123">**AddGroup**</span><span class="sxs-lookup"><span data-stu-id="a393d-123">**AddGroup**</span></span>](iamtimeline-addgroup.md)                           | <span data-ttu-id="a393d-124">Adiciona um grupo à linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="a393d-124">Adds a group to the timeline.</span></span><br/>                                                                                          |
| [<span data-ttu-id="a393d-125">**ClearAllGroups**</span><span class="sxs-lookup"><span data-stu-id="a393d-125">**ClearAllGroups**</span></span>](iamtimeline-clearallgroups.md)               | <span data-ttu-id="a393d-126">Remove todos os grupos da linha do tempo, juntamente com todos os objetos contidos nesses grupos.</span><span class="sxs-lookup"><span data-stu-id="a393d-126">Removes all groups from the timeline, along with all objects contained in those groups.</span></span><br/>                                |
| [<span data-ttu-id="a393d-127">**CreateEmptyNode**</span><span class="sxs-lookup"><span data-stu-id="a393d-127">**CreateEmptyNode**</span></span>](iamtimeline-createemptynode.md)             | <span data-ttu-id="a393d-128">Cria um novo objeto de linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="a393d-128">Creates a new timeline object.</span></span><br/>                                                                                         |
| [<span data-ttu-id="a393d-129">**EffectsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a393d-129">**EffectsEnabled**</span></span>](iamtimeline-effectsenabled.md)               | <span data-ttu-id="a393d-130">Determina se os efeitos estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="a393d-130">Determines whether effects are enabled.</span></span><br/>                                                                                |
| [<span data-ttu-id="a393d-131">**EnableEffects**</span><span class="sxs-lookup"><span data-stu-id="a393d-131">**EnableEffects**</span></span>](iamtimeline-enableeffects.md)                 | <span data-ttu-id="a393d-132">Habilita ou desabilita todos os efeitos na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="a393d-132">Enables or disables all effects in the timeline.</span></span><br/>                                                                       |
| [<span data-ttu-id="a393d-133">**EnableTransitions**</span><span class="sxs-lookup"><span data-stu-id="a393d-133">**EnableTransitions**</span></span>](iamtimeline-enabletransitions.md)         | <span data-ttu-id="a393d-134">Habilita ou desabilita todas as transições na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="a393d-134">Enables or disables all transitions in the timeline.</span></span><br/>                                                                   |
| [<span data-ttu-id="a393d-135">**GetCountOfType**</span><span class="sxs-lookup"><span data-stu-id="a393d-135">**GetCountOfType**</span></span>](iamtimeline-getcountoftype.md)               | <span data-ttu-id="a393d-136">Recupera o número de objetos do tipo especificado que estão contidos em um grupo especificado e todos os seus filhos.</span><span class="sxs-lookup"><span data-stu-id="a393d-136">Retrieves the number of objects of the specified type that are contained in a specified group and all of its children.</span></span><br/> |
| [<span data-ttu-id="a393d-137">**GetDefaultEffect**</span><span class="sxs-lookup"><span data-stu-id="a393d-137">**GetDefaultEffect**</span></span>](iamtimeline-getdefaulteffect.md)           | <span data-ttu-id="a393d-138">Recupera o efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="a393d-138">Retrieves the default effect.</span></span><br/>                                                                                          |
| [<span data-ttu-id="a393d-139">**GetDefaultEffectB**</span><span class="sxs-lookup"><span data-stu-id="a393d-139">**GetDefaultEffectB**</span></span>](iamtimeline-getdefaulteffectb.md)         | <span data-ttu-id="a393d-140">Recupera o efeito padrão como um valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="a393d-140">Retrieves the default effect as a **BSTR** value.</span></span><br/>                                                                      |
| [<span data-ttu-id="a393d-141">**GetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="a393d-141">**GetDefaultFPS**</span></span>](iamtimeline-getdefaultfps.md)                 | <span data-ttu-id="a393d-142">Recupera a taxa de quadros de saída padrão, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="a393d-142">Retrieves the default output frame rate, in frames per second.</span></span><br/>                                                         |
| [<span data-ttu-id="a393d-143">**GetDefaultTransition**</span><span class="sxs-lookup"><span data-stu-id="a393d-143">**GetDefaultTransition**</span></span>](iamtimeline-getdefaulttransition.md)   | <span data-ttu-id="a393d-144">Recupera a transição padrão.</span><span class="sxs-lookup"><span data-stu-id="a393d-144">Retrieves the default transition.</span></span><br/>                                                                                      |
| [<span data-ttu-id="a393d-145">**GetDefaultTransitionB**</span><span class="sxs-lookup"><span data-stu-id="a393d-145">**GetDefaultTransitionB**</span></span>](iamtimeline-getdefaulttransitionb.md) | <span data-ttu-id="a393d-146">Recupera a transição padrão como um valor de **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="a393d-146">Retrieves the default transition as a **BSTR** value.</span></span><br/>                                                                  |
| [<span data-ttu-id="a393d-147">**GetDirtyRange**</span><span class="sxs-lookup"><span data-stu-id="a393d-147">**GetDirtyRange**</span></span>](iamtimeline-getdirtyrange.md)                 | <span data-ttu-id="a393d-148">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="a393d-148">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="a393d-149">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="a393d-149">**GetDuration**</span></span>](iamtimeline-getduration.md)                     | <span data-ttu-id="a393d-150">Recupera a duração da linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="a393d-150">Retrieves the timeline duration.</span></span><br/>                                                                                       |
| [<span data-ttu-id="a393d-151">**GetDuration2**</span><span class="sxs-lookup"><span data-stu-id="a393d-151">**GetDuration2**</span></span>](iamtimeline-getduration2.md)                   | <span data-ttu-id="a393d-152">Recupera a duração da linha do tempo como um **duplo**.</span><span class="sxs-lookup"><span data-stu-id="a393d-152">Retrieves the timeline duration as a **double**.</span></span><br/>                                                                       |
| [<span data-ttu-id="a393d-153">**Getgroup**</span><span class="sxs-lookup"><span data-stu-id="a393d-153">**GetGroup**</span></span>](iamtimeline-getgroup.md)                           | <span data-ttu-id="a393d-154">Recupera um grupo especificado.</span><span class="sxs-lookup"><span data-stu-id="a393d-154">Retrieves a specified group.</span></span><br/>                                                                                           |
| [<span data-ttu-id="a393d-155">**GetGroupCount**</span><span class="sxs-lookup"><span data-stu-id="a393d-155">**GetGroupCount**</span></span>](iamtimeline-getgroupcount.md)                 | <span data-ttu-id="a393d-156">Recupera o número de grupos contidos na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="a393d-156">Retrieves the number of groups that are contained in the timeline.</span></span><br/>                                                     |
| [<span data-ttu-id="a393d-157">**Getinsertmode**</span><span class="sxs-lookup"><span data-stu-id="a393d-157">**GetInsertMode**</span></span>](iamtimeline-getinsertmode.md)                 | <span data-ttu-id="a393d-158">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="a393d-158">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="a393d-159">**IsDirty**</span><span class="sxs-lookup"><span data-stu-id="a393d-159">**IsDirty**</span></span>](iamtimeline-isdirty.md)                             | <span data-ttu-id="a393d-160">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="a393d-160">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="a393d-161">**RemGroupFromList**</span><span class="sxs-lookup"><span data-stu-id="a393d-161">**RemGroupFromList**</span></span>](iamtimeline-remgroupfromlist.md)           | <span data-ttu-id="a393d-162">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="a393d-162">Not supported.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="a393d-163">**SetDefaultEffect**</span><span class="sxs-lookup"><span data-stu-id="a393d-163">**SetDefaultEffect**</span></span>](iamtimeline-setdefaulteffect.md)           | <span data-ttu-id="a393d-164">Define o efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="a393d-164">Sets the default effect.</span></span><br/>                                                                                               |
| [<span data-ttu-id="a393d-165">**SetDefaultEffectB**</span><span class="sxs-lookup"><span data-stu-id="a393d-165">**SetDefaultEffectB**</span></span>](iamtimeline-setdefaulteffectb.md)         | <span data-ttu-id="a393d-166">Define o efeito padrão como um valor **BSTR** .</span><span class="sxs-lookup"><span data-stu-id="a393d-166">Sets the default effect as a **BSTR** value.</span></span><br/>                                                                           |
| [<span data-ttu-id="a393d-167">**SetDefaultFPS**</span><span class="sxs-lookup"><span data-stu-id="a393d-167">**SetDefaultFPS**</span></span>](iamtimeline-setdefaultfps.md)                 | <span data-ttu-id="a393d-168">Define a taxa de quadros de saída padrão, em quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="a393d-168">Sets the default output frame rate, in frames per second.</span></span><br/>                                                              |
| [<span data-ttu-id="a393d-169">**SetDefaultTransition**</span><span class="sxs-lookup"><span data-stu-id="a393d-169">**SetDefaultTransition**</span></span>](iamtimeline-setdefaulttransition.md)   | <span data-ttu-id="a393d-170">Define a transição padrão.</span><span class="sxs-lookup"><span data-stu-id="a393d-170">Sets the default transition.</span></span><br/>                                                                                           |
| [<span data-ttu-id="a393d-171">**SetDefaultTransitionB**</span><span class="sxs-lookup"><span data-stu-id="a393d-171">**SetDefaultTransitionB**</span></span>](iamtimeline-setdefaulttransitionb.md) | <span data-ttu-id="a393d-172">Define a transição padrão como um valor de BSTR.</span><span class="sxs-lookup"><span data-stu-id="a393d-172">Sets the default transition as a BSTR value.</span></span><br/>                                                                           |
| [<span data-ttu-id="a393d-173">**Setinsertmode**</span><span class="sxs-lookup"><span data-stu-id="a393d-173">**SetInsertMode**</span></span>](iamtimeline-setinsertmode.md)                 | <span data-ttu-id="a393d-174">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a393d-174">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="a393d-175">**SetInterestRange**</span><span class="sxs-lookup"><span data-stu-id="a393d-175">**SetInterestRange**</span></span>](iamtimeline-setinterestrange.md)           | <span data-ttu-id="a393d-176">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="a393d-176">Not implemented.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="a393d-177">**TransitionsEnabled**</span><span class="sxs-lookup"><span data-stu-id="a393d-177">**TransitionsEnabled**</span></span>](iamtimeline-transitionsenabled.md)       | <span data-ttu-id="a393d-178">Determina se as transições estão habilitadas.</span><span class="sxs-lookup"><span data-stu-id="a393d-178">Determines whether transitions are enabled.</span></span><br/>                                                                            |
| [<span data-ttu-id="a393d-179">**ValidateSourceNames**</span><span class="sxs-lookup"><span data-stu-id="a393d-179">**ValidateSourceNames**</span></span>](iamtimeline-validatesourcenames.md)     | <span data-ttu-id="a393d-180">Valida os nomes de origem na linha do tempo.</span><span class="sxs-lookup"><span data-stu-id="a393d-180">Validates source names in the timeline.</span></span><br/>                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="a393d-181">Comentários</span><span class="sxs-lookup"><span data-stu-id="a393d-181">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a393d-182">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="a393d-182">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="a393d-183">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a393d-183">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="a393d-184">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="a393d-184">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a393d-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a393d-185">Requirements</span></span>



| <span data-ttu-id="a393d-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="a393d-186">Requirement</span></span> | <span data-ttu-id="a393d-187">Valor</span><span class="sxs-lookup"><span data-stu-id="a393d-187">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a393d-188">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a393d-188">Header</span></span><br/>  | <dl> <span data-ttu-id="a393d-189"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a393d-189"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="a393d-190">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a393d-190">Library</span></span><br/> | <dl> <span data-ttu-id="a393d-191"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a393d-191"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
