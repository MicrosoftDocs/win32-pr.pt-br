---
title: Alocação de espaço em disco para o arquivo de captura
description: Alocação de espaço em disco para o arquivo de captura
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- WM_CAP_FILE_ALLOCATE mensagem
- macro capFileAlloc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292096"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a><span data-ttu-id="29677-105">Alocação de espaço em disco para o arquivo de captura</span><span class="sxs-lookup"><span data-stu-id="29677-105">Disk Space Preallocation for the Capture File</span></span>

<span data-ttu-id="29677-106">A alocação de espaço em disco para o arquivo de captura cria um arquivo de um tamanho especificado no disco antes do início de uma operação de captura.</span><span class="sxs-lookup"><span data-stu-id="29677-106">Preallocating disk space for the capture file builds a file of a specified size on the disk before the start of a capture operation.</span></span> <span data-ttu-id="29677-107">A alocação de um arquivo de captura reduz o processamento necessário enquanto a captura está em andamento e resulta em menos quadros descartados.</span><span class="sxs-lookup"><span data-stu-id="29677-107">Preallocating a capture file reduces the processing required while capture is in progress and results in fewer dropped frames.</span></span> <span data-ttu-id="29677-108">Você pode prealocar um arquivo de captura usando a mensagem de [**alocação de arquivo do WM \_ \_ \_ Cap**](wm-cap-file-allocate.md) (ou a macro [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) ).</span><span class="sxs-lookup"><span data-stu-id="29677-108">You can preallocate a capture file by using the [**WM\_CAP\_FILE\_ALLOCATE**](wm-cap-file-allocate.md) message (or the [**capFileAlloc**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc) macro).</span></span>

<span data-ttu-id="29677-109">Normalmente, seu aplicativo deve prealocar espaço em disco suficiente para conter o maior arquivo de captura previsto.</span><span class="sxs-lookup"><span data-stu-id="29677-109">Typically, your application should preallocate enough disk space to contain the largest capture file anticipated.</span></span> <span data-ttu-id="29677-110">A alocação de espaço em disco não restringe o tamanho do arquivo capturado.</span><span class="sxs-lookup"><span data-stu-id="29677-110">Preallocating disk space does not restrict the size of the captured file.</span></span> <span data-ttu-id="29677-111">O tamanho do arquivo será automaticamente ampliado se os dados capturados excederem o espaço alocado.</span><span class="sxs-lookup"><span data-stu-id="29677-111">The file size is automatically enlarged if the captured data exceeds the allocated space.</span></span> <span data-ttu-id="29677-112">As operações de gravação subsequentes no arquivo de captura reutilizam as partes do espaço em disco alocadas para o arquivo, preservando o tamanho e a fragmentação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="29677-112">Subsequent write operations to the capture file reuse the portions of disk space allocated for the file, preserving the size and fragmentation of the file.</span></span>

<span data-ttu-id="29677-113">Você também pode melhorar o desempenho de captura desfragmentando o arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="29677-113">You can also improve capture performance by defragmenting the capture file.</span></span> <span data-ttu-id="29677-114">Para desfragmentar o arquivo, use um utilitário de desfragmentação, como o Desfragmentador de disco.</span><span class="sxs-lookup"><span data-stu-id="29677-114">To defragment the file, use a defragmentation utility such as Disk Defragmenter.</span></span> <span data-ttu-id="29677-115">Se você usar um arquivo de captura desfragmentado e mais tarde aumentá-lo, Desfragmente o arquivo ampliado.</span><span class="sxs-lookup"><span data-stu-id="29677-115">If you use a defragmented capture file and later enlarge it, you should defragment the enlarged file.</span></span> <span data-ttu-id="29677-116">A ampliação de um arquivo de captura desfragmentado pode fragmentar a parte expandida do arquivo e reduzir o desempenho na operação de captura.</span><span class="sxs-lookup"><span data-stu-id="29677-116">Enlarging a defragmented capture file can fragment the expanded portion of the file and reduce performance in the capture operation.</span></span>

<span data-ttu-id="29677-117">Você também pode melhorar o desempenho usando um disco descompactado para captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="29677-117">You might also improve performance by using an uncompressed disk for video capture.</span></span> <span data-ttu-id="29677-118">A compactação de dados durante a captura pode limitar a taxa de transferência de captura para o disco.</span><span class="sxs-lookup"><span data-stu-id="29677-118">Compressing data during capture can limit capture throughput to the disk.</span></span>

<span data-ttu-id="29677-119">Um aplicativo pode reservar um arquivo de captura permanente para eliminar o tempo necessário para prealocar e desfragmentar um arquivo toda vez que ele for iniciado.</span><span class="sxs-lookup"><span data-stu-id="29677-119">An application can reserve a permanent capture file to eliminate the time required to preallocate and defragment a file each time it is started.</span></span> <span data-ttu-id="29677-120">Como um arquivo de captura pode exigir um espaço considerável em disco e a alocação de um arquivo de captura remove todos os dados de um arquivo de captura existente, um aplicativo deve permitir que o usuário decida se o arquivo é permanente ou temporário.</span><span class="sxs-lookup"><span data-stu-id="29677-120">Because a capture file can require considerable disk space, and preallocating a capture file removes all data from an existing capture file, an application should let the user decide if the file is permanent or temporary.</span></span>

 

 




