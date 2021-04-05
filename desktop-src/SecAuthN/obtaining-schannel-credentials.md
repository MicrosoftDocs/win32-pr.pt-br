---
description: As credenciais são exigidas pelo processo de autenticação Schannel; tanto o cliente quanto o servidor devem obter credenciais válidas para estabelecer um contexto de segurança para a troca de mensagens. Para obter um exemplo que demonstra esse procedimento, consulte obtendo credenciais.
ms.assetid: ee4a9908-7ba8-4701-84a4-c50b6b989e82
title: Obtendo credenciais Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e5a5b82b3ed76e905c967009da52d17bff0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662134"
---
# <a name="obtaining-schannel-credentials"></a><span data-ttu-id="bced8-104">Obtendo credenciais Schannel</span><span class="sxs-lookup"><span data-stu-id="bced8-104">Obtaining Schannel Credentials</span></span>

<span data-ttu-id="bced8-105">As credenciais são exigidas pelo processo de autenticação Schannel; tanto o cliente quanto o servidor devem obter credenciais válidas para estabelecer um [*contexto de segurança*](../secgloss/s-gly.md) para a troca de mensagens.</span><span class="sxs-lookup"><span data-stu-id="bced8-105">Credentials are required by the Schannel authentication process; both client and server must obtain valid credentials to establish a [*security context*](../secgloss/s-gly.md) for message exchange.</span></span> <span data-ttu-id="bced8-106">Para obter um exemplo que demonstra esse procedimento, consulte [obtendo credenciais](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="bced8-106">For an example that demonstrates this procedure, see [Getting credentials](getting-a-certificate-for-schannel.md).</span></span>

<span data-ttu-id="bced8-107">Seu aplicativo obtém credenciais chamando a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , que retorna um identificador para as credenciais solicitadas.</span><span class="sxs-lookup"><span data-stu-id="bced8-107">Your application obtains credentials by calling the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function, which returns a handle to the requested credentials.</span></span> <span data-ttu-id="bced8-108">Como os identificadores de credenciais são usados para armazenar informações de configuração, o mesmo identificador não pode ser usado para operações do lado do cliente e do servidor.</span><span class="sxs-lookup"><span data-stu-id="bced8-108">Because credentials handles are used to store configuration information, the same handle cannot be used for both client-side and server-side operations.</span></span> <span data-ttu-id="bced8-109">Isso significa que os aplicativos que dão suporte a conexões de cliente e de servidor devem obter um mínimo de duas identificadores de credenciais.</span><span class="sxs-lookup"><span data-stu-id="bced8-109">This means that applications that support both client and server connections must obtain a minimum of two credentials handles.</span></span>

<span data-ttu-id="bced8-110">No Windows XP, uma estrutura de [**\_ credenciais Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) especifica o seguinte:</span><span class="sxs-lookup"><span data-stu-id="bced8-110">In Windows XP, an [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure specifies the following:</span></span>

-   <span data-ttu-id="bced8-111">Um protocolo de segurança</span><span class="sxs-lookup"><span data-stu-id="bced8-111">A security protocol</span></span>
-   <span data-ttu-id="bced8-112">As codificações permitidas</span><span class="sxs-lookup"><span data-stu-id="bced8-112">The allowable ciphers</span></span>
-   <span data-ttu-id="bced8-113">Níveis mínimo e máximo de codificação</span><span class="sxs-lookup"><span data-stu-id="bced8-113">Minimum and maximum cipher strengths</span></span>
-   <span data-ttu-id="bced8-114">Um certificado [*X. 509*](../secgloss/x-gly.md) usado para autenticação — necessário para o servidor, opcional para o cliente, a menos que o servidor solicite a autenticação do cliente.</span><span class="sxs-lookup"><span data-stu-id="bced8-114">An [*X.509*](../secgloss/x-gly.md) certificate used for authentication — Required for server, optional for client unless server requests client authentication.</span></span>

<span data-ttu-id="bced8-115">Passe a estrutura de [**\_ credenciais Schannel**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) (por meio do parâmetro *pAuthData* ) para a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) .</span><span class="sxs-lookup"><span data-stu-id="bced8-115">Pass the [**SCHANNEL\_CRED**](/windows/desktop/api/Schannel/ns-schannel-schannel_cred) structure (via the *pAuthData* parameter) to the [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) function.</span></span> <span data-ttu-id="bced8-116">Essa função retorna o identificador de credenciais necessário para estabelecer um [*contexto de segurança*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="bced8-116">This function returns the credentials handle required to establish a [*security context*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="bced8-117">Para obter informações detalhadas sobre como definir as codificações usadas com Schannel, consulte [especificando codificações Schannel e níveis de codificação](specifying-schannel-ciphers-and-cipher-strengths.md).</span><span class="sxs-lookup"><span data-stu-id="bced8-117">For detailed information on setting the ciphers used with Schannel, see [Specifying Schannel Ciphers and Cipher Strengths](specifying-schannel-ciphers-and-cipher-strengths.md).</span></span>

<span data-ttu-id="bced8-118">Para obter informações sobre certificados, consulte [funções de repositório de certificados e](../seccrypto/cryptography-functions.md)certificados.</span><span class="sxs-lookup"><span data-stu-id="bced8-118">For information about certificates, see [Certificate and Certificate Store Functions](../seccrypto/cryptography-functions.md).</span></span>

<span data-ttu-id="bced8-119">Para obter um exemplo que demonstra como abrir um [*repositório de certificados*](../secgloss/c-gly.md) e localizar um certificado a ser usado para autenticação Schannel, consulte [obter um certificado](getting-a-certificate-for-schannel.md).</span><span class="sxs-lookup"><span data-stu-id="bced8-119">For an example that demonstrates opening a [*certificate store*](../secgloss/c-gly.md) and locating a certificate to use for Schannel authentication, see [Getting a Certificate](getting-a-certificate-for-schannel.md).</span></span>

 

 
