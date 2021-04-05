---
description: Quando ele instala um provedor de rede, seu aplicativo deve criar as chaves do registro e os valores descritos neste tópico.
ms.assetid: cc5a4a7b-02b5-4ecd-967c-de0656f00846
title: Chaves do registro de autenticação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee2e42febe7516060dd61a7b751a33dcf62cb9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921949"
---
# <a name="authentication-registry-keys"></a><span data-ttu-id="217dd-103">Chaves do registro de autenticação</span><span class="sxs-lookup"><span data-stu-id="217dd-103">Authentication Registry Keys</span></span>

<span data-ttu-id="217dd-104">Quando ele instala um provedor de rede, seu aplicativo deve criar as chaves do registro e os valores descritos neste tópico.</span><span class="sxs-lookup"><span data-stu-id="217dd-104">When it installs a network provider, your application should create the registry keys and values described in this topic.</span></span> <span data-ttu-id="217dd-105">Essas chaves e valores fornecem informações para o MPR sobre os provedores de rede instalados no sistema.</span><span class="sxs-lookup"><span data-stu-id="217dd-105">These keys and values provide information to the MPR about the network providers installed on the system.</span></span> <span data-ttu-id="217dd-106">O MPR verifica essas chaves quando ele inicia e carrega as DLLs do provedor de rede que ele encontra.</span><span class="sxs-lookup"><span data-stu-id="217dd-106">The MPR checks these keys when it starts and loads the network provider DLLs that it finds.</span></span>

<span data-ttu-id="217dd-107">Antes de criar um conjunto de chaves para armazenar informações sobre seu provedor de rede, você deve adicionar o nome do seu provedor de rede à chave de **ordem** .</span><span class="sxs-lookup"><span data-stu-id="217dd-107">Before you create a set of keys to hold information about your network provider, you should add the name of your network provider to the **order** key.</span></span> <span data-ttu-id="217dd-108">Essa chave é uma subchave da seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="217dd-108">This key is a subkey of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
```

<span data-ttu-id="217dd-109">A chave **Order** contém um único valor, **ProviderOrder**, que lista os provedores instalados e especifica a ordem na qual eles devem ser testados durante as operações que alternam provedores até que um provedor de aceitação seja encontrado.</span><span class="sxs-lookup"><span data-stu-id="217dd-109">The **order** key contains a single value, **ProviderOrder**, which lists the installed providers and specifies the order in which they should be tried during operations that cycle through providers until an accepting provider is found.</span></span>

<span data-ttu-id="217dd-110">O valor **ProviderOrder** contém uma lista separada por vírgulas de nomes de chave.</span><span class="sxs-lookup"><span data-stu-id="217dd-110">The **ProviderOrder** value contains a comma-separated list of key names.</span></span> <span data-ttu-id="217dd-111">Cada nome de chave no **ProviderOrder** identifica um provedor de rede.</span><span class="sxs-lookup"><span data-stu-id="217dd-111">Each key name in **ProviderOrder** identifies a network provider.</span></span> <span data-ttu-id="217dd-112">Quando o MPR percorre os provedores, ele os chama na ordem em que aparecem nessa lista.</span><span class="sxs-lookup"><span data-stu-id="217dd-112">When MPR cycles through the providers, it calls them in the order in which they appear in this list.</span></span>

<span data-ttu-id="217dd-113">O nome do provedor definido em **ProviderOrder** também deve ser usado como o nome da chave do registro que contém informações sobre esse provedor.</span><span class="sxs-lookup"><span data-stu-id="217dd-113">The provider name set in **ProviderOrder** should also be used as the name of the registry key that contains information about that provider.</span></span> <span data-ttu-id="217dd-114">As chaves do registro específicas do provedor são criadas como subchaves da seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="217dd-114">The provider-specific registry keys are created as subkeys of the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="217dd-115">Em outras palavras, os nomes de provedor especificados em **ProviderOrder** são o caminho para o registro das chaves específicas do provedor de rede, em relação ao seguinte caminho:</span><span class="sxs-lookup"><span data-stu-id="217dd-115">In other words, the provider names specified in **ProviderOrder** are the path to the registry of the network provider-specific keys, relative to the following path:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
```

<span data-ttu-id="217dd-116">Quando o serviço do provedor de rede estiver instalado, o aplicativo de instalação deverá adicionar uma chave da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="217dd-116">When your network provider service is installed, the installation application should add a key as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Services
            ProviderName
