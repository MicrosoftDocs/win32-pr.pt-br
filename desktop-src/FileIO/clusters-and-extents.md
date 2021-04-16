---
description: 'Os clusters podem ser referidos de duas perspectivas diferentes: dentro do arquivo e no volume.'
ms.assetid: 8e999524-4fe9-49b0-8b59-081fa7a42c72
title: Clusters e extensões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6b379e0dbc4f70ccf001f0be0517e25c0c99a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761737"
---
# <a name="clusters-and-extents"></a><span data-ttu-id="c4e56-103">Clusters e extensões</span><span class="sxs-lookup"><span data-stu-id="c4e56-103">Clusters and Extents</span></span>

<span data-ttu-id="c4e56-104">Os clusters podem ser referidos de duas perspectivas diferentes: dentro do arquivo e no volume.</span><span class="sxs-lookup"><span data-stu-id="c4e56-104">Clusters may be referred to from two different perspectives: within the file and on the volume.</span></span> <span data-ttu-id="c4e56-105">Qualquer cluster em um arquivo tem um VCN ( *número de cluster virtual* ), que é seu deslocamento relativo desde o início do arquivo.</span><span class="sxs-lookup"><span data-stu-id="c4e56-105">Any cluster in a file has a *virtual cluster number* (VCN), which is its relative offset from the beginning of the file.</span></span> <span data-ttu-id="c4e56-106">Por exemplo, uma busca duas vezes o tamanho de um cluster, seguido por uma leitura, retornará dados que começam no terceiro VCN.</span><span class="sxs-lookup"><span data-stu-id="c4e56-106">For example, a seek to twice the size of a cluster, followed by a read, will return data beginning at the third VCN.</span></span> <span data-ttu-id="c4e56-107">Um LCN ( *número de cluster lógico* ) descreve o deslocamento de um cluster de um ponto arbitrário dentro do volume.</span><span class="sxs-lookup"><span data-stu-id="c4e56-107">A *logical cluster number* (LCN) describes the offset of a cluster from some arbitrary point within the volume.</span></span> <span data-ttu-id="c4e56-108">LCNs deve ser tratado somente como números ordinais ou relativos.</span><span class="sxs-lookup"><span data-stu-id="c4e56-108">LCNs should be treated only as ordinal, or relative, numbers.</span></span> <span data-ttu-id="c4e56-109">Não há nenhum mapeamento garantido de clusters lógicos para setores de unidade de disco rígido físico.</span><span class="sxs-lookup"><span data-stu-id="c4e56-109">There is no guaranteed mapping of logical clusters to physical hard disk drive sectors.</span></span>

<span data-ttu-id="c4e56-110">Uma *extensão* é uma execução de clusters contíguos.</span><span class="sxs-lookup"><span data-stu-id="c4e56-110">An *extent* is a run of contiguous clusters.</span></span> <span data-ttu-id="c4e56-111">Por exemplo, suponha que um arquivo que consiste em 30 clusters seja gravado em duas extensões.</span><span class="sxs-lookup"><span data-stu-id="c4e56-111">For example, suppose a file consisting of 30 clusters is recorded in two extents.</span></span> <span data-ttu-id="c4e56-112">A primeira extensão pode consistir em cinco clusters contíguos, o outro dos 25 clusters restantes.</span><span class="sxs-lookup"><span data-stu-id="c4e56-112">The first extent might consist of five contiguous clusters, the other of the remaining 25 clusters.</span></span>

<span data-ttu-id="c4e56-113">Não há nenhuma garantia de nenhuma relação no disco de qualquer extensão para qualquer outra extensão.</span><span class="sxs-lookup"><span data-stu-id="c4e56-113">There is no guarantee of any relationship on the disk of any extent to any other extent.</span></span> <span data-ttu-id="c4e56-114">Por exemplo, a primeira extensão pode estar em um LCN maior do que uma extensão subsequente.</span><span class="sxs-lookup"><span data-stu-id="c4e56-114">For example, the first extent may be at a higher LCN than a subsequent extent.</span></span>

 

 



