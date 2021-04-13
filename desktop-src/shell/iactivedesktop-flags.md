---
description: Esta seção descreve os sinalizadores usados pelos métodos de interface IActiveDesktop.
title: Sinalizadores IActiveDesktop (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104968786"
---
# <a name="iactivedesktop-flags"></a><span data-ttu-id="d9dbd-103">Sinalizadores de IActiveDesktop</span><span class="sxs-lookup"><span data-stu-id="d9dbd-103">IActiveDesktop Flags</span></span>

<span data-ttu-id="d9dbd-104">Esta seção descreve os sinalizadores usados pelos métodos de interface [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) .</span><span class="sxs-lookup"><span data-stu-id="d9dbd-104">This section describes the flags used by [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface methods.</span></span>

<dl> <dt>

<span data-ttu-id="d9dbd-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**\_aplicar \_ tudo ao AD**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD\_APPLY\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-106">Agregação de \* \* \* \* AD \_ Apply \_ salvar \* \* \* \*, \* \* \* \* AD \_ Apply \_ HTMLGEN \* \* \* \* e \* \* \* \* AD \_ aplicam a \_ atualização \* \* \* \* \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-106">Aggregate of the \*\*\*\*AD\_APPLY\_SAVE\*\*\*\*, \*\*\*\*AD\_APPLY\_HTMLGEN\*\*\*\*, and \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD \_ aplicar \_ atualização em buffer \_**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD\_APPLY\_BUFFERED\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-108">Inicia um temporizador e agrega todas as solicitações de atualização feitas com esse sinalizador durante esse intervalo de tempo em uma única atualização.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-108">Starts a timer and aggregates all the refresh requests made with this flag during that time interval into a single refresh.</span></span> <span data-ttu-id="d9dbd-109">Esse intervalo é definido em cinco segundos.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-109">This interval is set at five seconds.</span></span> <span data-ttu-id="d9dbd-110">No final do intervalo, ou se uma atualização for solicitada durante o intervalo sem um \* \* \* \* \* \_ o anúncio aplicar \_ \_ atualização em buffer \* \* \* \* sinalizador, a atualização será feita e o temporizador será interrompido.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-110">At the end of the interval, or if a refresh is requested during the interval without an \*\*\*\*AD\_APPLY\_BUFFERED\_REFRESH\*\*\*\* flag, the refresh is made and the timer is stopped.</span></span> <span data-ttu-id="d9dbd-111">Esse sinalizador deve ser combinado com o sinalizador \* \* \* \* AD \_ aplicar \_ atualização \* \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-111">This flag must be combined with the \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**\_DYNAMICREFRESH de aplicação ad \_**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD\_APPLY\_DYNAMICREFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-113">[Versão 5,0](versions.md).</span><span class="sxs-lookup"><span data-stu-id="d9dbd-113">[Version 5.0](versions.md).</span></span> <span data-ttu-id="d9dbd-114">Use HTML dinâmico para atualizar somente os itens que foram alterados desde a última atualização, não a área de trabalho inteira.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-114">Use dynamic HTML to refresh only those items that have changed since the last refresh, not the entire desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**\_força de aplicação do AD \_**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD\_APPLY\_FORCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-116">Forçar uma alteração no Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-116">Force an Active Desktop change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**\_HTMLGEN de aplicação ad \_**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD\_APPLY\_HTMLGEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-118">Gere novamente o arquivo HTML da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-118">Regenerate the desktop HTML file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**\_aplicar \_ atualização do AD**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD\_APPLY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-120">Atualize o item da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-120">Refresh the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**\_aplicar \_ salvamento de AD**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD\_APPLY\_SAVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-122">Salve o item da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-122">Save the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP \_ elem \_ tudo**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP\_ELEM\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-124">Agregação dos \_ valores elem de comp \_ \* .</span><span class="sxs-lookup"><span data-stu-id="d9dbd-124">Aggregate of the COMP\_ELEM\_\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP \_ elem \_ verificado**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP\_ELEM\_CHECKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-126">O item foi verificado.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-126">The item has been checked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP \_ elem \_ CURITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP\_ELEM\_CURITEMSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-128">O estado atual do item da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-128">The current state of the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP \_ elem \_ FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP\_ELEM\_FRIENDLYNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-130">O nome amigável do item.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-130">The friendly name of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP \_ elem \_ NoScroll**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP\_ELEM\_NOSCROLL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-132">O item não é rolável.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-132">The item is not scrollable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP \_ elem \_ original do \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP\_ELEM\_ORIGINAL\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-134">As informações do estado do item da área de trabalho original.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-134">The original desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP \_ elem \_ pos \_ esquerdo**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP\_ELEM\_POS\_LEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-136">A posição horizontal do item.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-136">The horizontal position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP \_ elem \_ pos \_ superior**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP\_ELEM\_POS\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-138">A posição vertical do item.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-138">The vertical position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP \_ elem \_ pos \_ ZINDEX**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP\_ELEM\_POS\_ZINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-140">O índice z do item.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-140">The z-index of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP \_ elem \_ restaurou o \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP\_ELEM\_RESTORED\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-142">As informações de estado do item da área de trabalho restaurado.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-142">The restored desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**altura do tamanho da COMP \_ elem \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**COMP\_ELEM\_SIZE\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-144">A altura do item.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-144">The height of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**largura do tamanho da COMP \_ elem \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**COMP\_ELEM\_SIZE\_WIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-146">A largura do item.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-146">The width of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**origem do COMP \_ elem \_**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP\_ELEM\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-148">A origem original do item.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-148">The original source of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**\_tipo de elem de comp \_**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP\_ELEM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-150">O tipo do item.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-150">The item type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**tipo de COMP \_ \_ CFHTML**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**COMP\_TYPE\_CFHTML**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-152">HTML de formato compactado.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-152">Compressed format HTML.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**\_controle de tipo de comp \_**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP\_TYPE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-154">O item é um controle.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-154">The item is a control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**tipo de COMP \_ \_ HTMLDOC**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**COMP\_TYPE\_HTMLDOC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-156">O item é um documento HTML.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-156">The item is an HTML document.</span></span> <span data-ttu-id="d9dbd-157">Esse sinalizador só deve ser usado quando absolutamente necessário.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-157">This flag should only be used when absolutely necessary.</span></span> <span data-ttu-id="d9dbd-158">Ele faz com que um documento HTML seja inserido literalmente no arquivo desktop. htt usado para controlar o layout da área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-158">It causes an HTML document to be inserted verbatim into the Desktop.htt file used to control layout of the desktop.</span></span> <span data-ttu-id="d9dbd-159">Na maioria dos casos, você deve usar o sinalizador \* \* \* \* tipo de COMP do \_ \_ site \* \* \* \* para adicionar itens à área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-159">For most cases, you should use the \*\*\*\*COMP\_TYPE\_WEBSITE\*\*\*\* flag to add items to the desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**tipo de COMP \_ \_ Max**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**COMP\_TYPE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-161">O valor máximo de um sinalizador de tipo de COMP \_ \_ \* .</span><span class="sxs-lookup"><span data-stu-id="d9dbd-161">The maximum value of a COMP\_TYPE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**\_imagem do tipo comp \_**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**COMP\_TYPE\_PICTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-163">O item é uma imagem.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-163">The item is a picture.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**tipo de COMP \_ \_ site**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**COMP\_TYPE\_WEBSITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-165">O item é um site.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-165">The item is a website.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**\_parte superior do componente**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPONENT\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-167">Um valor de ordem z que significa que o item está na parte superior.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-167">A z-order value meaning the item is at the top.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE \_ Center**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE\_CENTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-169">O papel de parede está centralizado.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-169">The wallpaper is centered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE \_ Max**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-171">O valor máximo de um \_ \* sinalizador WPSTYLE.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-171">The maximum value of a WPSTYLE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE \_ Stretch**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE\_STRETCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-173">O papel de parede é alongado para se ajustar à tela inteira.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-173">The wallpaper is stretched to fit the entire screen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**bloco do WPSTYLE \_**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**WPSTYLE\_TILE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-175">O papel de parede é enlado.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-175">The wallpaper is tiled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d9dbd-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE \_ span**</span><span class="sxs-lookup"><span data-stu-id="d9dbd-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE\_SPAN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="d9dbd-177">**Windows 8 e posterior**: o papel de parede abrange vários monitores.</span><span class="sxs-lookup"><span data-stu-id="d9dbd-177">**Windows 8 and later**: The wallpaper spans multiple monitors.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9dbd-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9dbd-178">Requirements</span></span>



| <span data-ttu-id="d9dbd-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9dbd-179">Requirement</span></span> | <span data-ttu-id="d9dbd-180">Valor</span><span class="sxs-lookup"><span data-stu-id="d9dbd-180">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d9dbd-181">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d9dbd-181">Header</span></span><br/> | <dl> <span data-ttu-id="d9dbd-182"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9dbd-182"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
