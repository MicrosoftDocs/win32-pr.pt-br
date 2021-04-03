---
title: Convertendo formatos de nome de conta de domínio
description: As funções do Microsoft Win32 para trabalhar com o SCM (Gerenciador de controle de serviço) em um servidor host usam o \ 0034; domínio \\ nome de usuário \ 0034; formato para contas de serviço.
ms.assetid: a8bb6331-5070-4f46-b03d-615a004b3982
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ab1a6d0022b0a47979c1f6b3434e6227c23c30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640426"
---
# <a name="converting-domain-account-name-formats"></a><span data-ttu-id="4066b-103">Convertendo formatos de nome de conta de domínio</span><span class="sxs-lookup"><span data-stu-id="4066b-103">Converting Domain Account Name Formats</span></span>

<span data-ttu-id="4066b-104">As funções do Microsoft Win32 para trabalhar com o SCM (Gerenciador de controle de serviço) em um servidor host usam o <domain> \\ <username> formato "" para contas de serviço.</span><span class="sxs-lookup"><span data-stu-id="4066b-104">The Microsoft Win32 functions for working with the service control manager (SCM) on a host server use the "<domain>\\<username>" format for service accounts.</span></span> <span data-ttu-id="4066b-105">Por exemplo, se você chamar a função [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) para recuperar a conta de usuário sob a qual seu serviço é executado, a função retornará o nome no formato "fabrikam \\ jeffsmith".</span><span class="sxs-lookup"><span data-stu-id="4066b-105">For example, if you call the [**QueryServiceConfig**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceconfiga) function to retrieve the user account under which your service runs, the function returns the name in "Fabrikam\\jeffsmith" format.</span></span> <span data-ttu-id="4066b-106">Para se associar à conta de usuário no diretório, por exemplo, para alterar a senha da conta, é necessário o nome distinto da conta, que tem o formato "CN = Jeff Smith, CN = Users, DC = Fabrikam, DC = COM".</span><span class="sxs-lookup"><span data-stu-id="4066b-106">To bind to the user account in the directory, for example to change the account password, the distinguished name of the account is required, which has the format "CN=Jeff Smith,CN=Users,DC=Fabrikam,DC=COM".</span></span>

<span data-ttu-id="4066b-107">Para converter entre os vários formatos de nome, use a função [**transtardianame**](/windows/desktop/api/secext/nf-secext-translatenamea) , que pode converter um nome para outros formatos, como um UPN (nome principal do usuário).</span><span class="sxs-lookup"><span data-stu-id="4066b-107">To convert between the various name formats, use the [**TranslateName**](/windows/desktop/api/secext/nf-secext-translatenamea) function, which can convert a name to other formats, such as a user principal name (UPN).</span></span>

 

 