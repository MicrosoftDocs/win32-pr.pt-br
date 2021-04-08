---
description: Para enviar dados por meio de uma mídia de comunicação, como uma linha telefônica, os dados devem ser serializados&\# 8212; ou seja, convertidos em uma cadeia de caracteres e zeros transmitidos em série na linha.
ms.assetid: ef8982dc-bbbc-466a-9afe-dd0425c23f1d
title: Dados codificados e decodificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b130232ac67503c6a20835c4c9b4e728b36f8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920817"
---
# <a name="encoded-and-decoded-data"></a>Dados codificados e decodificados

Para enviar dados por meio de uma mídia de comunicação, como uma linha telefônica, os dados devem ser [*serializados*](../secgloss/s-gly.md), ou seja, convertidos em uma cadeia de caracteres e zeros que são transmitidos em série na linha. A serialização deve ser feita de forma que o computador que recebe os dados possa converter os dados de volta em seu formato original. A forma como a serialização é realizada é chamada de [*protocolo de comunicação*](../secgloss/c-gly.md)e é controlada pelo software e pelo hardware de transmissão de dados. Há vários níveis nos quais os dados são convertidos. A ilustração a seguir mostra uma exibição bastante simplificada das camadas de protocolo de comunicação.

![camadas de protocolo de comunicação](images/layer.png)

A ilustração anterior mostra a camada de aplicativo no computador \# 1 que envia os dados a serem transmitidos (que geralmente consistem em alguma combinação de caracteres textuais e números) para a camada de codificação/decodificação. A camada de codificação/decodificação codifica os dados em um fluxo de bytes de computador. No nível mais baixo, a camada de hardware, o hardware converte os bytes de dados em um fluxo de série de uns e zeros transmitidos pela linha para o computador \# 2. A camada de hardware do computador \# 2 converte os e zeros de volta em bytes de computador e os passa para a camada de codificação/decodificação para decodificação. A camada de codificação/decodificação decodifica os bytes de volta em seu formato original e passa os dados para a camada de aplicativo.

Um princípio de design de software aceito é usar *abstração*, ou seja, o processo de descrever um problema ou objeto em termos de seus parâmetros gerais em vez de descrever todos os detalhes necessários para resolver o problema ou descrever todos os detalhes de um objeto. Usando a abstração, um designer pode especificar um objeto de software que tenha qualidades específicas sem preocupação com o modo como o objeto é realmente implementado no código do software. Essa prática deixa a implementação aberta. Ele também simplifica a especificação e torna possível o estado axioms sobre o objeto que pode ser comprovado quando o objeto é implementado. Esses axioms podem ser assumidos quando o objeto é empregado em outro objeto de nível mais alto. A abstração é a marca registrada das especificações de software mais contemporânea.

A maioria dos [*protocolos de comunicação*](../secgloss/c-gly.md) envolve uma boa dose de abstração. Os objetos em camadas mais altas são definidos de abstração e devem ser implementados usando objetos em camadas inferiores. Por exemplo, um serviço em uma camada pode exigir a transferência de determinados objetos abstratos entre computadores. Uma camada de nível inferior pode usar regras de codificação para transformar os objetos abstratos em cadeias de caracteres e zeros.

Um método comum de especificar objetos abstratos destinados a serem transmitidos em série [*é chamado de*](../secgloss/a-gly.md) ASN. 1). O ASN. 1 é definido na recomendação de CCITT [*X. 208*](../secgloss/x-gly.md). Um conjunto de regras de ASN. 1 para representar esses objetos como cadeias de caracteres e zeros é chamado de [*Distinguished Encoding Rules*](../secgloss/d-gly.md) (der) e é definido na recomendação de CCITT [*X. 509*](../secgloss/x-gly.md), seção 8,7. Esses são os métodos de codificação usados atualmente pelo CryptoAPI.

Para obter mais informações sobre as funções de codificação/decodificação, consulte [codificando objetos e funções de decodificação](cryptography-functions.md).

 

 
