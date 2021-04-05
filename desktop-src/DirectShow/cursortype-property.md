---
description: A propriedade CursorType define ou recupera o tipo de cursor atual.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: Propriedade CursorType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825800"
---
# <a name="cursortype-property"></a>Propriedade CursorType

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `CursorType` propriedade define ou recupera o tipo de cursor atual.

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a>Valor Retornado

Retorna um valor inteiro que representa o tipo de cursor.

## <a name="remarks"></a>Comentários

Os valores possíveis para essa propriedade são:



| Valor | Descrição |
|-------|-------------|
| 0     | Seta       |
| 1     | Ampliar     |
| 2     | Reduzir    |
| 3     | Existentes        |
| -1    | Nenhum        |



 

Essa propriedade é de leitura/gravação com um valor padrão de zero. Quando a imagem é ampliada, definir `CursorType` como **mão** (0x3) coloca o aplicativo no modo de arrastar, permitindo que o usuário mova a imagem dentro da área de exibição do vídeo.

 

 



