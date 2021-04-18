---
description: Para recuperar os elementos de um caminho, chame a função PdhParseCounterPath. A função analisa os elementos de um caminho de contador e os retorna em uma estrutura de elementos de caminho do contador de PDH \_ \_ \_ .
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Obtendo elementos do caminho do contador a partir de um caminho do contador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b8579033ddf7a97aec36b88bd067f9a240506d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778702"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>Obtendo elementos do caminho do contador a partir de um caminho do contador

Para recuperar os elementos de um caminho, chame a função [**PdhParseCounterPath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) . A função analisa os elementos de um caminho de contador e os retorna em uma estrutura de [**elementos de caminho do contador de PDH \_ \_ \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) .

Se você tiver um nome de instância complexo (um que contenha uma instância pai e um índice de instância), você poderá chamar a função [**PdhParseInstanceName**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) para extrair o nome da instância, o índice da instância e o nome do pai.

 

 



