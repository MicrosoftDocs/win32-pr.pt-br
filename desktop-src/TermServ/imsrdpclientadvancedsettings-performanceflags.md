---
title: Propriedade IMsRdpClientAdvancedSettings PerformanceFlags
description: Especifica um conjunto de recursos que podem ser definidos no servidor para melhorar o desempenho.
ms.assetid: dbbc7c13-ad8a-461d-9d2e-c454bf4b9dea
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade PerformanceFlags
- Propriedade PerformanceFlags Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings, Propriedade PerformanceFlags
- Propriedade PerformanceFlags Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings2, Propriedade PerformanceFlags
- Propriedade PerformanceFlags Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings3, Propriedade PerformanceFlags
- Propriedade PerformanceFlags Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings4, Propriedade PerformanceFlags
- Propriedade PerformanceFlags Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5, Propriedade PerformanceFlags
- Propriedade PerformanceFlags Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings6
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings6, Propriedade PerformanceFlags
- Propriedade PerformanceFlags Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings7
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings7, Propriedade PerformanceFlags
- Propriedade PerformanceFlags Serviços de Área de Trabalho Remota, interface IMsRdpClientAdvancedSettings8
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings8, Propriedade PerformanceFlags
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.PerformanceFlags
- IMsRdpClientAdvancedSettings.get_PerformanceFlags
- IMsRdpClientAdvancedSettings.put_PerformanceFlags
- IMsRdpClientAdvancedSettings2.PerformanceFlags
- IMsRdpClientAdvancedSettings2.get_PerformanceFlags
- IMsRdpClientAdvancedSettings2.put_PerformanceFlags
- IMsRdpClientAdvancedSettings3.PerformanceFlags
- IMsRdpClientAdvancedSettings3.get_PerformanceFlags
- IMsRdpClientAdvancedSettings3.put_PerformanceFlags
- IMsRdpClientAdvancedSettings4.PerformanceFlags
- IMsRdpClientAdvancedSettings4.get_PerformanceFlags
- IMsRdpClientAdvancedSettings4.put_PerformanceFlags
- IMsRdpClientAdvancedSettings5.PerformanceFlags
- IMsRdpClientAdvancedSettings5.get_PerformanceFlags
- IMsRdpClientAdvancedSettings5.put_PerformanceFlags
- IMsRdpClientAdvancedSettings6.PerformanceFlags
- IMsRdpClientAdvancedSettings6.get_PerformanceFlags
- IMsRdpClientAdvancedSettings6.put_PerformanceFlags
- IMsRdpClientAdvancedSettings7.PerformanceFlags
- IMsRdpClientAdvancedSettings7.get_PerformanceFlags
- IMsRdpClientAdvancedSettings7.put_PerformanceFlags
- IMsRdpClientAdvancedSettings8.PerformanceFlags
- IMsRdpClientAdvancedSettings8.get_PerformanceFlags
- IMsRdpClientAdvancedSettings8.put_PerformanceFlags
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1731afc6d58cede5da055da8cacaf11c8712d3c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369437"
---
# <a name="imsrdpclientadvancedsettingsperformanceflags-property"></a><span data-ttu-id="6b0a4-120">IMsRdpClientAdvancedSettings: Propriedade erformanceFlags de:P</span><span class="sxs-lookup"><span data-stu-id="6b0a4-120">IMsRdpClientAdvancedSettings::PerformanceFlags property</span></span>

<span data-ttu-id="6b0a4-121">Especifica um conjunto de recursos que podem ser definidos no servidor para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-121">Specifies a set of features that can be set at the server to improve performance.</span></span>

<span data-ttu-id="6b0a4-122">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b0a4-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b0a4-123">Syntax</span></span>


```C++
HRESULT put_PerformanceFlags(
  [in]  LONG DisableList = TS_PERF_DISABLE_NOTHING
);

HRESULT get_PerformanceFlags(
  [out] LONG *pDisableList
);
```



## <a name="property-value"></a><span data-ttu-id="6b0a4-124">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="6b0a4-124">Property value</span></span>

<span data-ttu-id="6b0a4-125">Os novos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-125">The new flags.</span></span> <span data-ttu-id="6b0a4-126">O padrão é 0 (**TS \_ perf \_ desabilita \_ Nothing**.)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-126">The default is 0 (**TS\_PERF\_DISABLE\_NOTHING**.)</span></span>

<dt>

<span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>

<span data-ttu-id="6b0a4-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS \_ DESEMPENHO \_ Disable \_ Nothing** (0x00000000)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-127"><span id="TS_PERF_DISABLE_NOTHING"></span><span id="ts_perf_disable_nothing"></span>**TS\_PERF\_DISABLE\_NOTHING** (0x00000000)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-128">Nenhum recurso está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-128">No features are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>

<span data-ttu-id="6b0a4-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS \_ \_Papel de \_ parede de desativação de desempenho** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-129"><span id="TS_PERF_DISABLE_WALLPAPER"></span><span id="ts_perf_disable_wallpaper"></span>**TS\_PERF\_DISABLE\_WALLPAPER** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-130">O papel de parede na área de trabalho não é exibido.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-130">Wallpaper on the desktop is not displayed.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>

<span data-ttu-id="6b0a4-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS \_ PERF \_ Disable \_ FULLWINDOWDRAG** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-131"><span id="TS_PERF_DISABLE_FULLWINDOWDRAG"></span><span id="ts_perf_disable_fullwindowdrag"></span>**TS\_PERF\_DISABLE\_FULLWINDOWDRAG** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-132">O recurso arrastar janela inteira está desabilitado; somente o contorno da janela é exibido quando a janela é movida.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-132">Full-window drag is disabled; only the window outline is displayed when the window is moved.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>

