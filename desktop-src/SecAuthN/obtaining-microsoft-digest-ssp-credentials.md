---
description: As credenciais do usuário são exigidas pelo Microsoft Digest; o cliente e o servidor devem apresentar credenciais válidas antes que possam estabelecer um contexto de segurança para a troca de mensagens. Os identificadores de credenciais são usados para obter e apresentar as credenciais.
ms.assetid: f97bdaf6-40a8-414e-a561-d3cb953d0bab
title: Obtendo credenciais do Microsoft Digest SSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c61895ecc8e49713665af4542689729bc491d9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461057"
---
# <a name="obtaining-microsoft-digest-ssp-credentials"></a><span data-ttu-id="48308-104">Obtendo credenciais do Microsoft Digest SSP</span><span class="sxs-lookup"><span data-stu-id="48308-104">Obtaining Microsoft Digest SSP Credentials</span></span>

<span data-ttu-id="48308-105">[*As credenciais*](../secgloss/c-gly.md) do usuário são exigidas pelo Microsoft Digest; o cliente e o servidor devem apresentar credenciais válidas antes que possam estabelecer um [*contexto de segurança*](../secgloss/s-gly.md) para a troca de mensagens.</span><span class="sxs-lookup"><span data-stu-id="48308-105">User [*credentials*](../secgloss/c-gly.md) are required by Microsoft Digest; both client and server must present valid credentials before they can establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="48308-106">Os identificadores de credenciais são usados para obter e apresentar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="48308-106">Credentials handles are used to obtain and present credentials.</span></span>

<span data-ttu-id="48308-107">Como o identificador de credencial é usado para armazenar informações de configuração, o mesmo identificador não pode ser usado para operações do lado do cliente e do servidor.</span><span class="sxs-lookup"><span data-stu-id="48308-107">Because the credential handle is used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="48308-108">Isso significa que os aplicativos que dão suporte a conexões de cliente e de servidor devem obter um mínimo de duas identificadores de credenciais.</span><span class="sxs-lookup"><span data-stu-id="48308-108">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="48308-109">Para obter um identificador para as credenciais exigidas pelo Microsoft Digest, chame a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .</span><span class="sxs-lookup"><span data-stu-id="48308-109">To get a handle to the credentials required by Microsoft Digest, call the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span>

<span data-ttu-id="48308-110">Os exemplos de linguagem C a seguir demonstram como obter credenciais.</span><span class="sxs-lookup"><span data-stu-id="48308-110">The following C language examples demonstrate obtaining credentials.</span></span>

-   [<span data-ttu-id="48308-111">Obtendo credenciais de resumo padrão</span><span class="sxs-lookup"><span data-stu-id="48308-111">Obtaining Default Digest Credentials</span></span>](obtaining-default-digest-credentials.md)
-   [<span data-ttu-id="48308-112">Obtendo credenciais de resumo alternativas</span><span class="sxs-lookup"><span data-stu-id="48308-112">Obtaining Alternate Digest Credentials</span></span>](obtaining-alternate-digest-credentials.md)

 

 
