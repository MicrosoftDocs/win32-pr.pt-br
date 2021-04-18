---
description: Após um tíquete de concessão de tíquete (TGT) e uma chave de sessão terem sido estabelecidos para o cliente, o cliente pode solicitar uma chave de sessão e um tíquete separados para o serviço.
ms.assetid: b4f63642-9282-4e11-b40c-eec406b2dd2b
title: Troca de serviços de concessão de tíquete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3b227ee551d762abd145ca56c6cced110b6a2dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750452"
---
# <a name="ticket-granting-service-exchange"></a><span data-ttu-id="93346-103">Troca de serviços de concessão de tíquete</span><span class="sxs-lookup"><span data-stu-id="93346-103">Ticket-Granting Service Exchange</span></span>

<span data-ttu-id="93346-104">Após um tíquete de concessão de tíquete (TGT) e uma [*chave de sessão*](../secgloss/s-gly.md) terem sido estabelecidos para o cliente, o cliente pode solicitar uma chave de sessão e um tíquete separados para o serviço.</span><span class="sxs-lookup"><span data-stu-id="93346-104">After a ticket-granting ticket (TGT) and [*session key*](../secgloss/s-gly.md) have been established for the client, the client can request a separate session key and ticket for the service.</span></span>

<span data-ttu-id="93346-105">**Para solicitar um tíquete para outro serviço**</span><span class="sxs-lookup"><span data-stu-id="93346-105">**To request a ticket for another service**</span></span>

1.  <span data-ttu-id="93346-106">O cliente Kerberos na estação de trabalho do usuário solicita [*credenciais*](../secgloss/c-gly.md) para o serviço enviando para o [*centro de distribuição de chaves*](../secgloss/k-gly.md) (KDC), uma mensagem do tipo KRB \_ TGS \_ req (Ticket-Granting solicitação de serviço Kerberos).</span><span class="sxs-lookup"><span data-stu-id="93346-106">The Kerberos client on the user's workstation requests [*credentials*](../secgloss/c-gly.md) for the service by sending, to the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC), a message of type KRB\_TGS\_REQ (Kerberos Ticket-Granting Service Request).</span></span> <span data-ttu-id="93346-107">Essa mensagem consiste na identidade do serviço para o qual o cliente está solicitando credenciais, uma mensagem de autenticador criptografada com a nova [*chave de sessão*](../secgloss/s-gly.md)de logon do usuário e o TGT obtido da [troca do serviço de autenticação](authentication-service-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="93346-107">This message consists of the identity of the service for which the client is requesting credentials, an authenticator message encrypted with the user's new logon [*session key*](../secgloss/s-gly.md), and the TGT obtained from the [Authentication Service Exchange](authentication-service-exchange.md).</span></span>
2.  <span data-ttu-id="93346-108">Quando o KDC recebe um KRB \_ TGS \_ req, o KDC DESCRIPTOGRAFA o TGT com sua chave secreta e extrai a chave de sessão de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="93346-108">When the KDC receives a KRB\_TGS\_REQ, the KDC decrypts the TGT with its secret key and extracts the user's logon session key.</span></span>
3.  <span data-ttu-id="93346-109">O KDC usa a [*chave de sessão*](../secgloss/s-gly.md) de logon para descriptografar a mensagem do autenticador do usuário e a avalia.</span><span class="sxs-lookup"><span data-stu-id="93346-109">The KDC uses the logon [*session key*](../secgloss/s-gly.md) to decrypt the user's authenticator message and evaluates it.</span></span> <span data-ttu-id="93346-110">Se o autenticador passar no teste, o KDC extrairá os dados de autorização do usuário do TGT e ininventará uma chave de sessão para o usuário compartilhar com o servidor solicitado.</span><span class="sxs-lookup"><span data-stu-id="93346-110">If the authenticator passes the test, the KDC extracts the user's authorization data from the TGT and invents a session key for the user to share with the requested server.</span></span>
4.  <span data-ttu-id="93346-111">O KDC criptografa uma cópia da chave de sessão de serviço com a chave de sessão de logon do usuário.</span><span class="sxs-lookup"><span data-stu-id="93346-111">The KDC encrypts one copy of the service session key with the user's logon session key.</span></span>
5.  <span data-ttu-id="93346-112">O KDC insere outra cópia da chave de sessão de serviço em um tíquete, juntamente com os dados de autorização do usuário, e criptografa o tíquete com a [*chave mestra*](../secgloss/m-gly.md)do servidor.</span><span class="sxs-lookup"><span data-stu-id="93346-112">The KDC embeds another copy of the service session key in a ticket, along with the user's authorization data, and encrypts the ticket with the server's [*master key*](../secgloss/m-gly.md).</span></span>
6.  <span data-ttu-id="93346-113">O KDC envia essas credenciais de volta para o cliente respondendo com uma mensagem do tipo KRB \_ TGS \_ Rep (Kerberos Ticket-Granting Service Reply).</span><span class="sxs-lookup"><span data-stu-id="93346-113">The KDC sends these credentials back to the client by replying with a message of type KRB\_TGS\_REP (Kerberos Ticket-Granting Service Reply).</span></span>
7.  <span data-ttu-id="93346-114">Quando o cliente recebe a resposta, ele descriptografa a chave de sessão de serviço com a chave de sessão de logon do usuário e armazena a chave de sessão de serviço em seu cache de tíquete.</span><span class="sxs-lookup"><span data-stu-id="93346-114">When the client receives the reply, it decrypts the service session key with the user's logon session key and stores the service session key in its ticket cache.</span></span>
8.  <span data-ttu-id="93346-115">O cliente extrai o tíquete para o servidor e o armazena em seu cache de tíquetes.</span><span class="sxs-lookup"><span data-stu-id="93346-115">The client extracts the ticket to the server and stores that in its ticket cache.</span></span>

 

 
