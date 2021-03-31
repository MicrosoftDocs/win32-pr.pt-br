---
title: Primitivos e comandos
description: Primitivos e comandos
ms.assetid: f838320f-3fab-4984-8d45-b0c8cbea6034
keywords:
- OpenGL, primitivos
- OpenGL, comandos
- primitivas OpenGL
- comandos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba52cad8436fbe97c83a6d0e214b6c7ba500d195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635555"
---
# <a name="primitives-and-commands"></a><span data-ttu-id="817ab-107">Primitivos e comandos</span><span class="sxs-lookup"><span data-stu-id="817ab-107">Primitives and Commands</span></span>

<span data-ttu-id="817ab-108">O OpenGL desenha pontos *primitivos* , segmentos de linha ou polygonssubject para vários modos selecionáveis.</span><span class="sxs-lookup"><span data-stu-id="817ab-108">OpenGL draws *primitives* points, line segments, or polygonssubject to several selectable modes.</span></span> <span data-ttu-id="817ab-109">Você pode controlar modos de forma independente um do outro.</span><span class="sxs-lookup"><span data-stu-id="817ab-109">You can control modes independently of one another.</span></span> <span data-ttu-id="817ab-110">Ou seja, definir um modo não afeta se outros modos estão definidos (embora muitos modos possam interagir para determinar o que eventualmente acaba no framebuffer).</span><span class="sxs-lookup"><span data-stu-id="817ab-110">That is, setting one mode doesn't affect whether other modes are set (although many modes may interact to determine what eventually ends up in the framebuffer).</span></span> <span data-ttu-id="817ab-111">Para especificar primitivos, definir modos e executar outras operações OpenGL, você emite comandos na forma de chamadas de função.</span><span class="sxs-lookup"><span data-stu-id="817ab-111">To specify primitives, set modes, and perform other OpenGL operations, you issue commands in the form of function calls.</span></span>

<span data-ttu-id="817ab-112">Os primitivos são definidos por um grupo de um ou mais *vértices*.</span><span class="sxs-lookup"><span data-stu-id="817ab-112">Primitives are defined by a group of one or more *vertices*.</span></span> <span data-ttu-id="817ab-113">Um vértice define um ponto, um ponto de extremidade de uma linha ou um canto de um polígono onde duas bordas se encontram.</span><span class="sxs-lookup"><span data-stu-id="817ab-113">A vertex defines a point, an endpoint of a line, or a corner of a polygon where two edges meet.</span></span> <span data-ttu-id="817ab-114">Os dados (que consistem em coordenadas de vértice, cores, normais, coordenadas de textura e sinalizadores de borda) são associados a um vértice, e cada vértice e seus dados associados são processados de forma independente, em ordem, e da mesma maneira.</span><span class="sxs-lookup"><span data-stu-id="817ab-114">Data (consisting of vertex coordinates, colors, normals, texture coordinates, and edge flags) is associated with a vertex, and each vertex and its associated data are processed independently, in order, and in the same way.</span></span> <span data-ttu-id="817ab-115">As únicas exceções a essa regra são casos em que o grupo de vértices deve ser recortado para que um primitivo específico caiba em uma região especificada.</span><span class="sxs-lookup"><span data-stu-id="817ab-115">The only exceptions to this rule are cases in which the group of vertices must be clipped so that a particular primitive fits within a specified region.</span></span> <span data-ttu-id="817ab-116">Nesse caso, os dados de vértice podem ser modificados e novos vértices criados.</span><span class="sxs-lookup"><span data-stu-id="817ab-116">In this case, vertex data may be modified and new vertices created.</span></span> <span data-ttu-id="817ab-117">O tipo de recorte depende de qual primitiva o grupo de vértices representa.</span><span class="sxs-lookup"><span data-stu-id="817ab-117">The type of clipping depends on which primitive the group of vertices represents.</span></span>

<span data-ttu-id="817ab-118">Os comandos são sempre processados na ordem em que são recebidos, embora possa haver um atraso indeterminado antes de um comando entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="817ab-118">Commands are always processed in the order in which they are received, although there may be an indeterminate delay before a command takes effect.</span></span> <span data-ttu-id="817ab-119">Isso significa que cada primitivo é desenhado completamente antes de qualquer comando subsequente entrar em vigor.</span><span class="sxs-lookup"><span data-stu-id="817ab-119">This means that each primitive is drawn completely before any subsequent command takes effect.</span></span> <span data-ttu-id="817ab-120">Isso também significa que os comandos de consulta de estado retornam dados consistentes com a execução completa de todos os comandos OpenGL emitidos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="817ab-120">It also means that state-querying commands return data that is consistent with complete execution of all previously issued OpenGL commands.</span></span>

 

 




