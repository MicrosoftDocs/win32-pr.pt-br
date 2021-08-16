---
title: Catálogo Global
description: Um Domínio executado por Active Directory Domain Services pode consistir em muitas partições ou contextos de nomen por nome.
ms.assetid: eac02c1f-0c37-4eee-822d-07913ea8775a
ms.tgt_platform: multiple
keywords:
- catálogo global do Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e81abf04ab3e4d95819f91b5db8753a265e49ca79b2f405a32665dc46a8f2db5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189102"
---
# <a name="global-catalog"></a>Catálogo Global

Um Domínio executado por Active Directory Domain Services pode consistir em muitas partições ou contextos de nomen por nome. O DN (nome diferenciado) de um objeto inclui informações suficientes para localizar uma réplica da partição que contém o objeto. Muitas vezes, no entanto, o usuário ou aplicativo não sabe o DN do objeto de destino ou qual partição pode conter o objeto . O [*GC (catálogo global)*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85)) permite que usuários e aplicativos encontrem objetos em uma árvore de domínio do Active Directory, considerando um ou mais atributos do objeto de destino.

O catálogo global contém uma réplica parcial de cada contexto de nomeação no diretório. Ele também contém os contextos de nomentura de esquema e configuração. Isso significa que o GC contém uma réplica de cada objeto no diretório, mas com apenas um pequeno número de seus atributos. Os atributos no GC são aqueles usados com mais frequência em operações de pesquisa (como nome e sobrenome de um usuário ou nomes de logon) e aqueles necessários para localizar uma réplica completa do objeto. O GC permite que os usuários encontrem rapidamente objetos de interesse sem saber qual domínio os contém e sem exigir um namespace estendido contíguo na empresa.

O catálogo global é criado automaticamente pelo Active Directory Domain Services de replicação. A topologia de replicação para o catálogo global é gerada automaticamente. As propriedades replicadas no catálogo global incluem um conjunto base definido pela Microsoft. Os administradores podem especificar propriedades adicionais para atender às necessidades de sua instalação.

 

 