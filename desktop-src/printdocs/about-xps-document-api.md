---
description: A API de documento XPS implementa o modelo de objeto XPS e permite que os desenvolvedores criem um OM XPS, manipulem conteúdo de documento XPS em programas nativos do Windows \\ \\ e salvem o OM XPS em um arquivo ou fluxo como um documento XPS.
ms.assetid: dbb48dae-1ee6-4a8b-9184-8b796755087e
title: Sobre a API de documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e24a93061b7f09697a987aa83be121dac42703c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770621"
---
# <a name="about-xps-document-api"></a><span data-ttu-id="64d93-103">Sobre a API de documento XPS</span><span class="sxs-lookup"><span data-stu-id="64d93-103">About XPS Document API</span></span>

<span data-ttu-id="64d93-104">A [API de documento XPS](documents-xps.md) implementa o modelo de objeto XPS e permite que os desenvolvedores criem um om XPS, manipulem conteúdo de documento XPS em programas nativos do Windows \\ \\ e salvem o OM XPS em um arquivo ou fluxo como um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="64d93-104">The [XPS Document API](documents-xps.md) implements the XPS object model and enables developers to create an XPS OM, manipulate XPS document content in native Windows \\\\ programs, and save the XPS OM to a file or stream as an XPS document.</span></span> <span data-ttu-id="64d93-105">Os desenvolvedores de módulos de pipeline de filtro XPSDrv também podem usar a API de documento XPS para manipular o conteúdo do documento XPS em um filtro de driver de impressora XPSDrv.</span><span class="sxs-lookup"><span data-stu-id="64d93-105">Developers of XPSDrv filter pipeline modules can also use the XPS Document API to manipulate XPS document content in an XPSDrv printer driver filter.</span></span>

## <a name="xps-document-api-overview"></a><span data-ttu-id="64d93-106">Visão geral da API de documento XPS</span><span class="sxs-lookup"><span data-stu-id="64d93-106">XPS Document API Overview</span></span>

<span data-ttu-id="64d93-107">O modelo de objeto XPS é o modelo de informações de um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="64d93-107">The XPS object model is the information model of an XPS document.</span></span> <span data-ttu-id="64d93-108">O modelo de informações do documento XPS é separado do modelo de marcação que é usado dentro das partes do documento.</span><span class="sxs-lookup"><span data-stu-id="64d93-108">The information model of the XPS document is separate from the markup model that is used inside the document parts.</span></span> <span data-ttu-id="64d93-109">O modelo de objeto XPS descreve a organização dos componentes internos que compõem um documento XPS e o modelo de marcação descreve o conteúdo desses componentes.</span><span class="sxs-lookup"><span data-stu-id="64d93-109">The XPS object model describes the organization of the internal components that make up an XPS document, and the markup model describes the contents of those components.</span></span>

<span data-ttu-id="64d93-110">Em um programa, o modelo de objeto XPS é instanciado como um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="64d93-110">In a program, the XPS object model is instantiated as an XPS OM.</span></span> <span data-ttu-id="64d93-111">O OM XPS é essencialmente uma versão na memória do conteúdo de um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="64d93-111">The XPS OM is essentially an in-memory version of an XPS document's contents.</span></span> <span data-ttu-id="64d93-112">Embora seja semelhante em uma organização lógica a um documento XPS, um OM XPS não é considerado um documento XPS até ser serializado para um arquivo ou um fluxo.</span><span class="sxs-lookup"><span data-stu-id="64d93-112">While similar in logical organization to an XPS document, an XPS OM is not considered an XPS document until it has been serialized to a file or a stream.</span></span>

<span data-ttu-id="64d93-113">A estrutura exata da marcação não está disponível para o OM XPS quando um documento XPS é desserializado de marcação para um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="64d93-113">The exact structure of the markup is not available to the XPS OM when an XPS document is deserialized from markup to an XPS OM.</span></span> <span data-ttu-id="64d93-114">Por exemplo, se a propriedade foi representada como um elemento ou um atributo na marcação, o valor da propriedade de um objeto de documento é apresentado pelo OM XPS exatamente da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="64d93-114">For example, whether the property was represented as an element or an attribute in the markup, the property value of a document object is presented by the XPS OM in exactly the same way.</span></span>

<span data-ttu-id="64d93-115">A [API de documento XPS](documents-xps.md) pode ser dividida nas seguintes categorias:</span><span class="sxs-lookup"><span data-stu-id="64d93-115">The [XPS Document API](documents-xps.md) can be divided into the following categories:</span></span>

