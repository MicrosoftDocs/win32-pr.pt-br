---
description: Especifica o arquivo inteiro por trás do objeto . Também é uma maneira de se referir a qualquer tipo de recurso, incluindo aqueles não cobertos por outros tipos de recursos Windows Dispositivos Portáteis, como um tipo de objeto personalizado.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d939cf58033baded231363b39410c2e527fe303075c94255a00ba96831a609b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805876"
---
# <a name="wpd_resource_default"></a>WPD \_ RESOURCE \_ DEFAULT

Especifica o arquivo inteiro por trás do objeto . Também é uma maneira de se referir a qualquer tipo de recurso, incluindo aqueles não cobertos por outros tipos de recursos Windows Dispositivos Portáteis, como um tipo de objeto personalizado.

Todos os recursos inseridos no recurso especificado serão incluídos. Por exemplo, o recurso padrão de uma pasta raiz de contatos pode incluir todos os contatos aninhados. No entanto, todos os recursos filho que são simplesmente *vinculados* por metadados ou referências não são incluídos. Um exemplo disso seria uma playlist, que só pode vincular a arquivos de áudio por meio de referências de metadados ou referências de caminho textual no arquivo.

O único valor *pid permitido* para essa **PROPERTYKEY** é zero.

Esse tipo de recurso deve dar suporte aos seguintes atributos.



| Nome do atributo                                                                                                            | Obrigatório ou Opcional                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [TAMANHO TOTAL \_ DO \_ ATRIBUTO DE RECURSO \_ WPD \_](resource-attribute-properties.md)              | Obrigatórios.                                              |
| [O ATRIBUTO DE RECURSO WPD \_ \_ PODE \_ \_ LER](attributes.md)                                     | Necessário se os clientes puderem ler esse recurso.            |
| [O ATRIBUTO DE RECURSO WPD \_ \_ PODE \_ \_ GRAVAR](attributes.md)                                   | Necessário se os clientes puderem gravar nesse recurso.        |
| [O ATRIBUTO \_ DE RECURSO \_ WPD PODE \_ \_ EXCLUIR](attributes.md)                                 | Necessário se os clientes puderem excluir esse recurso.          |
| [TAMANHO IDEAL DO BUFFER DE \_ \_ LEITURA DO ATRIBUTO \_ \_ \_ \_ DE RECURSO WPD](attributes.md)   | Necessário se os clientes têm acesso de leitura ao recurso.  |
| [TAMANHO IDEAL \_ DO BUFFER DE GRAVAÇÃO \_ DO ATRIBUTO \_ \_ \_ \_ DE RECURSO WPD](attributes.md) | Necessário se os clientes têm acesso de gravação ao recurso. |
| [FORMATO DE \_ ATRIBUTO DE \_ RECURSO WPD \_](resource-attribute-properties.md)                       | Obrigatórios.                                              |
| [CHAVE DE RECURSO \_ DO \_ ATRIBUTO DE RECURSO \_ \_ WPD](resource-attribute-properties.md)                                              | Recomendável.                                           |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Requisitos para recursos**](requirements-for-resources.md)
</dt> </dl>

 

 



