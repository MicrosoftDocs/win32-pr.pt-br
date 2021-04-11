---
description: O encobrimento é uma extensão da representação que permite um melhor controle sobre como o COM representa um cliente em um proxy. Como muitas formas de segurança de WMI, você define o encobrimento por meio das interfaces CoSetProxyBlanket e CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementando o encobrimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170613"
---
# <a name="implementing-cloaking"></a><span data-ttu-id="529b4-104">Implementando o encobrimento</span><span class="sxs-lookup"><span data-stu-id="529b4-104">Implementing Cloaking</span></span>

<span data-ttu-id="529b4-105">O encobrimento é uma extensão da representação que permite um melhor controle sobre como o COM representa um cliente em um proxy.</span><span class="sxs-lookup"><span data-stu-id="529b4-105">Cloaking is an extension to impersonation that allows for better control over how COM impersonates a client over a proxy.</span></span> <span data-ttu-id="529b4-106">Como muitas formas de segurança de WMI, você define o encobrimento por meio das interfaces [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .</span><span class="sxs-lookup"><span data-stu-id="529b4-106">Like many forms of WMI security, you set cloaking through the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) interfaces.</span></span>

<span data-ttu-id="529b4-107">COM fornece as seguintes formas de encobrimento:</span><span class="sxs-lookup"><span data-stu-id="529b4-107">COM provides the following forms of cloaking:</span></span>

-   <span data-ttu-id="529b4-108">Estático</span><span class="sxs-lookup"><span data-stu-id="529b4-108">Static</span></span>

    <span data-ttu-id="529b4-109">COM estabelece a identidade do token pelo thread ou token de processo na primeira chamada para o proxy.</span><span class="sxs-lookup"><span data-stu-id="529b4-109">COM establishes the token identity by the thread or process token on the first call to the proxy.</span></span> <span data-ttu-id="529b4-110">Se você usar o encobrimento estático com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), defina a identidade do proxy para a vida útil do proxy.</span><span class="sxs-lookup"><span data-stu-id="529b4-110">If you use static cloaking with [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), you set the identity of the proxy for the life of the proxy.</span></span>

-   <span data-ttu-id="529b4-111">Dinâmico</span><span class="sxs-lookup"><span data-stu-id="529b4-111">Dynamic</span></span>

    <span data-ttu-id="529b4-112">COM restabelece a identidade do token do thread ou do token de processo em cada chamada para o proxy.</span><span class="sxs-lookup"><span data-stu-id="529b4-112">COM reestablishes the token identity from the thread or process token on each call to the proxy.</span></span> <span data-ttu-id="529b4-113">Como o COM verifica a identidade em cada chamada, o encobrimento dinâmico permite um controle mais preciso sobre a identidade do cliente.</span><span class="sxs-lookup"><span data-stu-id="529b4-113">Because COM checks the identity on each call, dynamic cloaking allows for finer control over the client identity.</span></span> <span data-ttu-id="529b4-114">No entanto, o encobrimento dinâmico é menos eficiente do que o encobrimento estático.</span><span class="sxs-lookup"><span data-stu-id="529b4-114">However, dynamic cloaking is less efficient than static cloaking.</span></span>

<span data-ttu-id="529b4-115">Quando você define o encobrimento em conjunto com o nível de delegação de representação, um servidor pode propagar a identidade de um cliente entre servidores, mesmo que os servidores sejam remotos.</span><span class="sxs-lookup"><span data-stu-id="529b4-115">When you set cloaking in conjunction with the delegation level of impersonation, a server can propagate the identity of a client across servers, even if the servers are remote.</span></span> <span data-ttu-id="529b4-116">Se você não habilitar o encobrimento, o COM fará qualquer chamada de um servidor local para um servidor remoto sob o contexto do processo do servidor real.</span><span class="sxs-lookup"><span data-stu-id="529b4-116">If you do not enable cloaking, COM makes any call from a local server to a remote server under the context of the actual server process.</span></span>

<span data-ttu-id="529b4-117">O encobrimento permite que o WMI represente um cliente para acessar recursos de rede locais e remotos entre vários limites de computador.</span><span class="sxs-lookup"><span data-stu-id="529b4-117">Cloaking lets WMI impersonate a client to access both local and remote network resources across multiple computer boundaries.</span></span> <span data-ttu-id="529b4-118">O WMI pode passar a identidade do cliente para servidores locais e remotos, como outras instâncias remotas do WMI.</span><span class="sxs-lookup"><span data-stu-id="529b4-118">WMI can pass the identity of the client to local and remote servers, such as other remote instances of WMI.</span></span> <span data-ttu-id="529b4-119">Em seguida, esses servidores remotos podem executar operações no contexto inicial do cliente.</span><span class="sxs-lookup"><span data-stu-id="529b4-119">Those remote servers can then perform operations under the initial client context.</span></span>

<span data-ttu-id="529b4-120">O procedimento a seguir descreve como usar o encobrimento e a delegação em conjunto.</span><span class="sxs-lookup"><span data-stu-id="529b4-120">The following procedure describes how to use cloaking and delegation together.</span></span>

<span data-ttu-id="529b4-121">**Para usar o encobrimento e a delegação em conjunto**</span><span class="sxs-lookup"><span data-stu-id="529b4-121">**To use cloaking and delegation together**</span></span>

1.  <span data-ttu-id="529b4-122">Defina o serviço de autenticação como Kerberos.</span><span class="sxs-lookup"><span data-stu-id="529b4-122">Set the authentication service to Kerberos.</span></span>

    <span data-ttu-id="529b4-123">O Kerberos é o único serviço de autenticação que dá suporte ao encobrimento e à delegação remotas.</span><span class="sxs-lookup"><span data-stu-id="529b4-123">Kerberos is the only authentication service that supports remote cloaking and delegation.</span></span> <span data-ttu-id="529b4-124">Isso significa que o encobrimento e a delegação só podem ser usados em servidores remotos.</span><span class="sxs-lookup"><span data-stu-id="529b4-124">This means that cloaking and delegation can only be used on remote servers.</span></span>

2.  <span data-ttu-id="529b4-125">Marque a conta de logon do servidor como "confiável para delegação" nos serviços de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="529b4-125">Mark the server login account as "Trusted for Delegation" in the Active Directory services.</span></span>
3.  <span data-ttu-id="529b4-126">Marque a conta de logon do cliente como "a conta é confidencial e não pode ser delegada" em serviços Active Directorys.</span><span class="sxs-lookup"><span data-stu-id="529b4-126">Mark the client login account as "Account is sensitive and cannot be delegated" in Active Directory services.</span></span>

<span data-ttu-id="529b4-127">Por exemplo, uma chamada para o provedor de exibição, que pode retornar objetos de várias instâncias do WMI em vários computadores, pode se beneficiar da delegação e do encobrimento.</span><span class="sxs-lookup"><span data-stu-id="529b4-127">For example, a call to the View Provider, which may return objects from multiple instances of WMI on multiple computers, can benefit from delegation and cloaking.</span></span>

 

 
