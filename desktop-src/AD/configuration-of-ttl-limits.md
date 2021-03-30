---
title: Configuração dos limites de TTL
description: Um cliente pode solicitar um valor TTL para uma entrada que varia entre 1 e 31557600 (ou seja, de 1 segundo a 1 ano).
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Configuração de limites de TTL do AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cb3617bd59667f0284c4e383da54752adfbe25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634800"
---
# <a name="configuration-of-ttl-limits"></a>Configuração dos limites de TTL

Um cliente pode solicitar um valor TTL para uma entrada que varia entre 1 e 31557600 (ou seja, de 1 segundo a 1 ano). Esse intervalo de valores de atributo será imposto pelos valores de atributo **RangeLower** e **rangeUpper** na definição **attributeSchema** para o atributo **entryTTL** . De acordo com a RFC 2589, os servidores de diretório não precisam aceitar esse valor e podem retornar um valor de TTL diferente para o cliente. Os clientes devem ser capazes de usar esse valor determinado pelo servidor como seu período de atualização do cliente (CRP), que controlará com que frequência o cliente precisará executar a operação de atualização na entrada dinâmica.

Active Directory Domain Services fornecer aos administradores a capacidade de configurar os valores de TTL mínimos e padrão para uma floresta. O valor de TTL padrão é o que será atribuído a uma entrada dinâmica recém-criada se uma TTL não for especificada explicitamente. O TTL mínimo substituirá qualquer valor de TTL especificado pelo cliente que seja menor do que o mínimo configurado. Nenhum valor de TTL máximo configurável precisa ser fornecido porque um máximo será imposto pelo valor do atributo **rangeUpper** no objeto **attributeSchema** . Permitir que os administradores configurem esses valores permitirá que eles definam valores TTL que impedirão um tráfego de atualização baixa ou, no outro extremo, fornecem um diretório altamente atualizado.

Os valores padrão para os dois parâmetros de TTL configuráveis serão os seguintes:

-   Valor TTL padrão = 86400 segundos (1 dia)
-   Valor TTL mínimo = 900 segundos (15 minutos)

Os parâmetros de TTL configuráveis serão armazenados como entradas de AVA (declaração de valor de atributo) no formato "<valor-nome>=<value>"no atributo **MS-DS-Other-Settings** do objeto NTDS-Service fornecido pelo seguinte DN na partição de configuração:


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



A sintaxe AVA exata, para os dois parâmetros TTL configuráveis, é a seguinte, em que NNNN é expresso em segundos:


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



Esses valores podem ser definidos por um administrador por meio do utilitário de linha de comando Ntdsutil.

 

 




