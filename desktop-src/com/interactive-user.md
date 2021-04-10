---
title: Usuário interativo
description: O usuário interativo é o usuário que está conectado no momento ao computador em que o servidor COM está em execução.
ms.assetid: 6d43842c-0ad1-4563-b50c-5024bda480f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7fc8aeb5fd9674c09b40f6c46e4e173f5965a9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294521"
---
# <a name="interactive-user"></a><span data-ttu-id="c1033-103">Usuário interativo</span><span class="sxs-lookup"><span data-stu-id="c1033-103">Interactive User</span></span>

<span data-ttu-id="c1033-104">O *usuário interativo* é o usuário que está conectado no momento ao computador em que o servidor com está em execução.</span><span class="sxs-lookup"><span data-stu-id="c1033-104">The *interactive user* is the user that is currently logged on to the computer where the COM server is running.</span></span> <span data-ttu-id="c1033-105">Se a identidade for definida para ser o usuário interativo, todos os clientes usarão a mesma instância do servidor se o servidor registrar sua fábrica de classes como um uso múltiplo.</span><span class="sxs-lookup"><span data-stu-id="c1033-105">If the identity is set to be the interactive user, all clients use the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="c1033-106">Se nenhum usuário estiver conectado, o servidor não será executado.</span><span class="sxs-lookup"><span data-stu-id="c1033-106">If no user is logged on, the server will not run.</span></span> <span data-ttu-id="c1033-107">Se o servidor tiver uma GUI (interface gráfica do usuário) que o cliente precisa ver, você deverá usar o usuário interativo para a identidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="c1033-107">If the server has a graphical user interface (GUI) that the client needs to see, you should use interactive user for the server's identity.</span></span> <span data-ttu-id="c1033-108">No entanto, a escolha dessa identidade tem alguns riscos de segurança porque o servidor é executado sob a identidade do usuário conectado sem o conhecimento ou consentimento do usuário conectado.</span><span class="sxs-lookup"><span data-stu-id="c1033-108">However, choosing this identity carries some security risks because the server runs under the identity of the logged on user without the logged on user's knowledge or consent.</span></span> <span data-ttu-id="c1033-109">Além disso, um aplicativo de serviço não pode exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c1033-109">In addition, a service application cannot display a user interface.</span></span> <span data-ttu-id="c1033-110">Para obter mais informações, consulte [serviços interativos](/windows/desktop/Services/interactive-services).</span><span class="sxs-lookup"><span data-stu-id="c1033-110">For more information, see [Interactive Services](/windows/desktop/Services/interactive-services).</span></span>

<span data-ttu-id="c1033-111">Se um servidor COM estiver configurado para ser executado como usuário interativo, em um ambiente de serviços de terminal, o servidor será iniciado na sessão interativa que corresponde à identidade de usuário do cliente.</span><span class="sxs-lookup"><span data-stu-id="c1033-111">If a COM server is configured to run as the interactive user, in a terminal services environment, the server will be launched in the interactive session that matches the client's user identity.</span></span> <span data-ttu-id="c1033-112">No entanto, o aplicativo cliente pode usar o moniker de sessão para fazer referência a um objeto fornecido pelo servidor em uma sessão que não corresponde à identidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="c1033-112">However, the client application can use the session moniker to reference an object provided by the server in a session that does not match the client identity.</span></span> <span data-ttu-id="c1033-113">Quando isso é usado, o aplicativo cliente pode especificar qualquer sessão; nesse caso, o servidor será executado como o usuário que possui a sessão, não o usuário que está iniciando.</span><span class="sxs-lookup"><span data-stu-id="c1033-113">When this is used, the client application can specify any session, in which case the server will run as the user who owns the session, not the launching user.</span></span> <span data-ttu-id="c1033-114">As permissões de acesso padrão nesse cenário não permitem que o usuário de inicialização Chame métodos no servidor.</span><span class="sxs-lookup"><span data-stu-id="c1033-114">The default access permissions in this scenario would not allow the launching user to call methods on the server.</span></span> <span data-ttu-id="c1033-115">No entanto, os seguintes riscos de segurança permanecem:</span><span class="sxs-lookup"><span data-stu-id="c1033-115">However, the following security risks remain:</span></span>

-   <span data-ttu-id="c1033-116">Se o servidor COM expõe interfaces que não são controladas pelo COM, como portas TCP, pipes nomeados, portas LPC, seções de memória compartilhada e assim por diante, elas podem ser usadas pelo usuário que está iniciando para influenciar o servidor.</span><span class="sxs-lookup"><span data-stu-id="c1033-116">If the COM server exposes interfaces that are not controlled by COM, such as TCP ports, named pipes, LPC ports, shared memory sections, and so on, these could be used by the launching user to influence the server.</span></span> <span data-ttu-id="c1033-117">Objetos COM configurados para execução como o usuário interativo devem reduzir essa superfície de ataque o máximo possível.</span><span class="sxs-lookup"><span data-stu-id="c1033-117">COM objects configured to run as the interactive user should reduce this attack surface as much as possible.</span></span>
-   <span data-ttu-id="c1033-118">Objetos COM são livres para definir suas próprias permissões de acesso.</span><span class="sxs-lookup"><span data-stu-id="c1033-118">COM objects are free to set their own access permissions.</span></span> <span data-ttu-id="c1033-119">Se o objeto definir permissões de acesso, em seu registro AppID ou chamando [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), para permitir o acesso de usuário de inicialização, o usuário poderá iniciar o servidor para ser executado como outro usuário e, em seguida, acessar o objeto.</span><span class="sxs-lookup"><span data-stu-id="c1033-119">If the object sets access permissions, either in its AppID registration or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), to allow the launching user access, the user would be able to launch the server to run as another user, then access the object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1033-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1033-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1033-121">Identidade do Aplicativo</span><span class="sxs-lookup"><span data-stu-id="c1033-121">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="c1033-122">Iniciando usuário</span><span class="sxs-lookup"><span data-stu-id="c1033-122">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="c1033-123">Identidade do serviço</span><span class="sxs-lookup"><span data-stu-id="c1033-123">Service Identity</span></span>](service-identity.md)
</dt> <dt>

[<span data-ttu-id="c1033-124">Usuário especificado</span><span class="sxs-lookup"><span data-stu-id="c1033-124">Specified User</span></span>](specified-user.md)
</dt> </dl>

 

 