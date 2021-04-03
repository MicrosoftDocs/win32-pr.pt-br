---
title: Sinalizadores de registro
description: Sinalizadores de registro
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Plug-ins do Windows Media Player, sinalizadores de registro
- plug-ins, sinalizadores de registro
- plug-ins de interface do usuário, sinalizadores de registro
- Plug-ins de interface do usuário, sinalizadores de registro
- sinalizadores, plug-ins de interface do usuário
- registro, plug-ins de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac609b45866cd5f18edf61dffc2d3b7ac3c397ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007123"
---
# <a name="registration-flags"></a><span data-ttu-id="ed70c-109">Sinalizadores de registro</span><span class="sxs-lookup"><span data-stu-id="ed70c-109">Registration Flags</span></span>

<span data-ttu-id="ed70c-110">Quando o assistente de plug-in do Windows Media Player cria um novo projeto de plug-in de interface do usuário, ele cria uma chave no registro que contém informações sobre o plug-in.</span><span class="sxs-lookup"><span data-stu-id="ed70c-110">When the Windows Media Player Plug-in Wizard creates a new UI plug-in project, it creates a key in the registry that contains information about the plug-in.</span></span> <span data-ttu-id="ed70c-111">Essa chave é criada no seguinte local:</span><span class="sxs-lookup"><span data-stu-id="ed70c-111">This key is created in the following location:</span></span>


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



<span data-ttu-id="ed70c-112">*ClassID* é a ID de classe do plug-in.</span><span class="sxs-lookup"><span data-stu-id="ed70c-112">*ClassId* is the class id of the plug-in.</span></span>

<span data-ttu-id="ed70c-113">Essa chave inclui os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed70c-113">This key includes the following values.</span></span>



| <span data-ttu-id="ed70c-114">Nome</span><span class="sxs-lookup"><span data-stu-id="ed70c-114">Name</span></span>                     | <span data-ttu-id="ed70c-115">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed70c-115">Type</span></span>       | <span data-ttu-id="ed70c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed70c-116">Description</span></span>                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed70c-117">Funcionalidades</span><span class="sxs-lookup"><span data-stu-id="ed70c-117">Capabilities</span></span>             | <span data-ttu-id="ed70c-118">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="ed70c-118">REG\_DWORD</span></span> | <span data-ttu-id="ed70c-119">Um valor DWORD que consiste em pelo menos um sinalizador de tipo de plug-in que pode ser combinado com um ou mais sinalizadores de recursos de plug-in usando binary ou operações.</span><span class="sxs-lookup"><span data-stu-id="ed70c-119">A DWORD value that consists of at least one plug-in type flag that may be combined with one or more plug-in capabilities flags by using binary OR operations.</span></span>                             |
| <span data-ttu-id="ed70c-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed70c-120">Description</span></span>              | <span data-ttu-id="ed70c-121">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="ed70c-121">REG\_SZ</span></span>    | <span data-ttu-id="ed70c-122">Uma cadeia de caracteres que contém a descrição do plug-in.</span><span class="sxs-lookup"><span data-stu-id="ed70c-122">A string that contains the description of the plug-in.</span></span> <span data-ttu-id="ed70c-123">O assistente de plug-in cria um recurso de cadeia de caracteres e fornece a URL do recurso (usando o protocolo res) para esse valor.</span><span class="sxs-lookup"><span data-stu-id="ed70c-123">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span>         |
| <span data-ttu-id="ed70c-124">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ed70c-124">FriendlyName</span></span>             | <span data-ttu-id="ed70c-125">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="ed70c-125">REG\_SZ</span></span>    | <span data-ttu-id="ed70c-126">Uma cadeia de caracteres que contém o nome legível pelo usuário para o plug-in.</span><span class="sxs-lookup"><span data-stu-id="ed70c-126">A string that contains the user-readable name for the plug-in.</span></span> <span data-ttu-id="ed70c-127">O assistente de plug-in cria um recurso de cadeia de caracteres e fornece a URL do recurso (usando o protocolo res) para esse valor.</span><span class="sxs-lookup"><span data-stu-id="ed70c-127">The plug-in wizard creates a string resource and provides the URL of the resource (using the res protocol) for this value.</span></span> |
| <span data-ttu-id="ed70c-128">UninstallPath (opcional)</span><span class="sxs-lookup"><span data-stu-id="ed70c-128">UninstallPath (optional)</span></span> | <span data-ttu-id="ed70c-129">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="ed70c-129">REG\_SZ</span></span>    | <span data-ttu-id="ed70c-130">Uma cadeia de caracteres que contém o caminho para um arquivo executável que desinstala o plug-in.</span><span class="sxs-lookup"><span data-stu-id="ed70c-130">A string that contains the path to an executable file that uninstalls the plug-in.</span></span>                                                                                                        |



 

