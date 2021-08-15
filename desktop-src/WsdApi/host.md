---
description: Define os elementos ServiceId e types para o host de serviço.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: elemento host
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe0637c358fabe27f2a1203306cd53407d85ab8b52f2dcd7a827dd49becffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738602"
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



| Rótulo | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




