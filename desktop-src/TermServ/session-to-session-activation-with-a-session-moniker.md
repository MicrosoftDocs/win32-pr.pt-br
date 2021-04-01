---
title: Ativação de sessão para sessão com um moniker de sessão
description: A ativação de sessão para sessão (também chamada de ativação entre sessões) permite que um processo de cliente inicie (ative) um processo de servidor local em uma sessão especificada.
ms.assetid: d405c276-040b-4cde-aeb2-482a25e2867f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2714f3dbe7b23c8b7f04d4271018891960b87f76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641679"
---
# <a name="session-to-session-activation-with-a-session-moniker"></a><span data-ttu-id="19a22-103">Ativação de sessão para sessão com um moniker de sessão</span><span class="sxs-lookup"><span data-stu-id="19a22-103">Session-to-Session Activation with a Session Moniker</span></span>

<span data-ttu-id="19a22-104">A ativação de sessão para sessão (também chamada de ativação entre sessões) permite que um processo de cliente inicie (ative) um processo de servidor local em uma sessão especificada.</span><span class="sxs-lookup"><span data-stu-id="19a22-104">Session-to-session activation (also called cross-session activation) allows a client process to start (activate) a local server process on a specified session.</span></span> <span data-ttu-id="19a22-105">Esse recurso está disponível para aplicativos que são configurados para execução no contexto de segurança do usuário interativo, também conhecido como o modo de ativação de objeto "RunAs Interactive User".</span><span class="sxs-lookup"><span data-stu-id="19a22-105">This feature is available for applications that are configured to run in the security context of the interactive user, also known as the "RunAs Interactive User" object activation mode.</span></span> <span data-ttu-id="19a22-106">Para obter mais informações sobre contextos de segurança, consulte [o contexto de segurança do cliente](/windows/desktop/SecAuthZ/the-client-security-context).</span><span class="sxs-lookup"><span data-stu-id="19a22-106">For more information about security contexts, see [The Client's Security Context](/windows/desktop/SecAuthZ/the-client-security-context).</span></span>

<span data-ttu-id="19a22-107">O COM distribuído (DCOM) permite a ativação de objeto por sessão usando um [moniker de sessão](session-monikers.md)fornecido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="19a22-107">Distributed COM (DCOM) enables object activation on a per-session basis by using a system-supplied [Session Moniker](session-monikers.md).</span></span> <span data-ttu-id="19a22-108">Outros monikers fornecidos pelo sistema incluem [identificadores de arquivo](../com/file-monikers.md), [monikers de item](../com/item-monikers.md), [monikers compostos](../com/composite-monikers.md)genéricos, [antimonikers](../com/anti-monikers.md), [monikers de ponteiro](../com/pointer-monikers.md)e [identificadores de URL](../com/url-monikers.md).</span><span class="sxs-lookup"><span data-stu-id="19a22-108">Other system-supplied monikers include [file monikers](../com/file-monikers.md), [item monikers](../com/item-monikers.md), generic [composite monikers](../com/composite-monikers.md), [anti-monikers](../com/anti-monikers.md), [pointer monikers](../com/pointer-monikers.md), and [URL monikers](../com/url-monikers.md).</span></span>

<span data-ttu-id="19a22-109">Para poder usar o moniker da sessão, o aplicativo DCOM deve ser definido para ser executado como usuário interativo.</span><span class="sxs-lookup"><span data-stu-id="19a22-109">To be able to use the session moniker, the DCOM application must be set to run as the interactive user.</span></span> <span data-ttu-id="19a22-110">Isso pode ser definido usando a ferramenta administrativa serviços de componentes, exibindo as propriedades do aplicativo DCOM e selecionando **o usuário interativo** na guia **identidade** . Para obter mais informações sobre os possíveis riscos de segurança associados à definição de um aplicativo DCOM para ser executado como usuário interativo em um ambiente de Serviços de Área de Trabalho Remota, consulte a seção "identidade do aplicativo (COM)" da documentação COM do SDK (Software Development Kit) da plataforma.</span><span class="sxs-lookup"><span data-stu-id="19a22-110">This can be set by using the Component Services Administrative tool, viewing the Properties of the DCOM application, and selecting **The interactive user** on the **Identity** tab. For more information about the possible security risks associated with setting a DCOM application to run as the interactive user in a Remote Desktop Services environment, see the "Application Identity (COM)" section of the COM documentation in the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="19a22-111">Se qualquer outro tipo de usuário for selecionado para executar o aplicativo, o moniker da sessão será ignorado pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="19a22-111">If any other type of user is selected to run the application, the session moniker will be ignored by the application.</span></span> <span data-ttu-id="19a22-112">O moniker da sessão também é ignorado por aplicativos do servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="19a22-112">The session moniker is also ignored by COM+ server applications.</span></span> <span data-ttu-id="19a22-113">Para obter mais informações sobre outros métodos para selecionar o tipo de usuário para executar o aplicativo, consulte a documentação COM no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="19a22-113">For more information about other methods for selecting the type of user to run the application, see the COM documentation in the Platform SDK.</span></span>

<span data-ttu-id="19a22-114">Para criar um moniker de sessão, você deve compor a ID de sessão da sessão de Serviços de Área de Trabalho Remota com um moniker de classe que especifica a ID de classe do servidor de processo.</span><span class="sxs-lookup"><span data-stu-id="19a22-114">To create a session moniker, you must compose the session ID of the Remote Desktop Services session with a class moniker that specifies the process server's class ID.</span></span>

<span data-ttu-id="19a22-115">**Para criar um moniker de sessão**</span><span class="sxs-lookup"><span data-stu-id="19a22-115">**To create a session moniker**</span></span>

1.  <span data-ttu-id="19a22-116">Prefixe o nome de exibição do moniker da classe com o nome de exibição do moniker da sessão usando a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="19a22-116">Prefix the display name of the class moniker with the display name of the session moniker by using the following syntax:</span></span>

    ``` syntax
    "Session:[digits]!clsid:[class id]"
    ```

    <span data-ttu-id="19a22-117">em que *dígitos* representa a ID da sessão na qual o processo do servidor será iniciado e onde ID da *classe* representa a ID de classe do servidor.</span><span class="sxs-lookup"><span data-stu-id="19a22-117">where *digits* represents the session ID of the session on which the server process will be started, and where *class id* represents the class ID of the server.</span></span> <span data-ttu-id="19a22-118">Observe que a ID de sessão é um número de base 10.</span><span class="sxs-lookup"><span data-stu-id="19a22-118">Note that the session ID is a base-10 number.</span></span>

    <span data-ttu-id="19a22-119">Para computadores que executam o Windows XP ou posterior, usar a seguinte sintaxe resultará em COM enviando a ativação para a sessão de console físico ativa atualmente, independentemente de sua ID de sessão:</span><span class="sxs-lookup"><span data-stu-id="19a22-119">For computers that are running Windows XP or later, using the following syntax will result in COM sending the activation to the currently active physical console session, whatever its session ID is:</span></span>

    ``` syntax
    "Session:Console!clsid:[class id]"
    ```

2.  <span data-ttu-id="19a22-120">Depois de criar o moniker da sessão, você pode passar o resultado para a função [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) ou para a função [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="19a22-120">After you have created the session moniker, you can pass the result to either the [**MkParseDisplayName**](/windows/desktop/api/objbase/nf-objbase-mkparsedisplayname) function or the [MkParseDisplayNameEx](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775113(v=vs.85)) function.</span></span>

<span data-ttu-id="19a22-121">Você pode usar um moniker de sessão da mesma maneira que usaria qualquer outro moniker.</span><span class="sxs-lookup"><span data-stu-id="19a22-121">You can use a session moniker in the same way as you would use any other moniker.</span></span>

<span data-ttu-id="19a22-122">Para obter um exemplo de código que demonstra como ativar um processo de servidor local em uma sessão especificada, consulte [usando um moniker de sessão](using-a-session-moniker.md).</span><span class="sxs-lookup"><span data-stu-id="19a22-122">For a code sample that demonstrates how to activate a local server process on a specified session, see [Using a Session Moniker](using-a-session-moniker.md).</span></span>

<span data-ttu-id="19a22-123">Para obter mais informações sobre a ativação de objeto, identificadores de classe e identificadores de classes fornecidos pelo sistema, consulte a documentação COM no SDK da plataforma.</span><span class="sxs-lookup"><span data-stu-id="19a22-123">For more information about object activation, system-supplied monikers and class monikers, see the COM documentation in the Platform SDK.</span></span>

> [!Note]  
> <span data-ttu-id="19a22-124">Os processos criados entre as sessões têm um limite superior ao tamanho do bloco de ambiente.</span><span class="sxs-lookup"><span data-stu-id="19a22-124">Processes that are created across sessions have an upper limit on the size of the environment block.</span></span> <span data-ttu-id="19a22-125">Esse limite é de cerca de 4 KB, mas pode ser maior ou menor dependendo de quais outras informações são necessárias para criar o processo (por exemplo, nomes de arquivo, diretórios e parâmetros para o novo processo).</span><span class="sxs-lookup"><span data-stu-id="19a22-125">This limit is around 4 KB, but it can be larger or smaller depending on what other information is needed to create the process (for example file names, directories, and parameters for the new process).</span></span>

 

 

 