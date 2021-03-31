---
title: Canonização XML
description: A canonização XML resolve o problema de conversão de um conjunto de nós XML em bytes de forma que as alterações triviais no XML (como alterar a ordem dos atributos em um elemento) não alterem o formulário de byte resultante.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Serviços Web de canonização XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8b1aa00b99b604276a479f1a47aacb5bd8b1e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103824071"
---
# <a name="xml-canonicalization"></a><span data-ttu-id="f955d-106">Canonização XML</span><span class="sxs-lookup"><span data-stu-id="f955d-106">XML Canonicalization</span></span>

<span data-ttu-id="f955d-107">A canonização XML resolve o problema de conversão de um conjunto de nós XML em bytes de forma que as alterações triviais no XML (como alterar a ordem dos atributos em um elemento) não alterem o formulário de byte resultante.</span><span class="sxs-lookup"><span data-stu-id="f955d-107">XML canonicalization solves the problem of converting a set of XML nodes into bytes in such a way that trivial changes to the XML (such as changing the order of attributes in an element) do not change the resulting byte form.</span></span> <span data-ttu-id="f955d-108">Os bytes obtidos da canonização são comumente usados para gerar uma assinatura criptográfica sobre o conteúdo XML.</span><span class="sxs-lookup"><span data-stu-id="f955d-108">The bytes obtained from canonicalization are commonly used to generate a cryptographic signature over XML content.</span></span>


<span data-ttu-id="f955d-109">Os algoritmos de canonização XML comumente usados padronizam os seguintes aspectos:</span><span class="sxs-lookup"><span data-stu-id="f955d-109">The commonly used XML canonicalization algorithms standardize the following aspects:</span></span>

-   <span data-ttu-id="f955d-110">Codificação de caracteres (UTF-8 sem preâmbulo)</span><span class="sxs-lookup"><span data-stu-id="f955d-110">Character encoding (UTF-8 without preamble)</span></span>
-   <span data-ttu-id="f955d-111">Alimentação de linha e outros formulários de caracteres</span><span class="sxs-lookup"><span data-stu-id="f955d-111">Linefeed and other character forms</span></span>
-   <span data-ttu-id="f955d-112">Ordem de atributo em um elemento</span><span class="sxs-lookup"><span data-stu-id="f955d-112">Attribute order in an element</span></span>
-   <span data-ttu-id="f955d-113">Formulário de elemento vazio</span><span class="sxs-lookup"><span data-stu-id="f955d-113">Empty element form</span></span>
-   <span data-ttu-id="f955d-114">Renderizando declarações de namespace</span><span class="sxs-lookup"><span data-stu-id="f955d-114">Rendering namespace declarations</span></span>

<span data-ttu-id="f955d-115">As APIs [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) e [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) fornecem a funcionalidade de canonização XML ao ler um documento.</span><span class="sxs-lookup"><span data-stu-id="f955d-115">The APIs [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) and [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) provide the XML canonicalization functionality while reading a document.</span></span>

<span data-ttu-id="f955d-116">As APIs [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) e [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) fornecem a funcionalidade de canonização XML durante a gravação de um documento.</span><span class="sxs-lookup"><span data-stu-id="f955d-116">The APIs [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) and [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) provide the XML canonicalization functionality while writing a document.</span></span>

<span data-ttu-id="f955d-117">As seguintes enumerações são usadas com canonização:</span><span class="sxs-lookup"><span data-stu-id="f955d-117">The following enumerations are used with canonicalization:</span></span>

-   [<span data-ttu-id="f955d-118">**\_algoritmo de \_ canonização \_ XML do WS**</span><span class="sxs-lookup"><span data-stu-id="f955d-118">**WS\_XML\_CANONICALIZATION\_ALGORITHM**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [<span data-ttu-id="f955d-119">**\_ID da \_ propriedade de canonização do WS XML \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f955d-119">**WS\_XML\_CANONICALIZATION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

<span data-ttu-id="f955d-120">As funções a seguir são usadas com canonização:</span><span class="sxs-lookup"><span data-stu-id="f955d-120">The following functions are used with canonicalization:</span></span>

-   [<span data-ttu-id="f955d-121">**WsEndReaderCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="f955d-121">**WsEndReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [<span data-ttu-id="f955d-122">**WsEndWriterCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="f955d-122">**WsEndWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [<span data-ttu-id="f955d-123">**WsStartReaderCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="f955d-123">**WsStartReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [<span data-ttu-id="f955d-124">**WsStartWriterCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="f955d-124">**WsStartWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

<span data-ttu-id="f955d-125">As seguintes estruturas são usadas com canonização:</span><span class="sxs-lookup"><span data-stu-id="f955d-125">The following structures are used with canonicalization:</span></span>

-   [<span data-ttu-id="f955d-126">**prefixos do WS \_ XML em \_ formato \_ inclusivo \_**</span><span class="sxs-lookup"><span data-stu-id="f955d-126">**WS\_XML\_CANONICALIZATION\_INCLUSIVE\_PREFIXES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [<span data-ttu-id="f955d-127">**\_propriedade de \_ canonização do WS XML \_**</span><span class="sxs-lookup"><span data-stu-id="f955d-127">**WS\_XML\_CANONICALIZATION\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




