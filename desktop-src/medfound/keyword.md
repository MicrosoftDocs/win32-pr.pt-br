---
description: Especifica uma palavra-chave para um provedor de MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: elemento keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11632a257e7d51378ddb816124e51548746a178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763948"
---
# <a name="keyword-element"></a>elemento keyword

Especifica uma palavra-chave para um provedor de [MFTrace](mftrace.md) .

## <a name="usage"></a>Uso

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a>Atributos



| Atributo         | Type             | Obrigatório       | Descrição                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| **ID**<br/> | CDATA<br/> | Yes<br/> | O nome ou a máscara da palavra-chave<br/> <br/> |



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                   |
|-------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> |
| [**operador**](provider.md)<br/>   |



## <a name="remarks"></a>Comentários

Para o elemento [**mfdetours**](mfdetours.md) , as palavras-chave válidas são listadas no tópico [MFTrace Words](mftrace-keywords.md).

Para o elemento [**Provider**](provider.md) , as palavras-chave dependem do provedor de eventos. Você pode usar o utilitário Wevtutil.exe para listar as palavras-chave de um determinado provedor.

## <a name="element-information"></a>Informações do elemento



|              |     |
|--------------|-----|
| Pode estar vazio | Yes |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Arquivo de configuração MFTrace](mftrace-configuration-file.md)
</dt> <dt>

[Palavras-chave MFTrace](mftrace-keywords.md)
</dt> </dl>

 

 




