---
description: Os gravadores podem ajustar o desempenho de vários tipos de backup no nível de conjunto de arquivos, indicando por meio de um tipo de backup de especificação de arquivo, indicado por uma máscara de bits ou uma operação de bit ou de membros da \_ enumeração do tipo de backup spec do arquivo VSS \_ \_ \_ .
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Suporte a esquema de nível de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460d256a3eaa016933e697687d05e26838c14ae2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922716"
---
# <a name="file-level-schema-support"></a>Suporte a esquema de nível de arquivo

Os gravadores podem ajustar o desempenho de vários tipos de backup no nível de [*conjunto de arquivos*](vssgloss-f.md) , indicando por meio de um tipo de backup de especificação de arquivo, indicado por uma máscara de bits ou uma operação de bit ou de membros da enumeração do [**\_ \_ \_ \_ tipo de backup spec do arquivo VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) .

Para tipos de backup especificados, o gravador indica o seguinte:

-   Se será necessário fazer cópias de sombra do volume para fazer backup de um conjunto de arquivos corretamente. Por exemplo, se os arquivos em um conjunto de arquivos não forem abertos exclusivamente pelo gravador e ele puder garantir que seja estável, uma cópia de sombra não será necessária.
-   Se o solicitante precisa executar o backup de forma que, independentemente da hora da última modificação ou de outros problemas, a versão dos arquivos do conjunto de arquivo atual no backup será restaurada. Normalmente, isso significa que o conjunto de arquivos é copiado como parte do backup.

Os valores do [**\_ tipo de \_ \_ backup \_ de especificação do arquivo do VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que indicam o requisito de cópia de sombra são:

-   \_FSBT VSS \_ todos os \_ instantâneos \_ necessários
-   \_instantâneo completo do VSS FSBT \_ \_ \_ necessário
-   \_ \_ instantâneo diferencial do VSS FSBT \_ \_ necessário
-   \_instantâneo incremental do VSS FSBT \_ \_ \_ necessário
-   instantâneo de log de FSBT do VSS \_ \_ \_ \_ necessário

Os valores do [**\_ tipo de \_ \_ backup \_ de especificação do arquivo do VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que indicam a necessidade de fazer backup de um arquivo são:

-   BACKUP do VSS \_ FSBT \_ todo \_ \_ necessário
-   \_backup completo do VSS FSBT \_ \_ \_ necessário
-   \_ \_ backup diferencial do VSS FSBT \_ \_ necessário
-   \_backup incremental do VSS FSBT \_ \_ \_ necessário
-   \_backup de log FSBT do VSS \_ \_ \_ necessário

Por padrão, os conjuntos de arquivos são marcados com um tipo de backup de especificação de arquivo de VSS \_ FSBT \_ todos os \_ backups \_ necessários \| VSS \_ FSBT \_ todo o \_ instantâneo \_ necessário, o que significa que uma cópia de sombra é sempre necessária para lidar com os arquivos do conjunto de arquivos e que os arquivos devem ser copiados em todos os tipos de backup.

 

 



