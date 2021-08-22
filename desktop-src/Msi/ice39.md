---
description: ICE39 valida o Fluxo de Informações resumidas do banco de dados.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb912afbe7220eee1aa3bbcd494f6531736279b85c5736f6867fdf8779e39bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528436"
---
# <a name="ice39"></a>ICE39

ICE39 valida o Fluxo [de Informações resumidas](summary-information-stream.md) do banco de dados.

ICE39 verifica o formato das seguintes propriedades:

-   [**Resumo da contagem de palavras**](word-count-summary.md)
-   [**Resumo da contagem de páginas**](page-count-summary.md)
-   [**Resumo do modelo**](template-summary.md)
-   [**Resumo do número de revisão**](revision-number-summary.md)
-   [**Criar resumo de data/hora**](create-time-date-summary.md)
-   [**Resumo da data/hora da última salva**](last-saved-time-date-summary.md)
-   [**Resumo da Última Impressa**](last-printed-summary.md)

Se a [**propriedade Resumo**](word-count-summary.md) da Contagem de Palavras especificar que a origem está compactada, o ICE39 postará um aviso se algum arquivo também estiver marcado como compactado na coluna Atributos da [tabela Arquivo](file-table.md). Consulte [Usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).

ICE39 postará um aviso se a propriedade Resumo da Contagem de [**Palavras**](word-count-summary.md) especificar que o pacote é compatível com UAC e a [Tabela MsiPackageCertificate](msipackagecertificate-table.md) não estiver vazia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



