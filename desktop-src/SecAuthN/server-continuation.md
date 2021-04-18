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
# <a name="server-continuation"></a>Continuação do servidor

Com base no código de retorno de uma chamada anterior para [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext), o servidor pode aguardar uma resposta do cliente e pode participar de trocas adicionais com o cliente. Para continuar o protocolo de autenticação, o servidor repete as chamadas para **AcceptSecurityContext (geral)**.

O status retornado por [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) é verificado para ver se o servidor precisa aguardar mensagens adicionais do cliente. Na maioria dos protocolos de autenticação, há um número máximo de trocas, mesmo para autenticação mútua. Atualmente, os protocolos NTLM e [*Kerberos*](../secgloss/k-gly.md) fazem a autenticação mútua com três trocas.

 

 
