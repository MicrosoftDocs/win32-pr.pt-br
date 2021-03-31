---
title: Procurando grupos por escopo ou tipo em um domínio
description: Em domínios do Windows 2000, há uma classe única chamada grupo para todos os escopos de grupo (domínio local, global, universal) e tipos (segurança, distribuição).
ms.assetid: e32629d9-aa62-4953-aa49-43af726b7deb
ms.tgt_platform: multiple
keywords:
- Procurando grupos por escopo ou tipo em um AD de domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9aae5e2c7be7b9cba590f9bc80f0517bca918
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640381"
---
# <a name="searching-for-groups-by-scope-or-type-in-a-domain"></a>Procurando grupos por escopo ou tipo em um domínio

Em domínios do Windows 2000, há uma classe única chamada [**grupo**](/windows/desktop/ADSchema/c-group) para todos os escopos de grupo (domínio local, global, universal) e tipos (segurança, distribuição). O atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) do objeto Group especifica o tipo e o escopo do grupo.

Para usar tipo ou escopo para pesquisar grupos em domínios do Windows 2000, use um filtro que contenha uma regra de correspondência para o atributo [**GroupType**](/windows/desktop/ADSchema/a-grouptype) . Para obter mais informações sobre regras de correspondência, consulte [sintaxe do filtro de pesquisa](/windows/desktop/ADSI/search-filter-syntax).

Para obter mais informações e um exemplo de código que mostra como procurar grupos em um domínio, consulte [exemplo de código para pesquisar grupos em um domínio](example-code-for-performing-a-query-in-a-domain.md).

## <a name="example-ldap-query-strings"></a>Exemplo de cadeias de consulta LDAP

Os exemplos de cadeia de caracteres de consulta a seguir mostram como construir uma cadeia de caracteres de consulta LDAP usada para pesquisar ou filtrar tipos de grupos específicos.

A cadeia de caracteres de consulta a seguir pesquisará grupos de segurança. Este exemplo usa "-2147483648" como o equivalente Decimal do sinalizador **de \_ segurança de tipo de grupo ADS \_ \_ \_ habilitado** .


```C++
(&(objectCategory=group)(groupType:1.2.840.113556.1.4.803:=-2147483648))
```



A cadeia de caracteres de consulta a seguir pesquisará grupos de distribuição universal; ou seja, os grupos que contêm o sinalizador de **\_ \_ \_ \_ grupo de tipos de grupo ADS** e não contêm o sinalizador de segurança de tipo de **\_ grupo ADS \_ \_ \_ habilitado** . Este exemplo usa "8" como o equivalente Decimal do **tipo de grupo do ADS \_ \_ \_ \_ grupo universal** e "-2147483648" como o equivalente Decimal do sinalizador de **segurança de tipo de \_ grupo ADS \_ \_ \_ habilitado** .


```C++
(&(objectCategory=group)((&(groupType:1.2.840.113556.1.4.803:=8)(!(groupType:1.2.840.113556.1.4.803:=-2147483648)))))
```



 

 