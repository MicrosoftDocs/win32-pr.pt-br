---
title: Registrando plug-ins do DSP
description: Registrando plug-ins do DSP
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Plug-ins do Windows Media Player, entradas do registro
- plug-ins, entradas do registro
- plug-ins de processamento de sinal digital, entradas de registro
- Plug-ins do DSP, entradas do registro
- registro, plug-ins do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916997"
---
# <a name="registering-dsp-plug-ins"></a><span data-ttu-id="03861-108">Registrando plug-ins do DSP</span><span class="sxs-lookup"><span data-stu-id="03861-108">Registering DSP Plug-ins</span></span>

<span data-ttu-id="03861-109">Para disponibilizar seu plug-in do DSP no Windows Media Player, você deve criar as seguintes subchaves e entradas do registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="03861-109">To make your DSP plug-in available in Windows Media Player you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



<span data-ttu-id="03861-110">Na sintaxe de registro anterior, os símbolos em itálico são espaços reservados para nomes e identificadores globalmente exclusivos (GUIDs) que são específicos para o plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="03861-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="03861-111">A tabela a seguir descreve esses espaços reservados.</span><span class="sxs-lookup"><span data-stu-id="03861-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="03861-112">Espaço reservado</span><span class="sxs-lookup"><span data-stu-id="03861-112">Placeholder</span></span>               | <span data-ttu-id="03861-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="03861-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03861-114">*PluginClsid*</span><span class="sxs-lookup"><span data-stu-id="03861-114">*PluginClsid*</span></span>             | <span data-ttu-id="03861-115">Um GUID que é o identificador de classe para a classe principal do plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="03861-115">A GUID that is the class identifier for the DSP plug-in's primary class.</span></span> <span data-ttu-id="03861-116">Essa é a classe que implementa **IMediaObject**, **IPluginEnable** e possivelmente **ISpecifyPropertyPages**.</span><span class="sxs-lookup"><span data-stu-id="03861-116">This is the class that implements **IMediaObject**, **IPluginEnable**, and possibly **ISpecifyPropertyPages**.</span></span> <span data-ttu-id="03861-117">Em um plug-in de modo duplo, essa classe também implementa **IMFTransform** e **IMFGetService**. Esse GUID deve estar no formato de registro, completo com as chaves.</span><span class="sxs-lookup"><span data-stu-id="03861-117">In a dual-mode plug-in, this class also implements **IMFTransform** and **IMFGetService**.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="03861-118">Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="03861-118">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="03861-119">*PluginClassFriendlyName*</span><span class="sxs-lookup"><span data-stu-id="03861-119">*PluginClassFriendlyName*</span></span> | <span data-ttu-id="03861-120">Um nome amigável para a classe principal do plug-in do DSP. Exemplo: "classe ProsewareDSP"</span><span class="sxs-lookup"><span data-stu-id="03861-120">A friendly name for the DSP plug-in's primary class.Example: "ProsewareDSP Class"</span></span><br/>                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="03861-121">*PluginModuleName*</span><span class="sxs-lookup"><span data-stu-id="03861-121">*PluginModuleName*</span></span>        | <span data-ttu-id="03861-122">O caminho totalmente qualificado para a DLL que implementa o plug-in do DSP. Exemplo: "C: \\ arquivos de programa \\ Proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="03861-122">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="03861-123">*Threading*</span><span class="sxs-lookup"><span data-stu-id="03861-123">*Threading*</span></span>               | <span data-ttu-id="03861-124">Uma cadeia de caracteres que especifica o modelo de threading para o plug-in.</span><span class="sxs-lookup"><span data-stu-id="03861-124">A string that specifies the threading model for the plug-in.</span></span> <span data-ttu-id="03861-125">Se o plug-in for executado com o Windows Media Player 11 no Windows Vista, essa entrada de registro deverá ser igual a "both".</span><span class="sxs-lookup"><span data-stu-id="03861-125">If the plug-in is going to run with Windows Media Player 11 on Windows Vista, this registry entry must be equal to "Both".</span></span> <span data-ttu-id="03861-126">Se o plug-in for executado no Windows XP ou em sistemas operacionais mais antigos, essa entrada de registro poderá ser igual a "Apartment" ou "both".</span><span class="sxs-lookup"><span data-stu-id="03861-126">If the plug-in is going to run on Windows XP or older operating systems, this registry entry can be equal to either "Apartment" or "Both".</span></span>                                                                                           |



 

