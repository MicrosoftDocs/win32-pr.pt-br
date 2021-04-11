---
title: Identificadores de formato
description: Os valores do conjunto de propriedades são armazenados em uma seção marcada com um FMTID exclusivo.
ms.assetid: 3ffb6c5e-72ce-4769-847a-72db6f145d61
keywords:
- Identificadores de formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0202cd1287c3b4fef6e9e2b56e272541a03425b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292075"
---
# <a name="format-identifiers"></a>Identificadores de formato

Os valores do conjunto de propriedades são armazenados em uma seção marcada com um FMTID exclusivo. Por exemplo, o FMTID para o conjunto de propriedades de informações de resumo COM é **F29F85E0-4FF9-1068-AB91-08002B27B3D9**.

Para definir um FMTID para o conjunto de propriedades de informações de resumo, use a macro **definir \_ GUID** em um arquivo de inclusão para o código que manipula o conjunto de propriedades.


```C++
DEFINE_GUID(FMTID_SummaryInformation, 0xF29F85E0, 0x4FF9, 0x1068, 
0xAB, 0x91, 0x08, 0x00, 0x2B, 0x27, 0xB3, 0xD9);
```



Qualquer código que exija o FMTID para o conjunto de propriedades de informações resumidas pode acessá-lo por meio da variável *\_ SummaryInformation do FMTID* .

Ao armazenar conjuntos de propriedades em instâncias [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , converta o FMTID em um nome de cadeia de caracteres para o objeto de armazenamento.

 

 




