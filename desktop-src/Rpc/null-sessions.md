---
title: Sessões nulas
description: Às vezes, uma chamada que chega na sessão nula pode aparecer como uma chamada autenticada.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453700"
---
# <a name="null-sessions"></a><span data-ttu-id="416fd-103">Sessões nulas</span><span class="sxs-lookup"><span data-stu-id="416fd-103">Null Sessions</span></span>

<span data-ttu-id="416fd-104">Às vezes, uma chamada que chega na sessão nula pode aparecer como uma chamada autenticada.</span><span class="sxs-lookup"><span data-stu-id="416fd-104">Sometimes a call arriving on the null session can appear like an authenticated call.</span></span> <span data-ttu-id="416fd-105">Especificamente, chamar a função [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) retorna o nível de autenticação e o provedor de segurança usados para a chamada.</span><span class="sxs-lookup"><span data-stu-id="416fd-105">Specifically, calling the [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) function returns the authentication level and security provider used for the call.</span></span> <span data-ttu-id="416fd-106">Esta operação não significa que a chamada não estava em uma sessão nula.</span><span class="sxs-lookup"><span data-stu-id="416fd-106">This operation does not mean the call was not on a null session.</span></span> <span data-ttu-id="416fd-107">Os dois problemas são ortogonal.</span><span class="sxs-lookup"><span data-stu-id="416fd-107">The two issues are orthogonal.</span></span> <span data-ttu-id="416fd-108">No Microsoft Windows 2000, uma chamada de procedimento remoto pode tentar representar um chamador e verificar as permissões após a representação.</span><span class="sxs-lookup"><span data-stu-id="416fd-108">On Microsoft Windows 2000, a remote procedure call can attempt to impersonate a caller and check the permissions after impersonation.</span></span> <span data-ttu-id="416fd-109">No Microsoft Windows XP, é mais rápido chamar a função [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) e verificar o sinalizador **NullSession** .</span><span class="sxs-lookup"><span data-stu-id="416fd-109">On Microsoft Windows XP, it is faster to call the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function and check for the **NullSession** flag.</span></span>

<span data-ttu-id="416fd-110">Existe outra diferença relevante entre o Windows 2000 e o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="416fd-110">Another relevant difference exists between Windows 2000 and Windows XP.</span></span> <span data-ttu-id="416fd-111">Se apenas o \_ \_ \_ sinalizador permitir somente segurança \_ for especificado, as chamadas na sessão nula passarão pelo Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="416fd-111">If only the RPC\_IF\_ALLOW\_SECURE\_ONLY flag is specified, calls on the null session go through in Windows 2000.</span></span> <span data-ttu-id="416fd-112">No Windows XP, com o ajuste geral das configurações de segurança padrão, quando esse sinalizador é especificado, as chamadas na sessão nula são rejeitadas com acesso negado.</span><span class="sxs-lookup"><span data-stu-id="416fd-112">In Windows XP, with the general tightening of default security settings, when this flag is specified, calls on the null session are rejected with access denied.</span></span> <span data-ttu-id="416fd-113">No entanto, mesmo com o RPC \_ se \_ permitir \_ \_ sinalizador somente seguro, o RPC não garante o nível de privilégio do usuário que está chamando.</span><span class="sxs-lookup"><span data-stu-id="416fd-113">However, even with the RPC\_IF\_ALLOW\_SECURE\_ONLY flag, RPC does not guarantee the privilege level of the calling user.</span></span> <span data-ttu-id="416fd-114">Todas as verificações RPC são que o usuário tem credenciais válidas.</span><span class="sxs-lookup"><span data-stu-id="416fd-114">All RPC checks is that the user has valid credentials.</span></span> <span data-ttu-id="416fd-115">É possível que o usuário que está chamando esteja usando a conta de convidado ou outras contas com poucos privilégios.</span><span class="sxs-lookup"><span data-stu-id="416fd-115">It is possible that the calling user is using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="416fd-116">Verifique se o servidor não assume alto privilégio depois de RPC \_ se \_ permitir \_ \_ somente seguro for usado.</span><span class="sxs-lookup"><span data-stu-id="416fd-116">Make sure the server does not assume high privilege once RPC\_IF\_ALLOW\_SECURE\_ONLY is used.</span></span>

 

 




