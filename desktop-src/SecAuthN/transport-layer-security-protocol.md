---
description: O Schannel dá suporte às versões 1,0, 1,1 e 1,2 do protocolo TLS.
ms.assetid: af541a51-fabc-4abd-ae67-268bd984ab92
title: Protocolo TLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf35fbfb59fee80617e6eccab66d7cec538e61ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769196"
---
# <a name="transport-layer-security-protocol"></a><span data-ttu-id="224d5-103">Protocolo TLS</span><span class="sxs-lookup"><span data-stu-id="224d5-103">Transport Layer Security Protocol</span></span>

<span data-ttu-id="224d5-104">O Schannel dá suporte às versões 1,0, 1,1 e 1,2 do [*protocolo TLS*](../secgloss/t-gly.md).</span><span class="sxs-lookup"><span data-stu-id="224d5-104">Schannel supports versions 1.0, 1.1, and 1.2 of the [*Transport Layer Security (TLS) protocol*](../secgloss/t-gly.md).</span></span> <span data-ttu-id="224d5-105">Esse protocolo é um padrão da indústria projetado para proteger a privacidade das informações comunicadas pela Internet.</span><span class="sxs-lookup"><span data-stu-id="224d5-105">This protocol is an industry standard designed to protect the privacy of information communicated over the Internet.</span></span> <span data-ttu-id="224d5-106">O TLS pressupõe que um transporte orientado a conexão, normalmente, TCP, esteja em uso.</span><span class="sxs-lookup"><span data-stu-id="224d5-106">TLS assumes that a connection-oriented transport, typically TCP, is in use.</span></span> <span data-ttu-id="224d5-107">O protocolo TLS permite que aplicativos cliente/servidor detectem os seguintes riscos de segurança:</span><span class="sxs-lookup"><span data-stu-id="224d5-107">The TLS protocol allows client/server applications to detect the following security risks:</span></span>

-   <span data-ttu-id="224d5-108">Violação de mensagem</span><span class="sxs-lookup"><span data-stu-id="224d5-108">Message tampering</span></span>
-   <span data-ttu-id="224d5-109">Interceptação de mensagem</span><span class="sxs-lookup"><span data-stu-id="224d5-109">Message interception</span></span>
-   <span data-ttu-id="224d5-110">Falsificação de mensagem</span><span class="sxs-lookup"><span data-stu-id="224d5-110">Message forgery</span></span>

<span data-ttu-id="224d5-111">A especificação completa do protocolo TLS está disponível no site da IETF: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt) .</span><span class="sxs-lookup"><span data-stu-id="224d5-111">The full specification of the TLS Protocol is available from the IETF website: [https://www.ietf.org/rfc/rfc2246.txt](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="organization-of-tls"></a><span data-ttu-id="224d5-112">Organização do TLS</span><span class="sxs-lookup"><span data-stu-id="224d5-112">Organization of TLS</span></span>

<span data-ttu-id="224d5-113">As etapas a seguir estão envolvidas no uso de TLS para comunicação de cliente/servidor:</span><span class="sxs-lookup"><span data-stu-id="224d5-113">The following steps are involved in using TLS for client/server communication:</span></span>

 <span data-ttu-id="224d5-114">**Para usar o TLS para comunicação de cliente/servidor**</span><span class="sxs-lookup"><span data-stu-id="224d5-114">**To use TLS for client/server communication**</span></span>

1.  <span data-ttu-id="224d5-115">Negociação de handshake e Cipher Suite</span><span class="sxs-lookup"><span data-stu-id="224d5-115">Handshake and cipher suite negotiation</span></span>
2.  <span data-ttu-id="224d5-116">Autenticação de partes</span><span class="sxs-lookup"><span data-stu-id="224d5-116">Authentication of parties</span></span>
3.  <span data-ttu-id="224d5-117">Troca de informações relacionadas à chave</span><span class="sxs-lookup"><span data-stu-id="224d5-117">Key-related information exchange</span></span>
4.  <span data-ttu-id="224d5-118">Troca de dados de aplicativos</span><span class="sxs-lookup"><span data-stu-id="224d5-118">Application data exchange</span></span>

<span data-ttu-id="224d5-119">As etapas que compõem o TLS são divididas em dois protocolos que, juntos, fornecem segurança de conexão:</span><span class="sxs-lookup"><span data-stu-id="224d5-119">The steps that make up TLS are divided into two protocols that, together, provide connection security:</span></span>

-   <span data-ttu-id="224d5-120">[Protocolo de handshake TLS](tls-handshake-protocol.md)— (etapas 1 a 3)</span><span class="sxs-lookup"><span data-stu-id="224d5-120">[TLS Handshake Protocol](tls-handshake-protocol.md)— (steps 1 – 3)</span></span>
-   <span data-ttu-id="224d5-121">[Protocolo de registro TLS](tls-record-protocol.md)— (etapa 4)</span><span class="sxs-lookup"><span data-stu-id="224d5-121">[TLS Record Protocol](tls-record-protocol.md)— (step 4)</span></span>

## <a name="sspi-with-tls-implementations"></a><span data-ttu-id="224d5-122">SSPI com implementações de TLS</span><span class="sxs-lookup"><span data-stu-id="224d5-122">SSPI with TLS implementations</span></span>

<span data-ttu-id="224d5-123">Como o TLS não tem uma especificação de GSSAPI, os implementadores de TLS podem não estar familiarizados com as funções SSPI.</span><span class="sxs-lookup"><span data-stu-id="224d5-123">Because TLS does not have a GSSAPI specification, TLS implementers may not be familiar with the SSPI functions.</span></span> <span data-ttu-id="224d5-124">Os aplicativos chamam as funções SSPI para enumerar pacotes disponíveis, criar e trabalhar com identificadores para credenciais, criar contextos de segurança e garantir a privacidade da integridade da mensagem.</span><span class="sxs-lookup"><span data-stu-id="224d5-124">Applications call the SSPI functions to enumerate available packages, create and work with handles to credentials, create security contexts and ensure message integrity privacy.</span></span>

<span data-ttu-id="224d5-125">Para dar suporte às funções SSPI usadas por aplicativos de modo de usuário, as funções listadas em [funções implementadas por SSP/APS de modo de usuário](/windows/desktop/SecAuthN/authentication-functions) precisam ser suportadas por implementações de TLS, como schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="224d5-125">To support the SSPI functions used by user mode applications, the functions listed in [Functions Implemented by User-mode SSP/APs](/windows/desktop/SecAuthN/authentication-functions) need to be supported by TLS implementations such as schannel.dll.</span></span>

<span data-ttu-id="224d5-126">Para obter detalhes sobre as funções SSPI e funções do SSP, consulte [funções de autenticação](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="224d5-126">For details about the SSPI functions and SSP functions, see [Authentication Functions](authentication-functions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="224d5-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="224d5-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="224d5-128">Conjuntos de codificação TLS</span><span class="sxs-lookup"><span data-stu-id="224d5-128">TLS Cipher Suites</span></span>](tls-cipher-suites.md)
</dt> <dt>

[<span data-ttu-id="224d5-129">TLS vs. SSL</span><span class="sxs-lookup"><span data-stu-id="224d5-129">TLS vs. SSL</span></span>](tls-versus-ssl.md)
</dt> </dl>

 

 
