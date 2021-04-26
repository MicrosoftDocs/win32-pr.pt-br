---
description: Define um serviço a ser hospedado em uma função do construtor de hosts.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: elemento hostedService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96c9f6e010989f4844d93299bb34f1ab8893236
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994783"
---
# <a name="hostedservice-element"></a>elemento hostedService

Define um serviço a ser hospedado em uma função do construtor de hosts.

## <a name="usage"></a>Uso

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                     | Descrição                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codinome**](codename.md)<br/>     | Especifica o nome a ser usado para o tipo de porta no código gerado. Por padrão, o nome do código é gerado a partir do nome qualificado do tipo de porta.<br/> <br/> |
| [**portType**](porttype.md)<br/>     | Tipo de porta para o qual o código deve ser gerado.<br/> <br/>                                                                                                       |
| [**proxyClass**](proxyclass.md)<br/> | Nome da classe a ser gerada a partir da função do construtor.<br/> <br/>                                                                                                      |
| [**ServiceID**](serviceid.md)<br/>   | Um URI que representa o identificador de serviço.<br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a>Elementos pai



| Elemento                         | Descrição                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [**Grupo**](file.md)<br/> | A especificação do arquivo de saída para o gerador de código.<br/> <br/> |



## <a name="element-information"></a>Informações do elemento



| Label | Valor |
|-------------------------------------|---------------|
| Sistema mínimo com suporte<br/> | Windows Vista |
| Pode estar vazio                        | Não            |



 

 




