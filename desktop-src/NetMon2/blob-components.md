---
description: Componentes de BLOB
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: Componentes de BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170662"
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

 

 



