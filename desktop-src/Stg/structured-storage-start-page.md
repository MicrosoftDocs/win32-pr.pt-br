---
title: Armazenamento estruturado
description: O armazenamento estruturado fornece persistência de arquivos e dados em COM manipulando um único arquivo como uma coleção estruturada de objetos conhecidos como armazenamentos e fluxos.
ms.assetid: 57a5f34d-c3db-47c5-9836-6e2163732d30
keywords:
- Strctd de armazenamento estruturado STG
- Strctd de armazenamento estruturado STG, página inicial
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 606fef01d67cd78997f21dcd9008785d30985315
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294250"
---
# <a name="structured-storage"></a><span data-ttu-id="53c68-105">Armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="53c68-105">Structured Storage</span></span>

## <a name="purpose"></a><span data-ttu-id="53c68-106">Finalidade</span><span class="sxs-lookup"><span data-stu-id="53c68-106">Purpose</span></span>

<span data-ttu-id="53c68-107">O armazenamento estruturado fornece persistência de arquivos e dados em COM manipulando um único arquivo como uma coleção estruturada de objetos conhecidos como armazenamentos e fluxos.</span><span class="sxs-lookup"><span data-stu-id="53c68-107">Structured Storage provides file and data persistence in COM by handling a single file as a structured collection of objects known as storages and streams.</span></span>

<span data-ttu-id="53c68-108">A finalidade do armazenamento estruturado é reduzir as penalidades de desempenho e a sobrecarga associada ao armazenamento de objetos separados em um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="53c68-108">The purpose of Structured Storage is to reduce the performance penalties and overhead associated with storing separate objects in a single file.</span></span> <span data-ttu-id="53c68-109">O armazenamento estruturado fornece uma solução definindo como lidar com uma única entidade de arquivo como uma coleção estruturada de dois tipos de armazenamentos de objetos e fluxos por meio de uma implementação padrão chamada arquivos compostos.</span><span class="sxs-lookup"><span data-stu-id="53c68-109">Structured Storage provides a solution by defining how to handle a single file entity as a structured collection of two types of objects storages and streams through a standard implementation called Compound Files.</span></span> <span data-ttu-id="53c68-110">Isso permite que o usuário interaja e gerencie um arquivo composto como se fosse um único arquivo em vez de uma hierarquia aninhada de objetos separados.</span><span class="sxs-lookup"><span data-stu-id="53c68-110">This enables the user to interact with, and manage, a compound file as if it were a single file rather than a nested hierarchy of separate objects.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="53c68-111">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="53c68-111">Where applicable</span></span>

<span data-ttu-id="53c68-112">O armazenamento estruturado pode ser usado em sistemas operacionais baseados em Microsoft COM.</span><span class="sxs-lookup"><span data-stu-id="53c68-112">Structured Storage can be used on Microsoft COM-based operating systems.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="53c68-113">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="53c68-113">Developer audience</span></span>

<span data-ttu-id="53c68-114">A documentação de armazenamento estruturado destina-se a programadores experientes de C e C++ e a desenvolvedores de sistemas baseados em COM.</span><span class="sxs-lookup"><span data-stu-id="53c68-114">The Structured Storage documentation is intended for experienced C and C++ programmers and COM-based system developers.</span></span>

<span data-ttu-id="53c68-115">O armazenamento estruturado dá suporte principalmente às linguagens de programação C e C++. no entanto, qualquer tecnologia baseada em COM também dará suporte a qualquer linguagem de programação que utilize ponteiros de interface.</span><span class="sxs-lookup"><span data-stu-id="53c68-115">Structured Storage primarily supports C and C++ programming languages, however any COM-based technology will also support any programming language that utilizes interface pointers.</span></span>

<span data-ttu-id="53c68-116">Uma compreensão sólida das tecnologias COM é o pré-requisito para o uso de armazenamento estruturado de desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="53c68-116">A solid understanding of COM technologies is prerequisite to the developmental use of Structured Storage.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="53c68-117">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="53c68-117">Run-time requirements</span></span>

<span data-ttu-id="53c68-118">Para obter mais informações sobre quais sistemas operacionais são necessários para usar um elemento de API específico, consulte a seção requisitos da documentação do elemento.</span><span class="sxs-lookup"><span data-stu-id="53c68-118">For more information about which operating systems are required to use a particular API element, see the Requirements section of the documentation for the element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="53c68-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="53c68-119">In this section</span></span>



| <span data-ttu-id="53c68-120">Tópico</span><span class="sxs-lookup"><span data-stu-id="53c68-120">Topic</span></span>                                                               | <span data-ttu-id="53c68-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="53c68-121">Description</span></span>                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53c68-122">Visão geral</span><span class="sxs-lookup"><span data-stu-id="53c68-122">Overview</span></span>](about-structured-storage.md)<br/>                 | <span data-ttu-id="53c68-123">Informações gerais sobre o armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="53c68-123">General information about Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="53c68-124">Usando o armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="53c68-124">Using Structured Storage</span></span>](using-structured-storage.md)<br/> | <span data-ttu-id="53c68-125">Usando informações para o armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="53c68-125">Using information for Structured Storage.</span></span><br/>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="53c68-126">Referência</span><span class="sxs-lookup"><span data-stu-id="53c68-126">Reference</span></span>](structured-storage-reference.md)<br/>            | <span data-ttu-id="53c68-127">Documentação de interfaces, funções, estruturas e enumerações específicas de armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="53c68-127">Documentation of Structured Storage specific interfaces, functions, structures, and enumerations.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="53c68-128">Amostras</span><span class="sxs-lookup"><span data-stu-id="53c68-128">Samples</span></span>](samples.md)<br/>                                   | <span data-ttu-id="53c68-129">Exemplos de código escritos em C++.</span><span class="sxs-lookup"><span data-stu-id="53c68-129">Code examples written in C++.</span></span> <span data-ttu-id="53c68-130">Para obter mais informações, consulte [nomes em IStorage](names-in-istorage.md), [cabeçalho do conjunto de propriedades](property-set-header.md), [seção](section.md), [armazenando conjuntos de propriedades](storing-property-sets.md)e usando o [armazenamento estruturado](using-structured-storage.md).</span><span class="sxs-lookup"><span data-stu-id="53c68-130">For more information, see [Names in IStorage](names-in-istorage.md), [Property Set Header](property-set-header.md), [Section](section.md), [Storing Property Sets](storing-property-sets.md), and [Using Structured Storage](using-structured-storage.md).</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="53c68-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="53c68-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53c68-132">O Component Object Model</span><span class="sxs-lookup"><span data-stu-id="53c68-132">The Component Object Model</span></span>](../com/the-component-object-model.md)
</dt> </dl>

 

