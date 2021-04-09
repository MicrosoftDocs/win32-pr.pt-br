---
description: As assinaturas digitais podem ser usadas para distribuir uma mensagem em formato de texto sem formatação quando os destinatários devem identificar e verificar o remetente da mensagem.
ms.assetid: 10c33787-72d3-4e5d-b4dd-633b3fd29903
title: Assinaturas digitais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 299d84d1a1c71b6b6d709dbe67b4fa2c81f4b54e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090191"
---
# <a name="digital-signatures"></a>Assinaturas digitais

As [*assinaturas digitais*](../secgloss/d-gly.md) podem ser usadas para distribuir uma mensagem em formato de [*texto sem formatação*](../secgloss/p-gly.md) quando os destinatários devem identificar e verificar o remetente da mensagem. Assinar uma mensagem não altera a mensagem; Ele simplesmente gera uma cadeia de caracteres de assinatura digital que pode ser agrupada com a mensagem ou transmitida separadamente. Uma assinatura digital é uma pequena parte dos dados criptografados com a [*chave privada*](../secgloss/p-gly.md)do remetente. A descriptografia dos dados de assinatura usando a [*chave pública*](../secgloss/p-gly.md) do remetente comprova que os dados foram criptografados pelo remetente ou por alguém que tinha acesso à chave privada do remetente.

As assinaturas digitais são geradas usando algoritmos de assinatura de [*chave pública*](../secgloss/p-gly.md) . Uma [*chave privada*](../secgloss/p-gly.md) gera a assinatura e a chave pública correspondente deve ser usada para validar a assinatura. Esse processo é mostrado na ilustração a seguir.

![gerando uma assinatura digital](images/capi02.png)

Há duas etapas envolvidas na criação de uma assinatura digital a partir de uma mensagem. A primeira etapa envolve a criação de um valor de [*hash*](../secgloss/h-gly.md) (também conhecido como [*síntese de mensagem*](../secgloss/m-gly.md)) a partir da mensagem. Esse valor de hash é assinado, usando a chave privada do signatário. Veja a seguir uma ilustração das etapas envolvidas na criação de uma assinatura digital.

![Criando uma assinatura digital de uma mensagem](images/capi06.png)

Para verificar uma assinatura, a mensagem e a assinatura são necessárias. Primeiro, um valor de hash deve ser criado a partir da mensagem da mesma maneira que a assinatura foi criada. Esse valor de hash é então verificado em relação à assinatura usando a chave pública do Assinante. Se o valor de hash e a assinatura corresponderem, você poderá ter certeza de que a mensagem é, na verdade, o assinante assinado originalmente e que ele não foi adulterado. O diagrama a seguir ilustra o processo envolvido na verificação de uma assinatura digital.

![Verificando uma assinatura digital](images/capi07.png)

Um valor de hash consiste em uma pequena quantidade de dados binários, geralmente em cerca de 160 bits. Isso é produzido usando um [*algoritmo de hash*](../secgloss/h-gly.md). Vários desses algoritmos são listados posteriormente nesta seção.

Todos os valores de hash compartilham as seguintes propriedades, independentemente do algoritmo usado:

-   O comprimento do valor de hash é determinado pelo tipo de algoritmo usado e seu comprimento não varia com o tamanho da mensagem. Os comprimentos de valor de hash mais comuns são 128 ou 160 bits.
-   Cada par de mensagens não idênticas se traduz em um valor de hash completamente diferente, mesmo que as duas mensagens sejam diferentes apenas por um único bit. Usando a tecnologia de hoje, não é viável descobrir um par de mensagens que se traduz para o mesmo valor de hash sem interromper o algoritmo de hash.
-   Cada vez que uma mensagem específica é transformada em hash usando o mesmo algoritmo, o mesmo valor de hash é produzido.
-   Todos os algoritmos de hash são unidirecionais. Dado um valor de hash, não é possível recuperar a mensagem original. Na verdade, nenhuma das propriedades da mensagem original pode ser determinada dado apenas ao valor de hash.

 

 
