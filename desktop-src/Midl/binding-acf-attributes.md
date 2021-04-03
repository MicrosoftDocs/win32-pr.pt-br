---
title: Atributos de ACF de associação
description: Especifique como o cliente se conecta ao servidor para chamadas de procedimento remoto com os atributos listados na tabela a seguir.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- MIDL de ACF, atributos, associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2a2e9ac9ada0ee33c4930005add6a1ca031ee5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005916"
---
# <a name="binding-acf-attributes"></a>Atributos de ACF de associação

Especifique como o cliente se conecta ao servidor para chamadas de procedimento remoto com os atributos listados na tabela a seguir.



| Atributo                                                          | Uso                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Async**](async.md)                                             | Define um identificador que permite que o chamador faça uma chamada assíncrona e retorne imediatamente sem esperar pelos resultados e, em seguida, sincronize novamente com a função chamada para receber dados após a conclusão da chamada. |
| [**\_identificador automático**](auto-handle.md)                                | Informa ao MIDL para permitir que o código de stub controle a associação automaticamente. Esse será o padrão se você não especificar nenhum identificador de ligação.                                                                                    |
| [**identificador de contexto \_ \_ noserializeize**](context-handle-noserialize.md) | Garante que um identificador de contexto nunca será serializado, independentemente do comportamento padrão do aplicativo.                                                                                                       |
| [**\_serializar identificador de contexto \_**](context-handle-serialize.md)     | Garante que um identificador de contexto sempre será serializado, independentemente do comportamento padrão do aplicativo                                                                                                       |
| [**\_identificador explícito**](explicit-handle.md)                        | Permite que o aplicativo cliente controle a associação com um parâmetro explícito em cada procedimento.                                                                                                                      |
| [**\_identificador implícito**](implicit-handle.md)                        | Especifica um identificador para procedimentos que não têm um parâmetro identificador explícito. O aplicativo cliente ainda controla a associação.                                                                                |
| [**\_identificador de contexto estrito \_**](strict-context-handle.md)           | Garante que os métodos na interface aceitem apenas identificadores de contexto que foram criados por um método dessa interface.                                                                                     |



 

 

 




