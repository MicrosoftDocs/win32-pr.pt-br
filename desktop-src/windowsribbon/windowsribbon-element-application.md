---
title: Elemento Application
description: Representa o elemento de nível superior na especificação de marcação da estrutura Windows Faixa de Opções.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Elemento Application Windows Ribbon
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4055e271ecf3313596b73aa36a5cbea37250416d9b517fb4512b89fbc203293a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810806"
---
# <a name="application-element"></a>Elemento Application

Representa o elemento de nível superior na especificação de marcação da estrutura Windows Faixa de Opções.

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
| **xmlns**<br/> | xs:string<br/> | Sim<br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> O URI da associação de namespace de marcação da Faixa de Opções. <br/> </dd> </dl> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                               | Descrição                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [**Application.Commands**](windowsribbon-element-application-commands.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/>  |
| [**Application.Views**](windowsribbon-element-application-views.md)<br/>       | Deve ocorrer exatamente uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai

Não há elementos pai.

## <a name="remarks"></a>Comentários

Obrigatórios.

Deve ocorrer exatamente uma vez como o contêiner para toda a marcação da Faixa de Opções.

Os elementos filho do **elemento Application** devem ocorrer na ordem especificada:

1.  [**Application.Commands**](windowsribbon-element-application-commands.md)
2.  [**Application.Views**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra uma **declaração de elemento** Application.


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

[Declarando comandos e controles com marcação de faixa de opções](windowsribbon-schema.md)
</dt> </dl>

 

 





