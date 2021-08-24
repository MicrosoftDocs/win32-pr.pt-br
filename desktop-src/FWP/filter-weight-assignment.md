---
title: Atribuição de peso de filtro
description: Cada filtro na plataforma Windows filtragem (WFP) tem um peso associado, que é usado durante a mediação do filtro.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9042b15da0df5f81c71a32deb923369a54243854e86aeaed1ba30c7fc8484193
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119746866"
---
# <a name="filter-weight-assignment"></a>Atribuição de peso de filtro

Cada filtro na plataforma Windows filtragem (WFP) tem um peso associado, que é usado durante a [mediação do filtro.](filter-arbitration.md)

O peso do filtro usado pelo BFE (Mecanismo de Filtragem Base) é do tipo [**FWP \_ UINT64.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) Os chamadores têm três opções ao adicionar filtros.

-   De definir o peso como [**um \_ UINT64 FWP.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) O BFE usa o peso fornecido como está.
-   De definir o peso como [**FWP \_ EMPTY.**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) O BFE gera automaticamente um peso no intervalo \[ 0, 2).
-   De definir o peso como [**um \_ UINT8 FWP**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) no intervalo \[ 0, 15 \] . O BFE usa o peso fornecido como um identificador de intervalo de peso.

    O BFE gera automaticamente os 60 bits de ordem baixa (exatamente como se o peso tivesse sido definido como [**FWP \_ EMPTY)**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)e, em seguida, usa o valor fornecido para definir os 4 bits de ordem alta. Isso permite que os chamadores dividam manualmente o espaço de peso em 16 intervalos, enquanto ainda usam a ponderação automática dentro de um intervalo.

> [!Note]  
> Quando dois ou mais callouts são registrados na mesma subcamada, podem ocorrer problemas quando o mesmo peso é atribuído aos filtros. Esse problema pode ser evitado fazendo com que os callouts criem sua própria subcamada usando [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Filtrar identificadores de peso**](filter-weight-identifiers.md)
</dt> </dl>

 

 