<span data-ttu-id="03861-127">Se o seu plug-in do DSP implementar uma interface personalizada e se o seu plug-in for executado no Windows Media Player 11 no Windows Vista, você deverá criar as seguintes subchaves e entradas do registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="03861-127">If your DSP plug-in implements a custom interface and if your plug-in is going to run in Windows Media Player 11 on Windows Vista, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



<span data-ttu-id="03861-128">Na sintaxe de registro anterior, os símbolos em itálico são espaços reservados para nomes, valores numéricos e identificadores globalmente exclusivos (GUIDs) que são específicos para o plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="03861-128">In the preceding registry syntax, the symbols in italic are placeholders for names, numeric values, and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="03861-129">A tabela a seguir descreve esses espaços reservados.</span><span class="sxs-lookup"><span data-stu-id="03861-129">The following table describes those placeholders.</span></span>



| <span data-ttu-id="03861-130">Espaço reservado</span><span class="sxs-lookup"><span data-stu-id="03861-130">Placeholder</span></span>           | <span data-ttu-id="03861-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="03861-131">Description</span></span>                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03861-132">*ProxyStubClsid*</span><span class="sxs-lookup"><span data-stu-id="03861-132">*ProxyStubClsid*</span></span>      | <span data-ttu-id="03861-133">Um GUID que é o identificador de classe da classe que implementa os proxies e os stubs para as interfaces personalizadas do plug-in do DSP. Esse GUID deve estar no formato de registro, completo com as chaves.</span><span class="sxs-lookup"><span data-stu-id="03861-133">A GUID that is the class identifier for the class that implements the proxies and stubs for the DSP plug-in's custom interfaces.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="03861-134">Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="03861-134">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="03861-135">*ProxyStubModuleName*</span><span class="sxs-lookup"><span data-stu-id="03861-135">*ProxyStubModuleName*</span></span> | <span data-ttu-id="03861-136">O caminho totalmente qualificado para a DLL que implementa as interfaces de proxy e stub para o plug-in do DSP. Exemplo: "C: \\ arquivos de programa \\ Proseware \\ProsewareDspPS.dll"</span><span class="sxs-lookup"><span data-stu-id="03861-136">The fully qualified path to the DLL that implements the proxy and stub interfaces for the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDspPS.dll"</span></span><br/>                                                                                               |
| <span data-ttu-id="03861-137">*CustomInterfaceId*</span><span class="sxs-lookup"><span data-stu-id="03861-137">*CustomInterfaceId*</span></span>   | <span data-ttu-id="03861-138">Um GUID que é o identificador de interface para uma interface personalizada que é implementada pelo plug-in do DSP. Esse GUID deve estar no formato de registro, completo com as chaves.</span><span class="sxs-lookup"><span data-stu-id="03861-138">A GUID that is the interface identifier for a custom interface that is implemented by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="03861-139">Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="03861-139">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                           |
| <span data-ttu-id="03861-140">*CustomInterfaceName*</span><span class="sxs-lookup"><span data-stu-id="03861-140">*CustomInterfaceName*</span></span> | <span data-ttu-id="03861-141">O nome de uma interface personalizada que é implementada pelo plug-in do DSP. Exemplo: "IProsewareDsp"</span><span class="sxs-lookup"><span data-stu-id="03861-141">The name of a custom interface that is implemented by the DSP plug-in.Example: "IProsewareDsp"</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="03861-142">*NumberOfMethods*</span><span class="sxs-lookup"><span data-stu-id="03861-142">*NumberOfMethods*</span></span>     | <span data-ttu-id="03861-143">O número de métodos, incluindo os métodos herdados, definidos por uma interface personalizada. Exemplo: "5"</span><span class="sxs-lookup"><span data-stu-id="03861-143">The number of methods, including inherited methods, defined by a custom interface.Example: "5"</span></span><br/>                                                                                                                                                                  |



 

