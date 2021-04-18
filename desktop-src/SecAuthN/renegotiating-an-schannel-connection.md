---
description: Para alterar os atributos de uma conexão, como o pacote de codificação ou a autenticação de cliente, você pode solicitar um &\# 0034; refazer&\# 0034; ou renegociar a conexão.
ms.assetid: 681b607d-66d8-4012-9a84-d202c9778a26
title: Renegociar uma conexão Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fbcd25dad39ab7f35e77277eee9275004cd8a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751819"
---
# <a name="renegotiating-an-schannel-connection"></a>Renegociar uma conexão Schannel

Para alterar os atributos de uma conexão, como o pacote de codificação ou a autenticação de cliente, você pode solicitar uma "refazer" ou renegociar a conexão.

Se os atributos que você deseja alterar forem controlados por credenciais, você deverá obter novas credenciais antes de renegociar a conexão. Para obter mais informações, consulte [obtendo credenciais Schannel](obtaining-schannel-credentials.md).

Para solicitar uma refazer de um aplicativo cliente, chame a função [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) . Os aplicativos de servidor chamam a função [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) . Defina os parâmetros da seguinte maneira:

-   Especifique o [*contexto de segurança*](../secgloss/s-gly.md#_SECURITY_SECURITY_CONTEXT_GLY) existente no parâmetro *phContext* .
-   (Somente clientes) Especifique o mesmo nome de servidor (no parâmetro *pszTargetName* ) conforme especificado ao estabelecer o contexto.
-   Especifique novas credenciais, usando o parâmetro *phCredential* , se aplicável.
-   Se você quiser alterar atributos de contexto não relacionados às credenciais, especifique esses atributos usando o parâmetro *fContextReq* .

Depois de chamar a função apropriada, seu aplicativo deve enviar os resultados para o cliente e continuar processando mensagens de entrada usando a função [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) .

A função [**DecryptMessage (Schannel)**](decryptmessage--schannel.md) retornará SEC \_ que \_ renegociará quando o Schannel estiver pronto para o aplicativo continuar. Quando você recebe o \_ código de retorno s I \_ renegotiate, seu aplicativo deve chamar [**AcceptSecurityContext (Schannel)**](acceptsecuritycontext--schannel.md) (servidores) ou [**InitializeSecurityContext (Schannel)**](./initializesecuritycontext--schannel.md) (clientes) e passar o conteúdo de SECBUFFER_EXTRA retornado de DecryptMessage no SECBUFFER_TOKEN. Depois que essa chamada retornar um valor, prossiga como se seu aplicativo estivesse criando uma nova conexão.

 

 
