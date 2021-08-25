---
description: Os autores podem ajustar o desempenho de vários tipos de backup no nível do conjunto de arquivos indicando por meio de um tipo de backup de especificação de arquivo, indicado por uma máscara de bit ou OR bit a bit dos membros da enumeração TIPO de BACKUP DE ESPECIFICAÇÃO DE ARQUIVO \_ \_ \_ \_ VSS.
ms.assetid: a3ac69b4-894a-4536-8fab-f45ad7e5118a
title: Suporte ao esquema no nível do arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 550885a540e62fc145541bae979fad34cb9488f62f9f26ea17e647068c1fad46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006365"
---
# <a name="file-level-schema-support"></a>Suporte ao esquema no nível do arquivo

Os autores podem ajustar o desempenho de [](vssgloss-f.md) vários tipos de backup no nível do conjunto de arquivos indicando por meio de um tipo de backup de especificação de arquivo, indicado por uma máscara de bit ou OR bit a bit dos membros da enumeração TIPO de BACKUP DE [**\_ \_ \_ ESPECIFICAÇÃO \_**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) DE ARQUIVO VSS.

Para tipos de backup especificados, o autor indica o seguinte:

-   Se será necessário copiar o volume de sombra para fazer o back-up correto de um conjunto de arquivos. Por exemplo, se os arquivos em um conjunto de arquivos não são abertos exclusivamente pelo autor e podem garantir que ele seja estável, uma cópia de sombra não será necessária.
-   Se o solicitante precisa executar o backup de forma que, independentemente da hora da última modificação ou de outros problemas, a versão dos arquivos do conjunto de arquivos atual no backup será restaurada. Normalmente, isso significa que o conjunto de arquivos é copiado como parte do backup.

Os valores de [**TIPO DE BACKUP DE \_ \_ ESPECIFICAÇÃO \_ \_ DE ARQUIVO DO VSS que**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) indicam o requisito de cópia de sombra são:

-   VSS \_ FSBT \_ TODOS OS \_ \_ INSTANTÂNEOS NECESSÁRIOS
-   INSTANTÂNEO COMPLETO DO VSS \_ FSBT \_ \_ \_ NECESSÁRIO
-   INSTANTÂNEO \_ DIFERENCIAL DO VSS FSBT \_ \_ \_ NECESSÁRIO
-   INSTANTÂNEO \_ INCREMENTAL DO VSS FSBT \_ \_ \_ NECESSÁRIO
-   INSTANTÂNEO DE \_ LOG DO VSS FSBT \_ \_ \_ NECESSÁRIO

Os valores de [**TIPO DE BACKUP DE \_ \_ \_ ESPECIFICAÇÃO \_ DE ARQUIVO DO VSS**](/windows/desktop/api/Vss/ne-vss-vss_file_spec_backup_type) que indicam o requisito para fazer backup de um arquivo são:

-   VSS \_ FSBT \_ TODO O BACKUP \_ \_ NECESSÁRIO
-   BACKUP COMPLETO DO VSS \_ FSBT \_ \_ \_ NECESSÁRIO
-   BACKUP \_ DIFERENCIAL DO VSS FSBT \_ \_ \_ NECESSÁRIO
-   BACKUP INCREMENTAL DO VSS \_ FSBT \_ \_ \_ NECESSÁRIO
-   BACKUP DE LOG DO VSS \_ FSBT \_ \_ \_ NECESSÁRIO

Por padrão, os conjuntos de arquivos são marcados com um tipo de backup de especificação de arquivo do \_ VSS FSBT \_ ALL BACKUP \_ \_ \| REQUIRED \_ VSS FSBT \_ ALL SNAPSHOT \_ \_ REQUIRED, o que significa que uma cópia de sombra sempre é necessária para lidar com os arquivos do conjunto de arquivos e que os arquivos devem ser copiados em todos os tipos de backup.

 

 



