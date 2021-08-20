---
title: Associação de atributos do ACF
description: Especifique como o cliente se conecta ao servidor para chamadas de procedimento remoto com os atributos listados na tabela a seguir.
ms.assetid: 2a9fdd2f-c646-4ccd-bfa8-66fe973ef911
keywords:
- ACF MIDL, atributos, associação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32b4d53cea81ed2a69a702a1a58942834a538ffbef75cb11315dd792882bf89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385222"
---
# <a name="binding-acf-attributes"></a>Associação de atributos do ACF

Especifique como o cliente se conecta ao servidor para chamadas de procedimento remoto com os atributos listados na tabela a seguir.



| Atributo                                                          | Uso                                                                                                                                                                                                              |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Async**](async.md)                                             | Define um alça que permite que o chamador faça uma chamada assíncrona e retorne imediatamente sem aguardar os resultados e, em seguida, ressincronize com a função chamada para receber dados após a conclusão da chamada. |
| [**auto \_ handle**](auto-handle.md)                                | Informa a MIDL para permitir que o código stub controle a associação automaticamente. Esse será o padrão se você não especificar nenhum alça de associação.                                                                                    |
| [**\_ \_ naerialize do context handle**](context-handle-noserialize.md) | Garante que um handle de contexto nunca será serializado, independentemente do comportamento padrão do aplicativo.                                                                                                       |
| [**serializar \_ o \_ alça de contexto**](context-handle-serialize.md)     | Garante que um handle de contexto sempre será serializado, independentemente do comportamento padrão do aplicativo                                                                                                       |
| [**alça \_ explícita**](explicit-handle.md)                        | Permite que o aplicativo cliente controle a associação com um parâmetro explícito em cada procedimento.                                                                                                                      |
| [**alça \_ implícita**](implicit-handle.md)                        | Especifica um handle para procedimentos que não têm um parâmetro de alça explícito. O aplicativo cliente ainda controla a associação.                                                                                |
| [**strict \_ context \_ handle**](strict-context-handle.md)           | Garante que os métodos na interface aceitarão apenas os handles de contexto que foram criados por um método dessa interface.                                                                                     |



 

 

 




