---
description: ICE39 valida o fluxo de informações de resumo do banco de dados.
ms.assetid: 9de72de6-fd9c-4d94-92f7-61b85dff0f6a
title: ICE39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e72e7b4a73f3a134ec108b07666cc1c4e9af23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752258"
---
# <a name="ice39"></a>ICE39

ICE39 valida o [fluxo de informações de resumo](summary-information-stream.md) do banco de dados.

ICE39 verifica o formato das seguintes propriedades:

-   [**Resumo de contagem de palavras**](word-count-summary.md)
-   [**Resumo de contagem de páginas**](page-count-summary.md)
-   [**Resumo do modelo**](template-summary.md)
-   [**Resumo do número de revisão**](revision-number-summary.md)
-   [**Criar Resumo de data/hora**](create-time-date-summary.md)
-   [**Resumo de data/hora do último salvamento**](last-saved-time-date-summary.md)
-   [**Último Resumo impresso**](last-printed-summary.md)

Se a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) especificar que a origem está compactada, o ICE39 lançará um aviso se algum arquivo também estiver marcado como compactado na coluna atributos da [tabela de arquivos](file-table.md). Consulte [usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).

ICE39 posta um aviso se a propriedade de [**Resumo de contagem de palavras**](word-count-summary.md) especifica que o pacote é compatível com o UAC e a [tabela MsiPackageCertificate](msipackagecertificate-table.md) não está vazia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



