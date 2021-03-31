---
description: Define os elementos ServiceId e types para o host de serviço.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: elemento host
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec073a89cf1911ab363d757d36cd264c85c8a5c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827826"
---
# <a name="host-element"></a>elemento host

Define os elementos [**ServiceId**](serviceid.md) e [**Types**](types.md) para o host de serviço.

## <a name="usage"></a>Uso

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                   | Descrição                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [**ServiceID**](serviceid.md)<br/> | Define o identificador de serviço para o host de serviço.<br/> <br/> |
| [**Tipos**](types.md)<br/>         | Define uma lista de nomes qualificados XSD.<br/> <br/>               |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                                         | Descrição                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | Os metadados de hospedagem para o dispositivo a ser implementado.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




