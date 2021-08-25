---
description: As chaves de criptografia são essenciais para as operações criptográficas.
ms.assetid: dda7b527-1522-4b43-8d8e-44ce7983a9aa
title: Chaves de criptografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25647d64aafa8d996c60df37d1f5b5a86226451e1a0f3a3cfefc7ef405f3a11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876296"
---
# <a name="cryptographic-keys"></a>Chaves de criptografia

[*As chaves de criptografia*](../secgloss/c-gly.md) são essenciais para as operações criptográficas. Muitos esquemas criptográficos consistem em pares de operações, como criptografia e descriptografia, ou assinatura e verificação. Uma *chave* é uma parte dos dados variáveis que são alimentados como entrada em um algoritmo criptográfico para executar uma operação desse tipo. Em um esquema criptográfico bem projetado, a segurança do esquema depende apenas da segurança das chaves usadas.

As chaves de criptografia podem ser classificadas com base em seu uso dentro de um esquema criptográfico, como [chaves simétricas](symmetric-keys.md) ou [chaves assimétricas](public-private-key-pairs.md). Uma [*chave simétrica*](../secgloss/s-gly.md) é uma chave única que é usada para ambas as operações em um esquema criptográfico (por exemplo, para [*criptografar*](../secgloss/e-gly.md) e [*descriptografar*](../secgloss/d-gly.md) seus dados). Normalmente, a segurança do esquema depende de garantir que a chave seja conhecida apenas pelos participantes autorizados. As chaves assimétricas, por outro lado, são usadas em esquemas criptográficos em que chaves diferentes são necessárias para cada operação. Exemplos comuns desses esquemas são aqueles que usam [*pares de chaves pública/privada*](../secgloss/p-gly.md), em que a segurança do esquema depende de garantir que a [*chave privada*](../secgloss/p-gly.md) seja conhecida apenas por uma entidade. Por exemplo, os sistemas de criptografia de chave pública/privada usam duas chaves, uma [*chave pública*](../secgloss/p-gly.md) que qualquer pessoa pode usar para criptografar dados e uma [*chave privada*](../secgloss/p-gly.md) que apenas o destinatário autorizado possui e que pode ser usada para descriptografar os dados.

As chaves de criptografia podem ser classificadas ainda mais pela finalidade para a qual são usadas. Esses usos incluem geração de assinatura digital, verificação de assinatura digital, autenticação de mensagens, criptografia e descriptografia de dados, encapsulamento de chaves e transporte de chave. Para obter uma lista completa dos tipos de chave, conforme definido pelo [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST), consulte a seção 5 diretrizes gerais de gerenciamento de chaves da [publicação especial do NIST 800-57: recomendação para o gerenciamento de chaves – parte 1: geral (revisado)](https://csrc.nist.gov/publications/nistpubs/800-57/sp800-57-Part1-revised2_Mar08-2007.pdf).

 

 
