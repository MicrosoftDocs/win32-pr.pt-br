---
title: Gerenciamento de memória no WOW64
description: O gerenciamento de memória sob WOW64 depende da arquitetura do processador.
ms.assetid: a3fa6e51-2895-4941-9304-5939208e8102
keywords:
- programação de Windows de 64 bits de WOW64, gerenciamento de memória
- gerenciamento de memória 64-bit Windows programação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9908c8127f4fbe15b636d7d72fd19d2d8057c1d0a0c126393bc6c182e46925f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132829"
---
# <a name="memory-management-under-wow64"></a>Gerenciamento de memória no WOW64

O gerenciamento de memória sob WOW64 depende da arquitetura do processador.

## <a name="itanium-support"></a>Suporte do Itanium

O WOW64 simula as páginas de 4 KB na parte superior das páginas nativas de 8 KB que o processador Itanium usa. O processador auxilia fornecendo uma simulação excelente com baixa sobrecarga. O código de simulação não pode lidar com os seguintes casos:

-   Controle de gravação. As funções [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) e [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) são implementadas no kernel usando a granularidade de tamanho de página nativa, o que significa que a simulação de página de 4 KB do WOW64 não pode determinar quais páginas de 4 KB simuladas são gravadas na página de 8 KB subjacente.
-   [Extensões de janela de endereço (AWE)](/windows/desktop/Memory/address-windowing-extensions). As funções de AWE operam em números de página e não há como mapear números de página de 64 bits para números de página de 32 bits.
-   Alinhamento de seção. Para imagens executáveis com alinhamento de seção menor que 8 KB (o padrão é 4 KB para imagens x86), o WOW64 deve ter sujo todas as páginas de imagem. Isso efetivamente copia cada página para o arquivo de paginação e impede que páginas de imagem somente leitura sejam compartilhadas entre processos.
-   Não há suporte para as funções [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .

## <a name="x64-and-arm64-support"></a>Suporte a x64 e ARM64

O tamanho da página nativa é de 4 KB. Portanto, há suporte para os seguintes:

-   Há suporte para as funções [**GetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-getwritewatch) e [**ResetWriteWatch**](/windows/desktop/api/memoryapi/nf-memoryapi-resetwritewatch) .
-   Há suporte para as funções [**ReadFileScatter**](/windows/desktop/api/fileapi/nf-fileapi-readfilescatter) e [**WriteFileGather**](/windows/desktop/api/fileapi/nf-fileapi-writefilegather) .
-   Há vantagens em usar endereços grandes porque o WOW64 para x64 dá suporte a um espaço de endereço virtual de 4 GB.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[limites de memória para versões de Windows](/windows/desktop/Memory/memory-limits-for-windows-releases)
</dt> <dt>

[Ajuste de RAM 4GT](/windows/desktop/Memory/4-gigabyte-tuning)
</dt> </dl>

 

 