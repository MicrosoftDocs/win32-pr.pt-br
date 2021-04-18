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
# <a name="ice39"></a><span data-ttu-id="89060-103">ICE39</span><span class="sxs-lookup"><span data-stu-id="89060-103">ICE39</span></span>

<span data-ttu-id="89060-104">ICE39 valida o [fluxo de informações de resumo](summary-information-stream.md) do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="89060-104">ICE39 validates the [Summary Information Stream](summary-information-stream.md) of the database.</span></span>

<span data-ttu-id="89060-105">ICE39 verifica o formato das seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="89060-105">ICE39 checks the format of the following properties:</span></span>

-   [<span data-ttu-id="89060-106">**Resumo de contagem de palavras**</span><span class="sxs-lookup"><span data-stu-id="89060-106">**Word Count Summary**</span></span>](word-count-summary.md)
-   [<span data-ttu-id="89060-107">**Resumo de contagem de páginas**</span><span class="sxs-lookup"><span data-stu-id="89060-107">**Page Count Summary**</span></span>](page-count-summary.md)
-   [<span data-ttu-id="89060-108">**Resumo do modelo**</span><span class="sxs-lookup"><span data-stu-id="89060-108">**Template Summary**</span></span>](template-summary.md)
-   [<span data-ttu-id="89060-109">**Resumo do número de revisão**</span><span class="sxs-lookup"><span data-stu-id="89060-109">**Revision Number Summary**</span></span>](revision-number-summary.md)
-   [<span data-ttu-id="89060-110">**Criar Resumo de data/hora**</span><span class="sxs-lookup"><span data-stu-id="89060-110">**Create Time/Date Summary**</span></span>](create-time-date-summary.md)
-   [<span data-ttu-id="89060-111">**Resumo de data/hora do último salvamento**</span><span class="sxs-lookup"><span data-stu-id="89060-111">**Last Saved Time/Date Summary**</span></span>](last-saved-time-date-summary.md)
-   [<span data-ttu-id="89060-112">**Último Resumo impresso**</span><span class="sxs-lookup"><span data-stu-id="89060-112">**Last Printed Summary**</span></span>](last-printed-summary.md)

<span data-ttu-id="89060-113">Se a propriedade de [**Resumo contagem de palavras**](word-count-summary.md) especificar que a origem está compactada, o ICE39 lançará um aviso se algum arquivo também estiver marcado como compactado na coluna atributos da [tabela de arquivos](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="89060-113">If the [**Word Count Summary**](word-count-summary.md) Property specifies that the source is compressed, ICE39 posts a warning if any files are also marked as compressed in the Attributes column of the [File table](file-table.md).</span></span> <span data-ttu-id="89060-114">Consulte [usando gabinetes e fontes compactadas](using-cabinets-and-compressed-sources.md).</span><span class="sxs-lookup"><span data-stu-id="89060-114">See [Using Cabinets and Compressed Sources](using-cabinets-and-compressed-sources.md).</span></span>

<span data-ttu-id="89060-115">ICE39 posta um aviso se a propriedade de [**Resumo de contagem de palavras**](word-count-summary.md) especifica que o pacote é compatível com o UAC e a [tabela MsiPackageCertificate](msipackagecertificate-table.md) não está vazia.</span><span class="sxs-lookup"><span data-stu-id="89060-115">ICE39 posts a warning if the [**Word Count Summary**](word-count-summary.md) Property specifies that the package is UAC compliant and the [MsiPackageCertificate Table](msipackagecertificate-table.md) is not empty.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89060-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89060-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89060-117">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="89060-117">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



