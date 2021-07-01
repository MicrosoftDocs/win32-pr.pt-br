---
description: Especifica um provedor de rastreamento (ETW ou WPP) para MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: elemento provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118441"
---
# <a name="provider-element"></a>elemento provider

Especifica um provedor de rastreamento (ETW ou WPP) para [MFTrace.](mftrace.md)

## <a name="usage"></a>Uso

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a>Atributos



| Atributo            | Type             | Obrigatório       | Descrição                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| **ID**<br/>    | CDATA<br/> | Sim<br/> | O nome ou GUID do provedor.<br/> <br/> |
| **level**<br/> | CDATA<br/> | Sim<br/> | O nível de rastreamento.<br/> <br/>                  |



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

 

 




