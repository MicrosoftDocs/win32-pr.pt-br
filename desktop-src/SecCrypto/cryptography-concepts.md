---
description: 'A comunicação segura em redes não seguras geralmente envolve três áreas importantes de preocupação: privacidade, autenticação e integridade.'
ms.assetid: bfffe87d-8392-4b4a-8bbc-01b9c13fba47
title: Conceitos de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1909cf999bd5eb2f91bd5c7e0243b13969e692792c4ff32804e7c9a7d2940b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876147"
---
# <a name="cryptography-concepts"></a>Conceitos de criptografia

A comunicação segura em redes não seguras geralmente envolve três áreas importantes de preocupação: [privacidade,](#privacy) [autenticação](#authentication)e [integridade.](#integrity) A API de criptografia da Microsoft ([*CryptoAPI*](../secgloss/c-gly.md)) é um conjunto de funções, interfaces e ferramentas que os aplicativos podem usar para melhorar a confiança de segurança nessas áreas.

Além da funcionalidade de privacidade, autenticação e integridade, [*o CryptoAPI*](../secgloss/c-gly.md) também fornece:

-   Mensagens de codificação para o formulário ASN.1 (Abstract [*Syntax Notation One).*](../secgloss/a-gly.md)
-   Decodificação de mensagens ASN.1.
-   Gerenciando coleções [*de certificados*](../secgloss/c-gly.md) em [*armazenamentos de certificados.*](../secgloss/c-gly.md)
-   Trabalhando com [*listas de certificados de*](../secgloss/c-gly.md) confiança e cadeias de certificados para verificação da validade dos certificados.

## <a name="privacy"></a>Privacidade

Para obter privacidade, os usuários devem impedir que qualquer pessoa, exceto o destinatário pretendido, leia uma mensagem. Melhorar a probabilidade de privacidade geralmente envolve o uso de alguma forma [*de criptografia*](../secgloss/c-gly.md). Técnicas criptográficas são usadas para criptografar (embaralhar) mensagens antes que as mensagens sejam armazenadas ou transmitidas.

A criptografia de dados transforma [*texto não criptografado*](../secgloss/p-gly.md) em texto [*cifrado.*](../secgloss/c-gly.md) Os dados a serem criptografados podem ser [*texto ASCII,*](../secgloss/a-gly.md) um arquivo de banco de dados ou qualquer outro dado. Nesta documentação, [](../secgloss/m-gly.md) o termo mensagem é usado para se referir a qualquer dado, texto  não criptografado refere-se a dados que não foram criptografados e texto cifrado refere-se a dados que foram criptografados. Um bom sistema de criptografia de dados dificulta a transformação de dados criptografados em texto não criptografado sem uma chave secreta.

Os dados criptografados podem ser armazenados em mídia não segura ou transmitidos por uma rede não segura. Posteriormente, os dados podem ser descriptografados em sua forma original. Esse processo é mostrado na ilustração a seguir.

![ajudando a manter a privacidade em toda a criptografia e descriptografia](images/capi01.png)

Quando os dados são criptografados, a mensagem e uma [*chave de*](../secgloss/e-gly.md) criptografia são passadas para o algoritmo de criptografia. Para descriptografar os dados, o texto cifrado e uma chave [*de descriptografia*](../secgloss/d-gly.md) são passados para o algoritmo de descriptografia. A criptografia e a descriptografia podem ser feitas usando uma única chave em um processo chamado criptografia simétrica.

As chaves usadas para descriptografar uma mensagem devem ser mantidas o mais secretas e seguras possível e devem ser transmitidas a outros usuários usando técnicas de aprimoramento de segurança. Isso é discutido ainda mais em [Criptografia de Dados e Descriptografia.](data-encryption-and-decryption.md) O principal desafio é restringir corretamente o acesso à chave de descriptografia porque qualquer pessoa que a possui poderá descriptografar todas as mensagens criptografadas com sua chave de criptografia correspondente.

Para atender às metas de privacidade declarados, os desenvolvedores podem usar [*CryptoAPI*](../secgloss/c-gly.md) para criptografar e assinar dados digitalmente de maneira flexível, ajudando a fornecer proteção para os dados confidenciais da chave privada do usuário.

[*O CryptoAPI*](../secgloss/c-gly.md) fornece as seguintes áreas de funcionalidade para executar as tarefas de criptografia/descriptografia, assinatura de mensagens e armazenamento de chaves:

-   [Funções de criptografia base](cryptography-functions.md)
-   [Funções de mensagem simplificadas](cryptography-functions.md)
-   [Funções de mensagem de baixo nível](cryptography-functions.md)

## <a name="authentication"></a>Autenticação

Comunicações seguras exigem que os indivíduos que se comunicam saibam a identidade daqueles com quem se comunicam. A autenticação é o processo de verificar a identidade de uma pessoa ou entidade.

Por exemplo, no dia a dia, a documentação física, geralmente chamada de credenciais, é usada para verificar a identidade de uma pessoa. Quando uma verificação é esvasada, a pessoa que está dinheiro com a verificação pode pedir para ver uma licença de motorista. A licença do motorista é um documento físico que aumenta a confiança do comerciante na identidade da pessoa que está dinheiro com a verificação. Nesse caso, a pessoa que recebe a verificação confia que o estado que emissão da licença verificou adequadamente a identidade do titular da licença.

Os passports fornecem outro exemplo. Um oficial oficial de oficial de oficial vê um passaporte e aceita-o como uma prova de que uma pessoa é quem diz ser. Os funcionários confiam que o governo fez um trabalho adequado para identificar o titular do passaporte antes de emissão do passaporte. Em ambos os exemplos, existe um nível de confiança no emissor do documento físico.

A autenticação também envolve garantir que os dados recebidos são os dados que foram enviados. Se a parte A enviar uma mensagem para a parte B, a parte B precisará ser capaz de provar que a mensagem recebida foi a mensagem que a parte A enviou e não uma mensagem que foi substituída por essa mensagem. Para fornecer essa forma de autenticação, [*o CryptoAPI*](../secgloss/c-gly.md) fornece funções para assinar dados e verificar assinaturas usando pares de chaves públicas/privadas.

Como as comunicações em uma rede de computador ocorrem sem contato físico entre os comunicadores, verificar a identidade geralmente depende de uma credencial que pode ser enviada e recebida por uma rede. Essa credencial deve ser emitida por um emissor confiável de credenciais. Certificados digitais, normalmente conhecidos como certificados, são apenas uma credencial desse tipo. Eles são uma maneira de verificar a identidade e obter autenticação em uma rede de computador.

Um certificado digital é uma credencial emitida por uma organização ou entidade confiável chamada AC (autoridade de certificação). Essa credencial contém uma chave pública (consulte Pares de Chaves [Públicas/Privadas)](public-private-key-pairs.md)e dados que identificam a entidade do certificado. Um certificado é emitido por uma AC somente depois que a AC verificou a identidade da pessoa do certificado e confirmou que a chave pública incluída com o certificado pertence a essa pessoa.

A comunicação entre uma AC e um solicitante de certificado pode ser realizada pelo solicitante que carrega fisicamente as informações necessárias, talvez armazenadas em um disquete, para a AC. No entanto, a comunicação geralmente é realizada com uma mensagem assinada enviada por uma rede. A AC geralmente usa um aplicativo confiável chamado servidor de certificado para emite certificados.

[*O CryptoAPI dá*](../secgloss/c-gly.md) suporte à autenticação por meio do uso de certificados digitais, com funções de codificação/decodificar certificado e funções [*de armazenamento*](../secgloss/c-gly.md) de certificados.

Para obter mais informações sobre verificação de identidade e autenticação por meio do uso de certificados, consulte [Certificados Digitais](digital-certificates.md).

## <a name="integrity"></a>Integridade

Todos os dados enviados por uma mídia não segura podem ser alterados por acidente ou de propósito. No mundo real, os selos são usados para fornecer e provar a integridade. Um gargalo de leite, por exemplo, pode vir em empacotamento à prova de adulteração que tem um selo ininterrupto para provar que nada foi colocado no pacote depois que o pacote saiu do fabricante.

Da mesma maneira, um receptor de dados deve ser capaz de verificar a identidade do remetente dos dados e verificar se os dados recebidos são exatamente os dados que foram enviados; ou seja, que ele não foi adulterado. Estabelecer a [*integridade*](../secgloss/i-gly.md) dos dados recebidos geralmente é feito enviando não apenas os dados originais, mas também uma mensagem de verificação, chamada [*de hash*](../secgloss/h-gly.md), sobre esses dados. Os dados e a mensagem de verificação podem ser enviados com uma [*assinatura digital*](../secgloss/d-gly.md) que prova a origem de ambos.

A integridade é fornecida em CryptoAPI por meio do uso de [Assinaturas Digitais](digital-signatures.md) e [Hashes de Dados](data-hashes.md).

[*O CryptoAPI dá*](../secgloss/c-gly.md) suporte à integridade por meio do uso de funções de mensagem para assinar dados e verificar assinaturas digitais.

 

 
