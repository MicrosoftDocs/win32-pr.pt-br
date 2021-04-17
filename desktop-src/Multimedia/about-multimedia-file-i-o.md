---
title: Sobre e/s de arquivo multimídia
description: Sobre e/s de arquivo multimídia
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Multimídia do Windows, e/s de arquivo
- multimídia, e/s de arquivo
- entrada de multimídia, e/s de arquivo
- e/s de arquivo multimídia, sobre
- e/s de arquivo, sobre
- entrada e saída (e/s), sobre
- E/s (entrada e saída), sobre
- e/s básica
- formato de arquivo de intercâmbio de recursos (RIFF)
- RIFF (formato de arquivo de intercâmbio de recursos)
- E/S DO RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fa055411819d719636d2e248ea5c565e3f060d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105790028"
---
# <a name="about-multimedia-file-io"></a><span data-ttu-id="34d47-114">Sobre e/s de arquivo multimídia</span><span class="sxs-lookup"><span data-stu-id="34d47-114">About Multimedia File I/O</span></span>

<span data-ttu-id="34d47-115">A maioria dos aplicativos de multimídia requer entrada e saída (e/s) de arquivo, ou seja, a capacidade de criar, ler e gravar arquivos de disco.</span><span class="sxs-lookup"><span data-stu-id="34d47-115">Most multimedia applications require file input and output (I/O) — that is, the ability to create, read, and write disk files.</span></span> <span data-ttu-id="34d47-116">Os serviços de e/s de arquivo de multimídia fornecem e/s de arquivo em buffer e sem buffer e dão suporte a arquivos RIFF.</span><span class="sxs-lookup"><span data-stu-id="34d47-116">Multimedia file I/O services provide buffered and unbuffered file I/O and support for RIFF files.</span></span> <span data-ttu-id="34d47-117">Os serviços são extensíveis com procedimentos de e/s personalizados que podem ser compartilhados entre aplicativos.</span><span class="sxs-lookup"><span data-stu-id="34d47-117">The services are extensible with custom I/O procedures that can be shared among applications.</span></span>

<span data-ttu-id="34d47-118">A maioria dos aplicativos precisa apenas dos serviços de e/s de arquivo básico e dos serviços de e/s de arquivo RIFF.</span><span class="sxs-lookup"><span data-stu-id="34d47-118">Most applications need only the basic file I/O services and the RIFF file I/O services.</span></span> <span data-ttu-id="34d47-119">Aplicativos sensíveis a desempenho de e/s de arquivo, como aplicativos que transmitem dados de um CD em tempo real, podem otimizar o desempenho usando serviços para acessar diretamente o buffer de e/s de arquivo.</span><span class="sxs-lookup"><span data-stu-id="34d47-119">Applications sensitive to file I/O performance, such as applications that stream data from compact disc in real time, can optimize performance by using services to directly access the file I/O buffer.</span></span> <span data-ttu-id="34d47-120">Os aplicativos que acessam sistemas de armazenamento personalizados, como arquivos mortos de arquivos e bancos de dados, podem fornecer seu próprio procedimento de e/s que lê e grava elementos do sistema de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="34d47-120">Applications that access custom storage systems, such as file archives and databases, can provide their own I/O procedure that reads and writes elements of the storage system.</span></span>

 

 




