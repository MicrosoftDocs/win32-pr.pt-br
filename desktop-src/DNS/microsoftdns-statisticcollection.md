---
title: MicrosoftDNS_StatisticCollection
description: A \_ classe StatisticCollection MicrosoftDNS representa uma coleção de estatísticas de servidor DNS relacionadas.
ms.assetid: 74e080e9-a676-4a82-ae8b-ee904622eb9a
keywords:
- MicrosoftDNS_StatisticCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c44f9c65714fb3b1db58b5a6439ade5531792501
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005275"
---
# <a name="microsoftdns_statisticcollection"></a>\_Estatísticacollection de MicrosoftDNS

A \_ classe StatisticCollection MicrosoftDNS representa uma coleção de estatísticas de servidor DNS relacionadas.

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

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nomes**
</dt> <dd>

Nome da coleção de estatísticas.

</dd> <dt>

<span id="StatId"></span><span id="statid"></span><span id="STATID"></span>**StatID**
</dt> <dd>

Representação numérica da coleção de estatísticas.

</dd> <dt>

<span id="MicrosoftDNS_Statistic_Statistics__"></span><span id="microsoftdns_statistic_statistics__"></span><span id="MICROSOFTDNS_STATISTIC_STATISTICS__"></span>**Estatísticas de estatística de MicrosoftDNS \_\[\]**
</dt> <dd>

Matriz de valores associados à estatística.

</dd> </dl>

## <a name="methods"></a>Métodos

<dl> <dt>

<span id="This_class_has_no_methods."></span><span id="this_class_has_no_methods."></span><span id="THIS_CLASS_HAS_NO_METHODS."></span>Esta classe não tem métodos.
</dt> <dd></dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Estatística de MicrosoftDNS \_**](microsoftdns-statistic.md)
</dt> </dl>

 

 




