---
description: especifica um tipo de recurso que não foi definido de outra forma por Windows dispositivos portáteis.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c418299474373d8b960d15c429ea98d887cc404be49c8d38c7d2bb83611c4ca1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805866"
---
# <a name="wpd_resource_generic"></a>recurso de WPD \_ \_ genérico

especifica um tipo de recurso que não foi definido de outra forma por Windows dispositivos portáteis. você pode definir seus próprios recursos personalizados que dão suporte a qualquer atributo personalizado ou Windows os atributos definidos por dispositivos portáteis. No entanto, qualquer recurso que você criar deve dar suporte aos seguintes atributos.



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

 

 



