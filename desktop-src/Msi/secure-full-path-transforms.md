---
description: As transformações de caminho completo seguro devem ter uma origem localizada no caminho completo especificado na propriedade TRANSFORMS.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Transformações de caminho completo seguro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f55e16f40d99deceb8b625297cf447ebf5ec7dfb14a25518554804cf35b572e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040896"
---
# <a name="secure-full-path-transforms"></a>Transformações de caminho completo seguro

As transformações de caminho completo seguro devem ter uma origem localizada no caminho completo especificado na [**propriedade TRANSFORMS.**](transforms.md) Quando o pacote é instalado ou anunciado, o instalador salva as transformaçãos em um cache em que, em um sistema de arquivos seguro, o usuário não tem acesso de gravação. Se a cópia local da transformação ficar indisponível, ela só poderá restaurar o cache usando o caminho especificado. A remoção de um produto por qualquer usuário remove todas as transformação seguras desse produto do computador do usuário.

Para aplicar as transformação de caminhos completos seguros na instalação de um pacote, de definir a política [TransformsSecure](transformssecure-policy.md) ou a propriedade [**TRANSFORMSSECURE**](transformssecure.md) ou fazer com que o primeiro caractere seja passado na lista \| de transformação. Os caminhos completos para a origem de cada transformação devem ser passados na cadeia de caracteres de transformaçãos. Se algum caminho relativo estiver na lista, a instalação falhará. A origem da transformação não precisa estar localizada com a origem do pacote.

 

 



