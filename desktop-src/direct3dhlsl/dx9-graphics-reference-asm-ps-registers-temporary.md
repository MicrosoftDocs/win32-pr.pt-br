---
title: Registro temporário (referência do HLSL PS)
description: Os registros temporários de entrada do sombreador de pixel são usados para armazenar resultados intermediários.
ms.assetid: e61daaa1-0a9b-4b1c-b91c-56573be59ed9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7aebee99a693ac629d9cc8a372fba7589a9e29ef
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103823476"
---
# <a name="temporary-register-hlsl-ps-reference"></a>Registro temporário (referência do HLSL PS)

Os registros temporários de entrada do sombreador de pixel são usados para armazenar resultados intermediários.

Syntax


```
no declaration is required
```





| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro temporário    |      |      |      |      | x    | x     | x    | x    | x     |



 

-   Há 12 registros temporários de sombreador de pixel: R0 para R11.
-   Esses registros são usados para armazenar resultados intermediários durante cálculos.
-   Se um registro temporário usar componentes que não estão definidos no código anterior, a validação do sombreador falhará.
-   Essas são, pelo menos, a precisão de ponto flutuante.
-   Um máximo de três pode ser usado em uma única instrução.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




