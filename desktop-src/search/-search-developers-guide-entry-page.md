---
description: Terceiros podem criar aplicativos que consultam o índice em busca de dados programaticamente e podem estender o Windows Search para indexar dados de formatos de arquivo personalizados e armazenamentos de dados.
ms.assetid: 70046df0-ce48-472d-b24b-8231ea3a43c0
title: Guia do desenvolvedor do Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61593f47e081059966936a99a7d2baea114df92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460990"
---
# <a name="windows-search-developers-guide"></a><span data-ttu-id="4f156-103">Guia do desenvolvedor do Windows Search</span><span class="sxs-lookup"><span data-stu-id="4f156-103">Windows Search Developer's Guide</span></span>

<span data-ttu-id="4f156-104">Terceiros podem criar aplicativos que consultam o índice em busca de dados programaticamente e podem estender o Windows Search para indexar dados de formatos de arquivo personalizados e armazenamentos de dados.</span><span class="sxs-lookup"><span data-stu-id="4f156-104">Third parties can create applications that query the index for data programmatically and can extend Windows Search to index data from custom file formats and data stores.</span></span> <span data-ttu-id="4f156-105">Para criar aplicativos de pesquisa do Windows, os desenvolvedores de terceiros devem primeiro implementar um armazenamento de dados do Shell para obter uma experiência de usuário razoável.</span><span class="sxs-lookup"><span data-stu-id="4f156-105">To create Windows Search applications, third-party developers must first implement a Shell data store to a achieve a reasonable user experience.</span></span> <span data-ttu-id="4f156-106">Para obter mais informações, consulte [implementando as interfaces de objeto de pasta básica](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4f156-106">For more information, see [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).</span></span>

<span data-ttu-id="4f156-107">Você também deve baixar o [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) para as bibliotecas de pesquisa do Windows.</span><span class="sxs-lookup"><span data-stu-id="4f156-107">You must also download the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) for the Windows Search libraries.</span></span> <span data-ttu-id="4f156-108">Os [exemplos do SDK do Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contêm exemplos de código úteis e um assembly de interoperabilidade para o desenvolvimento com código gerenciado.</span><span class="sxs-lookup"><span data-stu-id="4f156-108">The [Windows Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8) contains useful code samples and an interopability assembly for developing with managed code.</span></span> <span data-ttu-id="4f156-109">Para obter mais informações sobre como usar os exemplos de código, consulte [exemplos de código do Windows Search](-search-3x-wds-sampleentry.md).</span><span class="sxs-lookup"><span data-stu-id="4f156-109">For more information on using the code samples, see [Windows Search Code Samples](-search-3x-wds-sampleentry.md).</span></span>

<span data-ttu-id="4f156-110">Esta seção é organizada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4f156-110">This section is organized as follows:</span></span>

- [<span data-ttu-id="4f156-111">Gerenciar o índice</span><span class="sxs-lookup"><span data-stu-id="4f156-111">Managing the Index</span></span>](-search-3x-wds-mngidx-overview.md)
- [<span data-ttu-id="4f156-112">Consulta do índice de maneira programática</span><span class="sxs-lookup"><span data-stu-id="4f156-112">Querying the Index Programmatically</span></span>](-search-3x-wds-qryidx-overview.md)
- [<span data-ttu-id="4f156-113">Estendendo o índice</span><span class="sxs-lookup"><span data-stu-id="4f156-113">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
- [<span data-ttu-id="4f156-114">Estendendo recursos de idioma</span><span class="sxs-lookup"><span data-stu-id="4f156-114">Extending Language Resources</span></span>](extending-language-resources-in-windows-search.md)

## <a name="additional-resources"></a><span data-ttu-id="4f156-115">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="4f156-115">Additional Resources</span></span>

- <span data-ttu-id="4f156-116">Para ver os quadros de mensagens de perguntas e discussões com suporte da Comunidade em tecnologias de pesquisa, consulte [Fórum do MSDN: desenvolvimento do Windows Desktop Search](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span><span class="sxs-lookup"><span data-stu-id="4f156-116">For community-supported question and discussion message boards on Search technologies, see [MSDN Forum: Windows Desktop Search Development](https://social.msdn.microsoft.com/Forums/windowsdesktopsearchdevelopment/threads).</span></span>
- <span data-ttu-id="4f156-117">Para baixar os exemplos de código de pesquisa:</span><span class="sxs-lookup"><span data-stu-id="4f156-117">To download the Search Code Samples:</span></span>
  - [<span data-ttu-id="4f156-118">Exemplos do Windows Search</span><span class="sxs-lookup"><span data-stu-id="4f156-118">Windows Search Samples</span></span>](-search-samples-ovw.md)
- <span data-ttu-id="4f156-119">Para baixar o SDK do Windows:</span><span class="sxs-lookup"><span data-stu-id="4f156-119">To download the Windows SDK:</span></span>
  - <span data-ttu-id="4f156-120">Para Windows 10: [SDK do Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span><span class="sxs-lookup"><span data-stu-id="4f156-120">For Windows 10: [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk)</span></span>
  - <span data-ttu-id="4f156-121">Para o Windows 7: [SDK do Windows para Windows 7 e .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span><span class="sxs-lookup"><span data-stu-id="4f156-121">For Windows 7: [Windows SDK for Windows 7 and .NET Framework](https://msdn.microsoft.com/windowsvista/bb980924.aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f156-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4f156-122">Related topics</span></span>

[<span data-ttu-id="4f156-123">Visão geral do Windows Search</span><span class="sxs-lookup"><span data-stu-id="4f156-123">Windows Search Overview</span></span>](-search-3x-wds-overview.md)

[<span data-ttu-id="4f156-124">Referência do Windows Search</span><span class="sxs-lookup"><span data-stu-id="4f156-124">Windows Search Reference</span></span>](-search-reference-entry-page.md)

[<span data-ttu-id="4f156-125">Exemplos de código do Windows Search</span><span class="sxs-lookup"><span data-stu-id="4f156-125">Windows Search Code Samples</span></span>](-search-samples-ovw.md)

[<span data-ttu-id="4f156-126">Pesquisa federada no Windows</span><span class="sxs-lookup"><span data-stu-id="4f156-126">Federated Search in Windows</span></span>](-search-federated-search-overview.md)

[<span data-ttu-id="4f156-127">Tecnologias de pesquisa relacionadas</span><span class="sxs-lookup"><span data-stu-id="4f156-127">Related Search Technologies</span></span>](-search-3x-wds-sampleentry.md)

[<span data-ttu-id="4f156-128">Glossário do Windows Search</span><span class="sxs-lookup"><span data-stu-id="4f156-128">Windows Search Glossary</span></span>](search-glossary.md)