<span data-ttu-id="6b0a4-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS \_ Desativação de desempenho \_ \_ MENUANIMATIONS** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-133"><span id="TS_PERF_DISABLE_MENUANIMATIONS"></span><span id="ts_perf_disable_menuanimations"></span>**TS\_PERF\_DISABLE\_MENUANIMATIONS** (0x00000004)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-134">As animações de menu estão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-134">Menu animations are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>

<span data-ttu-id="6b0a4-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS \_ 0x00000008 (desempenho de \_ desativação \_** )</span><span class="sxs-lookup"><span data-stu-id="6b0a4-135"><span id="TS_PERF_DISABLE_THEMING"></span><span id="ts_perf_disable_theming"></span>**TS\_PERF\_DISABLE\_THEMING** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-136">Os temas estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-136">Themes are disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>

<span data-ttu-id="6b0a4-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS \_ PERF \_ habilitar \_ gráficos aprimorados** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-137"><span id="TS_PERF_ENABLE_ENHANCED_GRAPHICS"></span><span id="ts_perf_enable_enhanced_graphics"></span>**TS\_PERF\_ENABLE\_ENHANCED GRAPHICS** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-138">Habilitar gráficos aprimorados.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-138">Enable enhanced graphics.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>

<span data-ttu-id="6b0a4-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS \_ \_Sombra do \_ cursor \_ de desativação de desempenho** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-139"><span id="TS_PERF_DISABLE_CURSOR_SHADOW"></span><span id="ts_perf_disable_cursor_shadow"></span>**TS\_PERF\_DISABLE\_CURSOR\_SHADOW** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-140">Nenhuma sombra é exibida para o cursor.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-140">No shadow is displayed for the cursor.</span></span>

</dd> <dt>

<span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>

<span data-ttu-id="6b0a4-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS \_ PERF \_ Disable \_ CURSORSETTINGS** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-141"><span id="TS_PERF_DISABLE_CURSORSETTINGS"></span><span id="ts_perf_disable_cursorsettings"></span>**TS\_PERF\_DISABLE\_CURSORSETTINGS** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-142">O cursor piscando está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-142">Cursor blinking is disabled.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>

<span data-ttu-id="6b0a4-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS \_ PERF \_ habilitar \_ a \_ suavização de fonte** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-143"><span id="TS_PERF_ENABLE_FONT_SMOOTHING"></span><span id="ts_perf_enable_font_smoothing"></span>**TS\_PERF\_ENABLE\_FONT\_SMOOTHING** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-144">Habilitar suavização de fontes.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-144">Enable font smoothing.</span></span>

</dd> <dt>

<span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>

<span data-ttu-id="6b0a4-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS \_ Composição do PERF \_ habilitar \_ área de trabalho \_** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-145"><span id="TS_PERF_ENABLE_DESKTOP_COMPOSITION"></span><span id="ts_perf_enable_desktop_composition"></span>**TS\_PERF\_ENABLE\_DESKTOP\_COMPOSITION** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-146">Habilitar composição de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-146">Enable desktop composition.</span></span>

</dd> <dt>

<span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>

<span data-ttu-id="6b0a4-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS \_ \_Configuração de \_ NONPERFCLIENT \_ padrão de desempenho** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-147"><span id="TS_PERF_DEFAULT_NONPERFCLIENT_SETTING"></span><span id="ts_perf_default_nonperfclient_setting"></span>**TS\_PERF\_DEFAULT\_NONPERFCLIENT\_SETTING** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-148">Defina internamente para clientes que não estão cientes dessa configuração.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-148">Set internally for clients not aware of this setting.</span></span>

</dd> <dt>

<span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>

<span data-ttu-id="6b0a4-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS \_ PERF \_ RESERVED1** (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="6b0a4-149"><span id="TS_PERF_RESERVED1"></span><span id="ts_perf_reserved1"></span>**TS\_PERF\_RESERVED1** (0x80000000)</span></span>


</dt> <dd>

<span data-ttu-id="6b0a4-150">Reservado e usado internamente pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-150">Reserved and used internally by the client.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="6b0a4-151">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6b0a4-151">Error codes</span></span>

<span data-ttu-id="6b0a4-152">Retornará **S \_ OK** se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="6b0a4-152">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b0a4-153">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b0a4-153">Remarks</span></span>

<span data-ttu-id="6b0a4-154">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6b0a4-154">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6b0a4-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b0a4-155">Requirements</span></span>



| <span data-ttu-id="6b0a4-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b0a4-156">Requirement</span></span> | <span data-ttu-id="6b0a4-157">Valor</span><span class="sxs-lookup"><span data-stu-id="6b0a4-157">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0a4-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b0a4-158">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0a4-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b0a4-159">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="6b0a4-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b0a4-160">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0a4-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b0a4-161">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="6b0a4-162">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6b0a4-162">Type library</span></span><br/>             | <dl> <span data-ttu-id="6b0a4-163"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b0a4-163"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6b0a4-164">DLL</span><span class="sxs-lookup"><span data-stu-id="6b0a4-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b0a4-165"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b0a4-165"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="6b0a4-166">IID</span><span class="sxs-lookup"><span data-stu-id="6b0a4-166">IID</span></span><br/>                      | <span data-ttu-id="6b0a4-167">IID \_ IMsRdpClientAdvancedSettings é definido como 3c65b4ab-12B3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="6b0a4-167">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6b0a4-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b0a4-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b0a4-169">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="6b0a4-169">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="6b0a4-170">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="6b0a4-170">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="6b0a4-171">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="6b0a4-171">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="6b0a4-172">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="6b0a4-172">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="6b0a4-173">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="6b0a4-173">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="6b0a4-174">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="6b0a4-174">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="6b0a4-175">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="6b0a4-175">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="6b0a4-176">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="6b0a4-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





