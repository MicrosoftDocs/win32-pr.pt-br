---
description: Para alterar os atributos de uma conexão, como o conjunto de criptografias ou a autenticação de cliente, você pode solicitar um &\# 0034;refazer&\# 0034 ou a renegociação da conexão.
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: Renegociar uma conexão Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b904400f5a440046214c39ea736c296685e0e56859f43b3a458f621d2a07d273
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919395"
---
# <a name="renegotiating-an-schannel-connection"></a>Renegociar uma conexão Schannel

Para alterar os atributos de uma conexão, como o conjunto de criptografias ou a autenticação de cliente, você pode solicitar uma "refazer" ou uma renegociação da conexão.

Se os atributos que você deseja alterar são controlados por credenciais, você deve obter novas credenciais antes de negociar a conexão. Para obter mais informações, [consulte Obtendo credenciais Schannel](obtaining-schannel-credentials.md).

Para solicitar uma refazer de um aplicativo cliente, chame a [**função InitializeSecurityContext (Schannel).**](./initializesecuritycontext--schannel.md) Os aplicativos de servidor [**chamam a função AcceptSecurityContext (Schannel).**](acceptsecuritycontext--schannel.md) De definir os parâmetros da seguinte forma:

-   Especifique o contexto [*de segurança*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) existente no *parâmetro phContext.*
-   (Somente clientes) Especifique o mesmo nome do servidor (no *parâmetro pszTargetName)* conforme especificado ao estabelecer o contexto.
-   Especifique novas credenciais, usando o *parâmetro phCredential,* se aplicável.
-   Se você quiser alterar atributos de contexto não relacionados às credenciais, especifique esses atributos usando o *parâmetro fContextReq.*

Depois de chamar a função apropriada, seu aplicativo deve enviar os resultados para o cliente e continuar processando mensagens de entrada usando a função [**DecryptMessage (Schannel).**](decryptmessage--schannel.md)

A [**função DecryptMessage (Schannel)**](decryptmessage--schannel.md) retornará SEC I RENEGOTIATE quando o Schannel estiver pronto \_ para que seu aplicativo \_ prossiga. Quando você recebe o código de retorno DA SEC I RENEGOTIATE, seu aplicativo deve chamar \_ \_ [**AcceptSecurityContext (Schannel) (servidores)**](acceptsecuritycontext--schannel.md) ou [**InitializeSecurityContext (Schannel) (clientes)**](./initializesecuritycontext--schannel.md) e passar o conteúdo de SECBUFFER_EXTRA retornado de DecryptMessage no SECBUFFER_TOKEN. Depois que essa chamada retornar um valor, continue como se seu aplicativo estivesse criando uma nova conexão.

 

 