<span data-ttu-id="ed70c-131">Para obter mais informações sobre o protocolo res, consulte o SDK de desenvolvimento da Internet.</span><span class="sxs-lookup"><span data-stu-id="ed70c-131">For more information about the res protocol, see the Internet Development SDK.</span></span>

<span data-ttu-id="ed70c-132">A tabela a seguir detalha os sinalizadores de tipo de plug-in.</span><span class="sxs-lookup"><span data-stu-id="ed70c-132">The following table details the plug-in type flags.</span></span>



| <span data-ttu-id="ed70c-133">Sinalizador de tipo de plug-in</span><span class="sxs-lookup"><span data-stu-id="ed70c-133">Plug-in Type Flag</span></span>                | <span data-ttu-id="ed70c-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ed70c-134">Value</span></span> | <span data-ttu-id="ed70c-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed70c-135">Description</span></span>                                       |
|----------------------------------|-------|---------------------------------------------------|
| <span data-ttu-id="ed70c-136">**plano de fundo do \_ tipo de plugin \_**</span><span class="sxs-lookup"><span data-stu-id="ed70c-136">**PLUGIN\_TYPE\_BACKGROUND**</span></span>     | <span data-ttu-id="ed70c-137">0x1</span><span class="sxs-lookup"><span data-stu-id="ed70c-137">0x1</span></span>   | <span data-ttu-id="ed70c-138">O plug-in da IU não exibe uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="ed70c-138">The UI plug-in does not display a user interface.</span></span> |
| <span data-ttu-id="ed70c-139">**tipo de plug-in \_ \_ SEPARATEWINDOW**</span><span class="sxs-lookup"><span data-stu-id="ed70c-139">**PLUGIN\_TYPE\_SEPARATEWINDOW**</span></span> | <span data-ttu-id="ed70c-140">0x2</span><span class="sxs-lookup"><span data-stu-id="ed70c-140">0x2</span></span>   | <span data-ttu-id="ed70c-141">O plug-in da interface do usuário é um plug-in de janela separado.</span><span class="sxs-lookup"><span data-stu-id="ed70c-141">The UI plug-in is a separate window plug-in.</span></span>      |
| <span data-ttu-id="ed70c-142">**tipo de plug-in \_ \_ DISPLAYAREA**</span><span class="sxs-lookup"><span data-stu-id="ed70c-142">**PLUGIN\_TYPE\_DISPLAYAREA**</span></span>    | <span data-ttu-id="ed70c-143">0x3</span><span class="sxs-lookup"><span data-stu-id="ed70c-143">0x3</span></span>   | <span data-ttu-id="ed70c-144">O plug-in da interface do usuário é um plug-in de área de exibição.</span><span class="sxs-lookup"><span data-stu-id="ed70c-144">The UI plug-in is a display area plug-in.</span></span>         |
| <span data-ttu-id="ed70c-145">**tipo de plug-in \_ \_ SETTINGSAREA**</span><span class="sxs-lookup"><span data-stu-id="ed70c-145">**PLUGIN\_TYPE\_SETTINGSAREA**</span></span>   | <span data-ttu-id="ed70c-146">0x4</span><span class="sxs-lookup"><span data-stu-id="ed70c-146">0x4</span></span>   | <span data-ttu-id="ed70c-147">O plug-in da interface do usuário é um plug-in de área de configurações.</span><span class="sxs-lookup"><span data-stu-id="ed70c-147">The UI plug-in is a settings area plug-in.</span></span>        |
| <span data-ttu-id="ed70c-148">**tipo de plug-in \_ \_ METADATAAREA**</span><span class="sxs-lookup"><span data-stu-id="ed70c-148">**PLUGIN\_TYPE\_METADATAAREA**</span></span>   | <span data-ttu-id="ed70c-149">0x5</span><span class="sxs-lookup"><span data-stu-id="ed70c-149">0x5</span></span>   | <span data-ttu-id="ed70c-150">O plug-in da interface do usuário é um plug-in de área de metadados.</span><span class="sxs-lookup"><span data-stu-id="ed70c-150">The UI plug-in is a metadata area plug-in.</span></span>        |



 

