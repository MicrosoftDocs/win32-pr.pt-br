---
title: Atributos de tipo de dados
description: Você pode aplicar esses atributos a tipos de dados em uma instrução typedef para definir ainda mais o uso ou o efeito do tipo de dados.
ms.assetid: 9a2e7c3d-f18f-4162-877c-5fc48a36b05d
keywords:
- IDL MIDL, atributos, tipo de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85142c13d9b478c449bf07955b85dd586b6312d891e17699861afb5bc2cc658b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067366"
---
# <a name="data-type-attributes"></a>Atributos de tipo de dados

Você pode aplicar esses atributos a tipos de dados em uma instrução [**typedef**](typedef.md) para definir ainda mais o uso ou o efeito do tipo de dados.



| Atributo                                 | Uso                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**alça de \_ contexto**](context-handle.md) | Identifica um identificador de associação que mantém informações de estado (contexto) em um servidor específico entre chamadas de procedimento remoto de um cliente específico. Não é válido para [**funções de**](object.md) interface de objeto.                                                                                                         |
| [**Lidar com**](handle.md)                  | Especifica um tipo de identificador personalizado específico para o aplicativo.                                                                                                                                                                                                                                                                |
| [**ms \_ union**](-ms-union.md)            | Controla o alinhamento de NDR de uniões não truncadas. Use em [**typedef**](typedef.md)s para compatibilidade com compatibilidade com backward com interfaces criadas com MIDL 1.0 ou 2.0.                                                                                                                                                            |
| [**Tubo**](pipe.md)                      | Permite a transmissão de um fluxo aberto de dados digitados em uma chamada de procedimento remoto. Um [**parâmetro no**](in.md) pipe permite que o servidor e pull do fluxo de dados do cliente durante uma chamada de procedimento remoto. Um [**parâmetro de**](-out.md) pipe out permite que o servidor es por push o fluxo de dados de volta para o cliente. |
| [**transmitir \_ como**](transmit-as.md)       | Especifica como um tipo de dados será transmitido por uma rede, usado para marshaling personalizado.                                                                                                                                                                                                                                  |
| [**enum v1 \_**](v1-enum.md)               | Direciona que o tipo enumerado especificado seja transmitido como uma entidade de 32 bits, em vez do padrão de 16 bits.                                                                                                                                                                                                              |
| [**wire \_ marshal**](wire-marshal.md)     | Semelhante a [**transmitir \_ como,**](transmit-as.md) mas você implementa as rotinas para tamanho, marshal, unmarshal e liberar os dados.                                                                                                                                                                                              |



 

 

 




