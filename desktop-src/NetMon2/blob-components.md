---
description: Componentes blob
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Componentes blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bd9ab8389cdd49a266855106891a91fcfbd0b4f69c7d22b5855143b34f376c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367478"
---
# <a name="blob-components"></a>Componentes blob

Um BLOB (objeto binário grande) inclui os seguintes componentes hierárquicos:

-   Proprietários
-   Categorias
-   Marcações
-   Valores

## <a name="textual-representation"></a>Representação textual

Para sua conveniência, os BLOBs aparecem no formato Owner:Category:Tag:Value em que aparecem quando salvos em um arquivo. A estrutura interna do BLOB é opaca porque representa ponteiros e tabelas. Por exemplo, aqui está uma entrada de um BLOB que pode ser usada para configurar um NPP:

``` syntax
NPP:Configure:BufferSize=32768
```

O Proprietário é NPP. A Categoria é Configurar, a Marca é BufferSize e o Valor é 32768.

 

 



