---
title: Elemento Application
description: Representa o elemento de nível superior na especificação de marcação do Windows Ribbon Framework.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Faixa de das janelas do elemento de aplicativo
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/20/2020
ms.locfileid: "103642953"
---
# <a name="application-element"></a>Elemento Application

Representa o elemento de nível superior na especificação de marcação do Windows Ribbon Framework.

## <a name="usage"></a>Uso

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a>Atributos



| Atributo            | Type                 | Obrigatório       | Descrição                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **xmlns**<br/> | xs:string<br/> | Sim<br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> O URI para a associação de namespace de marcação da faixa de faixas. <br/> </dd> </dl> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                               | Descrição                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [**Application. Commands**](windowsribbon-element-application-commands.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/>  |
| [**Application. views**](windowsribbon-element-application-views.md)<br/>       | Deve ocorrer exatamente uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai

Não há elementos pai.

## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer exatamente uma vez como o contêiner para toda a marcação da faixa de forma.

Os elementos filho do elemento **Application** devem ocorrer na ordem especificada:

1.  [**Application. Commands**](windowsribbon-element-application-commands.md)
2.  [**Application. views**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra uma declaração de elemento de **aplicativo** .


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a>Informações do elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo com suporte<br/> | Windows 7 |
| Pode estar vazio                        | Não        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Declarando comandos e controles com marcação de faixa de medida](windowsribbon-schema.md)
</dt> </dl>

 

 





