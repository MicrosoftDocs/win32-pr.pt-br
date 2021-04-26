---
description: Define os elementos ServiceId e types para o host de serviço.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: elemento host
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f051f6665715ecaa519a060e18a3cbf4912210
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993793"
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



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