-   [<span data-ttu-id="64d93-116">Interfaces de tronco do XPS OM</span><span class="sxs-lookup"><span data-stu-id="64d93-116">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)

    <span data-ttu-id="64d93-117">As interfaces de tronco fornecem acesso aos componentes de nível superior da estrutura do documento XPS.</span><span class="sxs-lookup"><span data-stu-id="64d93-117">The trunk interfaces provide access to the top-level components of the XPS document structure.</span></span> <span data-ttu-id="64d93-118">Essas interfaces também fornecem os meios para serializar um OM XPS e desserializar um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="64d93-118">These interfaces also provide the means to serialize an XPS OM and deserialize an XPS document.</span></span>

-   [<span data-ttu-id="64d93-119">Interfaces de página do XPS OM</span><span class="sxs-lookup"><span data-stu-id="64d93-119">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)

    <span data-ttu-id="64d93-120">As interfaces de página fornecem acesso ao conteúdo de uma página em um documento XPS.</span><span class="sxs-lookup"><span data-stu-id="64d93-120">The page interfaces provide access to the contents of a page in an XPS document.</span></span> <span data-ttu-id="64d93-121">As interfaces que descrevem o conteúdo da página também estão incluídas com as interfaces de página.</span><span class="sxs-lookup"><span data-stu-id="64d93-121">The interfaces that describe the content of the page are also included with the page interfaces.</span></span>

-   [<span data-ttu-id="64d93-122">Assinaturas digitais do XPS OM</span><span class="sxs-lookup"><span data-stu-id="64d93-122">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)

    <span data-ttu-id="64d93-123">O OM XPS dá suporte a assinaturas digitais.</span><span class="sxs-lookup"><span data-stu-id="64d93-123">The XPS OM supports digital signatures.</span></span> <span data-ttu-id="64d93-124">No entanto, você pode acessar assinaturas digitais em um documento XPS diretamente sem criar um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="64d93-124">However, you can access digital signatures in an XPS document directly without creating an XPS OM.</span></span> <span data-ttu-id="64d93-125">Para obter mais informações sobre como acessar as assinaturas digitais XPS sem um OM XPS, consulte [API de assinatura digital XPS](xps-digital-signatures.md).</span><span class="sxs-lookup"><span data-stu-id="64d93-125">For more information about how to access XPS digital signatures without an XPS OM, see [XPS Digital Signature API](xps-digital-signatures.md).</span></span>

-   [<span data-ttu-id="64d93-126">Interfaces de tíquete de impressão XPS OM</span><span class="sxs-lookup"><span data-stu-id="64d93-126">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)

    <span data-ttu-id="64d93-127">Os documentos XPS dão suporte a tíquetes de impressão no nível do pacote (trabalho), documento e página.</span><span class="sxs-lookup"><span data-stu-id="64d93-127">XPS documents support print tickets at the package (job), document, and page level.</span></span> <span data-ttu-id="64d93-128">Os tíquetes de impressão contêm informações sobre como formatar o conteúdo do documento para impressão ou exibição.</span><span class="sxs-lookup"><span data-stu-id="64d93-128">Print tickets contain information about how to format document content for printing or viewing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64d93-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="64d93-129">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="64d93-130">**Nesta seção**</span><span class="sxs-lookup"><span data-stu-id="64d93-130">**In This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="64d93-131">Interfaces de tronco do XPS OM</span><span class="sxs-lookup"><span data-stu-id="64d93-131">XPS OM Trunk Interfaces</span></span>](xps-om-trunk-interfaces.md)
</dt> <dt>

[<span data-ttu-id="64d93-132">Interfaces de página do XPS OM</span><span class="sxs-lookup"><span data-stu-id="64d93-132">XPS OM Page Interfaces</span></span>](xps-object-model-page-interfaces.md)
</dt> <dt>

[<span data-ttu-id="64d93-133">Assinaturas digitais do XPS OM</span><span class="sxs-lookup"><span data-stu-id="64d93-133">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="64d93-134">Interfaces de tíquete de impressão XPS OM</span><span class="sxs-lookup"><span data-stu-id="64d93-134">XPS OM Print Ticket Interfaces</span></span>](xps-object-model-print-ticket-interfaces.md)
</dt> <dt>

<span data-ttu-id="64d93-135">**Outros tópicos relacionados**</span><span class="sxs-lookup"><span data-stu-id="64d93-135">**Other Related Topics**</span></span>
</dt> <dt>

[<span data-ttu-id="64d93-136">Inicializar um OM XPS</span><span class="sxs-lookup"><span data-stu-id="64d93-136">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="64d93-137">Assinaturas digitais do XPS OM</span><span class="sxs-lookup"><span data-stu-id="64d93-137">XPS OM Digital Signatures</span></span>](using-the-xps-digital-signatures.md)
</dt> <dt>

[<span data-ttu-id="64d93-138">Referência da API do documento XPS</span><span class="sxs-lookup"><span data-stu-id="64d93-138">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="64d93-139">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="64d93-139">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



