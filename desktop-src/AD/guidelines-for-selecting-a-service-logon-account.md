---
title: Diretrizes para selecionar uma conta de logon de serviço
description: Um serviço baseado no Win32 pode ser executado no contexto de segurança de uma conta de usuário local, uma conta de usuário de domínio ou a conta LocalSystem.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Diretrizes para selecionar um anúncio de conta de logon de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bb8f5b4fe6a57863c09c9563454fc3ec09e75c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004914"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a><span data-ttu-id="f876d-104">Diretrizes para selecionar uma conta de logon de serviço</span><span class="sxs-lookup"><span data-stu-id="f876d-104">Guidelines for Selecting a Service Logon Account</span></span>

<span data-ttu-id="f876d-105">Um serviço baseado no Win32 pode ser executado no contexto de segurança de uma conta de usuário local, uma conta de usuário de domínio ou a conta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="f876d-105">A Win32-based service can run in the security context of a local user account, a domain user account, or the LocalSystem account.</span></span> <span data-ttu-id="f876d-106">Para decidir qual conta usar, um administrador deve instalar o serviço com o conjunto mínimo de permissões necessárias para executar as operações de serviço.</span><span class="sxs-lookup"><span data-stu-id="f876d-106">To decide which account to use, an administrator should install the service with the minimum set of permissions required to perform the service operations.</span></span> <span data-ttu-id="f876d-107">Em um serviço típico habilitado para diretório, isso significa que o instalador do serviço deve criar uma conta de usuário de domínio para o serviço e conceder a essa conta os direitos de acesso e privilégios específicos exigidos pelo serviço em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="f876d-107">In a typical directory-enabled service, this means the service installer should create a domain user account for the service and grant that account the specific access rights and privileges required by the service at run time.</span></span> <span data-ttu-id="f876d-108">Um serviço deve ser executado somente na conta LocalSystem se o serviço exigir privilégios administrativos ou deve atuar como parte do sistema operacional no computador local.</span><span class="sxs-lookup"><span data-stu-id="f876d-108">A service should only run under the LocalSystem account if the service requires administrative privileges or must act as part of the operating system on the local computer.</span></span>

<span data-ttu-id="f876d-109">Lembre-se de que o instalador do serviço deve, por padrão, configurar o serviço para ser executado em uma conta de usuário de domínio.</span><span class="sxs-lookup"><span data-stu-id="f876d-109">Be aware that the service installer should, by default, set up the service to run under a domain user account.</span></span> <span data-ttu-id="f876d-110">Para executar o serviço na conta LocalSystem, o instalador do serviço deve consultar o administrador para obter permissão para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="f876d-110">To run the service under the LocalSystem account, the service installer should query the administrator for permission to do so.</span></span>

<span data-ttu-id="f876d-111">Para obter mais informações sobre descrições, vantagens e desvantagens de cada tipo de conta, consulte:</span><span class="sxs-lookup"><span data-stu-id="f876d-111">For more information about descriptions, advantages, and disadvantages of each account type, see:</span></span>

-   <span data-ttu-id="f876d-112">[Contas de usuário local](local-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="f876d-112">[Local User Accounts](local-user-accounts.md).</span></span>
-   <span data-ttu-id="f876d-113">[Contas de usuário de domínio](domain-user-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="f876d-113">[Domain User Accounts](domain-user-accounts.md).</span></span>
-   <span data-ttu-id="f876d-114">[A conta LocalSystem](the-localsystem-account.md).</span><span class="sxs-lookup"><span data-stu-id="f876d-114">[The LocalSystem Account](the-localsystem-account.md).</span></span>

 

 