```

<span data-ttu-id="217dd-117">Em que *ProviderName* é o nome do provedor de rede, conforme especificado no valor **ProviderOrder** da chave **Order** .</span><span class="sxs-lookup"><span data-stu-id="217dd-117">Where *ProviderName* is the name of the network provider as specified in the **ProviderOrder** value of the **order** key.</span></span> <span data-ttu-id="217dd-118">O valor do **grupo** sob a chave *ProviderName* deve ser definido como "NetworkProvider".</span><span class="sxs-lookup"><span data-stu-id="217dd-118">The **Group** value under the *ProviderName* key should be set to "NetworkProvider".</span></span> <span data-ttu-id="217dd-119">Isso identifica o serviço como estando no grupo de provedores de rede.</span><span class="sxs-lookup"><span data-stu-id="217dd-119">This identifies the service as being in the network provider group.</span></span>

<span data-ttu-id="217dd-120">Você também deve criar uma subchave de *ProviderName*, **NetworkProvider**.</span><span class="sxs-lookup"><span data-stu-id="217dd-120">You must also create a subkey of *ProviderName*, **networkprovider**.</span></span> <span data-ttu-id="217dd-121">Essa chave contém os seguintes valores que descrevem o provedor de rede.</span><span class="sxs-lookup"><span data-stu-id="217dd-121">This key contains the following values that describe the network provider.</span></span>



| <span data-ttu-id="217dd-122">Valor</span><span class="sxs-lookup"><span data-stu-id="217dd-122">Value</span></span>                       | <span data-ttu-id="217dd-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="217dd-123">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="217dd-124">**Nome**</span><span class="sxs-lookup"><span data-stu-id="217dd-124">**Name**</span></span><br/>         | <span data-ttu-id="217dd-125">Contém o nome do provedor.</span><span class="sxs-lookup"><span data-stu-id="217dd-125">Contains the name of the provider.</span></span> <span data-ttu-id="217dd-126">Esse nome é exibido para o usuário como o nome da rede nas caixas de diálogo de procura e deve corresponder ao campo **lpProvider** retornado nas estruturas do [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) .</span><span class="sxs-lookup"><span data-stu-id="217dd-126">This name is displayed to the user as the name of the network in the browse dialog boxes and should match the **lpProvider** field returned in [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures.</span></span> <span data-ttu-id="217dd-127">Esse nome deve ser uma variação do nome do produto, preferencialmente com alguma indicação da empresa também, para que seja claro e exclusivo.</span><span class="sxs-lookup"><span data-stu-id="217dd-127">This name should be some variation of the product name, preferably with some indication of the company as well, so that it is clear and unique.</span></span> <span data-ttu-id="217dd-128">"MS-LanMan", por exemplo, é um bom nome, enquanto "The net" seria uma opção ruim.</span><span class="sxs-lookup"><span data-stu-id="217dd-128">"MS-LanMan" for example is a good name, whereas "The Net" would be a poor choice.</span></span><br/> |
| <span data-ttu-id="217dd-129">**ProviderPath**</span><span class="sxs-lookup"><span data-stu-id="217dd-129">**ProviderPath**</span></span><br/> | <span data-ttu-id="217dd-130">Contém o caminho completo da DLL que implementa o provedor de rede.</span><span class="sxs-lookup"><span data-stu-id="217dd-130">Contains the full path of the DLL that implements the network provider.</span></span> <span data-ttu-id="217dd-131">O MPR chama [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) neste caminho.</span><span class="sxs-lookup"><span data-stu-id="217dd-131">MPR calls [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) on this path.</span></span><br/>                                                                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="217dd-132">Os valores a seguir são usados somente por provedores de rede que dão suporte às funções de gerenciamento de credenciais, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) e [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span><span class="sxs-lookup"><span data-stu-id="217dd-132">The following values are used only by network providers that support the credential management functions, [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) and [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify).</span></span>



| <span data-ttu-id="217dd-133">Valor</span><span class="sxs-lookup"><span data-stu-id="217dd-133">Value</span></span>                              | <span data-ttu-id="217dd-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="217dd-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="217dd-135">**Classe**</span><span class="sxs-lookup"><span data-stu-id="217dd-135">**Class**</span></span><br/>               | <span data-ttu-id="217dd-136">Um **DWORD** que identifica a classe, ou tipo, da funcionalidade do provedor à qual esse provedor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="217dd-136">A **DWORD** that identifies the class, or type, of provider functionality that this provider supports.</span></span> <span data-ttu-id="217dd-137">Os valores podem ser Unidos pelo operador **or** quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="217dd-137">Values may be joined by the **OR** operator when appropriate.</span></span> <span data-ttu-id="217dd-138">Os valores válidos para isso são \_ \_ classe de rede Wn, \_ classe de credencial WN \_ , \_ \_ classe AUTHENT primária WN \_ e classe de \_ serviço WN \_ .</span><span class="sxs-lookup"><span data-stu-id="217dd-138">Valid values for this are WN\_NETWORK\_CLASS, WN\_CREDENTIAL\_CLASS, WN\_PRIMARY\_AUTHENT\_CLASS, and WN\_SERVICE\_CLASS.</span></span><br/> <span data-ttu-id="217dd-139">Embora um provedor possa dar suporte à funcionalidade de autenticador primário, outro meio será usado para determinar qual autenticador é primário.</span><span class="sxs-lookup"><span data-stu-id="217dd-139">Although a provider may support primary authenticator functionality, another means will be used to determine which authenticator is primary.</span></span><br/> <span data-ttu-id="217dd-140">**Windows XP/2000:** Não há suporte para a alternância de autenticadores primários, portanto, esse valor é ignorado.</span><span class="sxs-lookup"><span data-stu-id="217dd-140">**Windows XP/2000:** Switching primary authenticators is not supported, so this value is ignored.</span></span> <br/> |
| <span data-ttu-id="217dd-141">**AuthentProviderPath**</span><span class="sxs-lookup"><span data-stu-id="217dd-141">**AuthentProviderPath**</span></span><br/> | <span data-ttu-id="217dd-142">Esse é o nome de arquivo totalmente qualificado para a DLL que exporta as funções de gerenciamento de credenciais.</span><span class="sxs-lookup"><span data-stu-id="217dd-142">This is the fully qualified file name for the DLL that exports the Credential Management Functions.</span></span> <span data-ttu-id="217dd-143">Esse valor é útil (mas não obrigatório) somente quando o provedor é identificado como sendo uma classe de CREDENCIAl \_ ou \_ provedor de classe AUTHENT primário \_ .</span><span class="sxs-lookup"><span data-stu-id="217dd-143">This value is useful (but not required) only when the provider is identified as being a CREDENTIAL\_CLASS or PRIMARY\_AUTHENT\_CLASS provider.</span></span> <span data-ttu-id="217dd-144">Se esse valor não estiver presente para um provedor dessa classe, as funções de gerenciamento de credenciais deverão ser exportadas da DLL identificadas pelo valor ProviderPath.</span><span class="sxs-lookup"><span data-stu-id="217dd-144">If this value is not present for a provider of this class, the credential management functions are expected to be exported from the DLL identified by the ProviderPath value.</span></span> <span data-ttu-id="217dd-145">Esse valor será usado somente se for desejável empacotar as funções de rede e as funções do Gerenciador de credenciais em DLLs separadas.</span><span class="sxs-lookup"><span data-stu-id="217dd-145">This value is used only if it is desirable to package the network functions and the credential manager functions in separate DLLs.</span></span><br/>  |



 

<span data-ttu-id="217dd-146">Além dos valores usados para registrar provedores de rede e gerenciadores de credenciais, você pode adicionar um valor ao registro para registrar uma DLL para receber notificações de conexão.</span><span class="sxs-lookup"><span data-stu-id="217dd-146">In addition to the values used to register network providers and credential managers, you can add a value to the registry to register a DLL to receive connection notifications.</span></span> <span data-ttu-id="217dd-147">Para fazer isso, crie um \_ valor reg Expand \_ sz na seguinte chave:</span><span class="sxs-lookup"><span data-stu-id="217dd-147">To do so, create a REG\_EXPAND\_SZ value under the following key:</span></span>

```
HKEY_LOCAL_MACHINE
   SYSTEM
      CurrentControlSet
         Control
            NetworkProvider
               Notifyees
