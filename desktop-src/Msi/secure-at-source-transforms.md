---
description: As transformações de origem segura devem ter uma origem localizada na raiz da origem do pacote.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Transformações de origem segura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f591e6f30c11ec9fa7edf2f943ef1f660a0a3b12ff87c3c1de0984328652565b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040996"
---
# <a name="secure-at-source-transforms"></a>Transformações de origem segura

As transformações de origem segura devem ter uma origem localizada na raiz da origem do pacote. Quando o pacote é instalado ou anunciado, o instalador salva as transformações em um cache em que, em um sistema de arquivos seguro, o usuário não tem acesso de gravação. Se a cópia local da transformação ficar indisponível, o instalador procurará uma origem para restaurar o cache. O método é o mesmo que pesquisar a lista de origem de um arquivo de .msi. Para obter mais informações, consulte [resiliência de origem](source-resiliency.md). A remoção de um produto por qualquer usuário remove todas as transformações seguras desse produto do computador do usuário.

Para aplicar transformações de origem segura na instalação de um pacote, defina a [política TransformsSecure](transformssecure-policy.md) ou a propriedade [**TransformsSecure**](transformssecure.md) ou torne @ o primeiro caractere passado na lista de transformação. Cada transformação deve ser indicada por um nome de arquivo e deve estar localizada na raiz da origem do pacote. Se qualquer uma das transformações não estiver localizada na raiz da origem do pacote, a instalação falhará. Para obter mais informações, consulte [aplicando transformações](applying-transforms.md).

 

 



