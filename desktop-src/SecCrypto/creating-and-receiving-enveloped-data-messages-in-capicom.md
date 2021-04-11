---
description: A mensagem envelopada consiste na mensagem criptografada, nos certificados dos destinatários pretendidos e no conjunto de chaves criptografadas, uma para cada destinatário. A mensagem gerada está no \# formato PKCS 7/CMS.
ms.assetid: 2acd0b58-1028-478d-bfa1-b02fa457d7e3
title: Criando e recebendo mensagens de dados envelopadas no CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672d56383ac635a295847777c0e557bbe7c40b69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296279"
---
# <a name="creating-and-receiving-enveloped-data-messages-in-capicom"></a>Criando e recebendo mensagens de dados envelopadas no CAPICOM

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Uma mensagem envelopada é uma mensagem criptografada para um conjunto de destinatários. No processo Envelopment, uma chave de criptografia de sessão é gerada e a mensagem é criptografada com essa chave. A chave de criptografia em si é, então, criptografada separadamente para cada destinatário usando as chaves públicas do certificado do destinatário desejado. A mensagem envelopada consiste na mensagem criptografada, nos certificados dos destinatários pretendidos e no conjunto de chaves criptografadas, uma para cada destinatário. A mensagem gerada está no \# formato PKCS 7/CMS.

As seções a seguir mostram procedimentos e exemplos para tarefas de mensagens envelopadas:

-   [Enviando uma mensagem de dados envelopada](sending-an-enveloped-data-message.md)
-   [Recebendo uma mensagem de dados envelopada](receiving-an-enveloped-data-message.md)

 

 



