---
title: Atributos de ACF de otimização de stub
description: Esses atributos permitem otimizar o tamanho e a velocidade do seu código stub.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- MIDL de ACF, atributos, otimização de stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8386eb6a6077a994b6f9800ff237a9966e97bff5eb0d6d865ea313634790f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383188"
---
# <a name="stub-optimization-acf-attributes"></a>Atributos de ACF de otimização de stub

Esses atributos permitem otimizar o tamanho e a velocidade do seu código stub.



| Atributo                                    | Uso                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**código**](code.md)[**Nocode**](nocode.md) | Use os atributos [**Code**](code.md) e [**Nocode**](nocode.md) juntos para evitar a geração de código stub para funções não utilizadas. Aplique o atributo **Nocode** ao cabeçalho da interface e aplique o atributo **Code** a esses procedimentos que o aplicativo cliente irá implementar. O código stub do cliente será gerado somente para os procedimentos selecionados.                                                                |
| [**formato**](optimize.md)                 | Permite ajustar o nível de otimização que o compilador MIDL executa ao gerar código stub, especificando que os dados serão empacotados pelo método misto ou interpretado. Você pode aplicar o atributo [**Optimize**](optimize.md) a uma interface ou a funções selecionadas dentro da interface. Em ambos os casos, seu uso substituirá as otimizações de linha de comando e quaisquer padrões preexistentes. |



 

 

 




