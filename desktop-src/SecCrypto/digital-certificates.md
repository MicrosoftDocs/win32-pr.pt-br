---
description: Como os certificados digitais fornecem comunicações seguras e como usar CryptoAPI para usar e gerenciar esses certificados.
ms.assetid: e523b335-0156-4f47-b55c-b80495587c4f
title: Certificados Digitais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467f2df1a529d94fa5a04385c7f91f5aefbb40c0488ef0c5c484fe98c3874358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875296"
---
# <a name="digital-certificates"></a>Certificados Digitais

A autenticação é crucial para proteger as comunicações. Os usuários devem ser capazes de provar sua identidade para aqueles com quem se comunicam e devem ser capazes de verificar a identidade de outras pessoas. É difícil a comprovação de identidade em uma rede, pois as pessoas não se encontram fisicamente durante a comunicação, permitindo que um usuário mal-intencionado intercepte mensagens ou se faça passar por outra pessoa física ou jurídica. Um método deve ser trabalhado para manter o nível de confiança necessário dentro do processo de comunicação.

O [*certificado digital*](../secgloss/c-gly.md) é uma credencial comum que fornece um meio de verificar a identidade. Esta seção fornece uma visão geral de como os certificados fornecem comunicações seguras e como usar CryptoAPI para usar e gerenciar esses certificados.

Um certificado é um conjunto de dados que identifica uma entidade. Uma organização confiável atribui um certificado a um indivíduo ou a uma entidade que associa uma chave pública ao indivíduo. O indivíduo ou entidade para o qual um certificado é emitido é chamado de assunto desse certificado. A organização confiável que emite o certificado é uma AC [*(autoridade*](../secgloss/c-gly.md) de certificação) e é conhecida como emissor do certificado. Uma AC confiável emitirá apenas um certificado depois de verificar a identidade do assunto do certificado.

Os certificados usam técnicas criptográficas para resolver o problema da falta de contato físico entre os que se comunicam. O uso dessas técnicas limita a possibilidade de uma pessoa de interceptação, alteração ou falsificação de mensagens. Essas técnicas criptográficas dificultam a modificação de certificados. Portanto, é difícil para uma entidade representar outra pessoa.

Os dados em um certificado incluem a chave de criptografia pública do par de chaves [*pública/privada*](../secgloss/p-gly.md)da entidade do certificado. Uma mensagem assinada com a chave privada do remetente só pode ser recuperada pelo destinatário da mensagem usando a chave pública do remetente. Essa chave pode ser encontrada em uma cópia do certificado do remetente. A recuperação de uma assinatura com uma chave [*pública*](../secgloss/p-gly.md) de um certificado prova que a assinatura foi produzida usando a chave privada da entidade [*de certificado.*](../secgloss/p-gly.md) Se o remetente tiver sido atento e tiver mantido o segredo da chave privada, o receptor poderá ter confiança na identidade do remetente da mensagem.

Em uma rede, geralmente há um aplicativo confiável conhecido como servidor [*de certificados*](../secgloss/c-gly.md). Uma AC em execução em um computador seguro gerencia o servidor de certificados. Esse aplicativo tem acesso à chave pública de todos os seus clientes. Os servidores de certificados descartam mensagens conhecidas como certificados, cada uma contendo a chave pública de um de seus usuários cliente. Cada certificado é assinado com a chave privada da AC. Portanto, o receptor desse certificado pode verificar se uma AC especificada o enviou.

Os certificados digitais também incluem extensões e propriedades estendidas que fornecem informações adicionais sobre o assunto do certificado, como o endereço de email da pessoa e as atividades que o assunto do certificado pode executar.

 

 
