---
description: Clonagem e compartilhamento (Direct3D 9)
ms.assetid: 1dabe611-bf3b-49bf-99ab-dbdfd343f885
title: Clonagem e compartilhamento (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 983e674af4cdd24e21fcc2517eb8a32d6aec291c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826645"
---
# <a name="cloning-and-sharing-direct3d-9"></a><span data-ttu-id="d10d8-103">Clonagem e compartilhamento (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d10d8-103">Cloning and Sharing (Direct3D 9)</span></span>

## <a name="cloning-parameters"></a><span data-ttu-id="d10d8-104">Parâmetros de clonagem</span><span class="sxs-lookup"><span data-stu-id="d10d8-104">Cloning Parameters</span></span>

<span data-ttu-id="d10d8-105">A clonagem tem as seguintes restrições.</span><span class="sxs-lookup"><span data-stu-id="d10d8-105">Cloning has the following restrictions.</span></span>

-   <span data-ttu-id="d10d8-106">Os clones herdam o pool do efeito original.</span><span class="sxs-lookup"><span data-stu-id="d10d8-106">Clones inherit the original effect's pool.</span></span> <span data-ttu-id="d10d8-107">Consulte a seção parâmetros de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="d10d8-107">See the Sharing Parameters section.</span></span>
-   <span data-ttu-id="d10d8-108">Os clones herdam as técnicas, passagens, parâmetros e anotações do efeito original (incluindo todas as anotações adicionadas com [**ID3DXEffect**](id3dxeffect.md)).</span><span class="sxs-lookup"><span data-stu-id="d10d8-108">Clones inherit the original effect's techniques, passes, parameters, and annotations (including all annotations added with [**ID3DXEffect**](id3dxeffect.md)).</span></span>
-   <span data-ttu-id="d10d8-109">Os clones herdam as anotações adicionadas dinamicamente do efeito original.</span><span class="sxs-lookup"><span data-stu-id="d10d8-109">Clones inherit the original effect's dynamically added annotations.</span></span>
-   <span data-ttu-id="d10d8-110">A clonagem em um novo dispositivo falhará se o pool do efeito original não for **nulo** e o efeito original contivesse um parâmetro dependente de dispositivo compartilhado (como uma textura ou sombreador).</span><span class="sxs-lookup"><span data-stu-id="d10d8-110">Cloning onto a new device will fail if the original effect's pool was not **NULL** and the original effect contained a shared device-dependent parameter (such as a texture or shader).</span></span>

## <a name="sharing-parameters"></a><span data-ttu-id="d10d8-111">Compartilhando parâmetros</span><span class="sxs-lookup"><span data-stu-id="d10d8-111">Sharing Parameters</span></span>

<span data-ttu-id="d10d8-112">Um pool é um buffer que compartilha parâmetros de efeito entre diferentes efeitos.</span><span class="sxs-lookup"><span data-stu-id="d10d8-112">A pool is a buffer that shares effect parameters between different effects.</span></span> <span data-ttu-id="d10d8-113">Para adicionar parâmetros a um pool, especifique um uso compartilhado quando o efeito for criado.</span><span class="sxs-lookup"><span data-stu-id="d10d8-113">To add parameters to a pool, specify a shared usage when the effect is created.</span></span>

<span data-ttu-id="d10d8-114">Um pool tem as seguintes restrições.</span><span class="sxs-lookup"><span data-stu-id="d10d8-114">A pool has the following restrictions.</span></span>

-   <span data-ttu-id="d10d8-115">Um parâmetro é adicionado ao pool na primeira vez que um efeito contendo esse parâmetro (compartilhado) é adicionado ao pool.</span><span class="sxs-lookup"><span data-stu-id="d10d8-115">A parameter is added to the pool the first time an effect containing that (shared) parameter is added to the pool.</span></span>
-   <span data-ttu-id="d10d8-116">Um pool obtém valores iniciais do primeiro parâmetro compartilhado; os parâmetros compartilhados subsequentemente obtêm seus valores do pool.</span><span class="sxs-lookup"><span data-stu-id="d10d8-116">A pool gets initial values from the first shared parameter; parameters shared subsequently get their values from the pool.</span></span>
-   <span data-ttu-id="d10d8-117">Um parâmetro é excluído do pool quando todas as referências de efeito para o parâmetro compartilhado são liberadas.</span><span class="sxs-lookup"><span data-stu-id="d10d8-117">A parameter is deleted from the pool when all effect references to the shared parameter are released.</span></span>
-   <span data-ttu-id="d10d8-118">Todos os efeitos no pool que contêm o mesmo parâmetro dependente de dispositivo (compartilhado) devem ter o mesmo dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d10d8-118">All effects in the pool that contain the same (shared) device-dependent parameter must have the same device.</span></span>

<span data-ttu-id="d10d8-119">**NULL** pode ser usado para especificar nenhum pool; nesse caso, nenhum parâmetro é compartilhado.</span><span class="sxs-lookup"><span data-stu-id="d10d8-119">**NULL** can be used to specify no pool, in which case no parameters are shared.</span></span> <span data-ttu-id="d10d8-120">Isso é quase equivalente a especificar um pool exclusivo apenas para esse efeito.</span><span class="sxs-lookup"><span data-stu-id="d10d8-120">This is almost equivalent to specifying a unique pool just for this effect.</span></span> <span data-ttu-id="d10d8-121">A única diferença é que, quando o efeito é clonado, o clone não compartilhará seus parâmetros compartilhados com o original.</span><span class="sxs-lookup"><span data-stu-id="d10d8-121">The single difference is that when the effect is cloned, the clone will not share its shared parameters with the original.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d10d8-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d10d8-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d10d8-123">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="d10d8-123">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



