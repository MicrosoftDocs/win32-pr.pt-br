---
description: Um filtro de captura é um elemento de um aplicativo NPP que instrui o driver Monitor de Rede (Nmnt.sys) quais quadros de dados de rede reter e quais quadros ignorar.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Sobre filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d0d1eee25915c30b8ddffc475545cbd7f7d04d0fdcecf4119480b737980cd9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911356"
---
# <a name="about-capture-filters"></a>Sobre filtros de captura

Um filtro de captura é um elemento de um aplicativo NPP que instrui o driver Monitor de Rede (Nmnt.sys) quais quadros de dados de rede reter e quais quadros ignorar. A vantagem de definir um filtro de captura é maior eficiência. Você não precisa examinar quadros capturados; o Monitor de Rede driver os examina. Essa abordagem elimina a cópia de quadro, o que fornece uma vantagem de uso de memória.

## <a name="capture-filter-structure"></a>Estrutura de filtro de captura

Os filtros de captura consistem em três elementos:

-   Configurações de Etype/SAP
-   Endereço
-   Corresponder ao padrão

Juntos, esses elementos avaliam logicamente quais quadros incluir ou excluir durante a operação de um aplicativo NPP. O filtro de captura fornece combinações complexas e exclusões de elementos de quadro para o aplicativo NPP.

Monitor de Rede implementa o filtro de captura por meio de uma estrutura de dados, [**CAPTUREFILTER,**](the-capturefilter-structure.md)passado para o NPP e passado para o driver Monitor de Rede quando a captura é iniciada.

Para obter mais informações sobre operações NPP e funcionalidade de BLOB, consulte [Provedores](network-packet-providers.md) de pacotes de rede [e Monitor de Rede BLOBS](network-monitor-blobs.md).

 

 



