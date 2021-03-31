---
title: Catálogo Global
description: Um domínio executado por Active Directory Domain Services pode consistir em muitas partições ou contextos de nomenclatura.
ms.assetid: eac02c1f-0c37-4eee-822d-07913ea8775a
ms.tgt_platform: multiple
keywords:
- Active Directory de catálogo global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4496804d21e53cf2d87947288179e7f96ca75c8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103640402"
---
# <a name="global-catalog"></a>Catálogo Global

Um domínio executado por Active Directory Domain Services pode consistir em muitas partições ou contextos de nomenclatura. O DN (nome distinto) de um objeto inclui informações suficientes para localizar uma réplica da partição que contém o objeto. No entanto, muitas vezes o usuário ou o aplicativo não conhece o DN do objeto de destino ou qual partição pode conter o objeto. O [*catálogo global (GC)*](/previous-versions/windows/desktop/legacy/ms681905(v=vs.85)) permite que os usuários e aplicativos localizem objetos em uma árvore de domínio Active Directory, dado um ou mais atributos do objeto de destino.

O catálogo global contém uma réplica parcial de cada contexto de nomenclatura no diretório. Ele contém o esquema e os contextos de nomenclatura de configuração também. Isso significa que o GC mantém uma réplica de cada objeto no diretório, mas com apenas um pequeno número de seus atributos. Os atributos no GC são aqueles usados com mais frequência em operações de pesquisa (como nomes e sobrenome de um usuário ou nomes de logon) e aqueles necessários para localizar uma réplica completa do objeto. O GC permite aos usuários encontrar rapidamente objetos de interesse sem saber qual domínio os contém e sem exigir um namespace estendido contíguo na empresa.

O catálogo global é criado automaticamente pelo sistema de replicação de Active Directory Domain Services. A topologia de replicação para o catálogo global é gerada automaticamente. As propriedades replicadas no catálogo global incluem um conjunto base definido pela Microsoft. Os administradores podem especificar propriedades adicionais para atender às necessidades de sua instalação.

 

 