---
description: Use esta diretriz para Windows pacote do instalador que contém mais de 32767 arquivos.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Como autor de um pacote grande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d55f7933fe600bd6c0db0705328f18d7eae2f55e3463e3ea03be8118229eca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996876"
---
# <a name="authoring-a-large-package"></a>Como autor de um pacote grande

Use esta diretriz para Windows pacote do instalador que contém mais de 32767 arquivos.

Se o pacote Windows Instalador do Windows contiver mais de 32767 arquivos, você deverá alterar o esquema do banco de dados para aumentar o limite das seguintes colunas:

-   A coluna Sequência da [tabela Arquivo](file-table.md).
-   A coluna LastSequence da tabela [Mídia](media-table.md).
-   A coluna Sequência da tabela [Patch](patch-table.md).

Para obter mais informações, consulte [Formato de definição de coluna](column-definition-format.md).

**Para aumentar o limite de uma coluna de banco de dados**

1.  Exporte a tabela para um arquivo .idt. Para obter detalhes, [ consulteMsidb.exe](msidb-exe.md), [Exportar arquivos](export-files.md)e [Importando e exportando](importing-and-exporting.md).
2.  Edite o arquivo .idt para alterar o tipo de coluna de i2 para i4 ou de I2 para I4.
3.  Exporte [ \_ a tabela](-validation-table.md) Validação para um arquivo .idt.
4.  Edite o arquivo .idt para alterar os valores na coluna MaxValue da tabela [ \_ Validation](-validation-table.md) para acomodar as larguras de coluna aumentadas.
5.  Importe os arquivos .idt de volta para o banco de dados.

Observe que as transformação e patches não podem ser criados entre dois pacotes com tipos de coluna diferentes.

 

 



