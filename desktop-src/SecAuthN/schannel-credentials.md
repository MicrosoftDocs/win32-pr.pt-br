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
# <a name="schannel-credentials"></a>Credenciais do Schannel

Os protocolos Schannel exigem credenciais para autenticar servidores e, opcionalmente, clientes. Autenticação de servidor, em que o servidor fornece uma prova de sua identidade para o cliente, é exigido pelos [*protocolos de segurança*](../secgloss/s-gly.md)Schannel. A autenticação de cliente pode ser solicitada pelo servidor a qualquer momento.

As credenciais Schannel são certificados [*X. 509*](../secgloss/x-gly.md) . As informações de chave [*pública*](../secgloss/p-gly.md) e [*privada*](../secgloss/p-gly.md) de certificados são usadas para autenticar o servidor e, opcionalmente, o cliente. Essas chaves também são usadas para fornecer [*integridade*](../secgloss/i-gly.md) de mensagem enquanto o cliente e o servidor trocam as informações necessárias para gerar e trocar [*chaves de sessão*](../secgloss/s-gly.md).

Para obter informações de programação, consulte [obtendo credenciais Schannel](obtaining-schannel-credentials.md).

 

 
