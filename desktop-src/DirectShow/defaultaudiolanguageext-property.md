---
description: A propriedade DefaultAudioLanguageExt recupera a extensão de idioma de áudio de DVD padrão.
ms.assetid: 628af2aa-e528-4689-953b-558e13e1d513
title: Propriedade DefaultAudioLanguageExt
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5ce89099cd8e31cde9beb8bb3c8a9f1e16b3b0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500278"
---
# <a name="defaultaudiolanguageext-property"></a>Propriedade DefaultAudioLanguageExt

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `DefaultAudioLanguageExt` propriedade recupera a extensão de idioma de áudio de DVD padrão.

``` syntax
[ iLangExt = ] MSWebDVD.DefaultAudioLanguageExt
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que indica a extensão de idioma de áudio padrão. Consulte comentários para obter os valores possíveis.

## <a name="remarks"></a>Comentários

Esta propriedade é somente leitura sem valor padrão. A tabela a seguir mostra os possíveis valores para as extensões de linguagem de áudio de DVD.



| Valor | Descrição       |
|-------|-------------------|
| 0     | NotSpecified      |
| 1     | Legendas          |
| 2     | VisuallyImpaired  |
| 3     | DirectorComments1 |
| 4     | DirectorComments2 |



 

 

 



