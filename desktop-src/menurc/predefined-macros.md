---
title: Macros predefinidas
description: O RC não dá suporte às macros predefinida ANSI C ( \_ \_ \_ \_ DATE, \_ \_ \_ \_ FILE, \_ \_ \_ \_ LINE, \_ \_ \_ \_ STDC, TIME \_ \_ \_ \_ , \_ \_ TIMESTAMP \_ \_ ). Portanto, você não pode incluir essas macros em arquivos de header que incluirão em seu script de recurso.
ms.assetid: 2098d4a4-7c6f-4cdc-9c02-3d55907f8888
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9e48b915fae430bf776b9eebab7ac795e7b69a3d79e06a7ce6422b6d6eab6e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971945"
---
# <a name="predefined-macros"></a>Macros predefinidas

O RC não dá suporte às macros predefinida ANSI C (**\_ \_ \_ \_ DATE,** **\_ \_ \_ \_ FILE,** **\_ \_ LINE, \_ \_** **\_ \_ STDC, \_ \_** **\_ \_ TIME \_ \_**, **\_ \_ TIMESTAMP \_ \_**). Portanto, você não pode incluir essas macros em arquivos de header que incluirão em seu script de recurso.

O RC define RC INVOKED, que permite compilar condicionalmente partes de seus arquivos de header, dependendo se o compilador é o compilador C ou o \_ compilador RC. Isso é importante porque o compilador RC dá suporte apenas a um subconjunto das instruções que um compilador C dá suporte.

Para compilar condicionalmente seu código com o compilador RC, envolvem o código que o RC não pode compilar com \# ifndef RC \_ INVOKED e **\# endif**.

O exemplo a seguir é retirado dos exemplos do SDK. Ele demonstra como criar um arquivo de header que pode ser compilado condicionalmente.

``` syntax
#ifndef RC_INVOKED
#pragma message("Including CntrOutl.H from " __FILE__)
#endif
```

 

 




