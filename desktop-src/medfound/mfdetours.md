---
description: Especifica o provedor de destours Microsoft Media Foundation, que rastreia Media Foundation chamadas à API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cd03711c74c21a9a6ff33d2cc2560e4b6d6e0a3
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119331"
---
# <a name="mfdetours-element"></a>elemento mfdetours

Especifica o provedor de destours Microsoft Media Foundation, que rastreia Media Foundation chamadas à API.

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
| [**chaves**](keyword.md)<br/> |



### <a name="child-element-sequence"></a>Sequência de elementos filho

``` syntax
keyword+
```

## <a name="parent-elements"></a>Elementos pai

| Elemento                                   |
|-------------------------------------------|
| [**fornecedor**](providers.md)<br/> |



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

[Arquivo de configuração MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




