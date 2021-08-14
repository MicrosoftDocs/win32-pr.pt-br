---
description: Com base no código de retorno de uma chamada anterior para AcceptSecurityContext (Geral), o servidor pode aguardar uma resposta do cliente e pode participar de trocas adicionais com o cliente.
ms.assetid: 281e1f81-3524-4034-bee5-cef6b13cf402
title: Continuação do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06863a0e94fcfe65c7ab695d30be92044fe7341ffa0eb9091c5f1a81acdffc58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918285"
---
# <a name="server-continuation"></a>Continuação do servidor

Com base no código de retorno de uma chamada anterior para [**AcceptSecurityContext (Geral),**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext)o servidor pode aguardar uma resposta do cliente e pode participar de trocas adicionais com o cliente. Para continuar o protocolo de autenticação, o servidor repete chamadas para **AcceptSecurityContext (Geral).**

O status retornado por [**AcceptSecurityContext (Geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) é verificado para ver se o servidor precisa aguardar mensagens adicionais do cliente. Na maioria dos protocolos de autenticação, há um número máximo de trocas até mesmo para autenticação mútua. Atualmente, os protocolos NTLM e [*Kerberos*](../secgloss/k-gly.md) fazem autenticação mútua com três trocas.

 

 
