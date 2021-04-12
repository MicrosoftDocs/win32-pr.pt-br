---
title: Desativando a segurança da chamada
description: A chamada de segurança determina se um cliente tem permissão para chamar os métodos de um servidor. Há duas maneiras de desabilitar a segurança de chamada um envolve o uso de Dcomcnfg.exe para modificar o registro e o outro requer chamadas para CoInitializeSecurity.
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363773"
---
# <a name="turning-off-call-security"></a><span data-ttu-id="97d1c-104">Desativando a segurança da chamada</span><span class="sxs-lookup"><span data-stu-id="97d1c-104">Turning Off Call Security</span></span>

<span data-ttu-id="97d1c-105">A chamada de segurança determina se um cliente tem permissão para chamar os métodos de um servidor.</span><span class="sxs-lookup"><span data-stu-id="97d1c-105">Call security determines whether a client has permission to call a server's methods.</span></span> <span data-ttu-id="97d1c-106">Há duas maneiras de desabilitar a segurança da chamada: uma envolve o uso de Dcomcnfg.exe para modificar o registro e o outro requer chamadas para [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="97d1c-106">There are two ways to disable call security: One involves using Dcomcnfg.exe to modify the registry, and the other requires calls to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

-   [<span data-ttu-id="97d1c-107">Desligando a segurança da chamada usando DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="97d1c-107">Turning Off Call Security Using DCOMCNFG</span></span>](#turning-off-call-security-using-dcomcnfg)
-   [<span data-ttu-id="97d1c-108">Desligando a segurança da chamada de forma programática</span><span class="sxs-lookup"><span data-stu-id="97d1c-108">Turning Off Call Security Programmatically</span></span>](#turning-off-call-security-programmatically)
-   [<span data-ttu-id="97d1c-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97d1c-109">Related topics</span></span>](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a><span data-ttu-id="97d1c-110">Desligando a segurança da chamada usando DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="97d1c-110">Turning Off Call Security Using DCOMCNFG</span></span>

<span data-ttu-id="97d1c-111">A segurança da chamada pode ser desativada com mais facilidade usando Dcomcnfg.exe para modificar o registro.</span><span class="sxs-lookup"><span data-stu-id="97d1c-111">Call security can most easily be turned off by using Dcomcnfg.exe to modify the registry.</span></span> <span data-ttu-id="97d1c-112">No entanto, o uso de Dcomcnfg.exe para desativar a segurança só funcionará se o cliente e o servidor não chamarem [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="97d1c-112">However, using Dcomcnfg.exe to turn security off will work only if both the client and the server do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="97d1c-113">Isso ocorre porque quando **CoInitializeSecurity** é chamado, o DCOM ignora as configurações do registro e usa os valores fornecidos para **CoInitializeSecurity** em vez disso.</span><span class="sxs-lookup"><span data-stu-id="97d1c-113">This is because when **CoInitializeSecurity** is called, DCOM ignores the registry settings and uses the values supplied to **CoInitializeSecurity** instead.</span></span>

<span data-ttu-id="97d1c-114">Para desativar a segurança com Dcomcnfg.exe, o cliente e o servidor devem definir seus níveis de autenticação como nenhum.</span><span class="sxs-lookup"><span data-stu-id="97d1c-114">To turn off security with Dcomcnfg.exe, both the client and the server must set their Authentication Levels to None.</span></span> <span data-ttu-id="97d1c-115">As etapas a seguir devem ser concluídas:</span><span class="sxs-lookup"><span data-stu-id="97d1c-115">The following steps must be completed:</span></span>

1.  <span data-ttu-id="97d1c-116">Execute Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="97d1c-116">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="97d1c-117">Na página **aplicativos** , selecione o aplicativo que representa o servidor.</span><span class="sxs-lookup"><span data-stu-id="97d1c-117">On the **Applications** page, select the application that represents the server.</span></span> <span data-ttu-id="97d1c-118">Clique no botão **Propriedades** (ou clique duas vezes no aplicativo selecionado).</span><span class="sxs-lookup"><span data-stu-id="97d1c-118">Click the **Properties** button (or double-click the selected application).</span></span>
3.  <span data-ttu-id="97d1c-119">Clique na guia **Geral**.</span><span class="sxs-lookup"><span data-stu-id="97d1c-119">Click the **General** tab.</span></span>
4.  <span data-ttu-id="97d1c-120">Na caixa de listagem **nível de autenticação padrão** , selecione **(nenhum)**.</span><span class="sxs-lookup"><span data-stu-id="97d1c-120">From the **Default Authentication Level** list box, select **(None)**.</span></span>
5.  <span data-ttu-id="97d1c-121">Clique no botão **aplicar** para aplicar as alterações; no entanto, as alterações não são aplicadas a nenhuma instância em execução do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97d1c-121">Click the **Apply** button to apply changes; however, changes are not applied to any running instances of the application.</span></span>
6.  <span data-ttu-id="97d1c-122">Se o cliente aparecer na lista na página *aplicativos* , repita as etapas de 2 a 5, escolhendo o cliente em vez do servidor para a etapa 2.</span><span class="sxs-lookup"><span data-stu-id="97d1c-122">If the client appears on the list on the *Applications* page, repeat steps 2 through 5, choosing the client instead of the server for step 2.</span></span> <span data-ttu-id="97d1c-123">Em seguida, clique no botão **OK**.</span><span class="sxs-lookup"><span data-stu-id="97d1c-123">Then click the **OK** button.</span></span> <span data-ttu-id="97d1c-124">Se o cliente não estiver na lista, você poderá executar uma das três ações a seguir:</span><span class="sxs-lookup"><span data-stu-id="97d1c-124">If the client is not on the list, you can do one of the following three things:</span></span>
    -   <span data-ttu-id="97d1c-125">Você pode definir o nível de autenticação do cliente como nenhum em todo o computador usando Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="97d1c-125">You can set the client's Authentication Level to None on a computer-wide basis by using Dcomcnfg.exe.</span></span> <span data-ttu-id="97d1c-126">(Consulte o aviso e o procedimento abaixo.)</span><span class="sxs-lookup"><span data-stu-id="97d1c-126">(See the warning and the procedure below.)</span></span>
    -   <span data-ttu-id="97d1c-127">Você pode definir o nível de autenticação do cliente como nenhum programaticamente.</span><span class="sxs-lookup"><span data-stu-id="97d1c-127">You can set the client's authentication level to None programmatically.</span></span>
    -   <span data-ttu-id="97d1c-128">Você pode criar uma chave [AppID](appid-key.md) para o cliente para indicar um nível de autenticação de nenhum.</span><span class="sxs-lookup"><span data-stu-id="97d1c-128">You can create an [AppID](appid-key.md) key for the client to indicate an authentication level of None.</span></span> <span data-ttu-id="97d1c-129">(Consulte [definir Process-Wide segurança por meio do registro](setting-processwide-security-through-the-registry.md).)</span><span class="sxs-lookup"><span data-stu-id="97d1c-129">(See [Setting Process-Wide Security Through the Registry](setting-processwide-security-through-the-registry.md).)</span></span>

<span data-ttu-id="97d1c-130">Para definir o nível de autenticação como None em todo o computador:</span><span class="sxs-lookup"><span data-stu-id="97d1c-130">To set the Authentication Level to None on a computer-wide basis:</span></span>

> [!Note]  
> <span data-ttu-id="97d1c-131">Definir o nível de autenticação em todo o computador como nenhum é extremamente inseguro.</span><span class="sxs-lookup"><span data-stu-id="97d1c-131">Setting the computer-wide Authentication Level to None is extremely unsecure.</span></span>

 

1.  <span data-ttu-id="97d1c-132">Execute Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="97d1c-132">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="97d1c-133">Escolha a guia **propriedades padrão** .</span><span class="sxs-lookup"><span data-stu-id="97d1c-133">Choose the **Default Properties** tab.</span></span>
3.  <span data-ttu-id="97d1c-134">Na caixa de listagem **nível de autenticação padrão** , escolha **(nenhum)**.</span><span class="sxs-lookup"><span data-stu-id="97d1c-134">From the **Default Authentication Level** list box, choose **(None)**.</span></span>
4.  <span data-ttu-id="97d1c-135">Clique no botão **OK**.</span><span class="sxs-lookup"><span data-stu-id="97d1c-135">Click the **OK** button.</span></span>

## <a name="turning-off-call-security-programmatically"></a><span data-ttu-id="97d1c-136">Desligando a segurança da chamada de forma programática</span><span class="sxs-lookup"><span data-stu-id="97d1c-136">Turning Off Call Security Programmatically</span></span>

<span data-ttu-id="97d1c-137">Para desativar a segurança de chamada por meio de programação, o cliente e o servidor devem chamar **CoInitializeSecurity**, definindo o nível de autenticação no parâmetro *dwAuthnLevel* como RPC \_ C \_ Authn \_ nível \_ None.</span><span class="sxs-lookup"><span data-stu-id="97d1c-137">To turn call security off programmatically, both the client and the server must call **CoInitializeSecurity**, setting the authentication level in the *dwAuthnLevel* parameter to RPC\_C\_AUTHN\_LEVEL\_NONE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97d1c-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="97d1c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97d1c-139">Desativando a segurança de ativação</span><span class="sxs-lookup"><span data-stu-id="97d1c-139">Turning Off Activation Security</span></span>](turning-off-activation-security.md)
</dt> </dl>

 

 




