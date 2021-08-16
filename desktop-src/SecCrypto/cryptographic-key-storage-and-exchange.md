---
description: Há situações em que as chaves devem ser exportadas do ambiente seguro do CSP (provedor de serviços de criptografia) para o espaço de dados de um aplicativo. As chaves exportadas são armazenadas em estruturas blob de chaves criptografadas.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Chave criptográfica Armazenamento e Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3028efb449b59deb24a7097369d8894d0876907f3555c836e95e14d8c4bf5cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768753"
---
# <a name="cryptographic-key-storage-and-exchange"></a>Chave criptográfica Armazenamento e Exchange

Há situações em que as chaves devem ser exportadas do ambiente seguro do CSP [*(provedor*](../secgloss/c-gly.md) de serviços de criptografia) para o espaço de dados de um aplicativo. As chaves exportadas são armazenadas em estruturas [*blob de chaves criptografadas.*](../secgloss/k-gly.md)

Há duas situações específicas em que é necessário exportar chaves:

-   Para salvar uma [*chave*](../secgloss/s-gly.md) de sessão para uso posterior por um aplicativo, se, por exemplo, um aplicativo acabou de criptografar um arquivo de banco de dados para ser descriptografado posteriormente. O aplicativo é responsável por armazenar a chave de criptografia. Isso é necessário porque os CSPs não preservam [*chaves simétricas*](../secgloss/s-gly.md) da sessão para a sessão.
-   Para enviar uma chave para outra pessoa. Isso seria mais fácil se os respectivos CSPs pudessem se comunicar diretamente, mas não podem. Como os CSPs não podem se comunicar, a chave deve ser exportada de um CSP, transmitida para o aplicativo de destino e importada para o CSP de destino. Esse processo poderá se tornar mais complicado se o caminho de comunicação não for confiável.

Em ambos os casos, um aplicativo deve armazenar uma chave de sessão fora do CSP por um período de tempo. Para obter mais informações, [consulte Procedimento para armazenar uma chave de sessão](procedure-for-storing-a-session-key.md).

 

 
