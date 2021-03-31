---
description: Desligando uma conexão Schannel
ms.assetid: 7081ba1f-df3c-41b4-96da-24d44e74d714
title: Desligando uma conexão Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc61b67083ceee65da714069c2b30ba1bfd5c89b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646675"
---
# <a name="shutting-down-an-schannel-connection"></a>Desligando uma conexão Schannel

Quando um cliente ou servidor é concluído com uma conexão, ele deve desligá-lo. A outra parte, por sua vez, deve reconhecer o desligamento e excluir a conexão.

**Para desligar uma conexão Schannel**

1.  Chame a função [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken) , especificando o \_ token de controle de desligamento Schannel.
2.  Depois de receber um \_ \_ valor de retorno de s E OK de [**ApplyControlToken**](/windows/desktop/api/Sspi/nf-sspi-applycontroltoken), chame a função [**InitializeSecurityContext (Schannel)**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig) (clientes) ou [**AcceptSecurityContext (Schannel)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext) (servidores), passando buffers vazios.
3.  Prossiga como se o aplicativo estivesse criando uma nova conexão até que a função retorne o contexto de s \_ I, \_ \_ expirado ou s \_ e \_ OK, para indicar que a conexão foi desligada.
4.  Envie as informações de saída final, se houver, para a parte remota.
5.  Chame [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) para liberar recursos mantidos pela conexão.

## <a name="recognizing-a-shutdown"></a>Reconhecendo um desligamento

A função [**DecryptMessage (Schannel)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) retorna um \_ \_ contexto de s I \_ expirou quando o remetente da mensagem desligou a conexão. Depois de receber esse valor de retorno, siga o procedimento para desligar uma conexão Schannel, anteriormente neste tópico.

 

 
