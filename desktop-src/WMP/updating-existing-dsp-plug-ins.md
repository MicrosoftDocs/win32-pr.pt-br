---
title: Atualizando plug-ins de DSP existentes
description: Atualizando plug-ins de DSP existentes
ms.assetid: 0525030e-eb30-41a0-8191-4a5727736857
keywords:
- Plug-ins do Windows Media Player, processamento de sinal digital (DSP)
- plug-ins, processamento de sinal digital (DSP)
- plug-ins de processamento de sinal digital, atualizando
- Plug-ins do DSP, atualizando
- versões do Windows Media Player, plug-ins do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393cde356e0d86bb920825e731bb12ee0b7c2818
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640139"
---
# <a name="updating-existing-dsp-plug-ins"></a><span data-ttu-id="e9588-108">Atualizando plug-ins de DSP existentes</span><span class="sxs-lookup"><span data-stu-id="e9588-108">Updating Existing DSP Plug-ins</span></span>

<span data-ttu-id="e9588-109">Plug-ins do DSP criados antes do lançamento do SDK do Windows Media Player 11 podem não funcionar conforme o esperado com o Windows Media Player 11 em execução no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e9588-109">DSP plug-ins created before the release of the Windows Media Player 11 SDK might not work as expected with Windows Media Player 11 running on Windows Vista.</span></span> <span data-ttu-id="e9588-110">Para garantir que os clientes que executam o Windows Media Player 11 no Windows Vista possam usar seus plug-ins, você deve fazer algumas alterações no código do plug-in do DSP, recompilar seu projeto e distribuir o plug-in atualizado para seus clientes.</span><span class="sxs-lookup"><span data-stu-id="e9588-110">To ensure that customers who run Windows Media Player 11 on Windows Vista can use your plug-ins, you must make some changes to your DSP plug-in code, recompile your project, and distribute the updated plug-in to your customers.</span></span>

