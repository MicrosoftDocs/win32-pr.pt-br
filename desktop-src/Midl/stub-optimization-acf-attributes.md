---
title: Atributos de ACF de otimização de stub
description: Esses atributos permitem otimizar o tamanho e a velocidade do seu código stub.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- MIDL de ACF, atributos, otimização de stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822501"
---
# <a name="stub-optimization-acf-attributes"></a>Atributos de ACF de otimização de stub

Esses atributos permitem otimizar o tamanho e a velocidade do seu código stub.



| Atributo                                    | Uso                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**código**](code.md)[**Nocode**](nocode.md) | Use os atributos [**Code**](code.md) e [**Nocode**](nocode.md) juntos para evitar a geração de código stub para funções não utilizadas. Aplique o atributo **Nocode** ao cabeçalho da interface e aplique o atributo **Code** a esses procedimentos que o aplicativo cliente irá implementar. O código stub do cliente será gerado somente para os procedimentos selecionados.                                                                |
| [**formato**](optimize.md)                 | Permite ajustar o nível de otimização que o compilador MIDL executa ao gerar código stub, especificando que os dados serão empacotados pelo método misto ou interpretado. Você pode aplicar o atributo [**Optimize**](optimize.md) a uma interface ou a funções selecionadas dentro da interface. Em ambos os casos, seu uso substituirá as otimizações de linha de comando e quaisquer padrões preexistentes. |



 

 

 




