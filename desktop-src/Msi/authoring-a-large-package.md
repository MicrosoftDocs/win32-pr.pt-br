---
description: Use esta diretriz para criar um pacote Windows Installer que contenha mais de 32767 arquivos.
ms.assetid: 3145629f-cc0a-4216-8549-76bb61070772
title: Criando um pacote grande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca09c427336e4ca8a17fd8ebdf803f52ebe6c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754650"
---
# <a name="authoring-a-large-package"></a>Criando um pacote grande

Use esta diretriz para criar um pacote Windows Installer que contenha mais de 32767 arquivos.

Se seu pacote de Windows Installer contiver mais de 32767 arquivos, você deverá alterar o esquema do banco de dados para aumentar o limite das seguintes colunas:

-   A coluna sequence da [tabela de arquivos](file-table.md).
-   A coluna LastSequence da [tabela de mídia](media-table.md).
-   A coluna sequence da [tabela patch](patch-table.md).

Para obter mais informações, consulte [formato de definição de coluna](column-definition-format.md).

**Para aumentar o limite de uma coluna de banco de dados**

1.  Exporte a tabela para um arquivo. IDT. Para obter detalhes, consulte [Msidb.exe](msidb-exe.md), [exportar arquivos](export-files.md)e [importar e exportar](importing-and-exporting.md).
2.  Edite o arquivo. IDT para alterar o tipo de coluna de i2 para I4 ou de i2 para i4.
3.  Exporte a tabela de [ \_ validação](-validation-table.md) para um arquivo. IDT.
4.  Edite o arquivo. IDT para alterar os valores na coluna MaxValue da tabela de [ \_ validação](-validation-table.md) para acomodar as larguras de coluna aumentadas.
5.  Importe os arquivos. IDT de volta para o banco de dados.

Observe que as transformações e os patches não podem ser criados entre dois pacotes com tipos de coluna diferentes.

 

 



