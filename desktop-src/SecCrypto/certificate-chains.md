---
description: Para usar certificados de segurança, a autenticidade e a validade de cada certificado recebido devem ser verificadas. Essa verificação depende do conceito de confiança e da delegação do \[ SDK (Software Development Kit) da plataforma de confiança \] .
ms.assetid: e6cb0280-f531-40dc-bbb1-d8115d026e03
title: Cadeias de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bea42b6788997a86aade6f89d0f35d92a74daafc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461052"
---
# <a name="certificate-chains"></a>Cadeias de certificados

Para usar [*certificados*](../secgloss/c-gly.md) de segurança, a autenticidade e a validade de cada certificado recebido devem ser verificadas. Essa verificação depende do conceito de confiança e da delegação de confiança; para obter mais informações, consulte [hierarquia de confiança](hierarchy-of-trust.md).

Cada certificado contém um campo de assunto que identifica o indivíduo ou grupo para o qual o certificado foi emitido. Cada certificado também contém um campo emissor que identifica a autoridade de [*certificação*](../secgloss/c-gly.md) (CA) capacitada para certificar a identidade do assunto.

Uma cadeia de certificados consiste em todos os certificados necessários para certificar a entidade identificada pelo certificado final. Na prática, isso inclui o certificado final, os certificados de CAs intermediárias e o certificado de uma AC raiz confiável por todas as partes na cadeia. Cada CA intermediária na cadeia mantém um certificado emitido pela autoridade de certificação um nível acima dela na hierarquia de confiança. A CA raiz emite um certificado para si mesmo.

O processo de verificar a autenticidade e a validade de um certificado recebido recentemente envolve a verificação de todos os certificados na cadeia de certificados a partir da autoridade de certificação original, universalmente confiável, por meio de qualquer CAs intermediária, até o certificado que acabou de receber, que é chamado de certificado final. Um novo certificado só poderá ser confiável se cada certificado na cadeia do certificado for emitido e válido corretamente.

O acompanhamento de todos os certificados que retornam um novo certificado final pode se tornar complicado. Portanto, a tecnologia [*CryptoAPI*](../secgloss/c-gly.md) 2,0 fornece funções que automatizam a criação da cadeia de certificados que retornam qualquer certificado final específico. Essas funções também verificam e relatam a validade de cada certificado em uma cadeia.

As funções de criação de cadeia e verificação do [*CryptoAPI*](../secgloss/c-gly.md) 2,0 usam um mecanismo de cadeia para criar e verificar cadeias de certificados. Um mecanismo de cadeia define um namespace de armazenamento e o particionamento de cache para a infraestrutura de encadeamento de certificados. O CryptoAPI 2.0 fornece um mecanismo de cadeia padrão para qualquer processo de aplicativo que usa apenas repositórios de sistema padrão (por exemplo, MY, root, CA e Trust) para criação de cadeia e cache. Um aplicativo pode definir seu próprio namespace de repositório ou ter seu próprio cache particionado criando seu próprio mecanismo de cadeia. Para obter um comportamento de cache ideal, recomendamos que você crie um mecanismo de cadeia única na inicialização do aplicativo e use esse mecanismo de cadeia durante todo o tempo de vida do aplicativo.

Para obter uma lista de funções, consulte [funções de verificação da cadeia de certificados](cryptography-functions.md). Para um programa que cria cadeias de certificados e verifica certificados, consulte [exemplo C programa: criando uma cadeia de certificados](example-c-program-creating-a-certificate-chain.md).

 

 
