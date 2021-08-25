---
description: Especifica uma palavra-chave para um provedor MFTrace.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: elemento keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df1f7a648e7861dc8d248141f051e9911c9cb93257f47fee5f2b4d2fd9d5469
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827546"
---
# <a name="keyword-element"></a>elemento keyword

Especifica uma palavra-chave para um [provedor MFTrace.](mftrace.md)

## <a name="usage"></a>Uso

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a>Atributos



| Atributo         | Type             | Obrigatório       | Descrição                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| **ID**<br/> | CDATA<br/> | Sim<br/> | O nome ou a máscara da palavra-chave<br/> <br/> |



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai

| Elemento                                   |
|-------------------------------------------|
| [**mfdetours**](mfdetours.md)<br/> |
| [**Provedor**](provider.md)<br/>   |



## <a name="remarks"></a>Comentários

Para o [**elemento mfdetours,**](mfdetours.md) as palavras-chave válidas são listadas no tópico [Palavras-chave MFTrace](mftrace-keywords.md).

Para o [**elemento do**](provider.md) provedor, as palavras-chave dependem do provedor de eventos. Você pode usar o utilitário Wevtutil.exe para listar as palavras-chave de um determinado provedor.

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
</dt> <dt>

[Palavras-chave MFTrace](mftrace-keywords.md)
</dt> </dl>

 

 




