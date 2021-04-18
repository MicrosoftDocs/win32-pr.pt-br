---
description: 'A comunicação segura em redes não seguras geralmente envolve três áreas principais de preocupação: privacidade, autenticação e integridade.'
ms.assetid: bfffe87d-8392-4b4a-8bbc-01b9c13fba47
title: Conceitos de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aad1528032c20c5492a98798f8a175ca331e462
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755953"
---
# <a name="cryptography-concepts"></a>Conceitos de criptografia

A comunicação segura em redes não seguras geralmente envolve três áreas principais de preocupação: [privacidade](#privacy), [autenticação](#authentication)e [integridade](#integrity). O Microsoft Cryptography API ([*CryptoAPI*](../secgloss/c-gly.md)) é um conjunto de funções, interfaces e ferramentas que os aplicativos podem usar para melhorar a confiança da segurança nessas áreas.

Além da funcionalidade de privacidade, autenticação e integridade, o [*CryptoAPI*](../secgloss/c-gly.md) também fornece para:

-   Mensagens de codificação para um formulário de [*notação de sintaxe abstrata*](../secgloss/a-gly.md) (ASN. 1).
-   Decodificando mensagens ASN. 1.
-   Gerenciando coleções de [*certificados*](../secgloss/c-gly.md) em [*repositórios de certificados*](../secgloss/c-gly.md).
-   Trabalhando com [*listas*](../secgloss/c-gly.md) de certificados confiáveis e cadeias de certificados para verificação da validade dos certificados.

## <a name="privacy"></a>Privacidade

Para obter privacidade, os usuários devem impedir que qualquer pessoa, exceto o destinatário pretendido, leia uma mensagem. Melhorar a probabilidade de privacidade geralmente envolve o uso de alguma forma de [*criptografia*](../secgloss/c-gly.md). Técnicas de criptografia são usadas para criptografar (embaralhar) mensagens antes que as mensagens sejam armazenadas ou transmitidas.

A criptografia de dados transforma o [*texto não criptografado*](../secgloss/p-gly.md) em [*texto cifrado*](../secgloss/c-gly.md). Os dados a serem criptografados podem ser texto [*ASCII*](../secgloss/a-gly.md) , um arquivo de banco de dados ou qualquer outro dado. Nesta documentação, a [*mensagem*](../secgloss/m-gly.md) de termo é usada para se referir a qualquer dado, texto não criptografado refere-se aos dados que não foram codificados e *texto cifrado* refere-se aos dados que foram criptografados. Um bom sistema de criptografia de dados dificulta a transformação de dados criptografados de volta em texto sem formatação e uma chave secreta.

Os dados criptografados podem ser armazenados em mídia não segura ou transmitidos por uma rede não segura. Posteriormente, os dados podem ser descriptografados em seu formato original. Esse processo é mostrado na ilustração a seguir.

![ajudando a manter a privacidade durante a criptografia e a descriptografia](images/capi01.png)

Quando os dados são criptografados, a mensagem e uma chave de [*criptografia*](../secgloss/e-gly.md) são passadas para o algoritmo de criptografia. Para descriptografar os dados, o texto cifrado e uma chave de [*descriptografia*](../secgloss/d-gly.md) são passados para o algoritmo de descriptografia. A criptografia e a descriptografia podem ser feitas usando uma única chave em um processo chamado criptografia simétrica.

As chaves usadas para descriptografar uma mensagem devem ser mantidas como secretas e seguras possíveis, e devem ser transmitidas a outros usuários usando técnicas de aprimoramento de segurança. Isso é discutido mais detalhadamente em [criptografia e](data-encryption-and-decryption.md)descriptografia de dados. O principal desafio é restringir corretamente o acesso à chave de descriptografia porque qualquer pessoa que a possua poderá descriptografar todas as mensagens que foram criptografadas com sua chave de criptografia correspondente.

Para lidar com as metas declaradas de privacidade, os desenvolvedores podem usar o [*CryptoAPI*](../secgloss/c-gly.md) para criptografar e assinar dados digitalmente de maneira flexível, ao mesmo tempo em que ajudam a fornecer proteção para os dados confidenciais de chave privada do usuário.

O [*CryptoAPI*](../secgloss/c-gly.md) fornece as seguintes áreas de funcionalidade para executar as tarefas de criptografia/descriptografia, assinatura de mensagens e armazenamento de chaves:

-   [Funções de criptografia base](cryptography-functions.md)
-   [Funções de mensagens simplificadas](cryptography-functions.md)
-   [Funções de mensagem de nível baixo](cryptography-functions.md)

## <a name="authentication"></a>Autenticação

As comunicações seguras exigem que os indivíduos que se comunicam saibam a identidade daqueles com quem eles se comunicam. A autenticação é o processo de verificar a identidade de uma pessoa ou entidade.

Por exemplo, na vida útil do dia a dia, a documentação física, geralmente chamada de credenciais, é usada para verificar a identidade de uma pessoa. Quando uma verificação é encaixada, a pessoa que faz o pagamento da verificação pode pedir para ver a licença de um driver. A licença do driver é um documento físico que aumenta a confiança do comerciante na identidade da pessoa que está encaixando a verificação. Nesse caso, a pessoa que está encaixando a verificação confia que o estado que emite a licença verificou adequadamente a identidade do titular da licença.

Os passaportes fornecem outro exemplo. Um alfândega oficial examina um passaporte e o aceita como prova de que uma pessoa é quem ele diz. O oficial confia que o governo fez um trabalho adequado para identificar o titular do Passport antes de emitir o Passport. Em ambos os exemplos, existe um nível de confiança no emissor do documento físico.

A autenticação também envolve garantir que os dados recebidos sejam os dados que foram enviados. Se a parte A enviar uma mensagem para a parte B, a parte B deverá ser capaz de provar que a mensagem recebida foi a mensagem que a parte A enviou e não uma mensagem que foi substituída por essa mensagem. Para fornecer essa forma de autenticação, o [*CryptoAPI*](../secgloss/c-gly.md) fornece funções para assinar dados e verificar assinaturas usando pares de chaves públicas/privadas.

Como as comunicações em uma rede de computador ocorrem sem nenhum contato físico entre os Communicator, verificar a identidade geralmente depende de uma credencial que possa ser enviada e recebida pela rede. Essa credencial deve ser emitida por um emissor confiável de credenciais. Certificados digitais, comumente conhecidos como certificados, são apenas uma credencial. Eles são uma maneira de verificar a identidade e obter autenticação em uma rede de computadores.

Um certificado digital é uma credencial emitida por uma organização ou entidade confiável chamada autoridade de certificação (CA). Essa credencial contém uma chave pública (consulte [pares de chaves públicas/privadas](public-private-key-pairs.md)) e dados que identificam o assunto do certificado. Um certificado é emitido por uma autoridade de certificação somente depois que a autoridade de certificação verificou a identidade da entidade do certificado e confirmou que a chave pública incluída com o certificado pertence a esse assunto.

A comunicação entre uma autoridade de certificação e um solicitante de certificado pode ser realizada pelo solicitante que armazena fisicamente as informações necessárias, talvez armazenadas em um disquete, para a autoridade de certificação. No entanto, a comunicação normalmente é realizada com uma mensagem assinada enviada por uma rede. A AC geralmente usa um aplicativo confiável chamado servidor de certificado para emitir certificados.

O [*CryptoAPI*](../secgloss/c-gly.md) dá suporte à autenticação por meio do uso de certificados digitais, com funções de codificação/decodificação de certificado e funções de [*repositório de certificados*](../secgloss/c-gly.md) .

Para obter mais informações sobre a verificação de identidade e a autenticação por meio do uso de certificados, consulte [certificados digitais](digital-certificates.md).

## <a name="integrity"></a>Integridade

Todos os dados enviados por uma mídia não segura podem ser alterados por acidente ou por finalidade. No mundo real, os selos são usados para fornecer e provar a integridade. Uma garrafa de Aspirin, por exemplo, pode vir no empacotamento de adulteração que tem um selo não quebrado para provar que nada foi colocado no pacote depois que o pacote saiu do fabricante.

Da mesma maneira, um receptor de dados deve ser capaz de verificar a identidade do remetente dos dados e certificar-se de que os dados recebidos são exatamente os dados que foram enviados; ou seja, se ele não foi adulterado. O estabelecimento da [*integridade*](../secgloss/i-gly.md) dos dados recebidos geralmente é feito enviando-se não apenas os dados originais, mas também uma mensagem de verificação, chamada de [*hash*](../secgloss/h-gly.md), sobre esses dados. Os dados e a mensagem de verificação podem ser enviados com uma [*assinatura digital*](../secgloss/d-gly.md) que comprova a origem de ambos.

A integridade é fornecida no CryptoAPI por meio do uso de [assinaturas digitais](digital-signatures.md) e [hashes de dados](data-hashes.md).

O [*CryptoAPI*](../secgloss/c-gly.md) dá suporte à integridade por meio do uso de funções de mensagem para assinar dados e verificar assinaturas digitais.

 

 
