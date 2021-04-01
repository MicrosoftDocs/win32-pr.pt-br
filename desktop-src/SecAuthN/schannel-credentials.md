---
description: Os protocolos Schannel exigem credenciais para autenticar servidores e, opcionalmente, clientes.
ms.assetid: 8295b1bd-6ae1-4f7e-926d-a9da7ec6a524
title: Credenciais do Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f91556a7e3bfca67aa386f0264e78ae67052f02c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921617"
---
# <a name="schannel-credentials"></a><span data-ttu-id="49ab3-103">Credenciais do Schannel</span><span class="sxs-lookup"><span data-stu-id="49ab3-103">Schannel Credentials</span></span>

<span data-ttu-id="49ab3-104">Os protocolos Schannel exigem credenciais para autenticar servidores e, opcionalmente, clientes.</span><span class="sxs-lookup"><span data-stu-id="49ab3-104">Schannel protocols require credentials to authenticate servers and optionally, clients.</span></span> <span data-ttu-id="49ab3-105">Autenticação de servidor, em que o servidor fornece uma prova de sua identidade para o cliente, é exigido pelos [*protocolos de segurança*](../secgloss/s-gly.md)Schannel.</span><span class="sxs-lookup"><span data-stu-id="49ab3-105">Server authentication, where the server provides proof of its identity to the client, is required by the Schannel [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="49ab3-106">A autenticação de cliente pode ser solicitada pelo servidor a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="49ab3-106">Client authentication may be requested by the server at any time.</span></span>

<span data-ttu-id="49ab3-107">As credenciais Schannel são certificados [*X. 509*](../secgloss/x-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="49ab3-107">Schannel credentials are [*X.509*](../secgloss/x-gly.md) certificates.</span></span> <span data-ttu-id="49ab3-108">As informações de chave [*pública*](../secgloss/p-gly.md) e [*privada*](../secgloss/p-gly.md) de certificados são usadas para autenticar o servidor e, opcionalmente, o cliente.</span><span class="sxs-lookup"><span data-stu-id="49ab3-108">[*Public*](../secgloss/p-gly.md) and [*private key*](../secgloss/p-gly.md) information from certificates is used to authenticate the server and optionally, the client.</span></span> <span data-ttu-id="49ab3-109">Essas chaves também são usadas para fornecer [*integridade*](../secgloss/i-gly.md) de mensagem enquanto o cliente e o servidor trocam as informações necessárias para gerar e trocar [*chaves de sessão*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="49ab3-109">These keys are also used to provide message [*integrity*](../secgloss/i-gly.md) while client and server exchange the information required to generate and exchange [*session keys*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="49ab3-110">Para obter informações de programação, consulte [obtendo credenciais Schannel](obtaining-schannel-credentials.md).</span><span class="sxs-lookup"><span data-stu-id="49ab3-110">For programming information, see [Obtaining Schannel Credentials](obtaining-schannel-credentials.md).</span></span>

 

 
