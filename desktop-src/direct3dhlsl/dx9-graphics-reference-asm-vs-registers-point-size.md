---
title: Registro de tamanho do ponto
description: Este registro de saída do sombreador de vértice contém dados de tamanho de ponto por vértice.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363910"
---
# <a name="point-size-register"></a><span data-ttu-id="85c0a-103">Registro de tamanho do ponto</span><span class="sxs-lookup"><span data-stu-id="85c0a-103">Point Size Register</span></span>

<span data-ttu-id="85c0a-104">Este registro de saída do sombreador de vértice contém dados de tamanho de ponto por vértice.</span><span class="sxs-lookup"><span data-stu-id="85c0a-104">This vertex shader output register contains per-vertex point size data.</span></span>



| <span data-ttu-id="85c0a-105">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="85c0a-105">Vertex shader versions</span></span> | <span data-ttu-id="85c0a-106">1\_1</span><span class="sxs-lookup"><span data-stu-id="85c0a-106">1\_1</span></span> | <span data-ttu-id="85c0a-107">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="85c0a-107">2\_0</span></span> | <span data-ttu-id="85c0a-108">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="85c0a-108">2\_sw</span></span> | <span data-ttu-id="85c0a-109">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="85c0a-109">2\_x</span></span> | <span data-ttu-id="85c0a-110">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="85c0a-110">3\_0</span></span> | <span data-ttu-id="85c0a-111">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="85c0a-111">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="85c0a-112">Registro de tamanho do ponto</span><span class="sxs-lookup"><span data-stu-id="85c0a-112">Point Size Register</span></span>    | <span data-ttu-id="85c0a-113">x</span><span class="sxs-lookup"><span data-stu-id="85c0a-113">x</span></span>    | <span data-ttu-id="85c0a-114">x</span><span class="sxs-lookup"><span data-stu-id="85c0a-114">x</span></span>    | <span data-ttu-id="85c0a-115">x</span><span class="sxs-lookup"><span data-stu-id="85c0a-115">x</span></span>     | <span data-ttu-id="85c0a-116">x</span><span class="sxs-lookup"><span data-stu-id="85c0a-116">x</span></span>    | <span data-ttu-id="85c0a-117">x</span><span class="sxs-lookup"><span data-stu-id="85c0a-117">x</span></span>    | <span data-ttu-id="85c0a-118">x</span><span class="sxs-lookup"><span data-stu-id="85c0a-118">x</span></span>     |



 

<span data-ttu-id="85c0a-119">Um registro consiste em propriedades que determinam se o registro se comporta.</span><span class="sxs-lookup"><span data-stu-id="85c0a-119">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="85c0a-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="85c0a-120">Property</span></span>        | <span data-ttu-id="85c0a-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="85c0a-121">Description</span></span>                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85c0a-122">Name</span><span class="sxs-lookup"><span data-stu-id="85c0a-122">Name</span></span>            | <span data-ttu-id="85c0a-123">oPts</span><span class="sxs-lookup"><span data-stu-id="85c0a-123">oPts</span></span>                                                                                            |
| <span data-ttu-id="85c0a-124">Contagem</span><span class="sxs-lookup"><span data-stu-id="85c0a-124">Count</span></span>           | <span data-ttu-id="85c0a-125">1 vetor, do qual de apenas um componente pode ser usado e deve ser especificado pela máscara do componente.</span><span class="sxs-lookup"><span data-stu-id="85c0a-125">1 vector, of which of only 1 component can be used and must be specified by the component mask.</span></span> |
| <span data-ttu-id="85c0a-126">Permissões de e/s</span><span class="sxs-lookup"><span data-stu-id="85c0a-126">I/O permissions</span></span> | <span data-ttu-id="85c0a-127">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="85c0a-127">Write-only.</span></span>                                                                                     |



 

<span data-ttu-id="85c0a-128">Somente o componente x escalar do tamanho do ponto é usado.</span><span class="sxs-lookup"><span data-stu-id="85c0a-128">Only the scalar x-component of the point size is used.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85c0a-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85c0a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85c0a-130">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="85c0a-130">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




