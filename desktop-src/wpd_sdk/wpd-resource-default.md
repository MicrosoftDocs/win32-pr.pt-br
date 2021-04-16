---
description: Especifica o arquivo inteiro por trás do objeto. Também é uma maneira de se referir a qualquer tipo de recurso, incluindo aqueles não cobertos por outros tipos de recursos de dispositivos portáteis do Windows, como um tipo de objeto personalizado.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506140"
---
# <a name="wpd_resource_default"></a>\_padrão de recursos WPD \_

Especifica o arquivo inteiro por trás do objeto. Também é uma maneira de se referir a qualquer tipo de recurso, incluindo aqueles não cobertos por outros tipos de recursos de dispositivos portáteis do Windows, como um tipo de objeto personalizado.

Todos os recursos inseridos no recurso especificado serão incluídos. Por exemplo, o recurso padrão de uma pasta raiz de contatos pode incluir todos os contatos aninhados. No entanto, todos os recursos filho que são simplesmente *vinculados* por metadados ou referências não são incluídos. Um exemplo disso seria uma lista de reprodução, que só pode ser vinculada a arquivos de áudio por meio de referências de metadados ou referências de caminho textual no arquivo.

O único valor *pid* permitido para este **PROPERTYKEY** é zero.

Esse tipo de recurso deve dar suporte aos seguintes atributos.



| Nome do atributo                                                                                                            | Obrigatório ou opcional                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [\_ \_ Tamanho total do atributo de recurso WPD \_ \_](resource-attribute-properties.md)              | Obrigatórios.                                              |
| [o \_ atributo de recurso WPD \_ \_ pode \_ ler](attributes.md)                                     | Necessário se os clientes puderem ler este recurso.            |
| [o \_ atributo de recurso WPD \_ \_ pode \_ gravar](attributes.md)                                   | Necessário se os clientes puderem gravar nesse recurso.        |
| [o \_ atributo de recurso WPD \_ \_ pode \_ excluir](attributes.md)                                 | Necessário se os clientes puderem excluir esse recurso.          |
| [\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de leitura \_ \_](attributes.md)   | Necessário se os clientes tiverem acesso de leitura ao recurso.  |
| [\_atributo de recurso WPD \_ \_ ideal tamanho do \_ buffer de gravação \_ \_](attributes.md) | Necessário se os clientes tiverem acesso de gravação ao recurso. |
| [\_formato de \_ atributo de recurso WPD \_](resource-attribute-properties.md)                       | Obrigatórios.                                              |
| [\_chave de \_ recurso de atributo de recurso WPD \_ \_](resource-attribute-properties.md)                                              | Recomendável.                                           |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Requisitos para recursos**](requirements-for-resources.md)
</dt> </dl>

 

 



