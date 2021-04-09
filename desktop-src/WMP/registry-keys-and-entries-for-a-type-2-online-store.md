---
title: Chaves e entradas do registro para uma loja online tipo 2
description: Chaves e entradas do registro para uma loja online tipo 2
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Armazenamentos online do Windows Media Player, registro
- lojas online, registro
- tipo 2 lojas online, registro
- registro, tipo 2 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084390"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a><span data-ttu-id="438ea-107">Chaves e entradas do registro para uma loja online tipo 2</span><span class="sxs-lookup"><span data-stu-id="438ea-107">Registry Keys and Entries for a Type 2 Online Store</span></span>

> [!Note]  
> <span data-ttu-id="438ea-108">Esta seção descreve a funcionalidade projetada para uso por lojas online.</span><span class="sxs-lookup"><span data-stu-id="438ea-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="438ea-109">Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.</span><span class="sxs-lookup"><span data-stu-id="438ea-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="438ea-110">Para disponibilizar um armazenamento online tipo 2 no Windows Media Player, o provedor de loja online deve criar as seguintes subchaves de registro e entradas no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="438ea-110">To make a type 2 online store available in Windows Media Player, the online store provider must create the following registry subkeys and entries on the user's computer.</span></span>


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



<span data-ttu-id="438ea-111">Na sintaxe de registro anterior, os símbolos em itálico são espaços reservados para nomes e identificadores globalmente exclusivos (GUIDs) que são específicos para a loja online.</span><span class="sxs-lookup"><span data-stu-id="438ea-111">In the preceding registry syntax, the symbols in italic are placeholders for names and globally unique identifiers (GUIDs) that are specific to the online store.</span></span> <span data-ttu-id="438ea-112">A tabela a seguir descreve esses espaços reservados.</span><span class="sxs-lookup"><span data-stu-id="438ea-112">The following table describes those placeholders.</span></span>



