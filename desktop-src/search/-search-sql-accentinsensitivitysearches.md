---
description: Por padrão, o mecanismo de pesquisa do Windows e o catálogo não diferenciam sinais diacríticos, que são adicionados às letras para alterar o significado ou a pronúncia de uma palavra.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Sensibilidade de diacríticos em pesquisas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787725"
---
# <a name="diacritic-sensitivity-in-searches"></a>Sensibilidade de diacríticos em pesquisas

Por padrão, o mecanismo de pesquisa do Windows e o catálogo não diferenciam sinais diacríticos, que são adicionados às letras para alterar o significado ou a pronúncia de uma palavra. No entanto, o Windows Search permite que você altere isso para o catálogo usando o [Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) para definir a sensibilidade de diacríticos. Por exemplo, com a sensibilidade de diacríticos definida como **false**, o catálogo trataria "resume" e "resumé" como se fossem a mesma palavra.

Na camada de consulta, os termos de consulta com sinais diacríticos nas cláusulas FREETEXT e CONTAINS são passados para o mecanismo e, em seguida, são normalizados (como seriam no momento do índice) para correspondência. A correspondência com relação ao catálogo sempre é sensível ao diacrítico.

> [!Note]  
> Esse não é o caso para os intervalos de caracteres 0x2e81-F8FF e 0x1100-0x11ff.

 

 

 



