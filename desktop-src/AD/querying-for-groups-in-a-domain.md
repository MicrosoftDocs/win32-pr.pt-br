---
title: Consultando grupos em um domínio
description: Os grupos podem ser colocados em qualquer contêiner ou unidade organizacional em um domínio, bem como a raiz do domínio.
ms.assetid: 338a93dd-445d-4f74-a6d6-e5c8ba2e765e
ms.tgt_platform: multiple
keywords:
- Consultando grupos em um AD de domínio
- Grupos de anúncios, consultando grupos em um domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6079050519fca00a8e689d8af5c3fae9ce6baec2c02406ae56bccc3616a50bef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184910"
---
# <a name="querying-for-groups-in-a-domain"></a>Consultando grupos em um domínio

Os grupos podem ser colocados em qualquer contêiner ou unidade organizacional em um domínio, bem como a raiz do domínio. Os grupos não podem estar sempre em um contêiner. Portanto, é necessário pesquisar todo o domínio para localizar todos os grupos no domínio.

Para pesquisar todos os grupos em um domínio, defina o ponto de início da pesquisa para a raiz do domínio, defina o escopo da pesquisa como subárvore e pesquise todos os objetos que tenham um valor de [**objectClass**](/windows/desktop/ADSchema/a-objectclass) de "grupo".

Se os grupos que contêm valores de [**\_ enumeração de \_ tipo \_ de grupo ADS**](/windows/win32/api/iads/ne-iads-ads_group_type_enum) específicos tiverem sido encontrados, o operador de **regra de \_ correspondência LDAP \_ \_ \_ e** a regra de correspondência poderão ser usados para pesquisar grupos que tenham bits específicos definidos no atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) . Para obter mais informações sobre como usar regras de correspondência, consulte [sintaxe do filtro de pesquisa](/windows/desktop/ADSI/search-filter-syntax).

Para obter mais informações e um exemplo de código que mostra como procurar grupos em um domínio, consulte [exemplo de código para pesquisar grupos em um domínio](example-code-for-performing-a-query-in-a-domain.md).

 

 