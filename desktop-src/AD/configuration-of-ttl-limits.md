---
title: Configuração de limites de TTL
description: Um cliente pode solicitar um valor de TTL para uma entrada que varia entre 1 e 31557600 (ou seja, de 1 segundo a 1 ano).
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Configuração do AD de limites de TTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2786258d060ef4261dcd9fbfad359c71f2dbaeb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881599"
---
# <a name="configuration-of-ttl-limits"></a>Configuração de limites de TTL

Um cliente pode solicitar um valor de TTL para uma entrada que varia entre 1 e 31557600 (ou seja, de 1 segundo a 1 ano). Esse intervalo de valores de atributo será imposto pelos valores de atributo **rangeLower** e **rangeUpper** na definição **attributeSchema** para o **atributo entryTTL.** De acordo com o RFC 2589, os servidores de diretório não são necessários para aceitar esse valor e podem retornar um valor TTL diferente para o cliente. Os clientes devem ser capazes de usar esse valor determinado pelo servidor como seu CRP (período de atualização do cliente), que regerá a frequência com que o cliente precisará executar a operação de atualização na entrada dinâmica.

Active Directory Domain Services fornecer aos administradores a capacidade de configurar os valores de TTL padrão e mínimo para uma floresta. O valor de TTL padrão é o que será atribuído a uma entrada dinâmica recém-criada se uma TTL não for especificada explicitamente. O TTL mínimo substituirá qualquer valor TTL especificado pelo cliente que seja menor que o mínimo configurado. Nenhum valor máximo configurável de TTL precisa ser fornecido porque um máximo será imposto pelo valor do atributo **rangeUpper** no **objeto attributeSchema.** Permitir que os administradores configurem esses valores permitirá definir valores de TTL que imporão um tráfego de baixa atualização ou, em outro extremo, fornecerão um diretório altamente atualizado.

Os valores padrão para os dois parâmetros TTL configuráveis serão os seguinte:

-   Valor TTL padrão = 86400 segundos (1 dia)
-   Valor mínimo de TTL = 900 segundos (15 minutos)

Os parâmetros TTL configuráveis serão armazenados como entradas AVA (declaração de valor de atributo) do formato " value-name value " no atributo &lt; &gt; = &lt; &gt; **ms-DS-Other-Configurações** do objeto NTDS-Service dado pelo seguinte DN na partição De configuração:


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



A sintaxe ava exata, para os dois parâmetros TTL configuráveis, é a seguinte em que NNNN é expressa em segundos:


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



Esses valores podem ser definidos por um administrador por meio do utilitário de linha de comando ntdsutil.

 

 




