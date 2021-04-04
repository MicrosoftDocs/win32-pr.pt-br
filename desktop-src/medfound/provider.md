---
description: Especifica um provedor de rastreamento (ETW ou WPP) para MFTrace.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: elemento Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647749"
---
# <a name="provider-element"></a>elemento Provider

Especifica um provedor de rastreamento (ETW ou WPP) para [MFTrace](mftrace.md).

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



|              |     |
|--------------|-----|
| Pode estar vazio | Não  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