<span data-ttu-id="ed70c-151">A tabela a seguir detalha os sinalizadores de recursos de plug-in.</span><span class="sxs-lookup"><span data-stu-id="ed70c-151">The following table details the plug-in capabilities flags.</span></span>



| <span data-ttu-id="ed70c-152">Sinalizador de recursos de plug-in</span><span class="sxs-lookup"><span data-stu-id="ed70c-152">Plug-in Capabilities Flag</span></span>             | <span data-ttu-id="ed70c-153">Valor</span><span class="sxs-lookup"><span data-stu-id="ed70c-153">Value</span></span>      | <span data-ttu-id="ed70c-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed70c-154">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed70c-155">**sinalizadores de plug-in \_ \_ ACCEPTSMEDIA**</span><span class="sxs-lookup"><span data-stu-id="ed70c-155">**PLUGIN\_FLAGS\_ACCEPTSMEDIA**</span></span>       | <span data-ttu-id="ed70c-156">0x10000000</span><span class="sxs-lookup"><span data-stu-id="ed70c-156">0x10000000</span></span> | <span data-ttu-id="ed70c-157">O plug-in da interface do usuário pode aceitar matrizes de ponteiro de objeto de **mídia** quando o Windows Media Player chama [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="ed70c-157">The UI plug-in can accept **Media** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ed70c-158">**sinalizadores de plug-in \_ \_ ACCEPTSPLAYLISTS**</span><span class="sxs-lookup"><span data-stu-id="ed70c-158">**PLUGIN\_FLAGS\_ACCEPTSPLAYLISTS**</span></span>   | <span data-ttu-id="ed70c-159">0x8000000</span><span class="sxs-lookup"><span data-stu-id="ed70c-159">0x8000000</span></span>  | <span data-ttu-id="ed70c-160">O plug-in da interface do usuário pode aceitar matrizes de ponteiro de objeto de **lista de reprodução** quando o Windows Media Player chama [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span><span class="sxs-lookup"><span data-stu-id="ed70c-160">The UI plug-in can accept **Playlist** object pointer arrays when Windows Media Player calls [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ed70c-161">**sinalizadores de plug-in \_ \_ HASPRESETS**</span><span class="sxs-lookup"><span data-stu-id="ed70c-161">**PLUGIN\_FLAGS\_HASPRESETS**</span></span>         | <span data-ttu-id="ed70c-162">0x4000000</span><span class="sxs-lookup"><span data-stu-id="ed70c-162">0x4000000</span></span>  | <span data-ttu-id="ed70c-163">O plug-in da interface do usuário usa predefinições.</span><span class="sxs-lookup"><span data-stu-id="ed70c-163">The UI plug-in uses presets.</span></span> <span data-ttu-id="ed70c-164">Se o plug-in especificar esse sinalizador, o Windows Media Player consultará o plug-in para obter informações predefinidas chamando [**IWMPPluginUI:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="ed70c-164">If the plug-in specifies this flag, Windows Media Player will query the plug-in for preset information by calling [**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="ed70c-165">**sinalizadores de plug-in \_ \_ HASPROPERTYPAGE**</span><span class="sxs-lookup"><span data-stu-id="ed70c-165">**PLUGIN\_FLAGS\_HASPROPERTYPAGE**</span></span>    | <span data-ttu-id="ed70c-166">0x80000000</span><span class="sxs-lookup"><span data-stu-id="ed70c-166">0x80000000</span></span> | <span data-ttu-id="ed70c-167">O plug-in da interface do usuário fornece uma caixa de diálogo de página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="ed70c-167">The UI plug-in provides a property page dialog.</span></span> <span data-ttu-id="ed70c-168">O Windows Media Player chamará [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) se esse sinalizador for definido quando a página de Propriedades for chamada.</span><span class="sxs-lookup"><span data-stu-id="ed70c-168">Windows Media Player will call [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) if this flag is set when the property page is invoked.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="ed70c-169">**sinalizadores de plug-in \_ \_ ocultos**</span><span class="sxs-lookup"><span data-stu-id="ed70c-169">**PLUGIN\_FLAGS\_HIDDEN**</span></span>             | <span data-ttu-id="ed70c-170">0x02000000</span><span class="sxs-lookup"><span data-stu-id="ed70c-170">0x02000000</span></span> | <span data-ttu-id="ed70c-171">O plug-in da interface do usuário em segundo plano não aparece no menu **plug-ins** que é acessado por meio dos menus **Exibir** ou **ferramentas** ou o botão **selecionar opções em execução** agora está em execução.</span><span class="sxs-lookup"><span data-stu-id="ed70c-171">The background UI plug-in does not appear on the **Plug-ins** menu that is accessed from the **View** or **Tools** menus or the **Select Now Playing options** button in Now Playing.</span></span> <span data-ttu-id="ed70c-172">Ela aparece na guia **plug-ins** da caixa de diálogo opções.</span><span class="sxs-lookup"><span data-stu-id="ed70c-172">It does appear on the **Plug-ins** tab of the Options dialog.</span></span> <span data-ttu-id="ed70c-173">Isso faz com que o ícone de execução de plug-in em segundo plano apareça na barra de status. Esse sinalizador não tem efeito sobre plug-ins diferentes de plug-ins de interface do usuário em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ed70c-173">It does cause the Background Plug-in Running icon to appear in the status bar.This flag has no effect on plug-ins other than background UI plug-ins.</span></span><br/> |
| <span data-ttu-id="ed70c-174">**sinalizadores de plug-in \_ \_ INSTALLAUTORUN**</span><span class="sxs-lookup"><span data-stu-id="ed70c-174">**PLUGIN\_FLAGS\_INSTALLAUTORUN**</span></span>     | <span data-ttu-id="ed70c-175">0x40000000</span><span class="sxs-lookup"><span data-stu-id="ed70c-175">0x40000000</span></span> | <span data-ttu-id="ed70c-176">O Windows Media Player executa o plug-in da interface do usuário automaticamente quando o plug-in é instalado.</span><span class="sxs-lookup"><span data-stu-id="ed70c-176">Windows Media Player runs the UI plug-in automatically when the plug-in is installed.</span></span>                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ed70c-177">**sinalizadores de plug-in \_ \_ LAUNCHPROPERTYPAGE**</span><span class="sxs-lookup"><span data-stu-id="ed70c-177">**PLUGIN\_FLAGS\_LAUNCHPROPERTYPAGE**</span></span> | <span data-ttu-id="ed70c-178">0x20000000</span><span class="sxs-lookup"><span data-stu-id="ed70c-178">0x20000000</span></span> | <span data-ttu-id="ed70c-179">O Windows Media Player chama [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) quando o plug-in da interface do usuário é executado pela primeira vez. Se esse sinalizador for especificado, **os \_ sinalizadores \_ de plug-in HASPROPERTYPAGE** também deverão ser especificados.</span><span class="sxs-lookup"><span data-stu-id="ed70c-179">Windows Media Player calls [**IWMPPluginUI::DisplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) when the UI plug-in runs for the first time.If this flag is specified, **PLUGIN\_FLAGS\_HASPROPERTYPAGE** should be specified also.</span></span><br/>                                                                                                                                                             |



 

<span data-ttu-id="ed70c-180">As constantes a seguir são definidas em wmpplug. h.</span><span class="sxs-lookup"><span data-stu-id="ed70c-180">The following constants are defined in wmpplug.h.</span></span> <span data-ttu-id="ed70c-181">Não altere os valores associados a essas constantes.</span><span class="sxs-lookup"><span data-stu-id="ed70c-181">Do not change the values associated with these constants.</span></span>



| <span data-ttu-id="ed70c-182">Nome</span><span class="sxs-lookup"><span data-stu-id="ed70c-182">Name</span></span>                                    | <span data-ttu-id="ed70c-183">Descrição</span><span class="sxs-lookup"><span data-stu-id="ed70c-183">Description</span></span>                               |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="ed70c-184">**INSTALLREGKEY do plug-in \_**</span><span class="sxs-lookup"><span data-stu-id="ed70c-184">**PLUGIN\_INSTALLREGKEY**</span></span>               | <span data-ttu-id="ed70c-185">O local da chave do registro de plug-in.</span><span class="sxs-lookup"><span data-stu-id="ed70c-185">The location of the plug-in registry key.</span></span> |
| <span data-ttu-id="ed70c-186">**PLUGIN \_ INSTALLREGKEY \_ amigável**</span><span class="sxs-lookup"><span data-stu-id="ed70c-186">**PLUGIN\_INSTALLREGKEY\_FRIENDLYNAME**</span></span> | <span data-ttu-id="ed70c-187">O nome do valor de nome amigável.</span><span class="sxs-lookup"><span data-stu-id="ed70c-187">The name of the friendly name value.</span></span>      |
| <span data-ttu-id="ed70c-188">**Descrição do plug-in \_ INSTALLREGKEY \_**</span><span class="sxs-lookup"><span data-stu-id="ed70c-188">**PLUGIN\_INSTALLREGKEY\_DESCRIPTION**</span></span>  | <span data-ttu-id="ed70c-189">O nome do valor da descrição.</span><span class="sxs-lookup"><span data-stu-id="ed70c-189">The name of the description value.</span></span>        |
| <span data-ttu-id="ed70c-190">**\_recursos de INSTALLREGKEY do plug-in \_**</span><span class="sxs-lookup"><span data-stu-id="ed70c-190">**PLUGIN\_INSTALLREGKEY\_CAPABILITIES**</span></span> | <span data-ttu-id="ed70c-191">O nome do valor de recursos.</span><span class="sxs-lookup"><span data-stu-id="ed70c-191">The name of the capabilities value.</span></span>       |
| <span data-ttu-id="ed70c-192">**desinstalação do PLUGIN \_ INSTALLREGKEY \_**</span><span class="sxs-lookup"><span data-stu-id="ed70c-192">**PLUGIN\_INSTALLREGKEY\_UNINSTALL**</span></span>    | <span data-ttu-id="ed70c-193">O nome do valor do caminho de desinstalação.</span><span class="sxs-lookup"><span data-stu-id="ed70c-193">The name of the uninstall path value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="ed70c-194">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed70c-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed70c-195">**IWMPPluginUI::D isplayPropertyPage**</span><span class="sxs-lookup"><span data-stu-id="ed70c-195">**IWMPPluginUI::DisplayPropertyPage**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[<span data-ttu-id="ed70c-196">**IWMPPluginUI:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="ed70c-196">**IWMPPluginUI::GetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[<span data-ttu-id="ed70c-197">**IWMPPluginUI:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="ed70c-197">**IWMPPluginUI::SetProperty**</span></span>](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[<span data-ttu-id="ed70c-198">**Referência de programação de plug-ins de interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="ed70c-198">**User Interface Plug-ins Programming Reference**</span></span>](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





