---
title: Incrementando a contagem de referência do manipulador
description: Incrementando a contagem de referência do manipulador
ms.assetid: 9e71ce1f-5805-4240-9dcc-7e71fbabfe7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a990f2570fca0057156a39a955930cca2d71858
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006006"
---
# <a name="incrementing-the-handler-reference-count"></a>Incrementando a contagem de referência do manipulador

O método **AddRef** incrementa a contagem de referência de fluxo ou de controle de arquivo.


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::AddRef() 
{ 
    return ++m_refs; 
} 

```



 

 




