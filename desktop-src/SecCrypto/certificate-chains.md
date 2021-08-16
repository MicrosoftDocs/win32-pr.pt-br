---
description: Para usar certificados para segurança, a autenticidade e a validade de cada certificado recebido devem ser verificadas. Essa verificação depende do conceito de confiança e da delegação do SDK (Software Development Kit) da plataforma de \[ \] confiança.
ms.assetid: e6cb0280-f531-40dc-bbb1-d8115d026e03
title: Cadeias de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6efdd49cbd66c74805cc560286e5f15a981ef200df5523c602c2bb4b395a04e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771935"
---
# <a name="certificate-chains"></a>Cadeias de certificados

Para usar [*certificados*](../secgloss/c-gly.md) para segurança, a autenticidade e a validade de cada certificado recebido devem ser verificadas. Essa verificação depende do conceito de confiança e da delegação de confiança; Para obter mais informações, consulte [Hierarquia de confiança.](hierarchy-of-trust.md)

Cada certificado contém um campo de assunto que identifica o indivíduo ou grupo para o qual o certificado foi emitido. Cada certificado também contém um campo emissor que identifica a AC [*(autoridade*](../secgloss/c-gly.md) de certificação) capacitada a certificar a identidade da entidade.

Uma cadeia de certificados consiste em todos os certificados necessários para certificar o assunto identificado pelo certificado final. Na prática, isso inclui o certificado final, os certificados de AC intermediárias e o certificado de uma AC raiz confiável por todas as partes da cadeia. Cada AC intermediária na cadeia contém um certificado emitido pela AC um nível acima dele na hierarquia de confiança. A AC raiz emite um certificado para si mesmo.

O processo de verificar a autenticidade e a validade de um certificado recém-recebido envolve a verificação de todos os certificados na cadeia de certificados da AC original e universalmente confiável, por meio de qualquer AC intermediária, até o certificado recém-recebido, que é chamado de certificado final. Um novo certificado só poderá ser confiável se cada certificado na cadeia desse certificado for emitido corretamente e válido.

Acompanhar todos os certificados que acompanham um novo certificado final pode se tornar complicado. Portanto, [*a tecnologia CryptoAPI*](../secgloss/c-gly.md) 2.0 fornece funções que automatizam a criação da cadeia de certificados que faz backup de qualquer certificado final determinado. Essas funções também verificam e relatam a validade de cada certificado em uma cadeia.

As funções de criação e verificação de cadeia do [*CryptoAPI*](../secgloss/c-gly.md) 2.0 usam um mecanismo de cadeia para criar e verificar cadeias de certificados. Um mecanismo de cadeia define um namespace de armazenamento e um particionamento de cache para a Infraestrutura de Encadeamento de Certificados. CryptoAPI 2.0 fornece um mecanismo de cadeia padrão para qualquer processo de aplicativo que usa somente armazenamentos de sistema padrão (por exemplo, MY, Raiz, AC e Confiança) para criação e cache de cadeias. Um aplicativo pode definir seu próprio namespace de armazenamento ou ter seu próprio cache particionado criando seu próprio mecanismo de cadeia. Para obter o comportamento ideal de cache, recomendamos que você crie um mecanismo de cadeia única na inicialização do aplicativo e use esse mecanismo de cadeia durante todo o tempo de vida do aplicativo.

Para ver uma lista de funções, consulte [Funções de verificação de cadeia de certificados](cryptography-functions.md). Para um programa que cria cadeias de certificados e verifica certificados, consulte [Programa C de exemplo: criando uma cadeia de certificados](example-c-program-creating-a-certificate-chain.md).

 

 
