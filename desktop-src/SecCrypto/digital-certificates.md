---
description: Como os certificados digitais fornecem comunicações seguras e como usar o CryptoAPI para usar e gerenciar esses certificados.
ms.assetid: e523b335-0156-4f47-b55c-b80495587c4f
title: Certificados Digitais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161d200a0f8cab61594872f5182786a3e6597187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647000"
---
# <a name="digital-certificates"></a>Certificados Digitais

A autenticação é crucial para proteger as comunicações. Os usuários devem ser capazes de provar sua identidade para aqueles com quem eles se comunicam e devem ser capazes de verificar a identidade de outros. É difícil a comprovação de identidade em uma rede, pois as pessoas não se encontram fisicamente durante a comunicação, permitindo que um usuário mal-intencionado intercepte mensagens ou se faça passar por outra pessoa física ou jurídica. Um método deve ser trabalhado para manter o nível de confiança necessário no processo de comunicação.

O [*certificado digital*](../secgloss/c-gly.md) é uma credencial comum que fornece um meio para verificar a identidade. Esta seção fornece uma visão geral de como os certificados fornecem comunicações seguras e como usar o CryptoAPI para usar e gerenciar esses certificados.

Um certificado é um conjunto de dados que identifica uma entidade. Uma organização confiável atribui um certificado a um indivíduo ou a uma entidade que associa uma chave pública ao indivíduo. O indivíduo ou entidade para o qual um certificado é emitido é chamado de assunto do certificado. A organização confiável que emite o certificado é uma [*autoridade de certificação*](../secgloss/c-gly.md) (CA) e é conhecida como emissor do certificado. Uma AC confiável só emitirá um certificado depois de verificar a identidade do assunto do certificado.

Os certificados usam técnicas de criptografia para resolver o problema da falta de contato físico entre essas comunicações. O uso dessas técnicas limita a possibilidade de uma pessoa não ética interceptar, alterar ou falsificar mensagens. Essas técnicas de criptografia dificultam a modificação dos certificados. Portanto, é difícil para uma entidade representar outra pessoa.

Os dados em um certificado incluem a chave pública de criptografia do [*par de chaves pública/privada*](../secgloss/p-gly.md)da entidade do certificado. Uma mensagem assinada com a chave privada do remetente só pode ser recuperada pelo destinatário da mensagem usando a chave pública do remetente. Essa chave pode ser encontrada em uma cópia do certificado do remetente. Recuperar uma assinatura com uma [*chave pública*](../secgloss/p-gly.md) de um certificado comprova que a assinatura foi produzida usando a [*chave privada*](../secgloss/p-gly.md)da entidade do certificado. Se o remetente tiver sido vigilante e tiver mantido o segredo da chave privada, o receptor poderá confiar na identidade do remetente da mensagem.

Em uma rede, geralmente há um aplicativo confiável conhecido como servidor de [*certificados*](../secgloss/c-gly.md). Uma AC em execução em um computador seguro gerencia o servidor de certificado. Este aplicativo tem acesso à chave pública de todos os seus clientes. Os servidores de certificado dispensam mensagens conhecidas como certificados, cada uma contendo a chave pública de um de seus usuários clientes. Cada certificado é assinado com a chave privada da autoridade de certificação. Assim, o receptor desse certificado pode verificar se uma autoridade de certificação especificada o enviou.

Os certificados digitais também incluem extensões e propriedades estendidas que fornecem informações adicionais sobre a entidade do certificado, como o endereço de email da entidade e as atividades que a entidade do certificado pode executar.

 

 
