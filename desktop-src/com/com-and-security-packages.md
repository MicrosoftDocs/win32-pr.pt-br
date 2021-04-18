---
title: Pacotes de segurança e COM
description: O Windows dá suporte a NTLMSSP (provedor de suporte de segurança do LAN Manager), ao protocolo de autenticação Kerberos V5 e ao pacote de segurança Schannel, que fornece os protocolos PCT 1,0, SSL 2,0, SSL 3,0 e TLS 1,0.
ms.assetid: a0c095a8-93b7-4350-aac6-a9a066cccffd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6720ddd56869c5ce93ae70eb313fbe12c140b42
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105788757"
---
# <a name="com-and-security-packages"></a><span data-ttu-id="77385-103">Pacotes de segurança e COM</span><span class="sxs-lookup"><span data-stu-id="77385-103">COM and Security Packages</span></span>

<span data-ttu-id="77385-104">O Windows dá suporte a NTLMSSP (provedor de suporte de segurança do LAN Manager), ao protocolo de autenticação Kerberos V5 e ao pacote de segurança Schannel, que fornece os protocolos PCT 1,0, SSL 2,0, SSL 3,0 e TLS 1,0.</span><span class="sxs-lookup"><span data-stu-id="77385-104">Windows supports NTLMSSP (LAN Manager Security Support Provider), the Kerberos v5 authentication protocol, and the Schannel security package, which provides the PCT 1.0, SSL 2.0, SSL 3.0, and TLS 1.0 protocols.</span></span> <span data-ttu-id="77385-105">Também há suporte para Snego, que verifica os pacotes de segurança disponíveis e seleciona o mais apropriado.</span><span class="sxs-lookup"><span data-stu-id="77385-105">Also supported is Snego, which checks for available security packages and selects the most appropriate one.</span></span>

<span data-ttu-id="77385-106">A tabela a seguir mostra os níveis de autenticação com suporte nos vários pacotes de segurança.</span><span class="sxs-lookup"><span data-stu-id="77385-106">The following table shows the levels of authentication supported by the various security packages.</span></span>



| <span data-ttu-id="77385-107">Autenticação de servidor/cliente</span><span class="sxs-lookup"><span data-stu-id="77385-107">Server/Client Authentication</span></span>                                                                                           | <span data-ttu-id="77385-108">Suporte ao pacote de segurança</span><span class="sxs-lookup"><span data-stu-id="77385-108">Security Package Support</span></span>                                         |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="77385-109">Nem pode obter o nome do outro.</span><span class="sxs-lookup"><span data-stu-id="77385-109">Neither can get the name of the other.</span></span><br/>                                                                      | <span data-ttu-id="77385-110">Nenhum</span><span class="sxs-lookup"><span data-stu-id="77385-110">None</span></span><br/>                                                  |
| <span data-ttu-id="77385-111">O cliente pode autenticar o servidor, mas não vice-versa.</span><span class="sxs-lookup"><span data-stu-id="77385-111">The client can authenticate the server, but not vice versa.</span></span><br/>                                                 | <span data-ttu-id="77385-112">SChannel</span><span class="sxs-lookup"><span data-stu-id="77385-112">Schannel</span></span><br/>                                              |
| <span data-ttu-id="77385-113">O cliente não pode descobrir o servidor, mas o servidor pode obter a ID de usuário do cliente.</span><span class="sxs-lookup"><span data-stu-id="77385-113">The client cannot discover the server, but the server can get the user ID of the client.</span></span><br/>                    | <span data-ttu-id="77385-114">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="77385-114">NTLMSSP</span></span><br/>                                               |
| <span data-ttu-id="77385-115">Autenticação mútua: o cliente e o servidor podem saber o nome do outro, se a permissão for concedida.</span><span class="sxs-lookup"><span data-stu-id="77385-115">Mutual authentication: Both the client and server can know the name of the other, if permission is granted.</span></span><br/> | <span data-ttu-id="77385-116">NTLMSSP (localmente), protocolo Kerberos V5 e Schannel</span><span class="sxs-lookup"><span data-stu-id="77385-116">NTLMSSP (locally), Kerberos v5 protocol, and Schannel</span></span><br/> |



 

<span data-ttu-id="77385-117">Para obter mais informações sobre esses pacotes de segurança, consulte os seguintes tópicos nesta seção:</span><span class="sxs-lookup"><span data-stu-id="77385-117">For more information about these security packages, see the following topics in this section:</span></span>

-   [<span data-ttu-id="77385-118">NTLMSSP</span><span class="sxs-lookup"><span data-stu-id="77385-118">NTLMSSP</span></span>](ntlmssp.md)
-   [<span data-ttu-id="77385-119">Protocolo Kerberos V5</span><span class="sxs-lookup"><span data-stu-id="77385-119">Kerberos v5 Protocol</span></span>](kerberos-v5-protocol.md)
-   [<span data-ttu-id="77385-120">Schannel</span><span class="sxs-lookup"><span data-stu-id="77385-120">Schannel</span></span>](schannel.md)
-   [<span data-ttu-id="77385-121">Snego</span><span class="sxs-lookup"><span data-stu-id="77385-121">Snego</span></span>](snego.md)

## <a name="related-topics"></a><span data-ttu-id="77385-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77385-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77385-123">Segurança em COM</span><span class="sxs-lookup"><span data-stu-id="77385-123">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 





