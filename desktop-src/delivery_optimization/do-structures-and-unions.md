---
title: FAZER estruturas e uniões
description: As interfaces de otimização de entrega (do) usam as seguintes estruturas.
ms.assetid: 58A5361E-871A-4911-85BD-83F18CB9A2F5
ms.topic: article
ms.date: 07/03/2019
ms.openlocfilehash: 860672e72e1e5f134382fd46cd9b36d1d411361e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084732"
---
# <a name="do-structures-and-unions"></a>FAZER estruturas e uniões

As [interfaces](do-interfaces.md) de otimização de entrega (do) usam as seguintes estruturas.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [**BG_FILE_PROGRESS**](bg-file-progress.md) | A estrutura de **BG_FILE_PROGRESS** fornece informações de progresso relacionadas a arquivos, como o número de bytes transferidos. |
| [**BG_FILE_RANGE**](bg-file-range.md) | A estrutura de **BG_FILE_RANGE** identifica um intervalo de bytes para baixar de um arquivo. |
| [**BG_JOB_PROGRESS**](bg-job-progress.md) | A estrutura de **BG_JOB_PROGRESS** fornece informações de progresso relacionadas ao trabalho, como o número de bytes e arquivos transferidos. Para trabalhos de carregamento, o progresso se aplica ao arquivo de carregamento, não ao arquivo de resposta.  |
| [**BG_JOB_TIMES**](bg-job-times.md) | A estrutura de **BG_JOB_TIMES** fornece carimbos de data/hora relacionados ao trabalho. |
| [**BITS_FILE_PROPERTY_VALUE**](bits-file-property-value.md) | A **BITS_FILE_PROPERTY_VALUE** Union fornece o valor da Propriedade do arquivo do com base em um valor da enumeração [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) . |
| [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) | A **BITS_JOB_PROPERTY_VALUE** Union fornece o valor da propriedade da função do trabalho com base no valor da enumeração [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) . |
| [**DO_DOWNLOAD_ENUM_CATEGORY**](./do/ns-do-do_download_enum_category.md) | Usado por **IDOManager:: EnumDownloads** para filtrar a enumeração de downloads pelo valor da propriedade específica. |
| [**DO_DOWNLOAD_RANGE**](./deliveryoptimizationdownloadtypes/ns-deliveryoptimizationdownloadtypes-do_download_range.md) | Identifica um único intervalo de bytes para baixar de um arquivo. |
| [**DO_DOWNLOAD_RANGE_INFO**](./do/ns-do-do_download_range_info.md) | Identifica uma matriz de intervalos de bytes a serem baixados de um arquivo. |
| [**DO_DOWNLOAD_STATUS**](./do/ns-do-do_download_status.md) | Usado para obter o status de um download específico. |
| [**DOSwarmStats**](doswarmstats.md) | Contém campos para baixar e carregar estatísticas para um arquivo. |