---
description: Especifica o provedor Microsoft Media Foundation Detours, que Media Foundation chamadas à API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: Elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a0215d9d065bd27f0ad98ebea23abec8f7ecbbfc2223d522e0ddd1887990c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113636"
---
# <a name="mfdetours-element"></a>Elemento mfdetours

Especifica o provedor Microsoft Media Foundation Detours, que Media Foundation chamadas à API.

## <a name="usage"></a>Uso

``` syntax
<mfdetours
  level = "CDATA">
  child elements
</mfdetours>
```

## <a name="attributes"></a>Atributos



| Atributo            | Type             | Obrigatório       | Descrição                             |
|----------------------|------------------|----------------|-----------------------------------------|
| **level**<br/> | CDATA<br/> | Sim<br/> | O nível de rastreamento.<br/> <br/> |



## <a name="child-elements"></a>Elementos filho



| Elemento                               |
|---------------------------------------|
| [**Palavra**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
keyword+
```

## <a name="parent-elements"></a>Elementos pai

| Elemento                                   |
|-------------------------------------------|
| [**Provedores**](providers.md)<br/> |



## <a name="element-information"></a>Informações do elemento

:::row:::
    :::column:::
        Pode estar vazio
    :::column-end:::
    :::column span="2":::
        Não
    :::column-end:::
:::row-end:::

## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração do MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




