---
title: CPROPS. CPP
description: No exemplo de componente do provedor, um exemplo de uma implementação de cache de propriedade pode ser encontrado em cProps. cpp. Os métodos com suporte são listados na tabela a seguir.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66394b7375779f50a97505128178ec35106187c076ca5d6741375a7f71b8ec46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428995"
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



 

 

 




