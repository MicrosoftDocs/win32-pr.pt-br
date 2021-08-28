---
title: Atributos de estrutura e união
description: Use a opção \_ \ atributos para especificar a característica de uma união em uma chamada de procedimento remoto. Use o atributo ignore para designar determinados membros de estrutura ou união como locais para o aplicativo cliente.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- IDL MIDL, atributos, estrutura e união
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc179632bb7e0d64b777f3c8a08b9de2af7bbf818978d6bb0a7ee2ea8b515542
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066666"
---
# <a name="structure-and-union-attributes"></a>Atributos de estrutura e união

Use os **atributos \_ switch** para especificar a característica de uma \* união em uma chamada de procedimento remoto. Use o [**atributo ignore**](ignore.md) para designar determinados membros de estrutura ou união como locais para o aplicativo cliente.



| Atributo                           | Uso                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**Interruptor**](switch.md)            | Seleciona o discriminante para uma união encapsulada.                                                                           |
| [**switch \_ é**](switch-is.md)     | Identifica o discriminante para uma união não truncada.                                                                      |
| [**tipo \_ switch**](switch-type.md) | Identifica o tipo do discriminante para uma união não truncada.                                                          |
| [**Ignorar**](ignore.md)            | Designa que um ponteiro contido em uma estrutura ou união e o objeto indicado pelo ponteiro não deve ser transmitido. |



 

Você também pode usar os atributos de ponteiro de matriz [e dimensionado](array-and-sized-pointer-attributes.md) para especificar características de membros de estrutura ou união.

 

 




