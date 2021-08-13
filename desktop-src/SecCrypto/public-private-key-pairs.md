---
description: Chaves assimétricas, também conhecidas como pares de chaves pública/privada, são usadas para criptografia assimétrica. A criptografia assimétrica é usada principalmente para criptografar e descriptografar chaves de sessão e assinaturas digitais. A criptografia assimétrica usa algoritmos de criptografia de chave pública.
ms.assetid: f75e5e6c-0a84-47ac-97db-5063327f7931
title: Chaves assimétricas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374ba5ae17610154e306f7bdafd895116e83371ea446babfa19b5c92c29a2247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901468"
---
# <a name="asymmetric-keys"></a>Chaves assimétricas

[*Chaves assimétricas*](../secgloss/a-gly.md), também conhecidas como [*pares de chaves pública/privada*](../secgloss/p-gly.md), são usadas para criptografia assimétrica. A criptografia assimétrica é usada principalmente para criptografar e descriptografar [*chaves de sessão*](../secgloss/s-gly.md) e [*assinaturas digitais*](../secgloss/d-gly.md). A criptografia assimétrica usa algoritmos de [*criptografia de chave pública*](../secgloss/p-gly.md) .

Os algoritmos de chave pública usam duas chaves diferentes: uma [*chave pública*](../secgloss/p-gly.md) e uma [*chave privada*](../secgloss/p-gly.md). O membro de chave privada do par deve ser mantido privado e seguro. A chave pública, no entanto, pode ser distribuída para qualquer pessoa que a solicite. A chave pública de um par de chaves geralmente é distribuída por meio de um [*certificado digital*](../secgloss/c-gly.md). Quando uma chave de um par de chaves é usada para criptografar uma mensagem, a outra chave desse par é necessária para descriptografar a mensagem. Portanto, se a chave pública do usuário A for usada para criptografar dados, somente o usuário A (ou alguém que tenha acesso à chave privada do usuário A) poderá descriptografar os dados. Se a chave privada do usuário A for usada para criptografar dados, somente a chave pública do usuário A descriptografará os dados, indicando assim que o usuário A (ou alguém com acesso à chave privada do usuário A) fez a criptografia.

Se a chave privada for usada para assinar uma mensagem, a chave pública desse par deverá ser usada para validar a assinatura. Por exemplo, se Alice quiser enviar a alguém uma mensagem assinada digitalmente, ela assinaria a mensagem com a chave privada e a outra pessoa poderá verificar sua assinatura usando sua chave pública. Como supostamente apenas Alice tem acesso à sua chave privada, o fato de que a assinatura pode ser verificada com a chave pública de Alice indica que Alice criou a assinatura.

Infelizmente, os algoritmos de chave pública são muito lentos, aproximadamente 1.000 vezes mais lentos do que os algoritmos simétricos. Não é prático usá-los para criptografar grandes quantidades de dados. Na prática, os algoritmos de chave pública são usados para criptografar [*chaves de sessão*](../secgloss/s-gly.md). Os [*algoritmos simétricos*](../secgloss/s-gly.md) são usados para criptografia/descriptografia da maioria dos dados.

Da mesma forma, como assinar uma mensagem, na verdade, criptografa a mensagem, não é prático usar algoritmos de assinatura de chave pública para assinar mensagens grandes. Em vez disso, um [*hash*](../secgloss/h-gly.md) de comprimento fixo é feito da mensagem e o valor de hash é assinado. Para obter mais informações, consulte [hashes e assinaturas digitais](hashes-and-digital-signatures.md).

Cada usuário geralmente tem dois [*pares de chaves públicas/privadas*](../secgloss/p-gly.md). Um par de chaves é usado para criptografar chaves de sessão e o outro para criar [*assinaturas digitais*](../secgloss/d-gly.md). Eles são conhecidos como o [*par*](../secgloss/k-gly.md) de chaves de troca de chaves e o [*par de chaves de assinatura*](../secgloss/s-gly.md), respectivamente.

Observe que, embora os contêineres de chave criados pela maioria dos CSPs ( [*provedores de serviços de criptografia*](../secgloss/c-gly.md) ) contenham dois pares de chaves, isso não é necessário. Alguns CSPs não armazenam nenhum [*par de chaves*](../secgloss/k-gly.md) enquanto outros CSPs armazenam mais de dois pares.

Todas as chaves em CryptoAPI são armazenadas em CSPs. Os CSPs também são responsáveis por criar as chaves, destrui-las e usá-las para executar uma variedade de operações criptográficas. a exportação de chaves para fora do CSP para que elas possam ser enviadas a outros usuários é discutida na [chave de criptografia Armazenamento e Exchange](cryptographic-key-storage-and-exchange.md).

 

 
