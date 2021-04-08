---
description: Quando um documento ou texto precisa ter privacidade protegida por um único usuário ou quando o documento é compartilhado entre um pequeno grupo de pessoas que têm acesso à mesma senha secreta, a criptografia/descriptografia simples pode ser feita.
ms.assetid: 68eefd24-c924-4dd1-8cb3-cc20106f9605
title: Criptografando e descriptografando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd7123544fb9c8fa59291be2eae2c5bf9a120f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922359"
---
# <a name="encrypting-and-decrypting-data"></a>Criptografando e descriptografando dados

\[O CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o .NET Framework para implementar recursos de segurança. Para obter mais informações, consulte [alternativas ao uso do CApicom](alternatives-to-using-capicom.md).\]

Quando um documento ou texto precisa ter privacidade protegida por um único usuário ou quando o documento é compartilhado entre um pequeno grupo de pessoas que têm acesso à mesma senha secreta, a criptografia/descriptografia simples pode ser feita. O CAPICOM não oferece suporte ao \# tipo de conteúdo ENCRYPTEDDATA PKCS 7, mas usa uma estrutura ASN não padrão para EncryptedData. Portanto, somente o capicor pode descriptografar um objeto capicot EncryptedData.

As seções a seguir mostram exemplos de criptografia e tarefas de descriptografia:

-   [Criptografando uma mensagem no CAPICOM](encrypting-a-message-in-capicom.md)
-   [Descriptografando uma mensagem no CAPICOM](decrypting-a-message-in-capicom.md)

 

 