<span data-ttu-id="e9588-111">Os projetos criados com a versão mais recente do assistente de plug-in do Windows Media Player conterão as atualizações necessárias.</span><span class="sxs-lookup"><span data-stu-id="e9588-111">Projects created using the latest version of the Windows Media Player plug-in wizard will contain the required updates.</span></span> <span data-ttu-id="e9588-112">Consulte [atualizações para o assistente de plug-in do DSP para Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span><span class="sxs-lookup"><span data-stu-id="e9588-112">See [Updates to the DSP Plug-in Wizard for Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).</span></span> <span data-ttu-id="e9588-113">(É uma boa ideia executar o assistente para criar um novo projeto de exemplo e, em seguida, usar uma ferramenta como Windiff.exe, que vem com o Visual Studio, para inspecionar as diferenças entre o código de exemplo e o código de produção).</span><span class="sxs-lookup"><span data-stu-id="e9588-113">(It is a good idea to run the wizard to create a new sample project and then use a tool like Windiff.exe, which comes with Visual Studio, to inspect the differences between the sample code and your production code.)</span></span>

<span data-ttu-id="e9588-114">Há três alterações principais que você precisará fazer em qualquer plug-in de DSP existente:</span><span class="sxs-lookup"><span data-stu-id="e9588-114">There are three main changes you will need to make to any existing DSP plug-ins:</span></span>

-   <span data-ttu-id="e9588-115">Altere a maneira como o plug-in registra.</span><span class="sxs-lookup"><span data-stu-id="e9588-115">Change the way the plug-in registers.</span></span> <span data-ttu-id="e9588-116">Seu plug-in existente provavelmente registrará o modelo de Threading como "Apartment".</span><span class="sxs-lookup"><span data-stu-id="e9588-116">Your existing plug-in probably registers the threading model as "Apartment".</span></span> <span data-ttu-id="e9588-117">O Windows Media Player 11 em execução no Windows Vista exige que plug-ins do DSP registrem o modelo de Threading como "ambos".</span><span class="sxs-lookup"><span data-stu-id="e9588-117">Windows Media Player 11 running on Windows Vista requires that DSP plug-ins register the threading model as "Both".</span></span> <span data-ttu-id="e9588-118">Você pode corrigir isso alterando o valor do modelo de threading no arquivo *ProjectName*. rgs, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e9588-118">You can fix this by changing the threading model value in your *projectname*.rgs file, as follows:</span></span>

    ```C++
    val ThreadingModel = s 'Both'
    
    ```

    

    > [!Note]  
    > <span data-ttu-id="e9588-119">Especificar o modelo de Threading como "both" remove qualquer serialização que o COM forneça para chamadas para interfaces personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e9588-119">Specifying the threading model as "Both" removes any serialization that COM provides for calls to custom interfaces.</span></span> <span data-ttu-id="e9588-120">Se você fizer chamadas para suas interfaces personalizadas de vários threads, deverá fornecer essa serialização por conta própria.</span><span class="sxs-lookup"><span data-stu-id="e9588-120">If you make calls to your custom interfaces from multiple threads, you must provide this serialization yourself.</span></span>

     

    <span data-ttu-id="e9588-121">O Windows Media Player 11 garante que as chamadas para interfaces DMO sejam serializadas corretamente.</span><span class="sxs-lookup"><span data-stu-id="e9588-121">Windows Media Player 11 ensures that calls to DMO interfaces are properly serialized.</span></span>

    1.  <span data-ttu-id="e9588-122">Adicionar chamadas a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) e [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) com um novo tipo de plug-in: WMP \_ plugintype \_ DSP \_ OUTOFPROC em DllRegisterServer e DllUnregisterServer no seu arquivo *projectnamedll*. cpp.</span><span class="sxs-lookup"><span data-stu-id="e9588-122">Add calls to [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) and [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) with a new plug-in type: WMP\_PLUGINTYPE\_DSP\_OUTOFPROC in DllRegisterServer and DllUnregisterServer in your *projectnamedll*.cpp file.</span></span> <span data-ttu-id="e9588-123">Consulte as páginas de referência para esses métodos para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="e9588-123">See the reference pages for these methods for details.</span></span>
    2.  <span data-ttu-id="e9588-124">Crie e distribua uma DLL de proxy/stub para habilitar o marshaling COM de qualquer interface personalizada implementada ou criada pela classe de plug-in.</span><span class="sxs-lookup"><span data-stu-id="e9588-124">Create and distribute a proxy/stub DLL to enable COM marshaling of any custom interface implemented on or created by the plug-in class.</span></span> <span data-ttu-id="e9588-125">Uma interface personalizada é qualquer interface proprietária que você define e implementa para uso pelo objeto de plug-in.</span><span class="sxs-lookup"><span data-stu-id="e9588-125">A custom interface is any proprietary interface that you define and implement for use by the plug-in object.</span></span> <span data-ttu-id="e9588-126">Isso inclui a interface personalizada usada por sua página de propriedades, se você tiver fornecido uma, mas também pode incluir interfaces que se conectam a plug-ins de interface do usuário, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="e9588-126">This includes the custom interface used by your property page, if you provided one, but might also include interfaces that connect to UI plug-ins, for example.</span></span> <span data-ttu-id="e9588-127">Um exemplo de interface personalizada criada pelo assistente de plug-in é *Iprojectname*.</span><span class="sxs-lookup"><span data-stu-id="e9588-127">An example of a custom interface created by the plug-in wizard is *Iprojectname*.</span></span> <span data-ttu-id="e9588-128">Exemplos de interfaces que não são interfaces personalizadas incluem **IMediaObject** e **IWMPPluginEnable**.</span><span class="sxs-lookup"><span data-stu-id="e9588-128">Examples of interfaces that are not custom interfaces include **IMediaObject** and **IWMPPluginEnable**.</span></span>

<span data-ttu-id="e9588-129">Se o plug-in do DSP processar áudio, você também deverá adicionar suporte para os seguintes novos formatos de áudio:</span><span class="sxs-lookup"><span data-stu-id="e9588-129">If your DSP plug-in processes audio, you must also add support for the following new audio formats:</span></span>

-   <span data-ttu-id="e9588-130">\_formato Wave \_ IEEE \_ float</span><span class="sxs-lookup"><span data-stu-id="e9588-130">WAVE\_FORMAT\_IEEE\_FLOAT</span></span>
-   <span data-ttu-id="e9588-131">\_Formato Wave \_ extensível com SUBformato KSDATAFORMAT \_ subtipo \_ IEEE \_ float.</span><span class="sxs-lookup"><span data-stu-id="e9588-131">WAVE\_FORMAT\_EXTENSIBLE with subformat KSDATAFORMAT\_SUBTYPE\_IEEE\_FLOAT.</span></span>

<span data-ttu-id="e9588-132">Se o plug-in do DSP processar vídeo, você deverá adicionar suporte para o formato de vídeo NV12.</span><span class="sxs-lookup"><span data-stu-id="e9588-132">If your DSP plug-in processes video, you must add support for the NV12 video format.</span></span>

