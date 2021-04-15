---
description: Seguras-as transformações de caminho completo devem ter uma origem localizada no caminho completo especificado na propriedade transformações.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Alta segurança – transformações de caminho completo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8a60cf30beffe3831ed6489ea3827124ae319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506277"
---
# <a name="secure-full-path-transforms"></a>Alta segurança – transformações de caminho completo

Seguras-as transformações de caminho completo devem ter uma origem localizada no caminho completo especificado na propriedade [**TRANSformações**](transforms.md) . Quando o pacote é instalado ou anunciado, o instalador salva as transformações em um cache em que, em um sistema de arquivos seguro, o usuário não tem acesso de gravação. Se a cópia local da transformação ficar indisponível, ela só poderá restaurar o cache usando o caminho especificado. A remoção de um produto por qualquer usuário remove todas as transformações seguras desse produto do computador do usuário.

Para aplicar transformações de caminhos completos seguros na instalação de um pacote, defina a [política TransformsSecure](transformssecure-policy.md) ou a propriedade [**TransformsSecure**](transformssecure.md) ou faça com que \| o primeiro caractere seja passado na lista de transformação. Os caminhos completos para a origem de cada transformação devem ser passados na cadeia de caracteres de transformações. Se algum caminho relativo estiver na lista, a instalação falhará. A origem da transformação não precisa estar localizada com a origem do pacote.

 

 



