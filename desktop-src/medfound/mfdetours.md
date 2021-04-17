---
description: Especifica o provedor de destours Microsoft Media Foundation, que rastreia Media Foundation chamadas à API.
ms.assetid: 7c9abda9-7968-463c-b4a9-19b54012ef56
title: elemento mfdetours
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c09d39d6f8a7c7ff1d88471e71c6fc58aa49bd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762154"
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



|              |     |
|--------------|-----|
| Pode estar vazio | Não  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração MFTrace](mftrace-configuration-file.md)
</dt> </dl>

 

 




