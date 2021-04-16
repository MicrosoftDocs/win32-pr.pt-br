---
title: Chaves e entradas do registro para uma loja online tipo 1
description: Chaves e entradas do registro para uma loja online tipo 1
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Armazenamentos online do Windows Media Player, registro
- lojas online, registro
- tipo 1 lojas online, registro
- registro, tipo 1 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105761434"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a><span data-ttu-id="dd980-107">Chaves e entradas do registro para uma loja online tipo 1</span><span class="sxs-lookup"><span data-stu-id="dd980-107">Registry Keys and Entries for a Type 1 Online Store</span></span>

<span data-ttu-id="dd980-108">Para tornar um repositório online tipo 1 disponível no Windows Media Player, o provedor de loja online deve criar as seguintes subchaves e entradas do registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="dd980-108">To make a type 1 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> <span data-ttu-id="dd980-109">Definir o valor de DllSurrogate como a cadeia de caracteres vazia indica que o tempo de execução COM carregará o plug-in da loja online na DLL padrão como alternativa, dllhost.exe.</span><span class="sxs-lookup"><span data-stu-id="dd980-109">Setting the value of DllSurrogate to the empty string indicates that the COM runtime will load the online store's plug-in into the default DLL surrogate, dllhost.exe.</span></span>

 

<span data-ttu-id="dd980-110">Na sintaxe de registro anterior, os símbolos em itálico são espaços reservados para nomes e identificadores globalmente exclusivos (GUIDs) que são específicos para a loja online.</span><span class="sxs-lookup"><span data-stu-id="dd980-110">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="dd980-111">A tabela a seguir descreve esses espaços reservados.</span><span class="sxs-lookup"><span data-stu-id="dd980-111">The following table describes those placeholders.</span></span>



