---
title: Palavras-chave dinâmicas do firewall
description: Você usa as APIs de palavras-chave dinâmicas do firewall para gerenciar endereços de palavras-chave dinâmicas no Windows Defender firewall.
keywords:
- Palavras-chave dinâmicas do firewall
ms.topic: article
ms.date: 05/17/2021
ms.localizationpriority: low
ms.openlocfilehash: e60526d8a7889af3173913774790bdd209121040
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112681129"
---
# <a name="firewall-dynamic-keywords"></a><span data-ttu-id="859c7-104">Palavras-chave dinâmicas do firewall</span><span class="sxs-lookup"><span data-stu-id="859c7-104">Firewall dynamic keywords</span></span>

<span data-ttu-id="859c7-105">Você usa as APIs de palavras-chave dinâmicas do firewall para gerenciar *endereços de palavras-chave dinâmicas* no [Windows Defender firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span><span class="sxs-lookup"><span data-stu-id="859c7-105">You use the firewall dynamic keywords APIs to manage *dynamic keyword addresses* in [Windows Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span></span> <span data-ttu-id="859c7-106">Um endereço de palavra-chave dinâmica é usado para criar um conjunto de endereços IP aos quais uma ou mais regras de firewall podem se referir.</span><span class="sxs-lookup"><span data-stu-id="859c7-106">A dynamic keyword address is used to create a set of IP addresses to which one or more firewall rules can refer.</span></span> <span data-ttu-id="859c7-107">Os endereços de palavras-chave dinâmicas dão suporte a IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="859c7-107">Dynamic keyword addresses support both IPv4 and IPv6.</span></span>

> [!NOTE]
> <span data-ttu-id="859c7-108">Para o conteúdo de referência de API para as APIs apresentadas neste tópico, consulte [referência de palavras-chave dinâmicas do firewall](firewall-dynamic-keywords-reference.md).</span><span class="sxs-lookup"><span data-stu-id="859c7-108">For API reference content for the APIs introduced in this topic, see [Firewall dynamic keywords reference](firewall-dynamic-keywords-reference.md).</span></span>

## <a name="operations-on-dynamic-keyword-addresses"></a><span data-ttu-id="859c7-109">Operações em endereços de palavras-chave dinâmicas</span><span class="sxs-lookup"><span data-stu-id="859c7-109">Operations on dynamic keyword addresses</span></span>

<span data-ttu-id="859c7-110">Com as APIs de palavras-chave dinâmicas do firewall, você pode executar as seguintes operações.</span><span class="sxs-lookup"><span data-stu-id="859c7-110">With the Firewall dynamic keywords APIs, you can perform the following operations.</span></span>

* <span data-ttu-id="859c7-111">Adicionar endereços de palavras-chave dinâmicas</span><span class="sxs-lookup"><span data-stu-id="859c7-111">Add dynamic keyword addresses</span></span>
* <span data-ttu-id="859c7-112">Excluir endereços de palavras-chave dinâmicas</span><span class="sxs-lookup"><span data-stu-id="859c7-112">Delete dynamic keyword addresses</span></span>
* <span data-ttu-id="859c7-113">Enumerar endereços de palavras-chave dinâmicas por ID, ou por tipo</span><span class="sxs-lookup"><span data-stu-id="859c7-113">Enumerate dynamic keyword addresses by ID, or by type</span></span>
* <span data-ttu-id="859c7-114">Atualizar endereços de palavra-chave dinâmica</span><span class="sxs-lookup"><span data-stu-id="859c7-114">Update dynamic keyword addresses</span></span>
* <span data-ttu-id="859c7-115">Assinar e tratar notificações de alteração de endereço de palavra-chave dinâmica</span><span class="sxs-lookup"><span data-stu-id="859c7-115">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="859c7-116">Há exemplos de código para todas essas operações posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="859c7-116">There are code examples for all of those operations later in this topic.</span></span>

<span data-ttu-id="859c7-117">Depois de adicionar um endereço de palavra-chave dinâmica, ele persiste entre as reinicializações.</span><span class="sxs-lookup"><span data-stu-id="859c7-117">Once you've added a dynamic keyword address, it persists across reboots.</span></span> <span data-ttu-id="859c7-118">Você deve excluir um endereço de palavra-chave dinâmica quando terminar com o objeto.</span><span class="sxs-lookup"><span data-stu-id="859c7-118">You must delete a dynamic keyword address once you're done with the object.</span></span>

<span data-ttu-id="859c7-119">Há duas classes de endereços de palavra-chave dinâmicas, conforme descrito nas próximas duas seções.</span><span class="sxs-lookup"><span data-stu-id="859c7-119">There are two classes of dynamic keyword addresses, as described in the next two sections.</span></span>

## <a name="autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="859c7-120">Resolver automaticamente endereços de palavras-chave dinâmicas</span><span class="sxs-lookup"><span data-stu-id="859c7-120">AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="859c7-121">O primeiro tipo é *autoresolver*, onde o campo de *palavra-chave* representa um nome que possa ser resolvido e os endereços IP não são definidos na criação.</span><span class="sxs-lookup"><span data-stu-id="859c7-121">The first type is *AutoResolve*, where the *keyword* field represents a resolvable name, and the IP addresses aren't defined upon creation.</span></span>

<span data-ttu-id="859c7-122">Esses objetos devem ter seus endereços IP resolvidos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="859c7-122">These objects are intended to have their IP addresses resolved automatically.</span></span> <span data-ttu-id="859c7-123">Ou seja, não por meio de um administrador no momento da criação do objeto; Nem pelo sistema operacional (SO) propriamente dito.</span><span class="sxs-lookup"><span data-stu-id="859c7-123">That is, not through an admin at object creation time; nor through the operating system (OS) itself.</span></span> <span data-ttu-id="859c7-124">Um componente fora do serviço de firewall deve fazer a resolução de endereço IP para esses objetos e atualizá-los adequadamente.</span><span class="sxs-lookup"><span data-stu-id="859c7-124">A component outside of the firewall service must do the IP address resolution for these objects, and update them appropriately.</span></span> <span data-ttu-id="859c7-125">A implementação desse componente está fora do escopo deste conteúdo.</span><span class="sxs-lookup"><span data-stu-id="859c7-125">The implementation of such a component is outside the scope of this content.</span></span>

<span data-ttu-id="859c7-126">Um endereço de palavra-chave dinâmica é indicado como sendo *resolvido automaticamente* definindo o sinalizador **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** no objeto ao chamar a função [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) .</span><span class="sxs-lookup"><span data-stu-id="859c7-126">A dynamic keyword address is indicated as being *AutoResolve* by setting the **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** flag in the object when calling the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span> <span data-ttu-id="859c7-127">O campo de *palavra-chave* deve ser usado para representar o valor &mdash; que está sendo resolvido, ou seja, um FQDN (nome de domínio totalmente qualificado) ou nome de host.</span><span class="sxs-lookup"><span data-stu-id="859c7-127">The *keyword* field should be used to represent the value being resolved&mdash;that is, a fully qualified domain name (FQDN) or hostname.</span></span> <span data-ttu-id="859c7-128">Inicialmente, o campo de *endereços* deve ser nulo para esses objetos.</span><span class="sxs-lookup"><span data-stu-id="859c7-128">The *addresses* field must initially be NULL for these objects.</span></span> <span data-ttu-id="859c7-129">Esses objetos não terão seus endereços IP persistidos nos ciclos de inicialização e você deverá reavaliar/repopular seus endereços durante o próximo ciclo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="859c7-129">These objects won't have their IP addresses persisted across boot cycles, and you should re-evaluate/re-populate their addresses during the next boot cycle.</span></span>

> [!NOTE]
> <span data-ttu-id="859c7-130">Autoresolver os objetos de endereço de palavra-chave dinâmica dispara notificações em [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) e [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), mas não [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span><span class="sxs-lookup"><span data-stu-id="859c7-130">AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) and [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), but not [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="non-autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="859c7-131">Endereços de palavras-chave dinâmicas não autoresolvidos</span><span class="sxs-lookup"><span data-stu-id="859c7-131">Non-AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="859c7-132">O segundo tipo é *não AutoResolve*, onde o campo de *palavra-chave* é qualquer cadeia de caracteres e os endereços são definidos no momento da criação.</span><span class="sxs-lookup"><span data-stu-id="859c7-132">The second type is *non-AutoResolve*, where the *keyword* field is any string, and the addresses are defined at creation time.</span></span>

<span data-ttu-id="859c7-133">Esses objetos são usados para armazenar um conjunto de endereços IP, sub-redes ou intervalos.</span><span class="sxs-lookup"><span data-stu-id="859c7-133">These objects are used to store a set of IP address, subnets, or ranges.</span></span> <span data-ttu-id="859c7-134">O campo de *palavra-chave* aqui é usado para conveniência de gerenciamento e pode ser definido como qualquer cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="859c7-134">The *keyword* field here is used for management convenience, and it can be set to any string.</span></span> <span data-ttu-id="859c7-135">O campo de *endereços* não deve ser nulo na criação.</span><span class="sxs-lookup"><span data-stu-id="859c7-135">The *addresses* field must be non-NULL upon creation.</span></span> <span data-ttu-id="859c7-136">Os endereços para esses objetos são persistidos entre as reinicializações.</span><span class="sxs-lookup"><span data-stu-id="859c7-136">Addresses for these objects are persisted across reboots.</span></span>

> [!NOTE]
> <span data-ttu-id="859c7-137">Objetos de endereço de palavra-chave dinâmica não autoresolvem notificações em [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)e também [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span><span class="sxs-lookup"><span data-stu-id="859c7-137">Non-AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), and also [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="more-about-dynamic-keyword-addresses"></a><span data-ttu-id="859c7-138">Mais sobre endereços de palavras-chave dinâmicas</span><span class="sxs-lookup"><span data-stu-id="859c7-138">More about dynamic keyword addresses</span></span> 

<span data-ttu-id="859c7-139">Todos os endereços de palavra-chave dinâmicas devem ter um identificador [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) exclusivo para representá-los.</span><span class="sxs-lookup"><span data-stu-id="859c7-139">All dynamic keyword addresses must have a unique [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) identifier to represent them.</span></span>

<span data-ttu-id="859c7-140">A API [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) fornece notificações para um cliente quando os endereços de palavras-chave dinâmicas são alterados.</span><span class="sxs-lookup"><span data-stu-id="859c7-140">The [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) API delivers notifications to a client when dynamic keyword addresses change.</span></span> <span data-ttu-id="859c7-141">Não há nenhuma carga entregue ao cliente que descreve exatamente o que mudou no sistema.</span><span class="sxs-lookup"><span data-stu-id="859c7-141">There's no payload delivered to the client describing exactly what changed on the system.</span></span> <span data-ttu-id="859c7-142">Se você precisar saber quais objetos foram alterados, deverá consultar o estado atual dos objetos no sistema usando as APIs [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) ou [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) .</span><span class="sxs-lookup"><span data-stu-id="859c7-142">If you need to know what objects changed, then you should query the current state of objects on the system using the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) or [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) APIs.</span></span> <span data-ttu-id="859c7-143">Você pode usar os vários sinalizadores para solicitar notificações apenas para um subconjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="859c7-143">You can use the various flags to request notifications for only a subset of objects.</span></span> <span data-ttu-id="859c7-144">Se você não usar nenhum sinalizador, as notificações de alteração serão entregues para todos os objetos.</span><span class="sxs-lookup"><span data-stu-id="859c7-144">If you use no flags, then change notifications will be delivered for all objects.</span></span>

<span data-ttu-id="859c7-145">Uma regra de firewall pode usar endereços de palavras-chave dinâmicas em vez de definir explicitamente endereços IP para sua condição de endereço remoto.</span><span class="sxs-lookup"><span data-stu-id="859c7-145">A firewall rule can use dynamic keyword addresses instead of explicitly defining IP addresses for its remote address condition.</span></span> <span data-ttu-id="859c7-146">Uma regra de firewall pode usar endereços de palavras-chave dinâmicos e intervalos de endereços remotos definidos estaticamente.</span><span class="sxs-lookup"><span data-stu-id="859c7-146">A firewall rule can use both dynamic keyword addresses and statically defined remote address ranges.</span></span> <span data-ttu-id="859c7-147">Um único objeto de endereço de palavra-chave dinâmica pode ser usado novamente em várias regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="859c7-147">A single dynamic keyword address object can be re-used across multiple firewall rules.</span></span> <span data-ttu-id="859c7-148">Se uma regra de firewall não tiver nenhum endereço remoto configurado (ou seja, configurado apenas com objetos de autoresolver que ainda não foram resolvidos), a regra não será imposta.</span><span class="sxs-lookup"><span data-stu-id="859c7-148">If a firewall rule doesn't have any configured remote addresses (that is, configured with only AutoResolve objects which have not yet been resolved), then the rule won't be enforced.</span></span> <span data-ttu-id="859c7-149">Além disso, se uma regra usar vários endereços de palavras-chave dinâmicas, a regra será imposta para todos os endereços que estão atualmente resolvidos, mesmo se houver outros objetos que ainda não foram resolvidos.</span><span class="sxs-lookup"><span data-stu-id="859c7-149">Furthermore, if a rule uses multiple dynamic keyword addresses, then the rule will be enforced for all addresses that are currently resolved, even if there are other objects that are not yet resolved.</span></span> <span data-ttu-id="859c7-150">Quando um endereço de palavra-chave dinâmica é atualizado, todos os objetos de regra associados também terão seus endereços remotos atualizados.</span><span class="sxs-lookup"><span data-stu-id="859c7-150">When a dynamic keyword address is updated, all associated rule objects will have their remote addresses updated as well.</span></span>

<span data-ttu-id="859c7-151">O so (sistema operacional) em si não impõe nenhuma dependência entre uma regra e um endereço de palavra-chave dinâmico.</span><span class="sxs-lookup"><span data-stu-id="859c7-151">The operating system (OS) itself doesn't enforce any dependencies between a rule and a dynamic keyword address.</span></span> <span data-ttu-id="859c7-152">Isso significa que qualquer objeto pode ser criado primeiro &mdash; a regra pode fazer referência a IDs de endereço de palavra-chave dinâmica que ainda não existem (nesse caso, a regra não será imposta).</span><span class="sxs-lookup"><span data-stu-id="859c7-152">This means that either object can be created first&mdash;the rule can reference dynamic keyword address IDs that don't yet exist (in which case, the rule won't be enforced).</span></span> <span data-ttu-id="859c7-153">Além disso, você pode excluir um endereço de palavra-chave dinâmico mesmo se ele estiver em uso por uma regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="859c7-153">Furthermore, you can delete a dynamic keyword address even if it's in use by a firewall rule.</span></span> <span data-ttu-id="859c7-154">Este tópico descreve como um administrador pode configurar regras para usar o endereço de palavra-chave dinâmica.</span><span class="sxs-lookup"><span data-stu-id="859c7-154">This topic outlines how an admin can configure rules to use dynamic keyword address.</span></span>

## <a name="code-examples"></a><span data-ttu-id="859c7-155">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="859c7-155">Code examples</span></span>

<span data-ttu-id="859c7-156">Para testar cada um desses exemplos de código, primeiro inicie o Visual Studio e crie um novo projeto com base no modelo de projeto de **aplicativo de console** .</span><span class="sxs-lookup"><span data-stu-id="859c7-156">To try out each of these code examples, first launch Visual Studio and create a new project based on the **Console App** project template.</span></span> <span data-ttu-id="859c7-157">Você pode simplesmente substituir o conteúdo de `main.cpp` pela listagem de código.</span><span class="sxs-lookup"><span data-stu-id="859c7-157">You can just replace the contents of `main.cpp` with the code listing.</span></span>

<span data-ttu-id="859c7-158">A maioria dos exemplos de código usa as [bibliotecas de implementação do Windows (colocará)](https://github.com/Microsoft/wil).</span><span class="sxs-lookup"><span data-stu-id="859c7-158">Most of the code examples use the [Windows Implementation Libraries (WIL)](https://github.com/Microsoft/wil).</span></span> <span data-ttu-id="859c7-159">Uma maneira conveniente de instalar o colocará é acessar o Visual Studio, clicar em **projeto** \> **gerenciar pacotes NuGet...** \> **procurar**, digitar ou colar **Microsoft. Windows. ImplementationLibrary** na caixa de pesquisa, selecionar o item nos resultados da pesquisa e, em seguida, clicar em **instalar** para instalar o pacote para esse projeto.</span><span class="sxs-lookup"><span data-stu-id="859c7-159">A convenient way to install WIL is to go to Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.Windows.ImplementationLibrary** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

> [!NOTE]
> <span data-ttu-id="859c7-160">Os tipos de ponteiro para as funções gratuitas NetFw são publicados por meio `NetFw.h` de, mas uma biblioteca de vínculo estático não é publicada.</span><span class="sxs-lookup"><span data-stu-id="859c7-160">Pointer types for the NetFw free functions are published via `NetFw.h`, but a static-link library isn't published.</span></span> <span data-ttu-id="859c7-161">Use o [](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) / padrão de[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) LoadLibraryExW para chamar essas funções, conforme mostrado nesses exemplos de código.</span><span class="sxs-lookup"><span data-stu-id="859c7-161">Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling these functions, as shown in these code examples.</span></span>

### <a name="add-a-dynamic-keyword-address"></a><span data-ttu-id="859c7-162">Adicionar um endereço de palavra-chave dinâmica</span><span class="sxs-lookup"><span data-stu-id="859c7-162">Add a dynamic keyword address</span></span>

<span data-ttu-id="859c7-163">Este exemplo mostra como usar a função [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) .</span><span class="sxs-lookup"><span data-stu-id="859c7-163">This example shows how to use the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWADDDYNAMICKEYWORDADDRESS0 addDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    FW_DYNAMIC_KEYWORD_ADDRESS0 autoResolveKeywordAddress = { 0 };
    FW_DYNAMIC_KEYWORD_ADDRESS0 nonAutoResolveKeywordAddress = { 0 };

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        addDynamicKeywordAddressFn = (PFN_FWADDDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWAddDynamicKeywordAddress0"
        );
    }

    if (addDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Ensure the ID is unique. If not, the add operation will fail with ERROR_ALREADY_EXISTS
    // and you should invoke the API with a new ID.

    // Initialize and add an auto-resolve dynamic keyword address
    autoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_1;
    autoResolveKeywordAddress.keyword = L"bing.com";
    autoResolveKeywordAddress.flags = FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE;
    // must be NULL as we have set the auto resolve flag
    autoResolveKeywordAddress.addresses = NULL;

    error = addDynamicKeywordAddressFn(&autoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    // Initialize and add a non auto-resolve dynamic keyword address
    nonAutoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_2;
    nonAutoResolveKeywordAddress.keyword = L"myServerIPs";
    nonAutoResolveKeywordAddress.flags = 0;
    nonAutoResolveKeywordAddress.addresses = L"10.0.0.5,20.0.0.0/24,30.0.0.0-40.0.0.0";

    error = addDynamicKeywordAddressFn(&nonAutoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }
    return error;
}
```

### <a name="delete-a-dynamic-keyword-address"></a><span data-ttu-id="859c7-164">Excluir um endereço de palavra-chave dinâmica</span><span class="sxs-lookup"><span data-stu-id="859c7-164">Delete a dynamic keyword address</span></span>

<span data-ttu-id="859c7-165">Este exemplo mostra como usar a função [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) .</span><span class="sxs-lookup"><span data-stu-id="859c7-165">This example shows how to use the [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};


// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWDELETEDYNAMICKEYWORDADDRESS0 deleteDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });


    if (moduleHandle != NULL)
    {
        deleteDynamicKeywordAddressFn = (PFN_FWDELETEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWDeleteDynamicKeywordAddress0"
        );
    }

    if (deleteDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the functions
    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_1);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 1, err=[%d]", error);
    }

    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_2);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 2, err=[%d]", error);
    }

    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a><span data-ttu-id="859c7-166">Enumerar e liberar endereços de palavra-chave dinâmicas por ID</span><span class="sxs-lookup"><span data-stu-id="859c7-166">Enumerate and free dynamic keyword addresses by ID</span></span>

<span data-ttu-id="859c7-167">Este exemplo mostra como usar as funções [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) e [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) .</span><span class="sxs-lookup"><span data-stu-id="859c7-167">This example shows how to use the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0 enumDynamicKeywordAddressByIdFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressByIdFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressById0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressByIdFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    error = enumDynamicKeywordAddressByIdFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    if (dynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address
    }

    // Free the dynamic keyword address
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);
    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a><span data-ttu-id="859c7-168">Enumerar e liberar endereços de palavra-chave dinâmica por tipo</span><span class="sxs-lookup"><span data-stu-id="859c7-168">Enumerate and free dynamic keyword addresses by type</span></span>

<span data-ttu-id="859c7-169">Este exemplo mostra como usar as funções [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) e [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) .</span><span class="sxs-lookup"><span data-stu-id="859c7-169">This example shows how to use the [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke enum for ALL dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_ALL,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        // iterate to the next one in the list
        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    return error;
}
```

### <a name="update-dynamic-keyword-addresses"></a><span data-ttu-id="859c7-170">Atualizar endereços de palavra-chave dinâmica</span><span class="sxs-lookup"><span data-stu-id="859c7-170">Update dynamic keyword addresses</span></span>

<span data-ttu-id="859c7-171">Este exemplo mostra como usar a função [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) .</span><span class="sxs-lookup"><span data-stu-id="859c7-171">This example shows how to use the [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWUPDATEDYNAMICKEYWORDADDRESS0 updateDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    BOOL appendToCurrentAddresses = TRUE;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        updateDynamicKeywordAddressFn = (PFN_FWUPDATEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWUpdateDynamicKeywordAddress0"
        );
    }

    if (updateDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the function
    error = updateDynamicKeywordAddressFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        L"20.0.0.5",
        appendToCurrentAddresses);
    return error;
}
```

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a><span data-ttu-id="859c7-172">Assinar e tratar notificações de alteração de endereço de palavra-chave dinâmica</span><span class="sxs-lookup"><span data-stu-id="859c7-172">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="859c7-173">Este exemplo mostra como usar as funções [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) e [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) e o retorno de chamada [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) .</span><span class="sxs-lookup"><span data-stu-id="859c7-173">This example shows how to use the [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) and [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) functions, and the [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) callback.</span></span>

```cppwinrt
// main.cpp in a Console App project.
#include <windows.h>
#include <netfw.h>
#include <fwpmu.h>
#pragma comment(lib, "Fwpuclnt")

void CALLBACK TestCallback(_Inout_ VOID* /*pNotification*/, _Inout_ VOID* pContext)
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;
    HANDLE* waitHandle = (HANDLE*)pContext;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryW(L"firewallapi.dll");
    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        return;
    }

    // Invoke enum for ALL AutoResolve dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    SetEvent(*waitHandle);
}

int main()
{
    DWORD error = ERROR_SUCCESS;
    HANDLE notifyHandle;
    HANDLE waitHandle;

    waitHandle = CreateEventW(
        NULL,
        TRUE,
        FALSE,
        L"subscriptionWaitEvent"
    );


    // Subscribe for change notifications
    error = FwpmDynamicKeywordSubscribe0(
        FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE,
        TestCallback,
        &waitHandle,
        &notifyHandle);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    WaitForSingleObject(waitHandle, INFINITE);

    // When client is ready to unsubscribe
    error = FwpmDynamicKeywordUnsubscribe0(notifyHandle);

    return error;
}
```

## <a name="related-topics"></a><span data-ttu-id="859c7-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="859c7-174">Related topics</span></span>

* [<span data-ttu-id="859c7-175">Referência de palavras-chave dinâmicas do firewall</span><span class="sxs-lookup"><span data-stu-id="859c7-175">Firewall dynamic keywords reference</span></span>](firewall-dynamic-keywords-reference.md)
