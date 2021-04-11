---
description: Troca de cliente/servidor
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Troca de cliente/servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6274705ef6719c846f0551f90fca8790ba89f2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091326"
---
# <a name="clientserver-exchange"></a><span data-ttu-id="b3414-103">Troca de cliente/servidor</span><span class="sxs-lookup"><span data-stu-id="b3414-103">Client/Server Exchange</span></span>

<span data-ttu-id="b3414-104">Depois que um usuário tem um tíquete para um servidor, o cliente de estação de trabalho pode estabelecer uma sessão de comunicações segura com esse servidor.</span><span class="sxs-lookup"><span data-stu-id="b3414-104">After a user has a ticket to a server, the workstation client can establish a secure communications session with that server.</span></span>

<span data-ttu-id="b3414-105">**Para estabelecer uma sessão de comunicações segura com um servidor**</span><span class="sxs-lookup"><span data-stu-id="b3414-105">**To establish a secure communications session with a server**</span></span>

1.  <span data-ttu-id="b3414-106">O cliente envia ao servidor uma mensagem do tipo KRB \_ AP \_ req (solicitação de aplicativo Kerberos).</span><span class="sxs-lookup"><span data-stu-id="b3414-106">The client sends the server a message of type KRB\_AP\_REQ (Kerberos Application Request).</span></span> <span data-ttu-id="b3414-107">Essa mensagem contém uma mensagem de autenticador que é criptografada com a chave enviada pelo [*centro de distribuição de chaves*](/windows/desktop/SecGloss/k-gly) (KDC) para a sessão com o servidor, o tíquete para sessões com o servidor e um sinalizador que indica se o cliente solicita autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="b3414-107">This message contains an authenticator message that is encrypted with the key sent by the [*Key Distribution Center*](/windows/desktop/SecGloss/k-gly) (KDC) for the session with the server, the ticket for sessions with the server, and a flag that indicates whether the client requests mutual authentication.</span></span> <span data-ttu-id="b3414-108">Definir o sinalizador que solicita autenticação mútua é uma das opções na configuração do [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="b3414-108">Setting the flag that requests mutual authentication is one of the options in configuring [*Kerberos*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="b3414-109">O usuário nunca será perguntado se a autenticação mútua deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="b3414-109">The user is never asked whether mutual authentication should be used.</span></span>
2.  <span data-ttu-id="b3414-110">O servidor recebe o KRB \_ AP \_ req, descriptografa o tíquete e extrai os dados de autorização do usuário e a [*chave de sessão*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="b3414-110">The server receives KRB\_AP\_REQ, decrypts the ticket, and extracts the user's authorization data and the [*session key*](/windows/desktop/SecGloss/s-gly).</span></span>
3.  <span data-ttu-id="b3414-111">O servidor usa a chave de sessão do tíquete para descriptografar a mensagem do autenticador do usuário e avalia o carimbo de data/hora dentro do.</span><span class="sxs-lookup"><span data-stu-id="b3414-111">The server uses the session key from the ticket to decrypt the user's authenticator message and evaluates the time stamp inside.</span></span>
4.  <span data-ttu-id="b3414-112">Se a mensagem do autenticador for válida, o servidor verificará o sinalizador de autenticação mútua na solicitação do cliente.</span><span class="sxs-lookup"><span data-stu-id="b3414-112">If the authenticator message is valid, the server checks the mutual authentication flag in the client's request.</span></span>
5.  <span data-ttu-id="b3414-113">Se o sinalizador de autenticação mútua estiver definido, o servidor usará a chave de sessão para criptografar a hora da mensagem do autenticador do usuário e retornará o resultado em uma mensagem do tipo KRB \_ AP \_ Rep (resposta do aplicativo Kerberos).</span><span class="sxs-lookup"><span data-stu-id="b3414-113">If the mutual authentication flag is set, the server uses the session key to encrypt the time from the user's authenticator message and returns the result in a message of type KRB\_AP\_REP (Kerberos Application Reply).</span></span>
6.  <span data-ttu-id="b3414-114">Quando o cliente recebe o \_ Rep KRB AP \_ , ele descriptografa a mensagem de autenticador do servidor com a chave de sessão que ele compartilha com o servidor e compara o tempo enviado de volta pelo serviço com o tempo em sua mensagem de autenticador original.</span><span class="sxs-lookup"><span data-stu-id="b3414-114">When the client receives KRB\_AP\_REP, it decrypts the server's authenticator message with the session key it shares with the server and compares the time sent back by the service with the time in its original authenticator message.</span></span> <span data-ttu-id="b3414-115">Se eles corresponderem, o cliente terá certeza de que o serviço é original e a conexão continuará.</span><span class="sxs-lookup"><span data-stu-id="b3414-115">If they match, the client is assured that the service is genuine, and the connection proceeds.</span></span>

 

 
