---
description: por padrão, o mecanismo de pesquisa Windows e o catálogo não diferenciam sinais diacríticos, que são adicionados às letras para alterar o significado ou a pronúncia de uma palavra.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Sensibilidade de diacríticos em pesquisas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fcde4eb6cde6fe7a0b25a1d58f8026176de2fe30b6b0e2f020275821891a404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863679"
---
# <a name="diacritic-sensitivity-in-searches"></a>Sensibilidade de diacríticos em pesquisas

por padrão, o mecanismo de pesquisa Windows e o catálogo não diferenciam sinais diacríticos, que são adicionados às letras para alterar o significado ou a pronúncia de uma palavra. no entanto, Windows pesquisa permite que você altere isso para o catálogo usando o [gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) para definir a sensibilidade de diacríticos. Por exemplo, com a sensibilidade de diacríticos definida como **false**, o catálogo trataria "resume" e "resumé" como se fossem a mesma palavra.

Na camada de consulta, os termos de consulta com sinais diacríticos nas cláusulas FREETEXT e CONTAINS são passados para o mecanismo e, em seguida, são normalizados (como seriam no momento do índice) para correspondência. A correspondência com relação ao catálogo sempre é sensível ao diacrítico.

> [!Note]  
> Esse não é o caso para os intervalos de caracteres 0x2e81-F8FF e 0x1100-0x11ff.

 

 

 



