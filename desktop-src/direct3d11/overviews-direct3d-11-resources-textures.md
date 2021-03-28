---
title: Texturas
description: Esta seção descreve as texturas usadas no Direct3D 11 e links para a documentação baseada em tarefas para cenários comuns.
ms.assetid: ec833431-a7b4-4aea-91c8-e99b718de2c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afc3909f354b0709e82ffd2bdffafe6cdb35516
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160129"
---
# <a name="textures"></a><span data-ttu-id="362fa-103">Texturas</span><span class="sxs-lookup"><span data-stu-id="362fa-103">Textures</span></span>

<span data-ttu-id="362fa-104">Uma textura armazena informações de Texel.</span><span class="sxs-lookup"><span data-stu-id="362fa-104">A texture stores texel information.</span></span> <span data-ttu-id="362fa-105">Esta seção descreve as texturas usadas no Direct3D 11 e links para a documentação baseada em tarefas para cenários comuns.</span><span class="sxs-lookup"><span data-stu-id="362fa-105">This section describes textures that are used in Direct3D 11 and links to task-based documentation for common scenarios.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="362fa-106">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="362fa-106">In this section</span></span>



| <span data-ttu-id="362fa-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="362fa-107">Topic</span></span>                                                                                                    | <span data-ttu-id="362fa-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="362fa-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="362fa-109">Introdução às texturas no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="362fa-109">Introduction To Textures in Direct3D 11</span></span>](overviews-direct3d-11-resources-textures-intro.md)<br/> | <span data-ttu-id="362fa-110">Um recurso de textura é uma coleção estruturada de dados projetada para armazenar texels.</span><span class="sxs-lookup"><span data-stu-id="362fa-110">A texture resource is a structured collection of data designed to store texels.</span></span> <span data-ttu-id="362fa-111">Um texel representa a menor unidade de uma textura que pode ser lida ou gravada pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="362fa-111">A texel represents the smallest unit of a texture that can be read or written to by the pipeline.</span></span> <span data-ttu-id="362fa-112">Diferente dos buffers, as texturas podem ser filtradas por amostras de texturas à medida que são lidas por unidades de sombreador.</span><span class="sxs-lookup"><span data-stu-id="362fa-112">Unlike buffers, textures can be filtered by texture samplers as they are read by shader units.</span></span> <span data-ttu-id="362fa-113">O tipo de textura afeta como a textura é filtrada.</span><span class="sxs-lookup"><span data-stu-id="362fa-113">The type of texture impacts how the texture is filtered.</span></span> <span data-ttu-id="362fa-114">Cada Texel contém de 1 a 4 componentes, organizados em um dos formatos DXGI definidos pela enumeração de \_ formato dxgi.</span><span class="sxs-lookup"><span data-stu-id="362fa-114">Each texel contains 1 to 4 components, arranged in one of the DXGI formats defined by the DXGI\_FORMAT enumeration.</span></span><br/> |
| [<span data-ttu-id="362fa-115">Compactação de bloco de textura no Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="362fa-115">Texture Block Compression in Direct3D 11</span></span>](texture-block-compression-in-direct3d-11.md)<br/>      | <span data-ttu-id="362fa-116">O suporte para texturas de compactação de bloco (BC) foi estendido no Direct3D 11 para incluir os algoritmos de BC6H e BC7.</span><span class="sxs-lookup"><span data-stu-id="362fa-116">Block Compression (BC) support for textures has been extended in Direct3D 11 to include the BC6H and BC7 algorithms.</span></span> <span data-ttu-id="362fa-117">O BC6H dá suporte a dados de origem de cor de intervalo altamente dinâmico e o BC7 fornece compactação de qualidade melhor que a média com menos artefatos para dados de origem RGB padrão.</span><span class="sxs-lookup"><span data-stu-id="362fa-117">BC6H supports high-dynamic range color source data, and BC7 provides better-than-average quality compression with less artifacts for standard RGB source data.</span></span><br/>                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="362fa-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="362fa-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="362fa-119">Como: criar uma textura</span><span class="sxs-lookup"><span data-stu-id="362fa-119">How to: Create a Texture</span></span>](overviews-direct3d-11-resources-textures-create.md)
</dt> <dt>

[<span data-ttu-id="362fa-120">Como: inicializar uma textura programaticamente</span><span class="sxs-lookup"><span data-stu-id="362fa-120">How to: Initialize a Texture Programmatically</span></span>](overviews-direct3d-11-resources-textures-how-to-fill-manually.md)
</dt> <dt>

[<span data-ttu-id="362fa-121">Como: inicializar uma textura a partir de um arquivo</span><span class="sxs-lookup"><span data-stu-id="362fa-121">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)
</dt> <dt>

[<span data-ttu-id="362fa-122">Recursos</span><span class="sxs-lookup"><span data-stu-id="362fa-122">Resources</span></span>](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





