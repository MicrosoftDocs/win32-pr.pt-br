---
description: Contém uma lista de provedores de rastreamento para MFTrace.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: elemento providers
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38a86bf3ca8ffa1ea9e3da20e0244e7abec8513
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118481"
---
# <a name="providers-element"></a>elemento providers

Contém uma lista de provedores de rastreamento para [o MFTrace.](mftrace.md)

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
| [**mfdetours**](mfdetours.md)<br/> | Especifica o provedor Media Foundation Detours, que Media Foundation chamadas à API.<br/> <br/> |
| [**Provedor**](provider.md)<br/>   | Especifica um provedor de rastreamento (ETW ou WPP).<br/> <br/>                                                  |



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

:::row:::
    :::column:::
        Pode estar vazio
    :::column-end:::
    :::column span="2":::
        Sim
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração do MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




