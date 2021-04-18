---
description: Há situações em que as chaves devem ser exportadas do ambiente seguro do CSP (provedor de serviços de criptografia) para o espaço de dados de um aplicativo. As chaves que foram exportadas são armazenadas em estruturas de BLOB de chaves criptografadas.
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: Armazenamento de chaves de criptografia e Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771813"
---
# <a name="cryptographic-key-storage-and-exchange"></a>Armazenamento de chaves de criptografia e Exchange

Há situações em que as chaves devem ser exportadas do ambiente seguro do CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) para o espaço de dados de um aplicativo. As chaves que foram exportadas são armazenadas em estruturas de [*blob de chaves*](../secgloss/k-gly.md) criptografadas.

Há duas situações específicas em que é necessário exportar chaves:

-   Para salvar uma [*chave de sessão*](../secgloss/s-gly.md) para uso posterior por um aplicativo, se, por exemplo, um aplicativo tiver apenas criptografado um arquivo de banco de dados para ser descriptografado posteriormente. O aplicativo é responsável por armazenar a chave de criptografia. Isso é necessário porque os CSPs não preservam [*as chaves simétricas*](../secgloss/s-gly.md) da sessão para a sessão.
-   Para enviar uma chave para outra pessoa. Isso seria mais fácil se os respectivos CSPs pudessem se comunicar diretamente, mas não conseguirem. Como os CSPs não podem se comunicar, a chave deve ser exportada de um CSP, transmitida para o aplicativo de destino e, em seguida, importada para o CSP de destino. Esse processo pode se tornar mais complicado se o caminho de comunicação não for confiável.

Em ambos os casos, um aplicativo deve armazenar uma chave de sessão fora do CSP por um período de tempo. Para obter mais informações, consulte [procedimento para armazenar uma chave de sessão](procedure-for-storing-a-session-key.md).

 

 
