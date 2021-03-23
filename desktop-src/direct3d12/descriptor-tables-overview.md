---
title: Visão geral das tabelas de descritores
description: Cada tabela de descritores armazena os descritores de um ou mais tipos-SRVs, UAVe, CBVs e amostras. Uma tabela de descritores não é uma alocação de memória; é simplesmente um deslocamento e um comprimento em um heap de descritor.
ms.assetid: 4A5749CE-DD84-40E1-B67F-31828165A631
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d446a0570cf813eacaa4d036781e8cd4b8def3c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104024"
---
# <a name="descriptor-tables-overview"></a><span data-ttu-id="87cf3-104">Visão geral das tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="87cf3-104">Descriptor Tables Overview</span></span>

<span data-ttu-id="87cf3-105">Cada tabela de descritores armazena os descritores de um ou mais tipos-SRVs, UAVe, CBVs e amostras.</span><span class="sxs-lookup"><span data-stu-id="87cf3-105">Each descriptor table stores descriptors of one or more types - SRVs, UAVe, CBVs, and Samplers.</span></span> <span data-ttu-id="87cf3-106">Uma tabela de descritores não é uma alocação de memória; é simplesmente um deslocamento e um comprimento em um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="87cf3-106">A descriptor table is not an allocation of memory; it is simply an offset and length into a descriptor heap.</span></span>

-   [<span data-ttu-id="87cf3-107">Referenciando tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="87cf3-107">Referencing descriptor tables</span></span>](#referencing-descriptor-tables)
-   [<span data-ttu-id="87cf3-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87cf3-108">Related topics</span></span>](#related-topics)

## <a name="referencing-descriptor-tables"></a><span data-ttu-id="87cf3-109">Referenciando tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="87cf3-109">Referencing descriptor tables</span></span>

<span data-ttu-id="87cf3-110">O pipeline de gráficos, por meio da assinatura raiz, tem acesso aos recursos fazendo referência a tabelas de descritores por índice.</span><span class="sxs-lookup"><span data-stu-id="87cf3-110">The graphics pipeline, through the root signature, gain access to resources by referencing into descriptor tables by index.</span></span>

<span data-ttu-id="87cf3-111">Na verdade, uma tabela de descritores é apenas um subintervalo de um heap de descritor.</span><span class="sxs-lookup"><span data-stu-id="87cf3-111">A descriptor table is actually just a sub-range of a descriptor heap.</span></span> <span data-ttu-id="87cf3-112">Heaps de descritor representam a alocação de memória subjacente para uma coleção de descritores.</span><span class="sxs-lookup"><span data-stu-id="87cf3-112">Descriptor heaps represent the underlying memory allocation for a collection of descriptors.</span></span> <span data-ttu-id="87cf3-113">Como a alocação de memória é uma propriedade de criação de um heap de descritor, a definição de uma tabela de descritores de um é garantida para ser tão barata quanto a identificação de uma região no heap para o hardware.</span><span class="sxs-lookup"><span data-stu-id="87cf3-113">Since memory allocation is a property of a creating a descriptor heap, defining a descriptor table out of one is guaranteed to be as cheap as identifying a region in the heap to the hardware.</span></span> <span data-ttu-id="87cf3-114">As tabelas de descritores não precisam ser criadas ou destruídas no nível de API – elas são meramente identificadas para drivers como um deslocamento e tamanho fora de um heap sempre que forem referenciados.</span><span class="sxs-lookup"><span data-stu-id="87cf3-114">Descriptor tables don’t need to be created or destroyed at the API level– they are merely identified to drivers as an offset and size out of a heap whenever referenced.</span></span>

<span data-ttu-id="87cf3-115">Certamente, é possível que um aplicativo defina tabelas de descritor muito grandes quando seus sombreadores desejam ter a liberdade de selecionar de um grande conjunto de descritores disponíveis (geralmente fazendo referência a texturas) em tempo real (talvez orientado por dados materiais).</span><span class="sxs-lookup"><span data-stu-id="87cf3-115">It is certainly possible for an app to define very large descriptor tables when its shaders want the freedom to select from a vast set of available descriptors (often referencing textures) on the fly (perhaps driven by material data).</span></span>

<span data-ttu-id="87cf3-116">A assinatura raiz faz referência à entrada da tabela de descritores com uma referência ao heap, o local de início da tabela (um deslocamento do início do heap) e o comprimento (em entradas) da tabela.</span><span class="sxs-lookup"><span data-stu-id="87cf3-116">The Root Signature references the descriptor table entry with a reference to the heap, the start location of the table (an offset from the start of the heap), and the length (in entries) of the table.</span></span> <span data-ttu-id="87cf3-117">A imagem abaixo mostra esses conceitos: os ponteiros da tabela de descritores da assinatura raiz e os descritores dentro do heap de descritores que fazem referência a dados de textura ou de buffer completos em um heap de carregamento.</span><span class="sxs-lookup"><span data-stu-id="87cf3-117">The image below shows these concepts: the descriptor table pointers from the Root Signature and the descriptors within the descriptor heap referencing the full texture or buffer data in an upload heap.</span></span>

![tabelas de descritores](images/descriptor-table.png)

## <a name="related-topics"></a><span data-ttu-id="87cf3-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87cf3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87cf3-120">Tabelas de descritores</span><span class="sxs-lookup"><span data-stu-id="87cf3-120">Descriptor Tables</span></span>](descriptor-tables.md)
</dt> </dl>

 

 




