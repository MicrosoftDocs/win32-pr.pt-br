---
description: resolução de nomes e modelo de registro para o SPI do Windows sockets (Winsock).
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: Modelo de resolução de nomes para o SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f012a5c14a6dae9045b303ecb7c4e39f1d93d264285138d98c0e93274ef921
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132109"
---
# <a name="name-resolution-model-for-the-spi"></a>Modelo de resolução de nomes para o SPI

No desenvolvimento de um aplicativo cliente/servidor independente de protocolo, há dois requisitos básicos que existem em relação à resolução de nomes e ao registro:

-   A capacidade da metade de servidor do aplicativo (daqui em diante chamada de serviço) para registrar sua existência dentro (ou se tornar acessível a) um ou mais namespaces.
-   A capacidade do aplicativo cliente de localizar o serviço em um namespace e obter o protocolo de transporte e as informações de endereçamento necessários.

Para aqueles acostumados a desenvolver aplicativos baseados em TCP/IP, isso pode envolver pouco mais do que pesquisar um endereço de host e, em seguida, usar um número de porta acordado. Outros esquemas de rede, no entanto, permitem o local do serviço, o protocolo usado para o serviço e outros atributos a serem descobertos em tempo de execução. para acomodar o intervalo de recursos encontrados nos serviços de nome existentes, a interface Windows sockets 2 adota o modelo descrito abaixo.

Um *namespace* refere-se a algum recurso para associar (como um mínimo) o protocolo e os atributos de endereçamento de um serviço de rede com um ou mais nomes amigáveis. Muitos namespaces estão atualmente em uso amplo, incluindo o DNS (sistema de nomes de domínio) da Internet, Serviços de diretório do NetWare (NDS), X. 500, etc. Esses namespaces variam muito em como são organizados e implementados. algumas de suas propriedades são particularmente importantes para entender a partir da perspectiva da resolução de nomes de soquetes de Windows.

 

 



