---
title: Usando uma conta de usuário local como uma conta de logon de serviço
description: Uma conta de usuário local (formato de nome \ 0034;. \\ Nome de usuário \ 0034;) existe somente no banco de dados SAM do computador host; Ele não tem um objeto de usuário em Active Directory Domain Services.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84da502e99d2e5cd74e98e9f792e06f74f4852e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084019"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a><span data-ttu-id="a45e7-103">Usando uma conta de usuário local como uma conta de logon de serviço</span><span class="sxs-lookup"><span data-stu-id="a45e7-103">Using a Local User Account as a Service Logon Account</span></span>

<span data-ttu-id="a45e7-104">Uma conta de usuário local (formato de nome: ". \\ *Username*") existe apenas no banco de dados Sam do computador host; Ele não tem um objeto de usuário em Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="a45e7-104">A local user account (name format: ".\\*UserName*") exists only in the SAM database of the host computer; it does not have a user object in Active Directory Domain Services.</span></span> <span data-ttu-id="a45e7-105">Isso significa que uma conta local não pode ser autenticada pelo domínio.</span><span class="sxs-lookup"><span data-stu-id="a45e7-105">This means that a local account cannot be authenticated by the domain.</span></span> <span data-ttu-id="a45e7-106">Consequentemente, um serviço executado no contexto de segurança de uma conta de usuário local não tem acesso aos recursos de rede (exceto como um usuário anônimo) e não pode dar suporte à autenticação mútua Kerberos na qual o serviço é autenticado por seus clientes.</span><span class="sxs-lookup"><span data-stu-id="a45e7-106">Consequently, a service that runs in the security context of a local user account does not have access to network resources (except as an anonymous user), and it cannot support Kerberos mutual authentication in which the service is authenticated by its clients.</span></span> <span data-ttu-id="a45e7-107">Por esses motivos, as contas de usuário local normalmente são inadequadas para serviços habilitados para diretório.</span><span class="sxs-lookup"><span data-stu-id="a45e7-107">For these reasons, local user accounts are typically inappropriate for directory-enabled services.</span></span> <span data-ttu-id="a45e7-108">No lado de mais, os bugs no serviço não podem danificar o sistema.</span><span class="sxs-lookup"><span data-stu-id="a45e7-108">On the plus side, bugs in the service cannot damage the system.</span></span> <span data-ttu-id="a45e7-109">Se o serviço puder ser executado sob essas limitações, ele deverá.</span><span class="sxs-lookup"><span data-stu-id="a45e7-109">If your service can run under those limitations, it should.</span></span>

 

 




