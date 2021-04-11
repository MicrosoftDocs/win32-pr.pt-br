---
title: Atribuição de peso de filtro
description: Cada filtro na WFP (Windows Filtering Platform) tem um peso associado, que é usado durante a arbitragem de filtro.
ms.assetid: c78854c2-9aa1-408f-82d6-4b9e52f38e84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c77982258bb9c8ef14e22b20e28b6a3039456ae
ms.sourcegitcommit: 013de6f5280f28a9b04c3cce9387e629b07d70fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/26/2020
ms.locfileid: "104365763"
---
# <a name="filter-weight-assignment"></a>Atribuição de peso de filtro

Cada filtro na WFP (Windows Filtering Platform) tem um peso associado, que é usado durante a [arbitragem de filtro](filter-arbitration.md).

O peso do filtro usado pelo mecanismo de filtragem base (BFE) é do tipo [**fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). Os chamadores têm três opções ao adicionar filtros.

-   Defina o peso para um [**fwp \_ UINT64**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). O BFE usa o peso fornecido como está.
-   Defina o peso como [**fwp \_ vazio**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). O BFE gera automaticamente um peso no intervalo de \[ 0, 2 ⁶ ⁰).
-   Defina o peso para um [**fwp \_ UINT8**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type) no intervalo de \[ 0, 15 \] . O BFE usa o peso fornecido como um identificador de intervalo de peso.

    O BFE gera automaticamente os bits 60 de ordem inferior (exatamente como se o peso tivesse sido definido como [**fwp \_ vazio**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type)) e, em seguida, usa o valor fornecido para definir os 4 bits de ordem superior. Isso permite que os chamadores dividam manualmente o espaço de peso em 16 intervalos, enquanto ainda usam o peso automático em um intervalo.

> [!Note]  
> Quando dois ou mais textos explicativos são registrados na mesma subcamada, podem ocorrer problemas quando o mesmo peso é atribuído aos filtros. Esse problema pode ser evitado fazendo com que os textos explicativos criem sua própria subcamada usando [**FwpmSubLayerAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsublayeradd0).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Identificadores de peso de filtro**](filter-weight-identifiers.md)
</dt> </dl>

 

 