<span data-ttu-id="03861-144">Se o plug-in do DSP fornecer uma página de propriedades, você deverá criar as seguintes subchaves e entradas do registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="03861-144">If your DSP plug-in provides a property page, you must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="03861-145">Na sintaxe de registro anterior, os símbolos em itálico são espaços reservados para nomes e identificadores globalmente exclusivos (GUIDs) que são específicos para o plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="03861-145">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the DSP plug-in.</span></span> <span data-ttu-id="03861-146">A tabela a seguir descreve esses espaços reservados.</span><span class="sxs-lookup"><span data-stu-id="03861-146">The following table describes those placeholders.</span></span>



| <span data-ttu-id="03861-147">Espaço reservado</span><span class="sxs-lookup"><span data-stu-id="03861-147">Placeholder</span></span>                 | <span data-ttu-id="03861-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="03861-148">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03861-149">*PropPageClsid*</span><span class="sxs-lookup"><span data-stu-id="03861-149">*PropPageClsid*</span></span>             | <span data-ttu-id="03861-150">Um GUID que é o identificador de classe para a classe de página de propriedades fornecida pelo plug-in DSP. Esse GUID deve estar no formato de registro, completo com as chaves.</span><span class="sxs-lookup"><span data-stu-id="03861-150">A GUID that is the class identifier for the property page class provided by the DSP plug-in.This GUID must be in registry format, complete with the curly braces.</span></span><br/> <span data-ttu-id="03861-151">Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="03861-151">Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/> |
| <span data-ttu-id="03861-152">*PropPageClassFriendlyName*</span><span class="sxs-lookup"><span data-stu-id="03861-152">*PropPageClassFriendlyName*</span></span> | <span data-ttu-id="03861-153">Um nome amigável para a classe da página de propriedades. Exemplo: "classe de página da propriedade ProsewareDSP"</span><span class="sxs-lookup"><span data-stu-id="03861-153">A friendly name for the property page class.Example: "ProsewareDSP Property Page Class"</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="03861-154">*PluginModuleName*</span><span class="sxs-lookup"><span data-stu-id="03861-154">*PluginModuleName*</span></span>          | <span data-ttu-id="03861-155">O caminho totalmente qualificado para a DLL que implementa o plug-in do DSP. Exemplo: "C: \\ arquivos de programa \\ Proseware \\ProsewareDsp.dll"</span><span class="sxs-lookup"><span data-stu-id="03861-155">The fully qualified path to the DLL that implements the DSP plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareDsp.dll"</span></span><br/>                                                                                               |



 

<span data-ttu-id="03861-156">**Chamando IWMPPluginRegistrar**</span><span class="sxs-lookup"><span data-stu-id="03861-156">**Calling IWMPPluginRegistrar**</span></span>

