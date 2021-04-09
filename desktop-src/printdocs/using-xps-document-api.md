---
description: Esta seção descreve como usar a API de documento XPS para executar tarefas de programação.
ms.assetid: 05b3d7b6-7628-4a5f-87b7-9d51ead51c79
title: Usando a API de documento XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8870c64bfa8fe478fb71174703c82a96e3723c53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922569"
---
# <a name="using-xps-document-api"></a><span data-ttu-id="b9ba2-103">Usando a API de documento XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-103">Using XPS Document API</span></span>

<span data-ttu-id="b9ba2-104">Esta seção descreve como usar a [API de documento XPS](documents-xps.md) para executar tarefas de programação.</span><span class="sxs-lookup"><span data-stu-id="b9ba2-104">This section describes how to use the [XPS Document API](documents-xps.md) to perform programming tasks.</span></span>

<span data-ttu-id="b9ba2-105">Para obter exemplos de como usar a [API de documento XPS](documents-xps.md) em um programa, consulte a seção [tarefas de programação de API de documento XPS](#xps-document-api-programming-tasks) .</span><span class="sxs-lookup"><span data-stu-id="b9ba2-105">For examples of how to use the [XPS Document API](documents-xps.md) in a program, see the [XPS Document API Programming Tasks](#xps-document-api-programming-tasks) section.</span></span>

<span data-ttu-id="b9ba2-106">Para obter informações sobre como usar o modelo de objeto XPS e como ele é implementado pela [API de documento XPS](documents-xps.md), consulte [sobre a API de documento XPS](about-xps-document-api.md).</span><span class="sxs-lookup"><span data-stu-id="b9ba2-106">For information about how to use the XPS Object Model and how it is implemented by the [XPS Document API](documents-xps.md), see [About XPS Document API](about-xps-document-api.md).</span></span>

## <a name="getting-started-with-the-xps-document-api"></a><span data-ttu-id="b9ba2-107">Introdução com a API de documento XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-107">Getting Started with the XPS Document API</span></span>

<span data-ttu-id="b9ba2-108">Antes de começar a usar a API de documento XPS, verifique se você está familiarizado com os seguintes tópicos de programação:</span><span class="sxs-lookup"><span data-stu-id="b9ba2-108">Before you start using the XPS Document API, make sure that you are familiar with the following programming topics:</span></span><dl>

[<span data-ttu-id="b9ba2-109">Programação COM</span><span class="sxs-lookup"><span data-stu-id="b9ba2-109">COM Programming</span></span>](/windows/desktop/com/component-object-model--com--portal)  
[<span data-ttu-id="b9ba2-110">Tratamento de erro em COM</span><span class="sxs-lookup"><span data-stu-id="b9ba2-110">Error Handling in COM</span></span>](/windows/desktop/com/error-handling-in-com)  
</dl>

<span data-ttu-id="b9ba2-111">Ao usar a API de documento XPS, talvez você também queira usar as seguintes tecnologias:</span><span class="sxs-lookup"><span data-stu-id="b9ba2-111">When using the XPS Document API, you might also want to use the following technologies:</span></span><dl>

[<span data-ttu-id="b9ba2-112">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="b9ba2-112">DirectWrite</span></span>](/windows/desktop/DirectWrite/direct-write-portal)  
[<span data-ttu-id="b9ba2-113">API de impressão XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-113">XPS Print API</span></span>](./printing-with-the-xpsprint-api.md)  
[<span data-ttu-id="b9ba2-114">API de assinatura digital XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-114">XPS Digital Signature API</span></span>](xps-digital-signatures.md)  
</dl>

## <a name="xps-document-api-programming-tasks"></a><span data-ttu-id="b9ba2-115">Tarefas de programação da API do documento XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-115">XPS Document API Programming Tasks</span></span>

<span data-ttu-id="b9ba2-116">Os tópicos nesta seção descrevem como usar a API de [documento XPS](documents-xps.md) em um programa e demonstrar como executar algumas tarefas comuns de programação.</span><span class="sxs-lookup"><span data-stu-id="b9ba2-116">The topics in this section describe how to use the [XPS Document API](documents-xps.md) in a program and demonstrate how to perform some common programming tasks.</span></span>

<span data-ttu-id="b9ba2-117">A API de documento XPS usa coleções para trabalhar com grupos de interfaces.</span><span class="sxs-lookup"><span data-stu-id="b9ba2-117">The XPS Document API uses collections to work with groups of interfaces.</span></span> <span data-ttu-id="b9ba2-118">[Trabalhar com interfaces de coleta de OM XPS](working-with-xps-object-model-collection-interfaces.md) descreve como programar com essas coleções.</span><span class="sxs-lookup"><span data-stu-id="b9ba2-118">[Working with XPS OM Collection Interfaces](working-with-xps-object-model-collection-interfaces.md) describes how to program with these collections.</span></span>

<span data-ttu-id="b9ba2-119">As [tarefas comuns de programação de documento XPS](common-xps-document-tasks.md) incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b9ba2-119">The [Common XPS Document Programming Tasks](common-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="b9ba2-120">Inicializar um OM XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-120">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)  
[<span data-ttu-id="b9ba2-121">Criar um OM XPS em branco</span><span class="sxs-lookup"><span data-stu-id="b9ba2-121">Create a Blank XPS OM</span></span>](create-a-blank-xps-om.md)  
[<span data-ttu-id="b9ba2-122">Ler um documento XPS em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-122">Read an XPS Document into an XPS OM</span></span>](read-an-xps-document-into-an-xps-om.md)  
[<span data-ttu-id="b9ba2-123">Navegar no OM XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-123">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)  
[<span data-ttu-id="b9ba2-124">Gravar texto em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-124">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)  
[<span data-ttu-id="b9ba2-125">Desenhar gráficos em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-125">Draw Graphics in an XPS OM</span></span>](draw-graphics-in-an-xps-om.md)  
[<span data-ttu-id="b9ba2-126">Coloque as imagens em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-126">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)  
[<span data-ttu-id="b9ba2-127">Gravar um OM XPS em um documento XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-127">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)  
[<span data-ttu-id="b9ba2-128">Imprimir um OM XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-128">Print an XPS OM</span></span>](print-an-xps-om.md)  
  
</dl>

<span data-ttu-id="b9ba2-129">As [tarefas avançadas de programação de documentos XPS](advanced-xps-document-tasks.md) incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b9ba2-129">The [Advanced XPS Document Programming Tasks](advanced-xps-document-tasks.md) include the following:</span></span>

<dl>

[<span data-ttu-id="b9ba2-130">Mesclar documentos XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-130">Merge XPS Documents</span></span>](merging-xps-documents.md)  
[<span data-ttu-id="b9ba2-131">Processando documentos XPS em um filtro XPSDrv</span><span class="sxs-lookup"><span data-stu-id="b9ba2-131">Processing XPS Documents in an XPSDrv Filter</span></span>](processing-xps-documents-in-an-xpsdrv-filter.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="b9ba2-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9ba2-132">Related topics</span></span>

<dl> <span data-ttu-id="b9ba2-133"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="b9ba2-133"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="b9ba2-134">Referência da API do documento XPS</span><span class="sxs-lookup"><span data-stu-id="b9ba2-134">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="b9ba2-135">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="b9ba2-135">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
