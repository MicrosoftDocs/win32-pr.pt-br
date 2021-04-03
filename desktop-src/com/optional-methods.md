---
title: Métodos opcionais
description: Métodos opcionais
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084914"
---
# <a name="optional-methods"></a><span data-ttu-id="d08d7-103">Métodos opcionais</span><span class="sxs-lookup"><span data-stu-id="d08d7-103">Optional Methods</span></span>

<span data-ttu-id="d08d7-104">Um componente OLE pode implementar uma interface sem implementar toda a semântica de cada método na interface, em vez de retornar E \_ NOTIMPL ou S \_ OK conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="d08d7-104">An OLE component can implement an interface without implementing all the semantics of every method in the interface, instead returning E\_NOTIMPL or S\_OK as appropriate.</span></span> <span data-ttu-id="d08d7-105">A tabela a seguir descreve os métodos que um contêiner de controle ActiveX não precisa implementar (ou seja, o contêiner de controle pode retornar E \_ NOTIMPL).</span><span class="sxs-lookup"><span data-stu-id="d08d7-105">The following table describes those methods that an ActiveX control container is not required to implement (i.e. the control container can return E\_NOTIMPL).</span></span>

<span data-ttu-id="d08d7-106">A tabela a seguir descreve os métodos opcionais; Observe que o método ainda deve existir, mas pode simplesmente retornar E \_ NOTIMPL em vez de implementar a semântica real.</span><span class="sxs-lookup"><span data-stu-id="d08d7-106">The table below describes optional methods; note that the method must still exist, but can simply return E\_NOTIMPL instead of implementing real semantics.</span></span> <span data-ttu-id="d08d7-107">Observe que qualquer método de uma interface obrigatória que não esteja listada abaixo deve ser considerado obrigatório e não pode retornar e \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="d08d7-107">Note that any method from a mandatory interface that is not listed below must be considered mandatory and may not return E\_NOTIMPL.</span></span>

## <a name="ioleclientsite"></a><span data-ttu-id="d08d7-108">IOleClientSite</span><span class="sxs-lookup"><span data-stu-id="d08d7-108">IOleClientSite</span></span>



