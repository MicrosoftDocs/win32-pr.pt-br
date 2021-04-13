---
description: A propriedade DefaultSubpictureLanguageExt recupera a extensão de linguagem de subimagem de DVD padrão.
ms.assetid: bd437844-6e5c-4237-a968-700a53e18635
title: Propriedade DefaultSubpictureLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bba455a26df4eaa6676b77447c3faed408609
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500224"
---
# <a name="defaultsubpicturelanguageext-property"></a>Propriedade DefaultSubpictureLanguageExt

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `DefaultSubpictureLanguageExt` propriedade recupera a extensão de linguagem de subimagem do DVD padrão.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultSubpictureLanguageExt
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que indica a extensão de linguagem de subimagem do DVD padrão.

## <a name="remarks"></a>Comentários

Esta propriedade é somente leitura sem valor padrão. A tabela a seguir mostra os valores possíveis.



| Valor | Descrição                    |
|-------|--------------------------------|
| 0     | Extensão não especificada        |
| 1     | Legendas normais                |
| 2     | Legendas grandes                   |
| 3     | Legendas das crianças            |
| 5     | Legendas normais ocultas         |
| 6     | Legendas grandes ocultas            |
| 7     | Legendas ocultas de filhos     |
| 9     | Forced (forçado)                         |
| 13    | Comentários do diretor normal     |
| 14    | Comentários do Big Director        |
| 15    | Comentários de Director's dos filhos |



 

## <a name="see-also"></a>Confira também

<dl> <dt>

[**SelectDefaultSubpictureLanguage**](selectdefaultsubpicturelanguage-method.md)
</dt> </dl>

 

 



