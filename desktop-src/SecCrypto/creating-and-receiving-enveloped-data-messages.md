---
description: Uma mensagem envelopada é uma mensagem criptografada para um destinatário ou conjunto de destinatários.
ms.assetid: caf86ec8-48b6-4017-95ad-7a21fcaed4cf
title: Criando e recebendo mensagens de dados envelopadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63abf31d582ae9ae184dc15d85d827a3741d317e3bad75c8b07cce25e457bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768901"
---
# <a name="creating-and-receiving-enveloped-data-messages"></a>Criando e recebendo mensagens de dados envelopadas

Uma mensagem envelopada é uma mensagem criptografada para um conjunto de destinatários. No processo Envelopment, uma chave de criptografia de sessão é gerada e a mensagem é criptografada com essa chave. A chave de criptografia em si é, então, criptografada separadamente para cada destinatário usando as chaves públicas do certificado do destinatário desejado. A mensagem envelopada consiste na mensagem criptografada, nos certificados dos destinatários pretendidos e no conjunto de chaves criptografadas, uma para cada destinatário. A mensagem gerada está no formato/CMS [*PKCS \# 7*](../secgloss/p-gly.md).

As seções a seguir mostram procedimentos e exemplos para tarefas de mensagens envelopadas:

-   [Codificando dados Envelopos](encoding-enveloped-data.md)
-   [Decodificando dados envelopado](decoding-enveloped-data.md)
-   [Código alternativo para codificar uma mensagem envelopada](alternate-code-for-encoding-an-enveloped-message.md)
-   [Programa C de exemplo: codificando uma mensagem envelopada e assinada](example-c-program-encoding-an-enveloped-signed-message.md)

 

 
