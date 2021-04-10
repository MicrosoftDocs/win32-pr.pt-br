---
description: Contém uma lista de provedores de rastreamento para MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: elemento providers
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164893"
---
# <a name="providers-element"></a>elemento providers

Contém uma lista de provedores de rastreamento para [MFTrace](mftrace.md).

## <a name="usage"></a>Uso

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                   | Descrição                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> | Especifica o provedor de destours Media Foundation, que rastreia Media Foundation chamadas à API.<br/> <br/> |
| [**operador**](provider.md)<br/>   | Especifica um provedor de rastreamento (ETW ou WPP).<br/> <br/>                                                  |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a>Elementos pai

Não há elementos pai.

## <a name="element-information"></a>Informações do elemento



|              |     |
|--------------|-----|
| Pode estar vazio | Yes |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




