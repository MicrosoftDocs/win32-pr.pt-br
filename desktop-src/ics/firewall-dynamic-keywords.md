---
title: Palavras-chave dinâmicas do firewall
description: Use as APIs de palavras-chave dinâmicas do firewall para gerenciar endereços de palavra-chave dinâmicos Microsoft Defender Firewall.
keywords:
- Palavras-chave dinâmicas do firewall
ms.topic: article
ms.date: 05/17/2021
ms.localizationpriority: low
ms.openlocfilehash: 15e35f26b72ed8d685e8302f6222836507e5c6a3
ms.sourcegitcommit: ae8c320a757558262167a4f4e385235b8d89035c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112765530"
---
# <a name="firewall-dynamic-keywords"></a><span data-ttu-id="e94fb-104">Palavras-chave dinâmicas do firewall</span><span class="sxs-lookup"><span data-stu-id="e94fb-104">Firewall dynamic keywords</span></span>

<span data-ttu-id="e94fb-105">Use as APIs de palavras-chave dinâmicas do firewall para gerenciar endereços *de palavra-chave* dinâmicos [no Microsoft Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span><span class="sxs-lookup"><span data-stu-id="e94fb-105">You use the firewall dynamic keywords APIs to manage *dynamic keyword addresses* in [Microsoft Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span></span> <span data-ttu-id="e94fb-106">Um endereço de palavra-chave dinâmico é usado para criar um conjunto de endereços IP aos quais uma ou mais regras de firewall podem se referir.</span><span class="sxs-lookup"><span data-stu-id="e94fb-106">A dynamic keyword address is used to create a set of IP addresses to which one or more firewall rules can refer.</span></span> <span data-ttu-id="e94fb-107">Endereços de palavra-chave dinâmicos são suportados por IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="e94fb-107">Dynamic keyword addresses support both IPv4 and IPv6.</span></span>

> [!NOTE]
> <span data-ttu-id="e94fb-108">Para conteúdo de referência de API para as APIs introduzidas neste tópico, consulte [Referência de palavras-chave dinâmicas do firewall](firewall-dynamic-keywords-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e94fb-108">For API reference content for the APIs introduced in this topic, see [Firewall dynamic keywords reference](firewall-dynamic-keywords-reference.md).</span></span>

## <a name="operations-on-dynamic-keyword-addresses"></a><span data-ttu-id="e94fb-109">Operações em endereços de palavra-chave dinâmicos</span><span class="sxs-lookup"><span data-stu-id="e94fb-109">Operations on dynamic keyword addresses</span></span>

<span data-ttu-id="e94fb-110">Com as APIs de palavras-chave dinâmicas do Firewall, você pode executar as operações a seguir.</span><span class="sxs-lookup"><span data-stu-id="e94fb-110">With the Firewall dynamic keywords APIs, you can perform the following operations.</span></span>

* <span data-ttu-id="e94fb-111">Adicionar endereços de palavra-chave dinâmicos</span><span class="sxs-lookup"><span data-stu-id="e94fb-111">Add dynamic keyword addresses</span></span>
* <span data-ttu-id="e94fb-112">Excluir endereços de palavra-chave dinâmicos</span><span class="sxs-lookup"><span data-stu-id="e94fb-112">Delete dynamic keyword addresses</span></span>
* <span data-ttu-id="e94fb-113">Enumerar endereços de palavra-chave dinâmicos por ID ou por tipo</span><span class="sxs-lookup"><span data-stu-id="e94fb-113">Enumerate dynamic keyword addresses by ID, or by type</span></span>
* <span data-ttu-id="e94fb-114">Atualizar endereços de palavra-chave dinâmicos</span><span class="sxs-lookup"><span data-stu-id="e94fb-114">Update dynamic keyword addresses</span></span>
* <span data-ttu-id="e94fb-115">Assinar e manipular notificações de alteração de endereço de palavra-chave dinâmica</span><span class="sxs-lookup"><span data-stu-id="e94fb-115">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="e94fb-116">Há exemplos de código para todas essas operações posteriormente neste tópico.</span><span class="sxs-lookup"><span data-stu-id="e94fb-116">There are code examples for all of those operations later in this topic.</span></span>

<span data-ttu-id="e94fb-117">Depois de adicionar um endereço de palavra-chave dinâmico, ele persiste entre reinicializações.</span><span class="sxs-lookup"><span data-stu-id="e94fb-117">Once you've added a dynamic keyword address, it persists across reboots.</span></span> <span data-ttu-id="e94fb-118">Você deve excluir um endereço de palavra-chave dinâmico depois de terminar com o objeto .</span><span class="sxs-lookup"><span data-stu-id="e94fb-118">You must delete a dynamic keyword address once you're done with the object.</span></span>

<span data-ttu-id="e94fb-119">Há duas classes de endereços de palavra-chave dinâmicos, conforme descrito nas próximas duas seções.</span><span class="sxs-lookup"><span data-stu-id="e94fb-119">There are two classes of dynamic keyword addresses, as described in the next two sections.</span></span>

## <a name="autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="e94fb-120">Endereços de palavra-chave dinâmicos autoResolve</span><span class="sxs-lookup"><span data-stu-id="e94fb-120">AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="e94fb-121">O primeiro tipo é *AutoResolve,* em que o campo de palavra-chave representa um nome resolvível e os endereços IP não são definidos após a criação. </span><span class="sxs-lookup"><span data-stu-id="e94fb-121">The first type is *AutoResolve*, where the *keyword* field represents a resolvable name, and the IP addresses aren't defined upon creation.</span></span>

<span data-ttu-id="e94fb-122">Esses objetos destinam-se a ter seus endereços IP resolvidos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="e94fb-122">These objects are intended to have their IP addresses resolved automatically.</span></span> <span data-ttu-id="e94fb-123">Ou seja, não por meio de um administrador no momento da criação do objeto; nem por meio do sistema operacional em si.</span><span class="sxs-lookup"><span data-stu-id="e94fb-123">That is, not through an admin at object creation time; nor through the operating system (OS) itself.</span></span> <span data-ttu-id="e94fb-124">Um componente fora do serviço de firewall deve fazer a resolução de endereço IP para esses objetos e atualizá-los adequadamente.</span><span class="sxs-lookup"><span data-stu-id="e94fb-124">A component outside of the firewall service must do the IP address resolution for these objects, and update them appropriately.</span></span> <span data-ttu-id="e94fb-125">A implementação desse componente está fora do escopo desse conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e94fb-125">The implementation of such a component is outside the scope of this content.</span></span>

<span data-ttu-id="e94fb-126">Um endereço de palavra-chave dinâmico é indicado como *AutoResolve* definindo o sinalizador **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** no objeto ao chamar a [**função FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="e94fb-126">A dynamic keyword address is indicated as being *AutoResolve* by setting the **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** flag in the object when calling the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span> <span data-ttu-id="e94fb-127">O *campo* de palavra-chave deve ser usado para representar o valor que está sendo resolvido, ou seja, um &mdash; FQDN (nome de domínio totalmente qualificado) ou nome de host.</span><span class="sxs-lookup"><span data-stu-id="e94fb-127">The *keyword* field should be used to represent the value being resolved&mdash;that is, a fully qualified domain name (FQDN) or hostname.</span></span> <span data-ttu-id="e94fb-128">O *campo* de endereços deve inicialmente ser NULL para esses objetos.</span><span class="sxs-lookup"><span data-stu-id="e94fb-128">The *addresses* field must initially be NULL for these objects.</span></span> <span data-ttu-id="e94fb-129">Esses objetos não terão seus endereços IP persistentes entre os ciclos de inicialização e você deverá reavalidar/preencher seus endereços durante o próximo ciclo de inicialização.</span><span class="sxs-lookup"><span data-stu-id="e94fb-129">These objects won't have their IP addresses persisted across boot cycles, and you should re-evaluate/re-populate their addresses during the next boot cycle.</span></span>

> [!NOTE]
> <span data-ttu-id="e94fb-130">Objetos de endereço de palavra-chave dinâmica AutoResolve disparam notificações [**em FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) e [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), mas não [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span><span class="sxs-lookup"><span data-stu-id="e94fb-130">AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) and [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), but not [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="non-autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="e94fb-131">Endereços de palavra-chave dinâmicos não AutoResolve</span><span class="sxs-lookup"><span data-stu-id="e94fb-131">Non-AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="e94fb-132">O segundo tipo é *não AutoResolve,* em que o campo de palavra-chave é qualquer cadeia de caracteres e os endereços são definidos no momento da criação. </span><span class="sxs-lookup"><span data-stu-id="e94fb-132">The second type is *non-AutoResolve*, where the *keyword* field is any string, and the addresses are defined at creation time.</span></span>

<span data-ttu-id="e94fb-133">Esses objetos são usados para armazenar um conjunto de endereços IP, sub-redes ou intervalos.</span><span class="sxs-lookup"><span data-stu-id="e94fb-133">These objects are used to store a set of IP address, subnets, or ranges.</span></span> <span data-ttu-id="e94fb-134">O *campo de* palavra-chave aqui é usado para conveniência de gerenciamento e pode ser definido como qualquer cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="e94fb-134">The *keyword* field here is used for management convenience, and it can be set to any string.</span></span> <span data-ttu-id="e94fb-135">O *campo de* endereços deve ser não NULL após a criação.</span><span class="sxs-lookup"><span data-stu-id="e94fb-135">The *addresses* field must be non-NULL upon creation.</span></span> <span data-ttu-id="e94fb-136">Os endereços para esses objetos são persistentes entre reinicializações.</span><span class="sxs-lookup"><span data-stu-id="e94fb-136">Addresses for these objects are persisted across reboots.</span></span>

> [!NOTE]
> <span data-ttu-id="e94fb-137">Objetos de endereço de palavra-chave dinâmico não AutoResolve disparam notificações [**em FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)e [**também FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span><span class="sxs-lookup"><span data-stu-id="e94fb-137">Non-AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), and also [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="more-about-dynamic-keyword-addresses"></a><span data-ttu-id="e94fb-138">Mais sobre endereços de palavra-chave dinâmicos</span><span class="sxs-lookup"><span data-stu-id="e94fb-138">More about dynamic keyword addresses</span></span> 

<span data-ttu-id="e94fb-139">Todos os endereços de palavra-chave dinâmicos devem ter um [**identificador GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) exclusivo para representá-los.</span><span class="sxs-lookup"><span data-stu-id="e94fb-139">All dynamic keyword addresses must have a unique [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) identifier to represent them.</span></span>

<span data-ttu-id="e94fb-140">A API [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) fornece notificações a um cliente quando os endereços de palavra-chave dinâmicos mudam.</span><span class="sxs-lookup"><span data-stu-id="e94fb-140">The [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) API delivers notifications to a client when dynamic keyword addresses change.</span></span> <span data-ttu-id="e94fb-141">Não há nenhum payload entregue ao cliente que descreve exatamente o que mudou no sistema.</span><span class="sxs-lookup"><span data-stu-id="e94fb-141">There's no payload delivered to the client describing exactly what changed on the system.</span></span> <span data-ttu-id="e94fb-142">Se você precisar saber quais objetos foram alterados, consulte o estado atual dos objetos no sistema usando as APIs [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) ou [**FWEnumDynamicKeywordAddressesByType0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0)</span><span class="sxs-lookup"><span data-stu-id="e94fb-142">If you need to know what objects changed, then you should query the current state of objects on the system using the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) or [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) APIs.</span></span> <span data-ttu-id="e94fb-143">Você pode usar os vários sinalizadores para solicitar notificações apenas para um subconjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="e94fb-143">You can use the various flags to request notifications for only a subset of objects.</span></span> <span data-ttu-id="e94fb-144">Se você não usar sinalizadores, as notificações de alteração serão entregues para todos os objetos.</span><span class="sxs-lookup"><span data-stu-id="e94fb-144">If you use no flags, then change notifications will be delivered for all objects.</span></span>

<span data-ttu-id="e94fb-145">Uma regra de firewall pode usar endereços de palavra-chave dinâmicos em vez de definir explicitamente endereços IP para sua condição de endereço remoto.</span><span class="sxs-lookup"><span data-stu-id="e94fb-145">A firewall rule can use dynamic keyword addresses instead of explicitly defining IP addresses for its remote address condition.</span></span> <span data-ttu-id="e94fb-146">Uma regra de firewall pode usar endereços de palavra-chave dinâmicos e intervalos de endereços remotos definidos estaticamente.</span><span class="sxs-lookup"><span data-stu-id="e94fb-146">A firewall rule can use both dynamic keyword addresses and statically defined remote address ranges.</span></span> <span data-ttu-id="e94fb-147">Um único objeto de endereço de palavra-chave dinâmica pode ser rea usado em várias regras de firewall.</span><span class="sxs-lookup"><span data-stu-id="e94fb-147">A single dynamic keyword address object can be re-used across multiple firewall rules.</span></span> <span data-ttu-id="e94fb-148">Se uma regra de firewall não tiver endereços remotos configurados (ou seja, configurados apenas com objetos AutoResolve que ainda não foram resolvidos), a regra não será imposta.</span><span class="sxs-lookup"><span data-stu-id="e94fb-148">If a firewall rule doesn't have any configured remote addresses (that is, configured with only AutoResolve objects which have not yet been resolved), then the rule won't be enforced.</span></span> <span data-ttu-id="e94fb-149">Além disso, se uma regra usar vários endereços de palavra-chave dinâmicos, a regra será imposta para todos os endereços que estão resolvidos no momento, mesmo se houver outros objetos que ainda não foram resolvidos.</span><span class="sxs-lookup"><span data-stu-id="e94fb-149">Furthermore, if a rule uses multiple dynamic keyword addresses, then the rule will be enforced for all addresses that are currently resolved, even if there are other objects that are not yet resolved.</span></span> <span data-ttu-id="e94fb-150">Quando um endereço de palavra-chave dinâmico for atualizado, todos os objetos de regra associados também terão seus endereços remotos atualizados.</span><span class="sxs-lookup"><span data-stu-id="e94fb-150">When a dynamic keyword address is updated, all associated rule objects will have their remote addresses updated as well.</span></span>

<span data-ttu-id="e94fb-151">O sistema operacional em si não impõe nenhuma dependência entre uma regra e um endereço de palavra-chave dinâmico.</span><span class="sxs-lookup"><span data-stu-id="e94fb-151">The operating system (OS) itself doesn't enforce any dependencies between a rule and a dynamic keyword address.</span></span> <span data-ttu-id="e94fb-152">Isso significa que qualquer objeto pode ser criado primeiro, a regra pode referenciar IDs de endereço de palavra-chave dinâmicas que ainda não existem (nesse caso, a regra não &mdash; será imposta).</span><span class="sxs-lookup"><span data-stu-id="e94fb-152">This means that either object can be created first&mdash;the rule can reference dynamic keyword address IDs that don't yet exist (in which case, the rule won't be enforced).</span></span> <span data-ttu-id="e94fb-153">Além disso, você pode excluir um endereço de palavra-chave dinâmico mesmo que ele seja usado por uma regra de firewall.</span><span class="sxs-lookup"><span data-stu-id="e94fb-153">Furthermore, you can delete a dynamic keyword address even if it's in use by a firewall rule.</span></span> <span data-ttu-id="e94fb-154">Este tópico descreve como um administrador pode configurar regras para usar o endereço de palavra-chave dinâmico.</span><span class="sxs-lookup"><span data-stu-id="e94fb-154">This topic outlines how an admin can configure rules to use dynamic keyword address.</span></span>

## <a name="code-examples"></a><span data-ttu-id="e94fb-155">Exemplos de código</span><span class="sxs-lookup"><span data-stu-id="e94fb-155">Code examples</span></span>

<span data-ttu-id="e94fb-156">Para experimentar cada um desses exemplos de código, primeiro Visual Studio e criar um novo projeto com base no modelo de projeto **aplicativo** de console.</span><span class="sxs-lookup"><span data-stu-id="e94fb-156">To try out each of these code examples, first launch Visual Studio and create a new project based on the **Console App** project template.</span></span> <span data-ttu-id="e94fb-157">Você pode simplesmente substituir o conteúdo de `main.cpp` pela listagem de código.</span><span class="sxs-lookup"><span data-stu-id="e94fb-157">You can just replace the contents of `main.cpp` with the code listing.</span></span>

<span data-ttu-id="e94fb-158">A maioria dos exemplos de código usa o [WIL (Bibliotecas de Implementação do Windows).](https://github.com/Microsoft/wil)</span><span class="sxs-lookup"><span data-stu-id="e94fb-158">Most of the code examples use the [Windows Implementation Libraries (WIL)](https://github.com/Microsoft/wil).</span></span> <span data-ttu-id="e94fb-159">Uma maneira conveniente de instalar o WIL é  acessar o Visual Studio, clicar em Projeto Gerenciar Pacotes NuGet... Procurar , digitar ou colar \>  \>  **Microsoft.Windows.ImplementationLibrary**  na caixa de pesquisa, selecionar o item nos resultados da pesquisa e, em seguida, clicar em Instalar para instalar o pacote para esse projeto.</span><span class="sxs-lookup"><span data-stu-id="e94fb-159">A convenient way to install WIL is to go to Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.Windows.ImplementationLibrary** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

> [!NOTE]
> <span data-ttu-id="e94fb-160">Os tipos de ponteiro para as funções gratuitas do NetFw são publicados por meio de , mas uma biblioteca `NetFw.h` de link estático não é publicada.</span><span class="sxs-lookup"><span data-stu-id="e94fb-160">Pointer types for the NetFw free functions are published via `NetFw.h`, but a static-link library isn't published.</span></span> <span data-ttu-id="e94fb-161">Use o padrão GetProcAddress [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)para chamar essas funções, conforme / [](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) mostrado nesses exemplos de código.</span><span class="sxs-lookup"><span data-stu-id="e94fb-161">Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling these functions, as shown in these code examples.</span></span>

### <a name="add-a-dynamic-keyword-address"></a><span data-ttu-id="e94fb-162">Adicionar um endereço de palavra-chave dinâmico</span><span class="sxs-lookup"><span data-stu-id="e94fb-162">Add a dynamic keyword address</span></span>

<span data-ttu-id="e94fb-163">Este exemplo mostra como usar a [**função FWAddDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="e94fb-163">This example shows how to use the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span>

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

### <a name="delete-a-dynamic-keyword-address"></a><span data-ttu-id="e94fb-164">Excluir um endereço de palavra-chave dinâmico</span><span class="sxs-lookup"><span data-stu-id="e94fb-164">Delete a dynamic keyword address</span></span>

<span data-ttu-id="e94fb-165">Este exemplo mostra como usar a [**função FWDeleteDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="e94fb-165">This example shows how to use the [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) function.</span></span>

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

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a><span data-ttu-id="e94fb-166">Enumerar e liberar endereços de palavra-chave dinâmicos por ID</span><span class="sxs-lookup"><span data-stu-id="e94fb-166">Enumerate and free dynamic keyword addresses by ID</span></span>

<span data-ttu-id="e94fb-167">Este exemplo mostra como usar as funções [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) e [**FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)</span><span class="sxs-lookup"><span data-stu-id="e94fb-167">This example shows how to use the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

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

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a><span data-ttu-id="e94fb-168">Enumerar e liberar endereços de palavra-chave dinâmicos por tipo</span><span class="sxs-lookup"><span data-stu-id="e94fb-168">Enumerate and free dynamic keyword addresses by type</span></span>

<span data-ttu-id="e94fb-169">Este exemplo mostra como usar as funções [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) e [**FWFreeDynamicKeywordAddressData0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0)</span><span class="sxs-lookup"><span data-stu-id="e94fb-169">This example shows how to use the [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

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

### <a name="update-dynamic-keyword-addresses"></a><span data-ttu-id="e94fb-170">Atualizar endereços de palavra-chave dinâmicos</span><span class="sxs-lookup"><span data-stu-id="e94fb-170">Update dynamic keyword addresses</span></span>

<span data-ttu-id="e94fb-171">Este exemplo mostra como usar a [**função FWUpdateDynamicKeywordAddress0.**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)</span><span class="sxs-lookup"><span data-stu-id="e94fb-171">This example shows how to use the [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) function.</span></span>

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

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a><span data-ttu-id="e94fb-172">Assinar e manipular notificações de alteração de endereço de palavra-chave dinâmica</span><span class="sxs-lookup"><span data-stu-id="e94fb-172">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="e94fb-173">Este exemplo mostra como usar as funções [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) e [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) e o [**retorno FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e94fb-173">This example shows how to use the [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) and [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) functions, and the [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) callback.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="e94fb-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e94fb-174">Related topics</span></span>

* [<span data-ttu-id="e94fb-175">Referência de palavras-chave dinâmicas do firewall</span><span class="sxs-lookup"><span data-stu-id="e94fb-175">Firewall dynamic keywords reference</span></span>](firewall-dynamic-keywords-reference.md)