<span data-ttu-id="03861-157">Além das entradas e das subchaves do Registro descritas nas listas e tabelas anteriores, você deve criar algumas chaves e entradas do registro chamando [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span><span class="sxs-lookup"><span data-stu-id="03861-157">In addition to the registry subkeys and entries described in the preceding lists and tables, you must create some registry keys and entries by calling [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin).</span></span> <span data-ttu-id="03861-158">Esse método executa o registro necessário para habilitar o Windows Media Player a reconhecer seu plug-in e apresentá-lo como uma opção para o usuário.</span><span class="sxs-lookup"><span data-stu-id="03861-158">This method performs the necessary registration to enable Windows Media Player to recognize your plug-in and present it as an option to the user.</span></span>

<span data-ttu-id="03861-159">Chame **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** na função **DllRegisterServer** de seu plug-in e chame [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) na função **DllUnregisterServer** do seu plug-in.</span><span class="sxs-lookup"><span data-stu-id="03861-159">Call **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** in your plug-in's **DllRegisterServer** function, and call [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) in your plug-in's **DllUnregisterServer** function.</span></span> <span data-ttu-id="03861-160">Para obter um ponteiro para uma interface **IWMPMediaPluginRegistrar** , chame **COCREATEINSTANCE**, passando CLSID \_ WMPMediaPluginRegistrar como a ID de classe.</span><span class="sxs-lookup"><span data-stu-id="03861-160">To get a pointer to an **IWMPMediaPluginRegistrar** interface, call **CoCreateInstance**, passing CLSID\_WMPMediaPluginRegistrar as the Class ID.</span></span> <span data-ttu-id="03861-161">A constante CLSID \_ WMPMediaPluginRegistrar é definida em wmpservices. h.</span><span class="sxs-lookup"><span data-stu-id="03861-161">The constant CLSID\_WMPMediaPluginRegistrar is defined in wmpservices.h.</span></span>

<span data-ttu-id="03861-162">**Registro no assistente de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="03861-162">**Registration in the DSP Plug-in Wizard**</span></span>

<span data-ttu-id="03861-163">O assistente de plug-in do DSP, que está incluído na SDK do Windows, gera um código de exemplo baseado em Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="03861-163">The DSP plug-in wizard, which is included in the Windows SDK, generates sample code that is based on Active Template Library (ATL).</span></span> <span data-ttu-id="03861-164">A função **DllRegisterServer** do plug-in de exemplo chama a função **RegisterServer** da ATL, que cria subchaves e entradas do registro de acordo com dois arquivos de script do registro no projeto do Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="03861-164">The sample plug-in's **DllRegisterServer** function calls ATL's **RegisterServer** function, which creates registry subkeys and entries according to two registry script files in the Visual Studio project.</span></span> <span data-ttu-id="03861-165">O arquivo *ProjectName*. RGS contém o script para registrar a classe principal do plug-in e o arquivo *ProjectName* PropPage. RGS contém o script para registrar a classe da página de propriedades do plug-in.</span><span class="sxs-lookup"><span data-stu-id="03861-165">The file *ProjectName*.rgs contains the script for registering the plug-in's main class, and the file *ProjectName* PropPage.rgs contains the script for registering the plug-in's property page class.</span></span> <span data-ttu-id="03861-166">A função **DllRegisterServer** do plug-in de exemplo também chama **IWMPPluginRegistrar:: WMPRegisterPlayerPlugin**.</span><span class="sxs-lookup"><span data-stu-id="03861-166">The sample plug-in's **DllRegisterServer** function also calls **IWMPPluginRegistrar::WMPRegisterPlayerPlugin**.</span></span>

<span data-ttu-id="03861-167">O assistente de plug-in do DSP também gera código para um componente de stub de proxy que é um arquivo. dll de registro automático.</span><span class="sxs-lookup"><span data-stu-id="03861-167">The DSP plug-in wizard also generates code for a proxy-stub component that is a self-registering .dll file.</span></span> <span data-ttu-id="03861-168">O código de registro para esse arquivo está em dlldata. cpp.</span><span class="sxs-lookup"><span data-stu-id="03861-168">The registration code for that file is in dlldata.cpp.</span></span> <span data-ttu-id="03861-169">As **\_ rotinas de dlldata** de macros se expandem para incluir uma implementação de **DllRegisterServer**.</span><span class="sxs-lookup"><span data-stu-id="03861-169">The macro **DLLDATA\_ROUTINES** expands to include an implementation of **DllRegisterServer**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03861-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03861-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03861-171">**Visão geral do desenvolvedor de plug-in do DSP**</span><span class="sxs-lookup"><span data-stu-id="03861-171">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="03861-172">**IWMPMediaPluginRegistrar**</span><span class="sxs-lookup"><span data-stu-id="03861-172">**IWMPMediaPluginRegistrar**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





