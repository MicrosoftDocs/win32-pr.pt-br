---
title: Macros predefinidas
description: O RC não oferece suporte às macros predefinidas ANSI C ( \_ \_ Date \_ \_ , \_ \_ File \_ \_ , \_ \_ line \_ \_ , \_ \_ stdc \_ \_ , \_ \_ time \_ \_ , \_ \_ timestamp \_ \_ ). Portanto, você não pode incluir essas macros em arquivos de cabeçalho que serão incluídas no script de recurso.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 351674bc86ab56753bb49dba9e65edd97a7b1a04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084064"
---
# <a name="predefined-macros"></a>Macros predefinidas

O RC não oferece suporte às macros predefinidas ANSI C (**\_ \_ Date \_ \_**, **\_ \_ File \_ \_**, **\_ \_ line \_ \_**, **\_ \_ stdc \_ \_**, **\_ \_ time \_ \_**, **\_ \_ timestamp \_ ). \_** Portanto, você não pode incluir essas macros em arquivos de cabeçalho que serão incluídas no script de recurso.

O RC define \_ o RC chamado, que permite que você compile de forma condicional partes dos arquivos de cabeçalho, dependendo se o compilador é o compilador C ou o compilador RC. Isso é importante porque o compilador RC dá suporte apenas a um subconjunto das instruções que um compilador C dará suporte.

Para compilar condicionalmente seu código com o compilador RC, envolva o código que o RC não pode compilar com \# ifndef RC \_ invocado e **\# endif**.

O exemplo a seguir é extraído das amostras do SDK. Ele demonstra como criar um arquivo de cabeçalho que pode ser compilado condicionalmente.

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