| <span data-ttu-id="438ea-113">Espaço reservado</span><span class="sxs-lookup"><span data-stu-id="438ea-113">Placeholder</span></span>    | <span data-ttu-id="438ea-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="438ea-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="438ea-115">*keyName*</span><span class="sxs-lookup"><span data-stu-id="438ea-115">*keyName*</span></span>      | <span data-ttu-id="438ea-116">Uma cadeia de caracteres acordada entre a Microsoft e a loja online.</span><span class="sxs-lookup"><span data-stu-id="438ea-116">A string agreed upon between Microsoft and the online store.</span></span> <span data-ttu-id="438ea-117">Essa cadeia de caracteres identifica exclusivamente o repositório online. Exemplo: "Proseware"</span><span class="sxs-lookup"><span data-stu-id="438ea-117">This string uniquely identifies the online store.Example: "Proseware"</span></span><br/>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="438ea-118">*sinalizadores*</span><span class="sxs-lookup"><span data-stu-id="438ea-118">*flags*</span></span>        | <span data-ttu-id="438ea-119">Um operador de plug-in ou uma operação unificada **ou** de um ou mais sinalizadores especificam se o Windows Media Player deve chamar métodos específicos de [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) e [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span><span class="sxs-lookup"><span data-stu-id="438ea-119">A bitwise **OR** of one or more plug-in capability flags These flags specify whether Windows Media Player should call particular methods of [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) and [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2).</span></span> <span data-ttu-id="438ea-120">Para obter informações sobre sinalizadores com suporte, consulte a tabela de sinalizadores de recurso de plug-in que segue esta tabela. Exemplo: 00000037</span><span class="sxs-lookup"><span data-stu-id="438ea-120">For information about supported flags, see the table of plug-in capability flags that follows this table.Example: 00000037</span></span><br/> |
| <span data-ttu-id="438ea-121">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="438ea-121">*clsid*</span></span>        | <span data-ttu-id="438ea-122">Um GUID que é o identificador de classe (CLSID) para a classe que implementa **IWMPSubscriptionService** no plug-in da loja online.</span><span class="sxs-lookup"><span data-stu-id="438ea-122">A GUID that is the class identifier (CLSID) for the class that implements **IWMPSubscriptionService** in the online store's plug-in.</span></span> <span data-ttu-id="438ea-123">Esse GUID deve estar no formato de registro, completo com as chaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span><span class="sxs-lookup"><span data-stu-id="438ea-123">This GUID must be in registry format, complete with the curly braces.Format: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}</span></span><br/>                                                                                                                                    |
| <span data-ttu-id="438ea-124">*FriendlyName*</span><span class="sxs-lookup"><span data-stu-id="438ea-124">*friendlyname*</span></span> | <span data-ttu-id="438ea-125">Um nome amigável para a loja online. Exemplo: "serviço de música da Proseware"</span><span class="sxs-lookup"><span data-stu-id="438ea-125">A friendly name for the online store.Example: "Proseware Music Service"</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="438ea-126">*pluginName*</span><span class="sxs-lookup"><span data-stu-id="438ea-126">*pluginName*</span></span>   | <span data-ttu-id="438ea-127">Um nome para o plug-in da loja online. Exemplo: "plug-in de serviço de Proseware"</span><span class="sxs-lookup"><span data-stu-id="438ea-127">A name for the online store's plug-in.Example: "Proseware Service Plug-in"</span></span><br/>                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="438ea-128">*className*</span><span class="sxs-lookup"><span data-stu-id="438ea-128">*className*</span></span>    | <span data-ttu-id="438ea-129">O nome da classe que implementa **IWMPSubscriptionService** no plug-in da loja online. Exemplo: "CProsewareService"</span><span class="sxs-lookup"><span data-stu-id="438ea-129">The name of the class that implements **IWMPSubscriptionService** in the online store's plug-in.Example: "CProsewareService"</span></span><br/>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="438ea-130">*moduleName*</span><span class="sxs-lookup"><span data-stu-id="438ea-130">*moduleName*</span></span>   | <span data-ttu-id="438ea-131">O caminho totalmente qualificado para a DLL que implementa o plug-in da loja online. Exemplo: "C: \\ arquivos de programa \\ Proseware \\ProsewareService.dll"</span><span class="sxs-lookup"><span data-stu-id="438ea-131">The fully qualified path to the DLL that implements the online store's plug-in.Example: "C:\\Program Files\\Proseware\\ProsewareService.dll"</span></span><br/>                                                                                                                                                                                                                                                |



 

<span data-ttu-id="438ea-132">A tabela a seguir descreve os sinalizadores de capacidade de plug-in.</span><span class="sxs-lookup"><span data-stu-id="438ea-132">The following table describes the plug-in capability flags.</span></span>



| <span data-ttu-id="438ea-133">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="438ea-133">Flag</span></span>                                    | <span data-ttu-id="438ea-134">Valor</span><span class="sxs-lookup"><span data-stu-id="438ea-134">Value</span></span> | <span data-ttu-id="438ea-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="438ea-135">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="438ea-136">\_ALLOWPLAY do limite da assinatura \_</span><span class="sxs-lookup"><span data-stu-id="438ea-136">SUBSCRIPTION\_CAP\_ALLOWPLAY</span></span>            | <span data-ttu-id="438ea-137">0X1</span><span class="sxs-lookup"><span data-stu-id="438ea-137">0X1</span></span>   | <span data-ttu-id="438ea-138">O Windows Media Player deve chamar [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span><span class="sxs-lookup"><span data-stu-id="438ea-138">Windows Media Player should call [IWMPSubscriptionService::allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).</span></span>                                                                                                                      |
| <span data-ttu-id="438ea-139">\_ALLOWCDBURN do limite da assinatura \_</span><span class="sxs-lookup"><span data-stu-id="438ea-139">SUBSCRIPTION\_CAP\_ALLOWCDBURN</span></span>          | <span data-ttu-id="438ea-140">0X2</span><span class="sxs-lookup"><span data-stu-id="438ea-140">0X2</span></span>   | <span data-ttu-id="438ea-141">O Windows Media Player deve chamar [IWMPSubscriptionService:: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span><span class="sxs-lookup"><span data-stu-id="438ea-141">Windows Media Player should call [IWMPSubscriptionService::allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).</span></span>                                                                                                                  |
| <span data-ttu-id="438ea-142">\_ALLOWPDATRANSFER do limite da assinatura \_</span><span class="sxs-lookup"><span data-stu-id="438ea-142">SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER</span></span>     | <span data-ttu-id="438ea-143">0X4</span><span class="sxs-lookup"><span data-stu-id="438ea-143">0X4</span></span>   | <span data-ttu-id="438ea-144">O Windows Media Player deve chamar [IWMPSubscriptionService:: allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span><span class="sxs-lookup"><span data-stu-id="438ea-144">Windows Media Player should call [IWMPSubscriptionService::allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).</span></span>                                                                                                        |
| <span data-ttu-id="438ea-145">\_BACKGROUNDPROCESSING do limite da assinatura \_</span><span class="sxs-lookup"><span data-stu-id="438ea-145">SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING</span></span> | <span data-ttu-id="438ea-146">0X8</span><span class="sxs-lookup"><span data-stu-id="438ea-146">0X8</span></span>   | <span data-ttu-id="438ea-147">O Windows Media Player deve chamar [IWMPSubscriptionService:: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span><span class="sxs-lookup"><span data-stu-id="438ea-147">Windows Media Player should call [IWMPSubscriptionService::startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).</span></span>                                                                                      |
| <span data-ttu-id="438ea-148">\_DEVICEAVAILABLE do limite da assinatura \_</span><span class="sxs-lookup"><span data-stu-id="438ea-148">SUBSCRIPTION\_CAP\_DEVICEAVAILABLE</span></span>      | <span data-ttu-id="438ea-149">0X10</span><span class="sxs-lookup"><span data-stu-id="438ea-149">0X10</span></span>  | <span data-ttu-id="438ea-150">O Windows Media Player deve chamar [IWMPSubscriptionService2::D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span><span class="sxs-lookup"><span data-stu-id="438ea-150">Windows Media Player should call [IWMPSubscriptionService2::deviceAvailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).</span></span>                                                                                                        |
| <span data-ttu-id="438ea-151">\_PREPAREFORSYNC do limite da assinatura \_</span><span class="sxs-lookup"><span data-stu-id="438ea-151">SUBSCRIPTION\_CAP\_PREPAREFORSYNC</span></span>       | <span data-ttu-id="438ea-152">0X20</span><span class="sxs-lookup"><span data-stu-id="438ea-152">0X20</span></span>  | <span data-ttu-id="438ea-153">O Windows Media Player deve chamar [IWMPSubscriptionService2::P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span><span class="sxs-lookup"><span data-stu-id="438ea-153">Windows Media Player should call [IWMPSubscriptionService2::prepareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).</span></span>                                                                                                          |
| <span data-ttu-id="438ea-154">Limites de assinatura \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="438ea-154">SUBSCRIPTION\_V1\_CAPS</span></span>                  | <span data-ttu-id="438ea-155">0XF</span><span class="sxs-lookup"><span data-stu-id="438ea-155">0XF</span></span>   | <span data-ttu-id="438ea-156">Padrão.</span><span class="sxs-lookup"><span data-stu-id="438ea-156">Default.</span></span> <span data-ttu-id="438ea-157">Esse valor será usado se nenhum for registrado.</span><span class="sxs-lookup"><span data-stu-id="438ea-157">This value is used if none is registered.</span></span> <span data-ttu-id="438ea-158">Isso é equivalente a combinar \_ \_ ALLOWPLAY de extremidade de assinatura \_ , \_ ALLOWCDBURN de limite de assinatura, limite de assinatura \_ \_ ALLOWPDATRANSFER e limite de assinatura \_ \_ BACKGROUNDPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="438ea-158">This is equivalent to combining SUBSCRIPTION\_CAP\_ALLOWPLAY, SUBSCRIPTION\_CAP\_ALLOWCDBURN, SUBSCRIPTION\_CAP\_ALLOWPDATRANSFER, and SUBSCRIPTION\_CAP\_BACKGROUNDPROCESSING.</span></span> |



 

<span data-ttu-id="438ea-159">**Entradas de registro para desenvolvimento e teste**</span><span class="sxs-lookup"><span data-stu-id="438ea-159">**Registry Entries for Development and Testing**</span></span>

<span data-ttu-id="438ea-160">Quando você começa a desenvolver sua loja online, a Microsoft fornece duas chaves: uma chave de teste e uma chave de produção.</span><span class="sxs-lookup"><span data-stu-id="438ea-160">When you begin developing your online store, Microsoft provides you with two keys: a test key and a production key.</span></span> <span data-ttu-id="438ea-161">Durante a fase de desenvolvimento e teste, sua loja online será exibida no Windows Media Player somente se sua chave de teste ou sua chave de produção estiver no registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="438ea-161">During the development and testing phase, your online store will appear in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="438ea-162">Para obter mais informações sobre as chaves de teste e de produção, consulte [chaves de teste e de produção para uma loja online tipo 2](test-and-production-keys-for-a-type-2-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="438ea-162">For more information about the test and production keys, see [Test and Production Keys for a Type 2 Online Store](test-and-production-keys-for-a-type-2-online-store.md).</span></span>

<span data-ttu-id="438ea-163">Coloque sua chave de teste ou de produção no seguinte local do registro.</span><span class="sxs-lookup"><span data-stu-id="438ea-163">Place your test or production key in the following location in the registry.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



<span data-ttu-id="438ea-164">Observe que o valor da entrada do registro TestParameter pode especificar várias chaves de teste ou de produção.</span><span class="sxs-lookup"><span data-stu-id="438ea-164">Note that the value of the TestParameter registry entry can specify multiple test or production keys.</span></span> <span data-ttu-id="438ea-165">Por exemplo, suponha que o Proseware tenha uma chave de teste de "1234" e que a contoso tenha uma chave de teste de "2345".</span><span class="sxs-lookup"><span data-stu-id="438ea-165">For example, suppose that Proseware has a test key of "1234" and Contoso has a test key of "2345".</span></span> <span data-ttu-id="438ea-166">A seguinte entrada do Registro especifica que os repositórios de teste para a Proseware e a contoso serão exibidos no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="438ea-166">The following registry entry specifies that the test stores for Proseware and Contoso will appear in Windows Media Player.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



<span data-ttu-id="438ea-167">**Entrada do registro ActiveService**</span><span class="sxs-lookup"><span data-stu-id="438ea-167">**ActiveService Registry Entry**</span></span>

<span data-ttu-id="438ea-168">Quando o usuário ativa uma loja online, o Windows Media Player grava as informações no registro que identificam o repositório online ativo.</span><span class="sxs-lookup"><span data-stu-id="438ea-168">When the user activates an online store, Windows Media Player writes information in the registry that identifies the active online store.</span></span> <span data-ttu-id="438ea-169">O Windows Media Player coloca as informações no seguinte local no registro no computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="438ea-169">Windows Media Player places the information in the following location in the registry on the user's computer.</span></span>


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



<span data-ttu-id="438ea-170">Na sintaxe de registro anterior, o *serviceInfo* é um espaço reservado para uma cadeia de caracteres que contém informações descritivas sobre a loja online ativa.</span><span class="sxs-lookup"><span data-stu-id="438ea-170">In the preceding registry syntax, *serviceInfo* is a placeholder for a string that contains descriptive information about the active online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="438ea-171">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="438ea-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="438ea-172">**Referência para lojas online do tipo 2**</span><span class="sxs-lookup"><span data-stu-id="438ea-172">**Reference for Type 2 Online Stores**</span></span>](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





