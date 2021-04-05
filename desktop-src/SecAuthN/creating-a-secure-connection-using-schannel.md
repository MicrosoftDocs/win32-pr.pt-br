---
description: Como criar uma conexão segura usando Schannel.
ms.assetid: 94eb15c3-225b-4b6f-b29c-41e5d356a847
title: Criando uma conexão segura usando Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 335713a400804bc84fffa078496c53c9178e389b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662419"
---
# <a name="creating-a-secure-connection-using-schannel"></a><span data-ttu-id="6e747-103">Criando uma conexão segura usando Schannel</span><span class="sxs-lookup"><span data-stu-id="6e747-103">Creating a Secure Connection Using Schannel</span></span>

<span data-ttu-id="6e747-104">O [*pacote de segurança*](/windows/desktop/SecGloss/s-gly) Schannel fornece acesso a quatro [*protocolos de segurança*](/windows/desktop/SecGloss/s-gly):</span><span class="sxs-lookup"><span data-stu-id="6e747-104">The Schannel [*security package*](/windows/desktop/SecGloss/s-gly) provides access to four [*security protocols*](/windows/desktop/SecGloss/s-gly):</span></span>

-   [<span data-ttu-id="6e747-105">Segurança de camada de transporte (TLS 1,2)</span><span class="sxs-lookup"><span data-stu-id="6e747-105">Transport Layer Security (TLS 1.2)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="6e747-106">Segurança de camada de transporte (TLS 1,1)</span><span class="sxs-lookup"><span data-stu-id="6e747-106">Transport Layer Security (TLS 1.1)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="6e747-107">Segurança de camada de transporte (TLS 1,0)</span><span class="sxs-lookup"><span data-stu-id="6e747-107">Transport Layer Security (TLS 1.0)</span></span>](transport-layer-security-protocol.md)
-   [<span data-ttu-id="6e747-108">Protocolo SSL (SSL 3,0)</span><span class="sxs-lookup"><span data-stu-id="6e747-108">Secure Sockets Layer (SSL 3.0)</span></span>](secure-sockets-layer-protocol.md)
-   [<span data-ttu-id="6e747-109">Protocolo SSL (SSL 2,0)</span><span class="sxs-lookup"><span data-stu-id="6e747-109">Secure Sockets Layer (SSL 2.0)</span></span>](secure-sockets-layer-protocol.md)

> [!Note]  
> <span data-ttu-id="6e747-110">Os protocolos PCT e SSL 2,0 foram substituídos pelo protocolo TLS e não devem ser usados para um novo desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="6e747-110">The PCT and SSL 2.0 protocols have been superseded by the TLS protocol and should not be used for new development.</span></span>

 

<span data-ttu-id="6e747-111">**Para configurar uma conexão segura entre um cliente e um servidor**</span><span class="sxs-lookup"><span data-stu-id="6e747-111">**To set up a secure connection between a client and server**</span></span>

1.  <span data-ttu-id="6e747-112">Obter credenciais do Schannel ([obtendo credenciais Schannel](obtaining-schannel-credentials.md)).</span><span class="sxs-lookup"><span data-stu-id="6e747-112">Obtain Schannel credentials ([Obtaining Schannel Credentials](obtaining-schannel-credentials.md)).</span></span>
2.  <span data-ttu-id="6e747-113">Criar um contexto de segurança Schannel ([criando um contexto de segurança Schannel](creating-an-schannel-security-context.md)).</span><span class="sxs-lookup"><span data-stu-id="6e747-113">Create an Schannel security context ([Creating an Schannel Security Context](creating-an-schannel-security-context.md)).</span></span>

<span data-ttu-id="6e747-114">Depois que uma conexão é estabelecida, você pode recuperar informações sobre seus atributos.</span><span class="sxs-lookup"><span data-stu-id="6e747-114">After a connection is established, you can retrieve information about its attributes.</span></span> <span data-ttu-id="6e747-115">Para obter detalhes, consulte [obtendo informações sobre conexões Schannel](getting-information-about-schannel-connections.md).</span><span class="sxs-lookup"><span data-stu-id="6e747-115">For details, see [Getting Information About Schannel Connections](getting-information-about-schannel-connections.md).</span></span>

<span data-ttu-id="6e747-116">Se, depois de estabelecer uma conexão, os requisitos de segurança do aplicativo forem alterados ou a conexão for perdida, você poderá renegociar a conexão.</span><span class="sxs-lookup"><span data-stu-id="6e747-116">If, after you have established a connection, the security requirements of your application change or the connection is lost, you can renegotiate the connection.</span></span> <span data-ttu-id="6e747-117">Para obter detalhes, consulte [renegociando uma conexão Schannel](renegotiating-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6e747-117">For details, see [Renegotiating an Schannel Connection](renegotiating-an-schannel-connection.md).</span></span>

<span data-ttu-id="6e747-118">Quando terminar de usar uma conexão Schannel, você deverá executar a limpeza necessária.</span><span class="sxs-lookup"><span data-stu-id="6e747-118">When you have finished using an Schannel connection, you must perform the necessary cleanup.</span></span> <span data-ttu-id="6e747-119">Para obter detalhes, consulte [desligando uma conexão Schannel](shutting-down-an-schannel-connection.md).</span><span class="sxs-lookup"><span data-stu-id="6e747-119">For details, see [Shutting Down an Schannel Connection](shutting-down-an-schannel-connection.md).</span></span>

<span data-ttu-id="6e747-120">Para obter informações sobre exemplos fornecidos com o SDK (Software Development Kit) da plataforma que demonstram o [*pacote de segurança*](/windows/desktop/SecGloss/s-gly)Schannel, consulte os exemplos de PSDK usando Schannel.</span><span class="sxs-lookup"><span data-stu-id="6e747-120">For information about samples shipped with the Platform Software Development Kit (SDK) that demonstrate the Schannel [*security package*](/windows/desktop/SecGloss/s-gly), see the PSDK samples using Schannel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e747-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6e747-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e747-122">Especificando codificações Schannel e níveis de codificação</span><span class="sxs-lookup"><span data-stu-id="6e747-122">Specifying Schannel Ciphers and Cipher Strengths</span></span>](specifying-schannel-ciphers-and-cipher-strengths.md)
</dt> </dl>

 

 
