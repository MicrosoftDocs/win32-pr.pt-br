---
description: O TLS é um padrão bem relacionado ao SSL 3,0 e, às vezes, é chamado de &\# 0034; SSL 3,1&\# 0034;.
ms.assetid: 92b1b486-7e10-48a2-b1d2-56d4e472dbe4
title: TLS vs. SSL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac1a2e783b6f3355127a3148f1575f73119f6604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748409"
---
# <a name="tls-vs-ssl"></a><span data-ttu-id="b8419-103">TLS vs. SSL</span><span class="sxs-lookup"><span data-stu-id="b8419-103">TLS vs. SSL</span></span>

<span data-ttu-id="b8419-104">O TLS é um padrão bem relacionado ao SSL 3,0 e, às vezes, é chamado de "SSL 3,1".</span><span class="sxs-lookup"><span data-stu-id="b8419-104">TLS is a standard closely related to SSL 3.0, and is sometimes referred to as "SSL 3.1".</span></span> <span data-ttu-id="b8419-105">O TLS substitui o SSL 2,0 e deve ser usado em um novo desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="b8419-105">TLS supersedes SSL 2.0 and should be used in new development.</span></span> <span data-ttu-id="b8419-106">A partir do Windows 10, versão 1607 e Windows Server 2016, o SSL 2,0 foi removido e não tem mais suporte.</span><span class="sxs-lookup"><span data-stu-id="b8419-106">Beginning with Windows 10, version 1607 and Windows Server 2016, SSL 2.0 has been removed and is no longer supported.</span></span>

<span data-ttu-id="b8419-107">Os aplicativos que exigem um alto nível de interoperabilidade devem dar suporte a SSL 3,0 e TLS.</span><span class="sxs-lookup"><span data-stu-id="b8419-107">Applications that require a high level of interoperability should support SSL 3.0 and TLS.</span></span> <span data-ttu-id="b8419-108">Devido às semelhanças entre esses dois protocolos, os detalhes de SSL não são incluídos nesta documentação, exceto onde diferem do TLS.</span><span class="sxs-lookup"><span data-stu-id="b8419-108">Because of the similarities between these two protocols, SSL details are not included in this documentation, except where they differ from TLS.</span></span> <span data-ttu-id="b8419-109">O seguinte é do [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span><span class="sxs-lookup"><span data-stu-id="b8419-109">The following is from [RFC 2246](https://www.ietf.org/rfc/rfc2246.txt):</span></span>

<span data-ttu-id="b8419-110">"As diferenças entre esse protocolo e o SSL 3,0 não são dramáticas, mas são significativas o suficiente para que o TLS 1,0 e o SSL 3,0 não interoperem (embora o TLS 1,0 incorpore um mecanismo pelo qual uma implementação de TLS possa fazer o backup para SSL 3,0)."</span><span class="sxs-lookup"><span data-stu-id="b8419-110">"The differences between this protocol and SSL 3.0 are not dramatic, but they are significant enough that TLS 1.0 and SSL 3.0 do not interoperate (although TLS 1.0 does incorporate a mechanism by which a TLS implementation can back down to SSL 3.0)."</span></span>

 

 



