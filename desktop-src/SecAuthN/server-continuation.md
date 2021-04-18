---
description: Com base no código de retorno de uma chamada anterior para AcceptSecurityContext (geral), o servidor pode aguardar uma resposta do cliente e pode participar de trocas adicionais com o cliente.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Continuação do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fba8a60bea12daae0e6aaf93fed55fead5738c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756573"
---
# <a name="server-continuation"></a><span data-ttu-id="2d6d4-103">Continuação do servidor</span><span class="sxs-lookup"><span data-stu-id="2d6d4-103">Server Continuation</span></span>

<span data-ttu-id="2d6d4-104">Com base no código de retorno de uma chamada anterior para [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), o servidor pode aguardar uma resposta do cliente e pode participar de trocas adicionais com o cliente.</span><span class="sxs-lookup"><span data-stu-id="2d6d4-104">Based on the return code from a previous call to [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), the server can wait for a response from the client and can participate in additional exchanges with the client.</span></span> <span data-ttu-id="2d6d4-105">Para continuar o protocolo de autenticação, o servidor repete as chamadas para **AcceptSecurityContext (geral)**.</span><span class="sxs-lookup"><span data-stu-id="2d6d4-105">To continue the authentication protocol, the server repeats calls to **AcceptSecurityContext (General)**.</span></span>

<span data-ttu-id="2d6d4-106">O status retornado por [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) é verificado para ver se o servidor precisa aguardar mensagens adicionais do cliente.</span><span class="sxs-lookup"><span data-stu-id="2d6d4-106">The status returned by [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) is checked to see if the server needs to wait for additional messages from the client.</span></span> <span data-ttu-id="2d6d4-107">Na maioria dos protocolos de autenticação, há um número máximo de trocas, mesmo para autenticação mútua.</span><span class="sxs-lookup"><span data-stu-id="2d6d4-107">In most authentication protocols, there is a maximum number of exchanges even for mutual authentication.</span></span> <span data-ttu-id="2d6d4-108">Atualmente, os protocolos NTLM e [*Kerberos*](../secgloss/k-gly.md) fazem a autenticação mútua com três trocas.</span><span class="sxs-lookup"><span data-stu-id="2d6d4-108">Currently, both the NTLM and [*Kerberos protocols*](../secgloss/k-gly.md) do mutual authentication with three exchanges.</span></span>

 

 
