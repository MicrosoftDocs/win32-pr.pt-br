---
description: Mapeando certificados
ms.assetid: 4139f927-54f4-4968-a9eb-020401bb536d
title: Mapeando certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 397a9ef8822d4f191ae37cdb998166fa54c2b12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662741"
---
# <a name="mapping-certificates"></a><span data-ttu-id="218dc-103">Mapeando certificados</span><span class="sxs-lookup"><span data-stu-id="218dc-103">Mapping Certificates</span></span>

> [!Note]  
> <span data-ttu-id="218dc-104">As informações neste tópico são válidas somente para servidores que exigem autenticação de cliente.</span><span class="sxs-lookup"><span data-stu-id="218dc-104">The information in this topic is valid only for servers that require client authentication.</span></span>

 

<span data-ttu-id="218dc-105">Quando um aplicativo de servidor requer autenticação de cliente, o Schannel tenta mapear automaticamente o certificado fornecido pelo cliente para uma conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="218dc-105">When a server application requires client authentication, Schannel automatically attempts to map the certificate supplied by the client to a user account.</span></span>

<span data-ttu-id="218dc-106">Depois que [*o contexto de segurança*](../secgloss/s-gly.md) tiver sido estabelecido, o aplicativo de servidor poderá usar a função [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) para obter um token de [*acesso*](../secgloss/a-gly.md) para a conta de usuário para a qual o certificado de [*cliente*](../secgloss/c-gly.md) foi mapeado.</span><span class="sxs-lookup"><span data-stu-id="218dc-106">After the [*security context*](../secgloss/s-gly.md) has been established, the server application can use the [**QuerySecurityContextToken**](/windows/desktop/api/Sspi/nf-sspi-querysecuritycontexttoken) function to obtain an [*access token*](../secgloss/a-gly.md) for the user account to which the [*client certificate*](../secgloss/c-gly.md) was mapped.</span></span> <span data-ttu-id="218dc-107">Além disso, o servidor pode usar a função [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) para representar o cliente.</span><span class="sxs-lookup"><span data-stu-id="218dc-107">Also, the server can use the [**ImpersonateSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-impersonatesecuritycontext) function to impersonate the client.</span></span>

<span data-ttu-id="218dc-108">Para obter mais informações sobre autenticação, consulte [executando a autenticação usando Schannel](performing-authentication-using-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="218dc-108">For more information on authentication, see [Performing Authentication Using Schannel](performing-authentication-using-schannel.md).</span></span>

 

 