```

<span data-ttu-id="217dd-148">Esse valor deve especificar o caminho para uma DLL que implementa a [API de notificação de conexão](connection-notification-api.md).</span><span class="sxs-lookup"><span data-stu-id="217dd-148">This value should specify the path to a DLL that implements the [Connection Notification API](connection-notification-api.md).</span></span> <span data-ttu-id="217dd-149">O nome desse valor pode ser qualquer coisa que você desejar, desde que ele não entre em conflito com nomes de valores preexistentes.</span><span class="sxs-lookup"><span data-stu-id="217dd-149">The name of this value can be anything you want, as long as it does not conflict with preexisting value names.</span></span>

## <a name="example"></a><span data-ttu-id="217dd-150">Exemplo</span><span class="sxs-lookup"><span data-stu-id="217dd-150">Example</span></span>

<span data-ttu-id="217dd-151">O exemplo a seguir mostra as chaves do registro para um sistema que tem dois provedores de rede instalados: LanmanWorkStation e AnotherNetSvc.</span><span class="sxs-lookup"><span data-stu-id="217dd-151">The following example shows the registry keys for a system that has two network providers installed: LanmanWorkStation and AnotherNetSvc.</span></span> <span data-ttu-id="217dd-152">AnotherNetSvc também é um Gerenciador de credenciais.</span><span class="sxs-lookup"><span data-stu-id="217dd-152">AnotherNetSvc is also a credential manager.</span></span> <span data-ttu-id="217dd-153">No exemplo, os nomes de chave são negrito e os nomes de valores são itálico.</span><span class="sxs-lookup"><span data-stu-id="217dd-153">In the example, key names are bold and value names are italic.</span></span>

<span data-ttu-id="217dd-154">**HKEY \_ \_** Ordem do controle do sistema de computador local \\  \\ **CurrentControlSet** \\ **Control** \\ **NetworkProvider** \\ </span><span class="sxs-lookup"><span data-stu-id="217dd-154">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**order**</span></span>

<span data-ttu-id="217dd-155">*ProviderOrder* = "LanmanWorkStation, AnotherNetSvc"</span><span class="sxs-lookup"><span data-stu-id="217dd-155">*ProviderOrder* = "LanmanWorkStation,AnotherNetSvc"</span></span>

<span data-ttu-id="217dd-156">**HKEY \_ Sistema de \_ computador local** \\  \\ **CurrentControlSet** \\ **Control** o \\ **NetworkProvider** \\ **notifica** os</span><span class="sxs-lookup"><span data-stu-id="217dd-156">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**NetworkProvider**\\**Notifyees**</span></span>

<span data-ttu-id="217dd-157">*MyNotifyApp* = "c: \\ conectar \\connect.dll"</span><span class="sxs-lookup"><span data-stu-id="217dd-157">*MyNotifyApp* = "c:\\connect\\connect.dll"</span></span>

<span data-ttu-id="217dd-158">**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **LanmanWorkStation**</span><span class="sxs-lookup"><span data-stu-id="217dd-158">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**</span></span>\\

<span data-ttu-id="217dd-159">*Group* = "NetworkProvider"</span><span class="sxs-lookup"><span data-stu-id="217dd-159">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="217dd-160">**HKEY \_ \_Computador local** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **LanmanWorkStation** \\ **NetworkProvider**</span><span class="sxs-lookup"><span data-stu-id="217dd-160">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**LanmanWorkStation**\\**NetworkProvider**</span></span>

<span data-ttu-id="217dd-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span><span class="sxs-lookup"><span data-stu-id="217dd-161">*Name* = "NT LanMan"*ProviderPath* = "ntlanman.dll"</span></span>

<span data-ttu-id="217dd-162">*Classe* = 0x00000001 ( \_ classe de rede WN \_ )</span><span class="sxs-lookup"><span data-stu-id="217dd-162">*Class* = 0x00000001 (WN\_NETWORK\_CLASS)</span></span>

<span data-ttu-id="217dd-163">**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ **AnotherNetSvc**</span><span class="sxs-lookup"><span data-stu-id="217dd-163">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**</span></span>\\

<span data-ttu-id="217dd-164">*Group* = "NetworkProvider"</span><span class="sxs-lookup"><span data-stu-id="217dd-164">*Group* = "NetworkProvider"</span></span>

<span data-ttu-id="217dd-165">**HKEY \_ \_Computador local** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **AnotherNetSvc** \\ **NetworkProvider**</span><span class="sxs-lookup"><span data-stu-id="217dd-165">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**AnotherNetSvc**\\**NetworkProvider**</span></span>

<span data-ttu-id="217dd-166">*Name* = "outra rede"*ProviderPath* = "c: \\ outro \\anet.dll"</span><span class="sxs-lookup"><span data-stu-id="217dd-166">*Name* = "Another Network"*ProviderPath* = "c:\\another\\anet.dll"</span></span>

<span data-ttu-id="217dd-167">*Class* = 0x00000003 ( \_ classe de \_ credencial WN de classe de rede WN \| \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="217dd-167">*Class* = 0x00000003 (WN\_NETWORK\_CLASS \| WN\_CREDENTIAL\_CLASS)</span></span>

<span data-ttu-id="217dd-168">*AuthentProviderPath* = "c: \\ outro \\anetCM.dll"</span><span class="sxs-lookup"><span data-stu-id="217dd-168">*AuthentProviderPath* = "c:\\another\\anetCM.dll"</span></span>

 

