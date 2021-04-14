---
title: Atributos de estrutura e União
description: Use os \_ atributos switch \ para especificar a característica de uma União em uma chamada de procedimento remoto. Use o atributo ignorar para designar determinados membros da estrutura ou da União como locais para o aplicativo cliente.
ms.assetid: e06e5184-fa92-4446-964b-d56d0e5f2872
keywords:
- MIDL, atributos, estrutura e União de IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2a7764d56c8557bd71923021a9f324a118ac81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453571"
---
# <a name="structure-and-union-attributes"></a>Atributos de estrutura e União

Use os **atributos \_ switch** \* para especificar a característica de uma União em uma chamada de procedimento remoto. Use o atributo [**ignorar**](ignore.md) para designar determinados membros da estrutura ou da União como locais para o aplicativo cliente.



| Atributo                           | Uso                                                                                                                         |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**comutador**](switch.md)            | Seleciona o discriminante para uma União encapsulada.                                                                           |
| [**switch \_ é**](switch-is.md)     | Identifica o discriminante para uma União não encapsulada.                                                                      |
| [**tipo de comutador \_**](switch-type.md) | Identifica o tipo de discriminante para uma União não encapsulada.                                                          |
| [**ignorar**](ignore.md)            | Designa que um ponteiro contido em uma estrutura ou União e o objeto indicado pelo ponteiro não sejam transmitidos. |



 

Você também pode usar os [atributos de ponteiro de matriz e dimensionamento](array-and-sized-pointer-attributes.md) para especificar características de estrutura ou membros de União.

 

 




