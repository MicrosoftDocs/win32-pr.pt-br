---
title: Atributos de tipo de dados
description: Você pode aplicar esses atributos a tipos de dados em uma instrução typedef para definir ainda mais o uso ou o efeito do tipo de dados.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- MIDL, atributos, tipo de dados IDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57fb2a97639fc17454bfd1cad60466ad277e18ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637191"
---
# <a name="data-type-attributes"></a>Atributos de tipo de dados

Você pode aplicar esses atributos a tipos de dados em uma instrução [**typedef**](typedef.md) para definir ainda mais o uso ou o efeito do tipo de dados.



| Atributo                                 | Uso                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**identificador de contexto \_**](context-handle.md) | Identifica um identificador de associação que mantém informações de estado (contexto) em um servidor específico entre chamadas de procedimento remotos de um cliente específico. Não é válido para funções de interface de [**objeto**](object.md) .                                                                                                         |
| [**processamento**](handle.md)                  | Especifica um tipo de identificador personalizado específico para o aplicativo.                                                                                                                                                                                                                                                                |
| [**\_União MS**](-ms-union.md)            | Controla o alinhamento de NDR de uniões não encapsuladas. Use em [**typedef**](typedef.md)s para compatibilidade com versões anteriores com interfaces criadas com MIDL 1,0 ou 2,0.                                                                                                                                                            |
| [**pipe**](pipe.md)                      | Permite a transmissão de um fluxo aberto de dados digitados através de uma chamada de procedimento remoto. Um parâmetro [**no**](in.md) pipe permite que o servidor receba o fluxo de dados do cliente durante uma chamada de procedimento remoto. Um parâmetro [**out**](-out.md) pipe permite que o servidor envie por push o fluxo de dados de volta para o cliente. |
| [**transmitir \_ como**](transmit-as.md)       | Especifica como um tipo de dados será transmitido em uma rede, usado para marshaling personalizado.                                                                                                                                                                                                                                  |
| [**\_Enumeração v1**](v1-enum.md)               | Direciona que o tipo enumerado especificado seja transmitido como uma entidade de 32 bits, em vez do padrão de 16 bits.                                                                                                                                                                                                              |
| [**\_marshaling de transmissão**](wire-marshal.md)     | Semelhante a [**transmitir \_ como**](transmit-as.md) , mas você implementa as rotinas para dimensionar, realizar marshaling, desempacotar e liberar os dados.                                                                                                                                                                                              |



 

 

 




