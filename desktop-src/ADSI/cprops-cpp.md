---
title: CPROPS. Cpp
description: No componente do provedor de exemplo, um exemplo de uma implementação de cache de propriedade pode ser encontrado em cprops.cpp. Os métodos com suporte são listados na tabela a seguir.
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
# <a name="cpropscpp"></a>CPROPS. Cpp

No componente do provedor de exemplo, um exemplo de uma implementação de cache de propriedade pode ser encontrado em cprops.cpp. Os métodos com suporte são listados na tabela a seguir.



| Método                                           | Descrição                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| **CPropertyCache::addproperty**                  | Estenda o cache de propriedade adicionando um novo.                                                                      |
| **CPropertyCache::updateproperty**               | Procure a propriedade, livre seu conteúdo e use novos valores; em seguida, marque o cache alterado para essa propriedade. |
| **CPropertyCache::findproperty**                 | Procure essa propriedade por nome; salve seu índice.                                                                      |
| **CPropertyCache::getproperty**                  | Encontre a propriedade no cache, se disponível; caso contrário, chame **GetInfo**. De definir o índice e copiar os novos valores.  |
| **CPropertyCache::p utproperty**                  | Encontre a propriedade . Liberar o que estava lá e colocar em novos valores.                                                       |
| **CPropertyCache::CPropertyCache**               | Construtor padrão.                                                                                               |
| **CPropertyCache::~CPropertyCache**              | Destruidor padrão.                                                                                                |
| **CPropertyCache::createpropertycache**          | Crie o cache.                                                                                                   |
| **CPropertyCache::unboundgetproperty**           | Localisque a propriedade no cache e de defini-la com esses valores.                                                          |
| **CPropertyCache::SampleDSMarshallProperties**   | Marshal de valores e dados de propriedade.                                                                                   |
| **CPropertyCache::marshallproperty**             | Marshal de uma propriedade.                                                                                                 |
| **CPropertyCache::SampleDSUnMarshallProperties** | Valores e dados de propriedade unmarshal.                                                                                 |
| **CPropertyCache::unmarshallproperty**           | Unmarshal uma propriedade.                                                                                               |



 

 

 