| <span data-ttu-id="dd980-112">Espaço reservado</span><span class="sxs-lookup"><span data-stu-id="dd980-112">Placeholder</span></span>    | <span data-ttu-id="dd980-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd980-113">Description</span></span>                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd980-114">*keyName*</span><span class="sxs-lookup"><span data-stu-id="dd980-114">*keyName*</span></span>      | <span data-ttu-id="dd980-115">Uma cadeia de caracteres acordada entre a Microsoft e a loja online.</span><span class="sxs-lookup"><span data-stu-id="dd980-115">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="dd980-116">Essa cadeia de caracteres identifica exclusivamente o repositório online. Exemplo: "Proseware"</span><span class="sxs-lookup"><span data-stu-id="dd980-116">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                   |
| <span data-ttu-id="dd980-117">*sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="dd980-117">*flags*</span></span>        | <span data-ttu-id="dd980-118">Um ou **mais bits de** capacidade de plug-in de um ou mais sinalizadores especificam se o Windows Media Player deve chamar métodos específicos de [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span><span class="sxs-lookup"><span data-stu-id="dd980-118">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner).</span></span> <span data-ttu-id="dd980-119">Para obter informações sobre sinalizadores com suporte, consulte a tabela de sinalizadores de recurso de plug-in que segue esta tabela. Exemplo: 00000058</span><span class="sxs-lookup"><span data-stu-id="dd980-119">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000058</span></span><br/> |
| <span data-ttu-id="dd980-120">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="dd980-120">*clsid*</span></span>        | <span data-ttu-id="dd980-121">Um GUID que é o identificador de classe (CLSID) para a classe que implementa **IWMPContentPartner** no plug-in da loja online.</span><span class="sxs-lookup"><span data-stu-id="dd980-121">A GUID that is the class identifier (CLSID) for the class that implements **IWMPContentPartner** in the online store's plug-in.</span></span> <span data-ttu-id="dd980-122">Esse GUID deve estar no formato de registro, completo com as chaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="dd980-122">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                  |
| <span data-ttu-id="dd980-123">*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="dd980-123">*friendlyname*</span></span> | <span data-ttu-id="dd980-124">Um nome amigável para a loja online. Exemplo: "serviço de música da Proseware"</span><span class="sxs-lookup"><span data-stu-id="dd980-124">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="dd980-125">*appid*</span><span class="sxs-lookup"><span data-stu-id="dd980-125">*appid*</span></span>        | <span data-ttu-id="dd980-126">Um GUID que é o identificador de aplicativo (AppID) para o plug-in da loja online.</span><span class="sxs-lookup"><span data-stu-id="dd980-126">A GUID that is the application identifier (AppID) for the online store's plug-in.</span></span> <span data-ttu-id="dd980-127">Esse GUID deve estar no formato de registro, completo com as chaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="dd980-127">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                |
| <span data-ttu-id="dd980-128">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="dd980-128">*pluginName*</span></span>   | <span data-ttu-id="dd980-129">Um nome para o plug-in da loja online. Exemplo: "plug-in de parceiro de conteúdo da Proseware"</span><span class="sxs-lookup"><span data-stu-id="dd980-129">A name for the online store's plug-in.Example: "Proseware Content Partner Plug-in"</span></span><br/>                                                                                                                                                                                                                                   |
| <span data-ttu-id="dd980-130">*className*</span><span class="sxs-lookup"><span data-stu-id="dd980-130">*className*</span></span>    | <span data-ttu-id="dd980-131">O nome da classe que implementa **IWMPContentpartner** no plug-in da loja online. Exemplo: "CProsewarePartner"</span><span class="sxs-lookup"><span data-stu-id="dd980-131">The name of the class that implements **IWMPContentpartner** in the online store's plug-in.Example: "CProsewarePartner"</span></span><br/>                                                                                                                                                                                              |
| <span data-ttu-id="dd980-132">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="dd980-132">*moduleName*</span></span>   | <span data-ttu-id="dd980-133">O caminho totalmente qualificado para a DLL que implementa o plug-in da loja online. Exemplo: "C: \\ arquivos de programa \\ Proseware \\ProsewarePartner.dll"</span><span class="sxs-lookup"><span data-stu-id="dd980-133">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewarePartner.dll"</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="dd980-134">*Threading*</span><span class="sxs-lookup"><span data-stu-id="dd980-134">*threading*</span></span>    | <span data-ttu-id="dd980-135">O tipo de compartimento em que o plug-in é executado.</span><span class="sxs-lookup"><span data-stu-id="dd980-135">The type of apartment the plug-in runs in.</span></span> <span data-ttu-id="dd980-136">"ThreadingModel" = "Apartment" indica que o plug-in é executado em um STA (single-threaded apartment).</span><span class="sxs-lookup"><span data-stu-id="dd980-136">"ThreadingModel"="Apartment" indicates that the plug-in runs in a single-threaded apartment (STA).</span></span> <span data-ttu-id="dd980-137">"ThreadingModel" = "Free" indica que o plug-in é executado no MTA (multithreaded apartment).</span><span class="sxs-lookup"><span data-stu-id="dd980-137">"ThreadingModel"="Free" indicates that the plug-in runs in the multithreaded apartment (MTA).</span></span>                                                                                     |



 

