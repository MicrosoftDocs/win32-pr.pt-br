---
description: .
ms.assetid: f575109e-e9c4-4db5-945c-7c96b6b5d613
title: Interfaces da API de impressão XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 828e999417354678d77ad1de8c29beb5956f7762
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661810"
---
# <a name="xps-print-api-interfaces"></a><span data-ttu-id="616bd-103">Interfaces da API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="616bd-103">XPS Print API Interfaces</span></span>

<span data-ttu-id="616bd-104">\[As interfaces descritas nesta seção foram preteridas.</span><span class="sxs-lookup"><span data-stu-id="616bd-104">\[The interfaces described in this section are deprecated.</span></span> <span data-ttu-id="616bd-105">Em vez disso, os aplicativos cliente devem usar a [API de pacote de documentos de impressão](./tailored-app-printing-api.md) .\]</span><span class="sxs-lookup"><span data-stu-id="616bd-105">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="616bd-106">\[IXpsPrintJob não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="616bd-106">\[IXpsPrintJob is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="616bd-107">\]</span><span class="sxs-lookup"><span data-stu-id="616bd-107">\]</span></span>

<span data-ttu-id="616bd-108">\[IXpsPrintJobStream não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="616bd-108">\[IXpsPrintJobStream is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="616bd-109">\]</span><span class="sxs-lookup"><span data-stu-id="616bd-109">\]</span></span>

## <a name="in-this-section"></a><span data-ttu-id="616bd-110">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="616bd-110">In this section</span></span>



| <span data-ttu-id="616bd-111">Interface</span><span class="sxs-lookup"><span data-stu-id="616bd-111">Interface</span></span>                                                   | <span data-ttu-id="616bd-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="616bd-112">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="616bd-113">**IXpsPrintJob**</span><span class="sxs-lookup"><span data-stu-id="616bd-113">**IXpsPrintJob**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjob)<br/>             | <span data-ttu-id="616bd-114">Fornece acesso a um trabalho de impressão que está atualmente em andamento.</span><span class="sxs-lookup"><span data-stu-id="616bd-114">Provides access to a print job that is currently in progress.</span></span><br/>                  |
| [<span data-ttu-id="616bd-115">**IXpsPrintJobStream**</span><span class="sxs-lookup"><span data-stu-id="616bd-115">**IXpsPrintJobStream**</span></span>](/windows/desktop/api/XpsPrint/nn-xpsprint-ixpsprintjobstream)<br/> | <span data-ttu-id="616bd-116">Uma interface de fluxo somente gravação na qual um aplicativo grava dados de trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="616bd-116">A write-only stream interface into which an application writes print job data.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="616bd-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="616bd-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="616bd-118">Documentos</span><span class="sxs-lookup"><span data-stu-id="616bd-118">Documents</span></span>](./jobbindalldocuments.md)
</dt> <dt>

[<span data-ttu-id="616bd-119">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="616bd-119">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

