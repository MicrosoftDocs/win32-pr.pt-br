---
title: Identificadores de formato
description: Os valores do conjunto de propriedades são armazenados em uma seção marcada com um FMTID exclusivo.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Identificadores de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ec9e9843b1dfe843e89ebf85eadbbcb5da8cb58dfc1b289eb88c844aae7456
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663146"
---
# <a name="format-identifiers"></a>Identificadores de formato

Os valores do conjunto de propriedades são armazenados em uma seção marcada com um FMTID exclusivo. Por exemplo, o FMTID para o conjunto de propriedades informações de resumo COM é **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.

Para definir um FMTID para o conjunto de propriedades Informações resumidas, use a macro **\_ DEFINE GUID** em um arquivo de inclusão para o código que manipula o conjunto de propriedades.


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



Qualquer código que exija o FMTID para o conjunto de propriedades Informações resumidas pode acessá-lo por meio da *variável FMTID \_ SummaryInformation.*

Ao armazenar conjuntos de propriedades em [**instâncias de IStorage,**](/windows/desktop/api/Objidl/nn-objidl-istorage) converta o FMTID em um nome de cadeia de caracteres para o objeto de armazenamento.

 

 




