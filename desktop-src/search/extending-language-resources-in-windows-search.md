---
description: O Windows Search usa recursos de idioma como separadores de palavras e lematizadores para quebrar o texto em sua localidade nativa durante a criação do índice e o processamento de consultas.
ms.assetid: 6e8ab091-c22c-4425-b8b9-211d53816304
title: Estendendo recursos de idioma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 727f5812d0aee370c96d98f1c57dfffcbea5bc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765101"
---
# <a name="extending-language-resources"></a><span data-ttu-id="595a6-103">Estendendo recursos de idioma</span><span class="sxs-lookup"><span data-stu-id="595a6-103">Extending Language Resources</span></span>

<span data-ttu-id="595a6-104">O Windows Search usa recursos de idioma como separadores de palavras e lematizadores para quebrar o texto em sua localidade nativa durante a criação do índice e o processamento de consultas.</span><span class="sxs-lookup"><span data-stu-id="595a6-104">Windows Search uses language resources such as word breakers and stemmers to break text in its native locale during index creation and query processing.</span></span> <span data-ttu-id="595a6-105">A Microsoft fornece separadores de palavras e lematizadores para vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="595a6-105">Microsoft provides word breakers and stemmers for several languages.</span></span> <span data-ttu-id="595a6-106">Esta seção descreve como implementar e usar separadores de palavras e lematizadores personalizados para idiomas e localidades além daqueles fornecidos pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="595a6-106">This section describes how to implement and use custom word breakers and stemmers for languages and locales beyond those provided by Microsoft.</span></span>

-   [<span data-ttu-id="595a6-107">Noções básicas sobre componentes de recursos de idioma</span><span class="sxs-lookup"><span data-stu-id="595a6-107">Understanding Language Resource Components</span></span>](understanding-language-resource-components.md)
-   [<span data-ttu-id="595a6-108">Implementando um separador de palavras e lematizador</span><span class="sxs-lookup"><span data-stu-id="595a6-108">Implementing a Word Breaker and Stemmer</span></span>](implementing-a-word-breaker-and-stemmer.md)
-   [<span data-ttu-id="595a6-109">Considerações lingüísticas e Unicode</span><span class="sxs-lookup"><span data-stu-id="595a6-109">Linguistic and Unicode Considerations</span></span>](linguistic-and-unicode-considerations.md)
-   [<span data-ttu-id="595a6-110">Solucionando problemas de recursos de idioma e práticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="595a6-110">Troubleshooting Language Resources and Best Practices</span></span>](troubleshooting-language-resources.md)

## <a name="additional-resources"></a><span data-ttu-id="595a6-111">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="595a6-111">Additional Resources</span></span>

-   <span data-ttu-id="595a6-112">Para obter uma lista de lanuages com suporte de separadores de palavras, consulte [idiomas com suporte do Windows Search](-search-3x-wds-language-support.md).</span><span class="sxs-lookup"><span data-stu-id="595a6-112">For a list of lanuages supported by word breakers, see [Languages Supported by Windows Search](-search-3x-wds-language-support.md).</span></span>
-   <span data-ttu-id="595a6-113">Se você precisar identificar o idioma de uma parte do texto, poderá usar a detecção automática de idioma (LAD), que está disponível no Windows 7 e posterior.</span><span class="sxs-lookup"><span data-stu-id="595a6-113">If you need to identify the language of a piece of text, you can use Language Auto-Detection (LAD), which is available in Windows 7 and later.</span></span> <span data-ttu-id="595a6-114">Para obter mais informações, consulte Els ( [Serviços lingüísticos estendidos](../intl/extended-linguistic-services.md) ).</span><span class="sxs-lookup"><span data-stu-id="595a6-114">For more information, see [Extended Linguistic Services](../intl/extended-linguistic-services.md) (ELS).</span></span>
-   <span data-ttu-id="595a6-115">Para obter a documentação de referência aplicável, consulte [interfaces de suplemento de dados](-search-data-addins-interfaces-entry-page.md).</span><span class="sxs-lookup"><span data-stu-id="595a6-115">For applicable reference documentation, see [Data Add-in Interfaces](-search-data-addins-interfaces-entry-page.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="595a6-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="595a6-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="595a6-117">Gerenciar o índice</span><span class="sxs-lookup"><span data-stu-id="595a6-117">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
</dt> <dt>

[<span data-ttu-id="595a6-118">Consulta do índice de maneira programática</span><span class="sxs-lookup"><span data-stu-id="595a6-118">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[<span data-ttu-id="595a6-119">Estendendo o índice</span><span class="sxs-lookup"><span data-stu-id="595a6-119">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
