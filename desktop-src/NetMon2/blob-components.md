---
description: Componentes de BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Componentes de BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33bd9ab8389cdd49a266855106891a91fcfbd0b4f69c7d22b5855143b34f376c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118367478"
---
# <a name="blob-components"></a>Componentes de BLOB

Um BLOB (objeto binário grande) inclui os seguintes componentes hierárquicos:

-   Proprietários
-   Categorias
-   Marcações
-   Valores

## <a name="textual-representation"></a>Representação textual

Para sua conveniência, os BLOBs aparecem no formato proprietário: Categoria: marca: valor que eles aparecem quando salvos em um arquivo. A estrutura interna do BLOB é opaca porque ele representa ponteiros e tabelas. Por exemplo, aqui está uma entrada de um BLOB que pode ser usada para configurar um NPP:

``` syntax
NPP:Configure:BufferSize=32768
```

O proprietário é NPP. A categoria é configurada, a marca é BufferSize e o valor é 32768.

 

 



