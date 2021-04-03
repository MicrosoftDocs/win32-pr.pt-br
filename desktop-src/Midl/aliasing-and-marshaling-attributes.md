---
title: Atributos de alias e empacotamento
description: Os aplicativos distribuídos quase sempre passam dados entre os programas cliente e servidor quando chamam procedimentos de interface.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- MIDL de IDL, atributos MIDL, alias e marshaling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006099"
---
# <a name="aliasing-and-marshaling-attributes"></a>Atributos de alias e empacotamento

Os aplicativos distribuídos quase sempre passam dados entre os programas cliente e servidor quando chamam procedimentos de interface. Os desenvolvedores usam MIDL para descrever os dados que os programas de cliente e servidor passam de forma padrão. O compilador MIDL cria o stub do aplicativo, ou o proxy, programas para o cliente e o servidor que convertem os dados em um formato padronizado que pode ser enviado por uma rede. Esse formato, o formato NDR (representação de dados de rede), geralmente é chamado de formato de conexão dos dados. Os stubs devem converter dados de seu formato nativo no espaço de memória do programa para o NDR. Essa conversão é chamada de marshaling dos dados. Quando um cliente ou programa de servidor recebe dados, ele deve converter os dados do NDR para o formato nativo para esse programa. Isso é chamado de desempacotamento dos dados.

Use atributos de alias e de marshaling para controlar como os dados são empacotados em formato NDR e transmitidos pela rede.



| Atributo                             | Uso                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**chamar \_ como**](call-as.md)           | Mapeia uma função não Remotable para uma chamada de procedimento remoto.                                                                      |
| [**IID \_ é**](iid-is.md)             | Fornece o identificador de interface da interface COM que é o objeto do ponteiro.                                     |
| [**transmitir \_ como**](transmit-as.md)   | Converte um tipo de dados em um tipo mais simples para transmissão em uma rede.                                                       |
| [**\_marshaling de transmissão**](wire-marshal.md) | Semelhante a [**transmitir \_ como**](transmit-as.md) , mas você implementa as rotinas para dimensionar, realizar marshaling, desempacotar e liberar os dados. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conversão de tipo e empacotamento de atributos ACF](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




