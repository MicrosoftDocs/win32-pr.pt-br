---
description: A função DecryptMessage (geral) intercepta solicitações de renegociação proveniente do remetente da mensagem. Ele notifica seu aplicativo descriptografando os dados da mensagem e retornando o \_ valor s I \_ renegotiate.
ms.assetid: 036a93dc-7f52-42f8-945d-7f654289ef63
title: Reconhecendo uma solicitação para renegociar uma conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ae8083c59485b8b7c917fe03893fa363f5a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010982"
---
# <a name="recognizing-a-request-to-renegotiate-a-connection"></a>Reconhecendo uma solicitação para renegociar uma conexão

A função [**DecryptMessage (geral)**](decryptmessage--general.md) intercepta solicitações de renegociação proveniente do remetente da mensagem. Ele notifica seu aplicativo descriptografando os dados da mensagem e retornando o \_ valor s I \_ renegotiate.

Seu aplicativo deve lidar com essas solicitações chamando [**AcceptSecurityContext (geral)**](acceptsecuritycontext--general.md) (servidores) ou [**InitializeSecurityContext (geral)**](initializesecuritycontext--general.md) (clientes) e passando o conteúdo de SECBUFFER_EXTRA retornado de DecryptMessage no SECBUFFER_TOKEN. Depois que essa chamada inicial retorna um valor, continue como se seu aplicativo estivesse criando uma nova conexão.

 

 



