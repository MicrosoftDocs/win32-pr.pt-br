---
description: Por padrão, o Windows Search e o catálogo não são sensíveis a diacríticas, que são marcas de acento adicionadas às letras para alterar o significado ou a pronúncia de uma palavra.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Sensibilidade diacrítica em pesquisas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fcde4eb6cde6fe7a0b25a1d58f8026176de2fe30b6b0e2f020275821891a404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863679"
---
# <a name="diacritic-sensitivity-in-searches"></a>Sensibilidade diacrítica em pesquisas

Por padrão, o Windows Search e o catálogo não são sensíveis a diacríticas, que são marcas de acento adicionadas às letras para alterar o significado ou a pronúncia de uma palavra. No entanto, Windows Search permite que você altere [](-search-3x-wds-mngidx-catalog-manager.md) isso para seu catálogo usando o Gerenciador de Catálogo para definir a sensibilidade diacrítica. Por exemplo, com a sensibilidade diacrítica definida como **FALSE**, o catálogo trataria "resume" e "resumé" como se fossem a mesma palavra.

Na camada de consulta, os termos de consulta com diacríticas nas cláusulas FREETEXT e CONTAINS são passados para o mecanismo e, em seguida, normalizados (como seriam no tempo de índice) para correspondência. A correspondência com o catálogo é sempre diacrítica.

> [!Note]  
> Esse não é o caso para os intervalos de caracteres 0x2e81-f8ff e 0x1100-0x11ff.

 

 

 



