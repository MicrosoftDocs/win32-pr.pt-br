---
description: Interfaces da API de impressão XPS
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: Interfaces da API de impressão XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47cd01c169c82a9e3210f281ec6c44fa206c40b5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105184"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="bde31-103">Interfaces da API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="bde31-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="bde31-104">\[As interfaces descritas nesta seção foram preteridas.</span><span class="sxs-lookup"><span data-stu-id="bde31-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="bde31-105">Em vez disso, os aplicativos cliente devem usar a [API de pacote de documentos de impressão](./tailored-app-printing-api.md) .\]</span><span class="sxs-lookup"><span data-stu-id="bde31-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="bde31-106">\[IXpsPrintJob não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="bde31-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bde31-107">\]</span><span class="sxs-lookup"><span data-stu-id="bde31-107">\]</span></span>

<span data-ttu-id="bde31-108">\[IXpsPrintJobStream não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="bde31-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bde31-109">\]</span><span class="sxs-lookup"><span data-stu-id="bde31-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bde31-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="bde31-110">In this section</span></span>



| <span data-ttu-id="bde31-111">Interface</span><span class="sxs-lookup"><span data-stu-id="bde31-111">Interface</span></span>                                                   | <span data-ttu-id="bde31-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="bde31-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bde31-113">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="bde31-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="bde31-114">Fornece acesso a um trabalho de impressão que está atualmente em andamento.</span><span class="sxs-lookup"><span data-stu-id="bde31-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="bde31-115">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="bde31-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="bde31-116">Uma interface de fluxo somente gravação na qual um aplicativo grava dados de trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="bde31-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="bde31-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bde31-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bde31-118">Documentos</span><span class="sxs-lookup"><span data-stu-id="bde31-118">Documents</span></span>](./jobbindalldocuments.md)
</dt> <dt>

[<span data-ttu-id="bde31-119">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="bde31-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

