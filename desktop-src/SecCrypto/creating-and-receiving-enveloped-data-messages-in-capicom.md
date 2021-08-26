---
description: A mensagem envelopada consiste na mensagem criptografada, nos certificados dos destinatários pretendidos e no conjunto de chaves criptografadas, uma para cada destinatário. A mensagem gerada está no \# formato PKCS 7/CMS.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Criando e recebendo mensagens de dados envelopadas no CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4024516333b7dd416f788f181f2ac36e5e0f4e015953cdab26d08b48da16c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876535"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a>Criando e recebendo mensagens de dados envelopadas no CAPICOM

\[o capicom é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Uma mensagem envelopada é uma mensagem criptografada para um conjunto de destinatários. No processo Envelopment, uma chave de criptografia de sessão é gerada e a mensagem é criptografada com essa chave. A chave de criptografia em si é, então, criptografada separadamente para cada destinatário usando as chaves públicas do certificado do destinatário desejado. A mensagem envelopada consiste na mensagem criptografada, nos certificados dos destinatários pretendidos e no conjunto de chaves criptografadas, uma para cada destinatário. A mensagem gerada está no \# formato PKCS 7/CMS.

As seções a seguir mostram procedimentos e exemplos para tarefas de mensagens envelopadas:

-   [Enviando uma mensagem de dados envelopada](sending-an-enveloped-data-message.md)
-   [Recebendo uma mensagem de dados envelopada](receiving-an-enveloped-data-message.md)

 

 



