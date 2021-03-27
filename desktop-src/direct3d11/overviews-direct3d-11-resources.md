---
title: Recursos
description: Esta seção descreve os aspectos dos recursos do Direct3D 11.
ms.assetid: 5b8b1198-73ed-4058-9fc6-a1c43902d732
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9ed73d81d2521fe97b36e6bfc8d71e387f8c9c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008624"
---
# <a name="resources"></a><span data-ttu-id="d6f69-103">Recursos</span><span class="sxs-lookup"><span data-stu-id="d6f69-103">Resources</span></span>

<span data-ttu-id="d6f69-104">Os recursos fornecem dados para o pipeline e definem o que é renderizado durante a cena.</span><span class="sxs-lookup"><span data-stu-id="d6f69-104">Resources provide data to the pipeline and define what is rendered during your scene.</span></span> <span data-ttu-id="d6f69-105">Os recursos podem ser carregados a partir da mídia de jogo ou criados dinamicamente no momento de execução.</span><span class="sxs-lookup"><span data-stu-id="d6f69-105">Resources can be loaded from your game media or created dynamically at run time.</span></span> <span data-ttu-id="d6f69-106">Normalmente, os recursos incluem dados de textura, dados de vértice e dados de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d6f69-106">Typically, resources include texture data, vertex data, and shader data.</span></span> <span data-ttu-id="d6f69-107">A maioria dos aplicativos do Direct3D cria e destrói recursos extensivamente durante seu ciclo de vida.</span><span class="sxs-lookup"><span data-stu-id="d6f69-107">Most Direct3D applications create and destroy resources extensively throughout their lifespan.</span></span> <span data-ttu-id="d6f69-108">Esta seção descreve os aspectos dos recursos do Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="d6f69-108">This section describes aspects of Direct3D 11 resources.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="d6f69-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="d6f69-109">In this section</span></span>



| <span data-ttu-id="d6f69-110">Tópico</span><span class="sxs-lookup"><span data-stu-id="d6f69-110">Topic</span></span>                                                                                             | <span data-ttu-id="d6f69-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6f69-111">Description</span></span>                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d6f69-112">Introdução a um recurso no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d6f69-112">Introduction to a Resource in Direct3D 11</span></span>](overviews-direct3d-11-resources-intro.md)<br/> | <span data-ttu-id="d6f69-113">Este tópico apresenta recursos do Direct3D, como buffers e texturas.</span><span class="sxs-lookup"><span data-stu-id="d6f69-113">This topic introduces Direct3D resources such as buffers and textures.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="d6f69-114">Tipos de recursos</span><span class="sxs-lookup"><span data-stu-id="d6f69-114">Types of Resources</span></span>](overviews-direct3d-11-resources-types.md)<br/>                        | <span data-ttu-id="d6f69-115">Este tópico descreve os tipos de recursos do Direct3D 10, bem como os novos tipos no Direct3D 11, incluindo buffers estruturados e texturas e buffers graváveis.</span><span class="sxs-lookup"><span data-stu-id="d6f69-115">This topic describes the types of resources from Direct3D 10, as well as new types in Direct3D 11 including structured buffers and writable textures and buffers.</span></span><br/>                                                                       |
| [<span data-ttu-id="d6f69-116">Limites de recursos</span><span class="sxs-lookup"><span data-stu-id="d6f69-116">Resource Limits</span></span>](overviews-direct3d-11-resources-limits.md)<br/>                          | <span data-ttu-id="d6f69-117">Este tópico contém uma lista de recursos para os quais o Direct3D 11 dá suporte (especificamente, hardware de nível 11 ou 9. x de [recursos](overviews-direct3d-11-devices-downlevel-intro.md) ).</span><span class="sxs-lookup"><span data-stu-id="d6f69-117">This topic contains a list of resources that Direct3D 11 supports (specifically [feature level](overviews-direct3d-11-devices-downlevel-intro.md) 11 or 9.x hardware).</span></span><br/>                                 |
| [<span data-ttu-id="d6f69-118">Sub-recursos</span><span class="sxs-lookup"><span data-stu-id="d6f69-118">Subresources</span></span>](overviews-direct3d-11-resources-subresources.md)<br/>                       | <span data-ttu-id="d6f69-119">Este tópico descreve os subrecursos de textura ou partes de um recurso.</span><span class="sxs-lookup"><span data-stu-id="d6f69-119">This topic describes texture subresources, or portions of a resource.</span></span><br/>                                                                                                                                                                   |
| [<span data-ttu-id="d6f69-120">Buffers</span><span class="sxs-lookup"><span data-stu-id="d6f69-120">Buffers</span></span>](overviews-direct3d-11-resources-buffers.md)<br/>                                 | <span data-ttu-id="d6f69-121">Os buffers contêm dados que são usados para descrever a geometria, indexar informações de geometria e constantes de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d6f69-121">Buffers contain data that is used for describing geometry, indexing geometry information, and shader constants.</span></span> <span data-ttu-id="d6f69-122">Esta seção descreve os buffers usados no Direct3D 11 e links para a documentação baseada em tarefas para cenários comuns.</span><span class="sxs-lookup"><span data-stu-id="d6f69-122">This section describes buffers that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/> |
| [<span data-ttu-id="d6f69-123">Texturas</span><span class="sxs-lookup"><span data-stu-id="d6f69-123">Textures</span></span>](overviews-direct3d-11-resources-textures.md)<br/>                               | <span data-ttu-id="d6f69-124">Esta seção descreve as texturas usadas no Direct3D 11 e links para a documentação baseada em tarefas para cenários comuns.</span><span class="sxs-lookup"><span data-stu-id="d6f69-124">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="d6f69-125">Regras de ponto flutuante</span><span class="sxs-lookup"><span data-stu-id="d6f69-125">Floating-point rules</span></span>](floating-point-rules.md)<br/>                                       | <span data-ttu-id="d6f69-126">O Direct3D 11 dá suporte a várias representações de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="d6f69-126">Direct3D 11 supports several floating-point representations.</span></span> <span data-ttu-id="d6f69-127">Todos os cálculos de ponto flutuante operam em um subconjunto das regras de ponto flutuante de precisão única de 32 bits 754 IEEE definido.</span><span class="sxs-lookup"><span data-stu-id="d6f69-127">All floating-point computations operate under a defined subset of the IEEE 754 32-bit single precision floating-point rules.</span></span><br/>                                               |
| [<span data-ttu-id="d6f69-128">Recursos em ladrilho</span><span class="sxs-lookup"><span data-stu-id="d6f69-128">Tiled resources</span></span>](tiled-resources.md)<br/>                                                 | <span data-ttu-id="d6f69-129">Os recursos ao lado dos ladrilhos podem ser considerados como recursos lógicos grandes que usam pequenas quantidades de memória física.</span><span class="sxs-lookup"><span data-stu-id="d6f69-129">Tiled resources can be thought of as large logical resources that use small amounts of physical memory.</span></span><br/>                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="d6f69-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6f69-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6f69-131">Guia de programação para Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="d6f69-131">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 





