---
description: Desligando uma conexão Schannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Desligando uma conexão Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb700c8ac896d0e64b82b25371ea67cc343d8297c95445ca4126c5718d8024a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118918055"
---
# <a name="shutting-down-an-schannel-connection"></a>Desligando uma conexão Schannel

Quando um cliente ou servidor é concluído com uma conexão, ele deve desligá-lo. A outra parte, por sua vez, deve reconhecer o desligamento e excluir a conexão.

**Para desligar uma conexão Schannel**

1.  Chame a [**função ApplyControlToken,**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) especificando o token de controle SHUTDOWN SCHANNEL. \_
2.  Depois de receber um valor de retorno SEC E OK de ApplyControlToken , chame a função \_ \_ [**InitializeSecurityContext (Schannel) (clientes)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) ou [**AcceptSecurityContext (Schannel) (servidores),**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) passando buffers vazios. [](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken)
3.  Continue como se seu aplicativo estivesse criando uma nova conexão até que a função retorne SEC I CONTEXT EXPIRED ou SEC E OK para indicar que a \_ \_ conexão foi \_ \_ \_ desligado.
4.  Envie as informações de saída finais, se alguma, para a parte remota.
5.  Chame [**DeleteSecurityContext para**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) liberar recursos mantidos pela conexão.

## <a name="recognizing-a-shutdown"></a>Reconhecendo um desligamento

A [**função DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) retorna SEC I CONTEXT EXPIRED quando o remetente da mensagem \_ desliga a \_ \_ conexão. Depois de receber esse valor de retorno, siga o procedimento Para desligar uma conexão Schannel, anteriormente neste tópico.

 

 