<span data-ttu-id="dd980-138">A tabela a seguir descreve os sinalizadores de capacidade de plug-in.</span><span class="sxs-lookup"><span data-stu-id="dd980-138">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="dd980-139">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="dd980-139">Flag</span></span>                                    | <span data-ttu-id="dd980-140">Valor</span><span class="sxs-lookup"><span data-stu-id="dd980-140">Value</span></span> | <span data-ttu-id="dd980-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="dd980-141">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd980-142">\_BACKGROUNDPROCESSING do limite da assinatura \_</span><span class="sxs-lookup"><span data-stu-id="dd980-142">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="dd980-143">0x8</span><span class="sxs-lookup"><span data-stu-id="dd980-143">0x8</span></span>   | <span data-ttu-id="dd980-144">O Windows Media Player deve chamar [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) para informar o plug-in quando ele deve iniciar e parar o processamento em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="dd980-144">Windows Media Player should call [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) to inform the plug-in when it should start and stop background processing.</span></span>                                                                                                     |
| <span data-ttu-id="dd980-145">\_DEVICEAVAILABLE do limite da assinatura \_</span><span class="sxs-lookup"><span data-stu-id="dd980-145">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="dd980-146">0x10</span><span class="sxs-lookup"><span data-stu-id="dd980-146">0x10</span></span>  | <span data-ttu-id="dd980-147">O Windows Media Player deve chamar [IWMPContentPartner:: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span><span class="sxs-lookup"><span data-stu-id="dd980-147">Windows Media Player should call [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).</span></span>                                                                                                                                                                   |
| <span data-ttu-id="dd980-148">o \_ limite da assinatura \_ é \_ CONTENTPARTNER</span><span class="sxs-lookup"><span data-stu-id="dd980-148">SUBSCRIPTION\_CAP\_IS\_CONTENTPARTNER</span></span>   | <span data-ttu-id="dd980-149">0x40</span><span class="sxs-lookup"><span data-stu-id="dd980-149">0x40</span></span>  | <span data-ttu-id="dd980-150">Informa ao Windows Media Player que o plug-in implementa a interface **IWMPContentPartner** .</span><span class="sxs-lookup"><span data-stu-id="dd980-150">Informs Windows Media Player that the plug-in implements the **IWMPContentPartner** interface.</span></span> <span data-ttu-id="dd980-151">Todos os plug-ins da loja online tipo 1 devem definir esse sinalizador.</span><span class="sxs-lookup"><span data-stu-id="dd980-151">All type 1 online store plug-ins must set this flag.</span></span>                                                                                                                         |
| <span data-ttu-id="dd980-152">\_ALTLOGIN do limite da assinatura \_</span><span class="sxs-lookup"><span data-stu-id="dd980-152">SUBSCRIPTION\_CAP\_ALTLOGIN</span></span>             | <span data-ttu-id="dd980-153">0x80</span><span class="sxs-lookup"><span data-stu-id="dd980-153">0x80</span></span>  | <span data-ttu-id="dd980-154">Informa ao Windows Media Player que o plug-in dá suporte a um logon alternativo.</span><span class="sxs-lookup"><span data-stu-id="dd980-154">Informs Windows Media Player that the plug-in supports an alternate login.</span></span> <span data-ttu-id="dd980-155">Se o plug-in der suporte a um logon alternativo, o Windows Media Player recuperará a URL de logon alternativa e a legenda chamando [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span><span class="sxs-lookup"><span data-stu-id="dd980-155">If the plug-in supports an alternate login, Windows Media Player retrieves the alternate login URL and caption by calling [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo).</span></span> |



 

<span data-ttu-id="dd980-156">**Entradas de registro para desenvolvimento e teste**</span><span class="sxs-lookup"><span data-stu-id="dd980-156">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="dd980-157">Quando você começa a desenvolver sua loja online, a Microsoft fornece duas chaves: uma chave de teste e uma chave de produção.</span><span class="sxs-lookup"><span data-stu-id="dd980-157">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="dd980-158">Durante a fase de desenvolvimento e teste, sua loja online será exibida no Windows Media Player somente se sua chave de teste ou sua chave de produção estiver no registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="dd980-158">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="dd980-159">Para obter mais informações sobre as chaves de teste e de produção, consulte [chaves de teste e de produção para uma loja online tipo 1](test-and-production-keys-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="dd980-159">For more information about the test and production keys, see [Test and Production Keys for a Type 1 Online Store](test-and-production-keys-for-a-type-1-online-store.md).</span></span>

<span data-ttu-id="dd980-160">Coloque sua chave de teste ou de produção no seguinte local do registro.</span><span class="sxs-lookup"><span data-stu-id="dd980-160">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="dd980-161">Observe que o valor da entrada do registro TestParameter pode especificar várias chaves de teste ou de produção.</span><span class="sxs-lookup"><span data-stu-id="dd980-161">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="dd980-162">Por exemplo, suponha que o Proseware tenha uma chave de teste de "1234" e que a contoso tenha uma chave de teste de "2345".</span><span class="sxs-lookup"><span data-stu-id="dd980-162">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="dd980-163">A seguinte entrada do Registro especifica que os repositórios de teste para a Proseware e a contoso serão exibidos no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="dd980-163">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="dd980-164">**Entrada do registro ActiveService**</span><span class="sxs-lookup"><span data-stu-id="dd980-164">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="dd980-165">Quando o usuário ativa uma loja online, o Windows Media Player grava as informações no registro que identificam o repositório online ativo.</span><span class="sxs-lookup"><span data-stu-id="dd980-165">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="dd980-166">O Windows Media Player coloca as informações no seguinte local no registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="dd980-166">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="dd980-167">Na sintaxe de registro anterior, o *serviceInfo* é um espaço reservado para uma cadeia de caracteres que contém informações descritivas sobre a loja online ativa.</span><span class="sxs-lookup"><span data-stu-id="dd980-167">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd980-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd980-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd980-169">**Referência para lojas online do tipo 1**</span><span class="sxs-lookup"><span data-stu-id="dd980-169">**Reference for Type 1 Online Stores**</span></span>](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