| <span data-ttu-id="d08d7-109">Método</span><span class="sxs-lookup"><span data-stu-id="d08d7-109">Method</span></span>                                                     | <span data-ttu-id="d08d7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d08d7-110">Comments</span></span>                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d08d7-111">**Salvar como**</span><span class="sxs-lookup"><span data-stu-id="d08d7-111">**SaveObject**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | <span data-ttu-id="d08d7-112">Necessário para que a persistência seja suportada com êxito.</span><span class="sxs-lookup"><span data-stu-id="d08d7-112">Necessary for persistence to be successfully supported.</span></span><br/>                                       |
| [<span data-ttu-id="d08d7-113">**GetMoniker**</span><span class="sxs-lookup"><span data-stu-id="d08d7-113">**GetMoniker**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | <span data-ttu-id="d08d7-114">Necessário somente se o contêiner der suporte à vinculação de controles em seu próprio formulário ou documento.</span><span class="sxs-lookup"><span data-stu-id="d08d7-114">Necessary only if the container supports linking to controls within its own form or document.</span></span><br/> |



 

## <a name="ioleinplacesite"></a><span data-ttu-id="d08d7-115">IOleInPlaceSite</span><span class="sxs-lookup"><span data-stu-id="d08d7-115">IOleInPlaceSite</span></span>



| <span data-ttu-id="d08d7-116">Método</span><span class="sxs-lookup"><span data-stu-id="d08d7-116">Method</span></span>                                                                     | <span data-ttu-id="d08d7-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d08d7-117">Comments</span></span>                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="d08d7-118">**ContextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="d08d7-118">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | <span data-ttu-id="d08d7-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="d08d7-119">Optional</span></span><br/>                                      |
| [<span data-ttu-id="d08d7-120">**Rolagem**</span><span class="sxs-lookup"><span data-stu-id="d08d7-120">**Scroll**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | <span data-ttu-id="d08d7-121">Pode retornar S \_ false sem ação.</span><span class="sxs-lookup"><span data-stu-id="d08d7-121">May return S\_FALSE with no action.</span></span><br/>           |
| [<span data-ttu-id="d08d7-122">**DiscardUndoState**</span><span class="sxs-lookup"><span data-stu-id="d08d7-122">**DiscardUndoState**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | <span data-ttu-id="d08d7-123">Pode retornar S \_ OK sem ação.</span><span class="sxs-lookup"><span data-stu-id="d08d7-123">Can return S\_OK with no action.</span></span><br/>              |
| [<span data-ttu-id="d08d7-124">**DeactivateAndUndo**</span><span class="sxs-lookup"><span data-stu-id="d08d7-124">**DeactivateAndUndo**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | <span data-ttu-id="d08d7-125">A desativação é obrigatória; Desfazer é opcional.</span><span class="sxs-lookup"><span data-stu-id="d08d7-125">Deactivation is mandatory; Undo is optional.</span></span> <br/> |



 

## <a name="iolecontrolsite"></a><span data-ttu-id="d08d7-126">IOleControlSite</span><span class="sxs-lookup"><span data-stu-id="d08d7-126">IOleControlSite</span></span>



| <span data-ttu-id="d08d7-127">Método</span><span class="sxs-lookup"><span data-stu-id="d08d7-127">Method</span></span>                                                                          | <span data-ttu-id="d08d7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d08d7-128">Comments</span></span>                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d08d7-129">**GetExtendedControl**</span><span class="sxs-lookup"><span data-stu-id="d08d7-129">**GetExtendedControl**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | <span data-ttu-id="d08d7-130">Necessário para contêineres que dão suporte a controles estendidos.</span><span class="sxs-lookup"><span data-stu-id="d08d7-130">Necessary for containers that support extended controls.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="d08d7-131">**ShowPropertyFrame**</span><span class="sxs-lookup"><span data-stu-id="d08d7-131">**ShowPropertyFrame**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | <span data-ttu-id="d08d7-132">Necessário para contêineres que desejam incluir suas próprias páginas de propriedades para manipular propriedades de controle estendido além daqueles fornecidos por um controle.</span><span class="sxs-lookup"><span data-stu-id="d08d7-132">Necessary for containers that wish to include their own property pages to handle extended control properties in addition to those provided by a control.</span></span><br/> |
| [<span data-ttu-id="d08d7-133">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="d08d7-133">**TranslateAccelerator**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | <span data-ttu-id="d08d7-134">Pode retornar S \_ false sem ação.</span><span class="sxs-lookup"><span data-stu-id="d08d7-134">May return S\_FALSE with no action.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="d08d7-135">**LockInPlaceActive**</span><span class="sxs-lookup"><span data-stu-id="d08d7-135">**LockInPlaceActive**</span></span>](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | <span data-ttu-id="d08d7-136">Opcional</span><span class="sxs-lookup"><span data-stu-id="d08d7-136">Optional</span></span><br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a><span data-ttu-id="d08d7-137">IDispatch (Propriedades de ambiente)</span><span class="sxs-lookup"><span data-stu-id="d08d7-137">IDispatch (Ambient properties)</span></span>



| <span data-ttu-id="d08d7-138">Método</span><span class="sxs-lookup"><span data-stu-id="d08d7-138">Method</span></span>                      | <span data-ttu-id="d08d7-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="d08d7-139">Comments</span></span>                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d08d7-140">GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="d08d7-140">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="d08d7-141">Necessário para contêineres que dão suporte a propriedades de ambiente não padrão.</span><span class="sxs-lookup"><span data-stu-id="d08d7-141">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="d08d7-142">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="d08d7-142">GetTypeInfo</span></span><br/>      | <span data-ttu-id="d08d7-143">Necessário para contêineres que dão suporte a propriedades de ambiente não padrão.</span><span class="sxs-lookup"><span data-stu-id="d08d7-143">Necessary for containers that support non-standard ambient properties.</span></span><br/> |
| <span data-ttu-id="d08d7-144">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="d08d7-144">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="d08d7-145">Necessário para contêineres que dão suporte a propriedades de ambiente não padrão.</span><span class="sxs-lookup"><span data-stu-id="d08d7-145">Necessary for containers that support non-standard ambient properties.</span></span><br/> |



 

## <a name="idispatch-event-sink"></a><span data-ttu-id="d08d7-146">IDispatch (coletor de eventos)</span><span class="sxs-lookup"><span data-stu-id="d08d7-146">IDispatch (Event sink)</span></span>



| <span data-ttu-id="d08d7-147">Método</span><span class="sxs-lookup"><span data-stu-id="d08d7-147">Method</span></span>                      | <span data-ttu-id="d08d7-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="d08d7-148">Comments</span></span>                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d08d7-149">GetTypeInfoCount</span><span class="sxs-lookup"><span data-stu-id="d08d7-149">GetTypeInfoCount</span></span><br/> | <span data-ttu-id="d08d7-150">O controle sabe suas próprias informações de tipo, portanto, não é necessário chamá-la.</span><span class="sxs-lookup"><span data-stu-id="d08d7-150">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="d08d7-151">GetTypeInfo</span><span class="sxs-lookup"><span data-stu-id="d08d7-151">GetTypeInfo</span></span><br/>      | <span data-ttu-id="d08d7-152">O controle sabe suas próprias informações de tipo, portanto, não é necessário chamá-la.</span><span class="sxs-lookup"><span data-stu-id="d08d7-152">The control knows its own type information, so it has no need to call this.</span></span><br/> |
| <span data-ttu-id="d08d7-153">GetIDsOfNames</span><span class="sxs-lookup"><span data-stu-id="d08d7-153">GetIDsOfNames</span></span><br/>    | <span data-ttu-id="d08d7-154">O controle sabe suas próprias informações de tipo, portanto, não é necessário chamá-la.</span><span class="sxs-lookup"><span data-stu-id="d08d7-154">The control knows its own type information, so it has no need to call this.</span></span><br/> |



 

## <a name="ioleinplaceframe"></a><span data-ttu-id="d08d7-155">IOleInPlaceFrame</span><span class="sxs-lookup"><span data-stu-id="d08d7-155">IOleInPlaceFrame</span></span>



| <span data-ttu-id="d08d7-156">Método</span><span class="sxs-lookup"><span data-stu-id="d08d7-156">Method</span></span>                                                                           | <span data-ttu-id="d08d7-157">Comentários</span><span class="sxs-lookup"><span data-stu-id="d08d7-157">Comments</span></span>                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="d08d7-158">**ContextSensitiveHelp**</span><span class="sxs-lookup"><span data-stu-id="d08d7-158">**ContextSensitiveHelp**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [<span data-ttu-id="d08d7-159">**GetBorder**</span><span class="sxs-lookup"><span data-stu-id="d08d7-159">**GetBorder**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | <span data-ttu-id="d08d7-160">Necessário para contêineres com interface do usuário da barra de ferramentas (que é opcional)</span><span class="sxs-lookup"><span data-stu-id="d08d7-160">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="d08d7-161">**RequestBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="d08d7-161">**RequestBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | <span data-ttu-id="d08d7-162">Necessário para contêineres com interface do usuário da barra de ferramentas (que é opcional)</span><span class="sxs-lookup"><span data-stu-id="d08d7-162">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="d08d7-163">**SetBorderSpace**</span><span class="sxs-lookup"><span data-stu-id="d08d7-163">**SetBorderSpace**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | <span data-ttu-id="d08d7-164">Necessário para contêineres com interface do usuário da barra de ferramentas (que é opcional)</span><span class="sxs-lookup"><span data-stu-id="d08d7-164">Necessary for containers with toolbar UI (which is optional)</span></span><br/> |
| [<span data-ttu-id="d08d7-165">**InsertMenus**</span><span class="sxs-lookup"><span data-stu-id="d08d7-165">**InsertMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | <span data-ttu-id="d08d7-166">Necessário para contêineres com interface do usuário de menu (que é opcional)</span><span class="sxs-lookup"><span data-stu-id="d08d7-166">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="d08d7-167">**SetMenu**</span><span class="sxs-lookup"><span data-stu-id="d08d7-167">**SetMenu**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | <span data-ttu-id="d08d7-168">Necessário para contêineres com interface do usuário de menu (que é opcional)</span><span class="sxs-lookup"><span data-stu-id="d08d7-168">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="d08d7-169">**RemoveMenus**</span><span class="sxs-lookup"><span data-stu-id="d08d7-169">**RemoveMenus**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | <span data-ttu-id="d08d7-170">Necessário para contêineres com interface do usuário de menu (que é opcional)</span><span class="sxs-lookup"><span data-stu-id="d08d7-170">Necessary for containers with menu UI (which is optional)</span></span><br/>    |
| [<span data-ttu-id="d08d7-171">**SetStatusText**</span><span class="sxs-lookup"><span data-stu-id="d08d7-171">**SetStatusText**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | <span data-ttu-id="d08d7-172">Necessário somente para contêineres que têm uma linha de status</span><span class="sxs-lookup"><span data-stu-id="d08d7-172">Necessary only for containers that have a status line</span></span><br/>        |
| [<span data-ttu-id="d08d7-173">**EnableModeless**</span><span class="sxs-lookup"><span data-stu-id="d08d7-173">**EnableModeless**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | <span data-ttu-id="d08d7-174">Opcional</span><span class="sxs-lookup"><span data-stu-id="d08d7-174">Optional</span></span><br/>                                                     |
| [<span data-ttu-id="d08d7-175">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="d08d7-175">**TranslateAccelerator**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | <span data-ttu-id="d08d7-176">Opcional</span><span class="sxs-lookup"><span data-stu-id="d08d7-176">Optional</span></span><br/>                                                     |



 

## <a name="iolecontainer"></a><span data-ttu-id="d08d7-177">IOleContainer</span><span class="sxs-lookup"><span data-stu-id="d08d7-177">IOleContainer</span></span>



| <span data-ttu-id="d08d7-178">Método</span><span class="sxs-lookup"><span data-stu-id="d08d7-178">Method</span></span>                                                                    | <span data-ttu-id="d08d7-179">Comentários</span><span class="sxs-lookup"><span data-stu-id="d08d7-179">Comments</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d08d7-180">**ParseDisplayName**</span><span class="sxs-lookup"><span data-stu-id="d08d7-180">**ParseDisplayName**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | <span data-ttu-id="d08d7-181">Somente se houver suporte para vinculação a controles ou a outras incorporações no contêiner, como isso é necessário para a associação de moniker.</span><span class="sxs-lookup"><span data-stu-id="d08d7-181">Only if linking to controls or other embeddings in the container is supported, as this is necessary for moniker binding.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="d08d7-182">**LockContainer**</span><span class="sxs-lookup"><span data-stu-id="d08d7-182">**LockContainer**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | <span data-ttu-id="d08d7-183">Como para ParseDisplayName</span><span class="sxs-lookup"><span data-stu-id="d08d7-183">As for ParseDisplayName</span></span><br/>                                                                                                                                                                                                                   |
| [<span data-ttu-id="d08d7-184">**EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="d08d7-184">**EnumObjects**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | <span data-ttu-id="d08d7-185">Retorna todos os controles ActiveX por meio de um enumerador com [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), mas não necessariamente todos os objetos (porque não há nenhuma garantia de que todos os objetos são controles ActiveX; alguns podem ser controles regulares do Windows).</span><span class="sxs-lookup"><span data-stu-id="d08d7-185">Returns all ActiveX controls through an enumerator with [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown), but not necessarily all objects (because there's no guarantee that all objects are ActiveX controls; some may be regular Windows controls).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="d08d7-186">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d08d7-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d08d7-187">Contêineres</span><span class="sxs-lookup"><span data-stu-id="d08d7-187">Containers</span></span>](containers.md)
</dt> </dl>

 

