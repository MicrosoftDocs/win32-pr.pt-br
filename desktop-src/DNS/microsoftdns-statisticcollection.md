---
title: MicrosoftDNS_StatisticCollection
description: A classe \_ StatisticCollection do MicrosoftDNS representa uma coleção de estatísticas relacionadas do servidor DNS.
ms.assetid: 74e080e9-a676-4a82-ae8b-ee904622eb9a
keywords:
- MicrosoftDNS_StatisticCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fda276433290ab2b151b4b6a34abae7a0113ee3db75054f6c66c0536009dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109086"
---
# <a name="microsoftdns_statisticcollection"></a>MicrosoftDNS \_ StatisticCollection

A classe \_ StatisticCollection do MicrosoftDNS representa uma coleção de estatísticas relacionadas do servidor DNS.

A sintaxe a seguir é simplificada do código MOF.

``` syntax
class MicrosoftDNS_StatisticCollection : CIM_LogicalElement
{
  string Name;
  uint32 StatId;
  MicrosoftDNS_Statistic Statistics[];
};
```

## <a name="properties"></a>Propriedades

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nome**
</dt> <dd>

Nome da coleção de estatísticas.

</dd> <dt>

<span id="StatId"></span><span id="statid"></span><span id="STATID"></span>**StatId**
</dt> <dd>

Representação numérica da coleção de estatísticas.

</dd> <dt>

<span id="MicrosoftDNS_Statistic_Statistics__"></span><span id="microsoftdns_statistic_statistics__"></span><span id="MICROSOFTDNS_STATISTIC_STATISTICS__"></span>**Estatísticas de estatísticas do MicrosoftDNS \_\[\]**
</dt> <dd>

Matriz de valores associados à estatística.

</dd> </dl>

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="This_class_has_no_methods."></span><span id="this_class_has_no_methods."></span><span id="THIS_CLASS_HAS_NO_METHODS."></span>Essa classe não tem métodos.
</dt> <dd></dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Estatística do \_ MicrosoftDNS**](microsoftdns-statistic.md)
</dt> </dl>

 

 




