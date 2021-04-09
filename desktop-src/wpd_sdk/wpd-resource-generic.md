---
description: Especifica um tipo de recurso que não foi definido de outra forma por dispositivos portáteis do Windows.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090270"
---
# <a name="wpd_resource_generic"></a>recurso de WPD \_ \_ genérico

Especifica um tipo de recurso que não foi definido de outra forma por dispositivos portáteis do Windows. Você pode definir seus próprios recursos personalizados que dão suporte a qualquer atributo personalizado ou do Windows com dispositivos portáteis definidos. No entanto, qualquer recurso que você criar deve dar suporte aos seguintes atributos.



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

 

 



