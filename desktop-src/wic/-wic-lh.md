---
description: Windows Imaging Component
ms.assetid: b872baf9-9fcb-4604-a518-26e109eda792
title: Windows Imaging Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f00bb18e2e432abbe3cfb3b72d28ceb4182e63ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170454"
---
# <a name="windows-imaging-component"></a><span data-ttu-id="57050-103">Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="57050-103">Windows Imaging Component</span></span>

## <a name="purpose"></a><span data-ttu-id="57050-104">Finalidade</span><span class="sxs-lookup"><span data-stu-id="57050-104">Purpose</span></span>

<span data-ttu-id="57050-105">O Windows Imaging Component (WIC) é uma plataforma extensível que fornece uma API de nível baixo para imagens digitais.</span><span class="sxs-lookup"><span data-stu-id="57050-105">The Windows Imaging Component (WIC) is an extensible platform that provides low-level API for digital images.</span></span>  <span data-ttu-id="57050-106">O WIC dá suporte aos formatos de imagem da Web padrão, alta imagens de intervalo dinâmico e dados brutos da câmera.</span><span class="sxs-lookup"><span data-stu-id="57050-106">WIC supports the standard web image formats, high dynamic range images, and raw camera data.</span></span>  <span data-ttu-id="57050-107">O WIC também oferece suporte a recursos adicionais, como:</span><span class="sxs-lookup"><span data-stu-id="57050-107">WIC also supports additional features such as:</span></span>

-   <span data-ttu-id="57050-108">Suporte interno para formatos de metadados padrão</span><span class="sxs-lookup"><span data-stu-id="57050-108">Built-in support for standard metadata formats</span></span>
-   <span data-ttu-id="57050-109">Estrutura extensível para codecs de imagem, formatos de pixel e formatos de metadados.</span><span class="sxs-lookup"><span data-stu-id="57050-109">Extensible framework for image codecs, pixel formats, and metadata formats.</span></span>
-   <span data-ttu-id="57050-110">Ampla gama de suporte a formato de pixel.</span><span class="sxs-lookup"><span data-stu-id="57050-110">Wide range of pixel format support.</span></span>
-   <span data-ttu-id="57050-111">Suporte de alta cor; incluindo um intervalo estendido de 30 bits, alta precisão de 30 bits e formatos de pixel de grande precisão de 48 bits e de gama ampla.</span><span class="sxs-lookup"><span data-stu-id="57050-111">High-color support; including 30-bit extended range, 30-bit high precision, and 48-bit high precision and wide gamut pixel formats.</span></span>
-   <span data-ttu-id="57050-112">Decodificação de imagem progressiva.</span><span class="sxs-lookup"><span data-stu-id="57050-112">Progressive image decoding.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="57050-113">Público do desenvolvedor</span><span class="sxs-lookup"><span data-stu-id="57050-113">Developer Audience</span></span>

<span data-ttu-id="57050-114">O WIC foi projetado para atender às necessidades das seguintes classes de desenvolvedores:</span><span class="sxs-lookup"><span data-stu-id="57050-114">WIC is designed to meet the needs of the following classes of developers:</span></span>

-   <span data-ttu-id="57050-115">Desenvolvedores que lêem e gravam dados de imagem em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="57050-115">Developers who read and write image data in an application.</span></span>
-   <span data-ttu-id="57050-116">Desenvolvedores que lêem e gravam metadados de imagem em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="57050-116">Developers who read and write image metadata in an application.</span></span>
-   <span data-ttu-id="57050-117">Desenvolvedores que desejam a descoberta de codecs de tempo de execução para codecs de imagem criados recentemente ou implementados.</span><span class="sxs-lookup"><span data-stu-id="57050-117">Developers who want run-time codec discovery for newly designed or implemented image codecs.</span></span>
-   <span data-ttu-id="57050-118">Desenvolvedores que projetam ou implementam novos codecs de imagem e formatos de metadados.</span><span class="sxs-lookup"><span data-stu-id="57050-118">Developers designing or implementing new image codecs and metadata formats.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="57050-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="57050-119">In this section</span></span>



| <span data-ttu-id="57050-120">Tópico</span><span class="sxs-lookup"><span data-stu-id="57050-120">Topic</span></span>                                                                 | <span data-ttu-id="57050-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="57050-121">Description</span></span>                                         |
|-----------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="57050-122">Novidades no WIC</span><span class="sxs-lookup"><span data-stu-id="57050-122">What's New in WIC</span></span>](what-s-new-in-wic-for-windows-8-1.md)<br/> |                                                     |
| [<span data-ttu-id="57050-123">Guia de programação</span><span class="sxs-lookup"><span data-stu-id="57050-123">Programming Guide</span></span>](-wic-programming-guide.md)<br/>            | <span data-ttu-id="57050-124">Descreve como usar as APIs do WIC.</span><span class="sxs-lookup"><span data-stu-id="57050-124">Describes how to use the WIC APIs.</span></span><br/>       |
| [<span data-ttu-id="57050-125">Referência</span><span class="sxs-lookup"><span data-stu-id="57050-125">Reference</span></span>](-wic-codec-reference.md)<br/>                      | <span data-ttu-id="57050-126">Contém a referência para as APIs do WIC.</span><span class="sxs-lookup"><span data-stu-id="57050-126">Contains the reference for the WIC APIs.</span></span><br/> |
| [<span data-ttu-id="57050-127">Exemplos de WIC</span><span class="sxs-lookup"><span data-stu-id="57050-127">WIC Samples</span></span>](-wic-samples.md)<br/>                            | <span data-ttu-id="57050-128">Fornece exemplos para o WIC.</span><span class="sxs-lookup"><span data-stu-id="57050-128">Provides samples for WIC.</span></span><br/>                |
| [<span data-ttu-id="57050-129">Glossário</span><span class="sxs-lookup"><span data-stu-id="57050-129">Glossary</span></span>](-wic-glossary.md)<br/>                              | <span data-ttu-id="57050-130">Define os termos que são usados no WIC.</span><span class="sxs-lookup"><span data-stu-id="57050-130">Defines terms that are used in WIC.</span></span><br/>      |



 

 

 




