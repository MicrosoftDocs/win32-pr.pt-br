---
title: CPROPS. CPP
description: No exemplo de componente do provedor, um exemplo de uma implementação de cache de propriedade pode ser encontrado em cProps. cpp. Os métodos com suporte são listados na tabela a seguir.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b9f4fddfea6900fd8d7a06bee9979744eefd30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822226"
---
# <a name="cpropscpp"></a>CPROPS. CPP

No exemplo de componente do provedor, um exemplo de uma implementação de cache de propriedade pode ser encontrado em cProps. cpp. Os métodos com suporte são listados na tabela a seguir.



| Método                                           | Descrição                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **CPropertyCache:: AddProperty**                  | Estenda o cache de propriedades adicionando um novo.                                                                      |
| **CPropertyCache:: updateproperty**               | Pesquise a propriedade, libere seu conteúdo e use novos valores, em vez disso; em seguida, marque o cache alterado para essa propriedade. |
| **CPropertyCache:: findproperty**                 | Pesquisar esta propriedade por nome; Salve seu índice.                                                                      |
| **CPropertyCache:: GetProperty**                  | Localize a propriedade no cache, se disponível, caso contrário, chame **GetInfo**. Defina o índice e a cópia nos novos valores.  |
| **CPropertyCache::p utproperty**                  | Localize a propriedade. Libere o que estava lá e coloque novos valores.                                                       |
| **CPropertyCache::CPropertyCache**               | Construtor padrão.                                                                                               |
| **CPropertyCache:: ~ CPropertyCache**              | Destruidor padrão.                                                                                                |
| **CPropertyCache::createpropertycache**          | Crie o cache.                                                                                                   |
| **CPropertyCache::unboundgetproperty**           | Localize a propriedade no cache e defina-a com esses valores.                                                          |
| **CPropertyCache::SampleDSMarshallProperties**   | Empacotar valores e dados de propriedade.                                                                                   |
| **CPropertyCache:: marshallproperty**             | Marshale de uma propriedade.                                                                                                 |
| **CPropertyCache::SampleDSUnMarshallProperties** | Desempacotar dados de propriedade e valores.                                                                                 |
| **CPropertyCache:: unmarshalproperty**           | Desempacotar uma propriedade.                                                                                               |



 

 

 




