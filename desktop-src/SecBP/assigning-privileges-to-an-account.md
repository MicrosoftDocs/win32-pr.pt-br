---
description: Você pode atribuir privilégios a contas usando o snap-in do MMC (console de gerenciamento Microsoft) da política de segurança local (secpol. msc) ou chamando a função LsaAddAccountRights.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Atribuindo privilégios a uma conta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0865a59b8bad75e687fd12f6bfc42c2cd39f664d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753237"
---
# <a name="assigning-privileges-to-an-account"></a><span data-ttu-id="a7d47-103">Atribuindo privilégios a uma conta</span><span class="sxs-lookup"><span data-stu-id="a7d47-103">Assigning Privileges to an Account</span></span>

<span data-ttu-id="a7d47-104">Você pode atribuir privilégios a contas usando o snap-in do MMC (console de gerenciamento Microsoft) da política de segurança local (secpol. msc) ou chamando a função [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) .</span><span class="sxs-lookup"><span data-stu-id="a7d47-104">You can assign privileges to accounts either by using the Local Security Policy Microsoft Management Console (MMC) snap-in (Secpol.msc) or by calling the [**LsaAddAccountRights**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights) function.</span></span>

<span data-ttu-id="a7d47-105">A atribuição de um privilégio a uma conta não afeta os tokens de usuário existentes.</span><span class="sxs-lookup"><span data-stu-id="a7d47-105">Assigning a privilege to an account does not affect existing user tokens.</span></span> <span data-ttu-id="a7d47-106">Um usuário deve fazer logoff e, em seguida, fazer logon novamente para obter um token de acesso com o privilégio atribuído recentemente.</span><span class="sxs-lookup"><span data-stu-id="a7d47-106">A user must log off and then log back on to get an access token with the newly assigned privilege.</span></span>

<span data-ttu-id="a7d47-107">Para atribuir privilégios usando o snap-in de política de segurança local do MMC, edite a lista de usuários para cada privilégio listado em **configurações de segurança/políticas locais/atribuição de direitos de usuário**.</span><span class="sxs-lookup"><span data-stu-id="a7d47-107">To assign privileges by using the Local Security Policy MMC snap-in, edit the list of users for each privilege listed under **Security Settings/Local Policies/User Rights Assignment**.</span></span>

 

 
