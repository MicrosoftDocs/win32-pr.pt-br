---
description: Veja a seguir um guia para proteger a programação do Windows Sockets.
ms.assetid: 70210e86-ead6-4b0c-ae47-66b2ef0a8d11
title: Programação de Winsock seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d7a0710a4446486835ec14435fa7d7ba1458c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661775"
---
# <a name="secure-winsock-programming"></a><span data-ttu-id="f777c-103">Programação de Winsock seguro</span><span class="sxs-lookup"><span data-stu-id="f777c-103">Secure Winsock Programming</span></span>

<span data-ttu-id="f777c-104">Veja a seguir um guia para proteger a programação do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="f777c-104">The following is a guide to secure Windows Sockets programming.</span></span> <span data-ttu-id="f777c-105">Ele foi projetado para fornecer uma compreensão da segurança do Winsock e das opções disponíveis para o desenvolvedor de aplicativo de rede seguro.</span><span class="sxs-lookup"><span data-stu-id="f777c-105">It is designed to provide an understanding of Winsock security and the options available to the secure network application developer.</span></span>

-   [<span data-ttu-id="f777c-106">Usando o \_ REUSEADDR e, portanto, \_ EXCLUSIVEADDRUSE</span><span class="sxs-lookup"><span data-stu-id="f777c-106">Using SO\_REUSEADDR and SO\_EXCLUSIVEADDRUSE</span></span>](using-so-reuseaddr-and-so-exclusiveaddruse.md)
-   [<span data-ttu-id="f777c-107">Extensões do Winsock Secure Socket</span><span class="sxs-lookup"><span data-stu-id="f777c-107">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)

<span data-ttu-id="f777c-108">As comunicações usando soquetes também podem ser criptografadas usando os padrões de SSL/TLS usando o canal seguro, também conhecido como tecnologia Schannel.</span><span class="sxs-lookup"><span data-stu-id="f777c-108">Communications using sockets can also be encrypted using the SSL/TLS standards using Secure Channel, also known as Schannel technology.</span></span> <span data-ttu-id="f777c-109">O Schannel é um SSP (provedor de suporte de segurança) que contém um conjunto de protocolos de segurança que fornecem autenticação de identidade e comunicação segura e privada por meio de criptografia.</span><span class="sxs-lookup"><span data-stu-id="f777c-109">Schannel is a security support provider (SSP) that contains a set of security protocols that provide identity authentication and secure, private communication through encryption.</span></span> <span data-ttu-id="f777c-110">O Schannel é usado principalmente para aplicativos de Internet que exigem comunicações HTTP (Hypertext Transfer Protocol) seguras.</span><span class="sxs-lookup"><span data-stu-id="f777c-110">Schannel is primarily used for Internet applications that require secure Hypertext Transfer Protocol (HTTP) communications.</span></span> <span data-ttu-id="f777c-111">Para obter mais informações, consulte [Secure Channel](../secauthn/secure-channel.md).</span><span class="sxs-lookup"><span data-stu-id="f777c-111">For more information, please see [Secure Channel](../secauthn/secure-channel.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f777c-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f777c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f777c-113">Canal Seguro</span><span class="sxs-lookup"><span data-stu-id="f777c-113">Secure Channel</span></span>](../secauthn/secure-channel.md)
</dt> </dl>

 

 
