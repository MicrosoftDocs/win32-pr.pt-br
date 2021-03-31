---
title: Suporte ao host de segurança RAS
description: O Windows NT 4,0 fornece uma maneira de uma DLL de segurança de RAS de terceiros para aprimorar os recursos de segurança RAS internos. O Windows 95 não oferece esse suporte.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Suporte a host, RAS
- Suporte ao host de segurança, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636315"
---
# <a name="ras-security-host-support"></a><span data-ttu-id="13768-106">Suporte ao host de segurança RAS</span><span class="sxs-lookup"><span data-stu-id="13768-106">RAS Security Host Support</span></span>

<span data-ttu-id="13768-107">O Windows NT 4,0 fornece uma maneira de uma DLL de segurança de RAS de terceiros para aprimorar os recursos de segurança RAS internos.</span><span class="sxs-lookup"><span data-stu-id="13768-107">Windows NT 4.0 provides a way for a third-party RAS security DLL to enhance the built-in RAS security features.</span></span> <span data-ttu-id="13768-108">O Windows 95 não oferece esse suporte.</span><span class="sxs-lookup"><span data-stu-id="13768-108">Windows 95 does not provide this support.</span></span>

<span data-ttu-id="13768-109">Um servidor RAS do Windows NT/Windows 2000 fornece mecanismos de segurança para validar o acesso à rede de usuários remotos.</span><span class="sxs-lookup"><span data-stu-id="13768-109">A Windows NT/Windows 2000 RAS server provides security mechanisms for validating the network access of remote users.</span></span> <span data-ttu-id="13768-110">Quando um servidor RAS recebe uma chamada, ele valida as credenciais do usuário em relação ao banco de dados de conta local ou de domínio.</span><span class="sxs-lookup"><span data-stu-id="13768-110">When a RAS server receives a call, it validates the user's credentials against the local or domain account database.</span></span> <span data-ttu-id="13768-111">O RAS também dá suporte à segurança de retorno de chamada, na qual o servidor RAS desliga e, em seguida, chama o usuário remoto para estabelecer a conexão.</span><span class="sxs-lookup"><span data-stu-id="13768-111">RAS also supports call-back security, in which the RAS server hangs up and then calls back to the remote user to establish the connection.</span></span> <span data-ttu-id="13768-112">Para redes em que esse nível de segurança não é suficiente, você pode instalar uma DLL de segurança de RAS de terceiros.</span><span class="sxs-lookup"><span data-stu-id="13768-112">For networks in which this level of security is not enough, you can install a third-party RAS security DLL.</span></span> <span data-ttu-id="13768-113">A DLL de segurança pode autenticar um usuário remoto, lendo informações de segurança de um banco de dados diferente do banco de dados da conta de usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="13768-113">The security DLL can then authenticate a remote user by reading security information from a database other than the standard user account database.</span></span>

<span data-ttu-id="13768-114">Quando o servidor RAS recebe uma chamada, ele invoca a DLL de segurança para autenticar o usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="13768-114">When the RAS server receives a call, it invokes the security DLL to authenticate the remote user.</span></span> <span data-ttu-id="13768-115">O suporte ao host de segurança RAS fornece um mecanismo para que a DLL de segurança se comunique com o usuário remoto por meio de uma janela de terminal no computador remoto.</span><span class="sxs-lookup"><span data-stu-id="13768-115">The RAS security host support provides a mechanism for the security DLL to communicate with the remote user through a terminal window on the remote computer.</span></span> <span data-ttu-id="13768-116">Em um cenário típico, a DLL de segurança solicita o nome de logon do usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="13768-116">In a typical scenario, the security DLL asks for the logon name of the remote user.</span></span> <span data-ttu-id="13768-117">Em seguida, a DLL usa seu banco de dados de segurança privada para formular um desafio para enviar ao terminal remoto.</span><span class="sxs-lookup"><span data-stu-id="13768-117">The DLL then uses its private security database to formulate a challenge to send to the remote terminal.</span></span> <span data-ttu-id="13768-118">Por exemplo, o desafio pode ser um código que o usuário deve fornecer como entrada para um leitor de Cardkey.</span><span class="sxs-lookup"><span data-stu-id="13768-118">For example, the challenge could be a code that the user must provide as input to a cardkey reader.</span></span> <span data-ttu-id="13768-119">O leitor do Cardkey, em seguida, exibe uma resposta que o usuário remoto digita na janela do terminal.</span><span class="sxs-lookup"><span data-stu-id="13768-119">The cardkey reader then displays a response that the remote user types in the terminal window.</span></span> <span data-ttu-id="13768-120">Em seguida, a DLL de segurança valida a resposta em relação às informações do usuário no banco de dados de segurança privada.</span><span class="sxs-lookup"><span data-stu-id="13768-120">The security DLL then validates the response against the user's information in the private security database.</span></span>

<span data-ttu-id="13768-121">Se a DLL de segurança autenticar o usuário remoto, o servidor RAS executará sua própria autenticação.</span><span class="sxs-lookup"><span data-stu-id="13768-121">If the security DLL authenticates the remote user, the RAS server performs its own authentication.</span></span> <span data-ttu-id="13768-122">Isso garante que a segurança RAS sempre autentique um usuário remoto, mesmo que uma DLL de segurança esteja instalada que conceda acesso a todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="13768-122">This ensures that RAS security always authenticates a remote user, even if a security DLL is installed that grants access to all users.</span></span>

> [!Note]  
> <span data-ttu-id="13768-123">O Windows NT/Windows 2000 atualmente fornece suporte ao host de segurança RAS somente para conexões de modem assíncronas; outros tipos de conexões, como Ethernet (que não é uma conexão de modem), VPN (que também não é uma conexão de modem) ou ISDN (que é síncrono), não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="13768-123">Windows NT/Windows 2000 currently provides RAS security host support only for asynchronous modem connections; other types of connections such as Ethernet (which is not a modem connection), VPN (which is also not a modem connection), or ISDN (which is synchronous), are not supported.</span></span>

 

 

 




