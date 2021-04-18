---
description: Um filtro de captura é um elemento de um aplicativo NPP que instrui o driver de Monitor de Rede (Nmnt.sys) quais quadros de dados de rede serão retidos e quais quadros serão ignorados.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Sobre filtros de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766852"
---
# <a name="about-capture-filters"></a>Sobre filtros de captura

Um filtro de captura é um elemento de um aplicativo NPP que instrui o driver de Monitor de Rede (Nmnt.sys) quais quadros de dados de rede serão retidos e quais quadros serão ignorados. A vantagem de definir um filtro de captura é maior eficiência. Você não precisa examinar os quadros capturados; o driver de Monitor de Rede os examina. Essa abordagem elimina a cópia de quadros, que fornece uma vantagem de uso de memória.

## <a name="capture-filter-structure"></a>Capturar estrutura do filtro

Os filtros de captura consistem em três elementos:

-   Configurações de ETYPE/SAP
-   Endereço
-   Correspondência de padrões

Juntos, esses elementos avaliam logicamente quais quadros incluir ou excluir, durante a operação de um aplicativo NPP. O filtro de captura fornece correspondências complexas e exclusões de elementos de quadro para o aplicativo NPP.

Monitor de Rede implementa o filtro de captura por meio de uma estrutura de dados, [**CAPTUREFILTER**](the-capturefilter-structure.md), passado para o NPP e, em seguida, passado para o driver de monitor de rede quando a captura é iniciada.

Para obter mais informações sobre operações NPP e funcionalidade de BLOB, consulte [provedores de pacotes de rede](network-packet-providers.md) e [blobs de monitor de rede](network-monitor-blobs.md).

 

 



