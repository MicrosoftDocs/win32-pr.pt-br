---
title: Incrementando a contagem de referência do manipulador
description: Incrementando a contagem de referência do manipulador
ms.assetid: 9e71ce1f-5805-4240-9dcc-7e71fbabfe7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 767efbd97525be49c0cf4604d2b90d068a2b81d78589627bf0654f3048e03548
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690586"
---
# <a name="incrementing-the-handler-reference-count"></a>Incrementando a contagem de referência do manipulador

O **método AddRef** incrementa a contagem de referência do manipulador de arquivos ou stream-hander.


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::AddRef() 
{ 
    return ++m_refs; 
} 

```



 

 




