---
description: Resolução de nomes independente de protocolo e Windows Sockets (Winsock).
ms.assetid: f55219b9-1518-4b49-a0da-6a3fa025cca3
title: Resolução de nomes de Protocol-Independent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cafed9759a4ca5431dafb230e7f09578ff1c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296344"
---
# <a name="protocol-independent-name-resolution"></a>Resolução de nomes de Protocol-Independent

No desenvolvimento de um aplicativo cliente/servidor independente de protocolo, há dois requisitos básicos que existem em relação à resolução de nomes e ao registro:

-   A capacidade da metade do servidor do aplicativo (serviço) de registrar sua existência dentro (ou se tornar acessível a) um ou mais namespaces.
-   A capacidade do aplicativo cliente de localizar o serviço em um namespace e obter o protocolo de transporte e as informações de endereçamento necessários.

Para aqueles acostumados a desenvolver aplicativos baseados em TCP/IP, isso pode parecer um pouco mais do que pesquisar um endereço de host e, em seguida, usar um número de porta acordado. Outros esquemas de rede, no entanto, permitem o local do serviço, o protocolo usado para o serviço e outros atributos a serem descobertos em tempo de execução. Para acomodar a ampla diversidade de recursos encontrados nos serviços de nome existentes, a interface do Windows Sockets 2 adota o modelo descrito nos tópicos desta seção.

Esta seção descreve os recursos de resolução de nomes independentes de protocolo disponíveis para desenvolvedores de Winsock. A lista a seguir descreve os tópicos nesta seção:

-   [Modelo de resolução de nomes](name-resolution-model-2.md)
-   [Resumo das funções de resolução de nomes](summary-of-name-resolution-functions-2.md)
-   [Estruturas de dados de resolução de nomes](name-resolution-data-structures-2.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registro e resolução de nome](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