<span data-ttu-id="e9588-133">Consulte o plug-in de exemplo de áudio ou vídeo DSP que o assistente cria para obter um exemplo de como processar esses tipos de formato.</span><span class="sxs-lookup"><span data-stu-id="e9588-133">See the sample audio or video DSP plug-in that the wizard creates for an example of how to process these format types.</span></span>

## <a name="about-the-proxystub-project"></a><span data-ttu-id="e9588-134">Sobre o projeto de proxy/stub</span><span class="sxs-lookup"><span data-stu-id="e9588-134">About the Proxy/Stub Project</span></span>

<span data-ttu-id="e9588-135">Talvez a maneira mais simples de criar um projeto de DLL de proxy/stub para seu plug-in do DSP seja executar o assistente de plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="e9588-135">Perhaps the simplest way to create a proxy/stub DLL project for your DSP plug-in is to run the DSP plug-in wizard.</span></span> <span data-ttu-id="e9588-136">Isso criará um exemplo de projeto de proxy/stub que você pode modificar para trabalhar com seu código existente.</span><span class="sxs-lookup"><span data-stu-id="e9588-136">This will create a sample proxy/stub project that you can modify to work with your existing code.</span></span> <span data-ttu-id="e9588-137">Você precisará fazer as seguintes alterações:</span><span class="sxs-lookup"><span data-stu-id="e9588-137">You will need to make the following changes:</span></span>

1.  <span data-ttu-id="e9588-138">Remova todas as definições existentes para suas interfaces personalizadas do seu código.</span><span class="sxs-lookup"><span data-stu-id="e9588-138">Remove any existing definitions for your custom interfaces from your code.</span></span> <span data-ttu-id="e9588-139">Por exemplo, o assistente de plug-in do DSP do SDK do Windows Media Player 10 criou a definição da interface *Iprojectname* no arquivo *ProjectName*. h usando a palavra-chave **interface** .</span><span class="sxs-lookup"><span data-stu-id="e9588-139">For example, the DSP plug-in wizard from the Windows Media Player 10 SDK created the *Iprojectname* interface definition in the *projectname*.h file by using the **interface** keyword.</span></span>
2.  <span data-ttu-id="e9588-140">Defina suas interfaces personalizadas no arquivo IDL do projeto de proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="e9588-140">Define your custom interfaces in the proxy/stub project's IDL file.</span></span>
3.  <span data-ttu-id="e9588-141">Crie o projeto de proxy/stub antes do projeto principal.</span><span class="sxs-lookup"><span data-stu-id="e9588-141">Build the proxy/stub project before your main project.</span></span> <span data-ttu-id="e9588-142">Você pode configurar o Visual Studio para fazer isso automaticamente se ambos os projetos fizerem parte da mesma solução.</span><span class="sxs-lookup"><span data-stu-id="e9588-142">You can configure Visual Studio to do this automatically if both projects are part of the same solution.</span></span>
4.  <span data-ttu-id="e9588-143">O compilador MIDL criará um novo arquivo de cabeçalho com um nome no formato *ProjectName* \_ h.h.</span><span class="sxs-lookup"><span data-stu-id="e9588-143">The MIDL compiler will create a new header file having a name in the format *projectname*\_h.h.</span></span> <span data-ttu-id="e9588-144">Você deve incluir esse cabeçalho em seu projeto principal (no *ProjectName*. h).</span><span class="sxs-lookup"><span data-stu-id="e9588-144">You must include this header in your main project (in *projectname*.h).</span></span> <span data-ttu-id="e9588-145">Ele contém as definições para suas interfaces personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e9588-145">It contains the definitions for your custom interfaces.</span></span>

## <a name="distributing-the-updated-plug-in"></a><span data-ttu-id="e9588-146">Distribuindo o plug-in atualizado</span><span class="sxs-lookup"><span data-stu-id="e9588-146">Distributing the Updated Plug-in</span></span>

<span data-ttu-id="e9588-147">Você pode instalar o plug-in atualizado nos computadores dos usuários exatamente como no passado.</span><span class="sxs-lookup"><span data-stu-id="e9588-147">You can install the updated plug-in on your users' computers exactly as you have in the past.</span></span> <span data-ttu-id="e9588-148">No entanto, agora você também deve distribuir e registrar a DLL de proxy/stub.</span><span class="sxs-lookup"><span data-stu-id="e9588-148">However, you must now also distribute and register the proxy/stub DLL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9588-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9588-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9588-150">**Visão geral do desenvolvedor de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="e9588-150">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




