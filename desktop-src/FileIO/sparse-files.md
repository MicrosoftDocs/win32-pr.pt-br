---
description: A compactação de arquivos que contêm principalmente zeros faz uso eficiente do espaço em disco.
ms.assetid: 7326041d-f11e-4b80-ac4e-07173e418ce7
title: Arquivos esparsos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c282ca89c9dc9e44800a2a7fc969c3f883006b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778769"
---
# <a name="sparse-files"></a><span data-ttu-id="2e485-103">Arquivos esparsos</span><span class="sxs-lookup"><span data-stu-id="2e485-103">Sparse Files</span></span>

<span data-ttu-id="2e485-104">Um arquivo no qual muitos dos dados são considerados zeros deve conter um conjunto de *dados esparsos*.</span><span class="sxs-lookup"><span data-stu-id="2e485-104">A file in which much of the data is zeros is said to contain a *sparse data set*.</span></span> <span data-ttu-id="2e485-105">Arquivos como esses são normalmente muito grandes, por exemplo, um arquivo que contém dados de imagem a serem processados ou uma matriz em um banco de dados de alta velocidade.</span><span class="sxs-lookup"><span data-stu-id="2e485-105">Files like these are typically very large for example, a file that contains image data to be processed or a matrix within a high-speed database.</span></span> <span data-ttu-id="2e485-106">O problema com arquivos que contêm conjuntos de dados esparsos é que a maioria do arquivo não contém dados úteis e, por isso, eles são um uso ineficiente de espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="2e485-106">The problem with files that contain sparse data sets is that the majority of the file does not contain useful data and, because of this, they are an inefficient use of disk space.</span></span>

<span data-ttu-id="2e485-107">A compactação de arquivo no sistema de arquivos NTFS é uma solução parcial para o problema.</span><span class="sxs-lookup"><span data-stu-id="2e485-107">The file compression in the NTFS file system is a partial solution to the problem.</span></span> <span data-ttu-id="2e485-108">Todos os dados no arquivo que não são explicitamente gravados são explicitamente definidos como zero.</span><span class="sxs-lookup"><span data-stu-id="2e485-108">All data in the file that is not explicitly written is explicitly set to zero.</span></span> <span data-ttu-id="2e485-109">A compactação de arquivo compacta esses intervalos de zeros.</span><span class="sxs-lookup"><span data-stu-id="2e485-109">File compression compacts these ranges of zeros.</span></span> <span data-ttu-id="2e485-110">No entanto, uma desvantagem da compactação de arquivos é que o tempo de acesso pode aumentar devido à compactação e descompactação de dados.</span><span class="sxs-lookup"><span data-stu-id="2e485-110">However, a drawback of file compression is that access time may increase due to data compression and decompression.</span></span>

<span data-ttu-id="2e485-111">O suporte para arquivos esparsos é introduzido no sistema de arquivos NTFS como outra maneira de tornar o uso do espaço em disco mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="2e485-111">Support for sparse files is introduced in the NTFS file system as another way to make disk space usage more efficient.</span></span> <span data-ttu-id="2e485-112">Quando a funcionalidade de arquivo esparso está habilitada, o sistema não aloca espaço de disco rígido para um arquivo, exceto em regiões em que ele contém dados sem zero.</span><span class="sxs-lookup"><span data-stu-id="2e485-112">When sparse file functionality is enabled, the system does not allocate hard disk drive space to a file except in regions where it contains nonzero data.</span></span> <span data-ttu-id="2e485-113">Quando uma operação de gravação é tentada onde uma grande quantidade de dados no buffer é zero, os zeros não são gravados no arquivo.</span><span class="sxs-lookup"><span data-stu-id="2e485-113">When a write operation is attempted where a large amount of the data in the buffer is zeros, the zeros are not written to the file.</span></span> <span data-ttu-id="2e485-114">Em vez disso, o sistema de arquivos cria uma lista interna contendo os locais dos zeros no arquivo e essa lista é consultada durante todas as operações de leitura.</span><span class="sxs-lookup"><span data-stu-id="2e485-114">Instead, the file system creates an internal list containing the locations of the zeros in the file, and this list is consulted during all read operations.</span></span> <span data-ttu-id="2e485-115">Quando uma operação de leitura é executada em áreas do arquivo em que os zeros foram localizados, o sistema de arquivos retorna o número apropriado de zeros no buffer alocado para a operação de leitura.</span><span class="sxs-lookup"><span data-stu-id="2e485-115">When a read operation is performed in areas of the file where zeros were located, the file system returns the appropriate number of zeros in the buffer allocated for the read operation.</span></span> <span data-ttu-id="2e485-116">Dessa forma, a manutenção do arquivo esparso é transparente para todos os processos que o acessam e é mais eficiente do que a compactação para esse cenário específico.</span><span class="sxs-lookup"><span data-stu-id="2e485-116">In this way, maintenance of the sparse file is transparent to all processes that access it, and is more efficient than compression for this particular scenario.</span></span>

<span data-ttu-id="2e485-117">O valor de dados padrão de um arquivo esparso é zero; no entanto, ele pode ser definido como outros valores.</span><span class="sxs-lookup"><span data-stu-id="2e485-117">The default data value of a sparse file is zero; however, it can be set to other values.</span></span>

<span data-ttu-id="2e485-118">Para obter mais informações sobre arquivos esparsos, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="2e485-118">For more information about sparse files, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2e485-119">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="2e485-119">In this section</span></span>



| <span data-ttu-id="2e485-120">Tópico</span><span class="sxs-lookup"><span data-stu-id="2e485-120">Topic</span></span>                                                                                     | <span data-ttu-id="2e485-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="2e485-121">Description</span></span>                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e485-122">Operações de arquivo esparsos</span><span class="sxs-lookup"><span data-stu-id="2e485-122">Sparse File Operations</span></span>](sparse-file-operations.md)<br/>                           | <span data-ttu-id="2e485-123">Determine se um sistema de arquivos dá suporte a arquivos esparsos chamando a função GetVolumeInformation.</span><span class="sxs-lookup"><span data-stu-id="2e485-123">Determine whether a file system supports sparse files by calling the GetVolumeInformation function.</span></span><br/>                                                                                |
| [<span data-ttu-id="2e485-124">Obtendo o tamanho de um arquivo esparso</span><span class="sxs-lookup"><span data-stu-id="2e485-124">Obtaining the Size of a Sparse File</span></span>](obtaining-the-size-of-a-sparse-file.md)<br/> | <span data-ttu-id="2e485-125">Obtenha o tamanho alocado ou o tamanho total de um arquivo usando a função [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) ou [**GetFiles**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) .</span><span class="sxs-lookup"><span data-stu-id="2e485-125">Get the allocated size or the total size for a file by using either the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) or the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function.</span></span><br/> |
| [<span data-ttu-id="2e485-126">Arquivos esparsos e cotas de disco</span><span class="sxs-lookup"><span data-stu-id="2e485-126">Sparse Files and Disk Quotas</span></span>](sparse-files-and-disk-quota.md)<br/>                | <span data-ttu-id="2e485-127">Um arquivo esparso afeta as cotas de usuário pelo tamanho nominal do arquivo, não pela quantidade real alocada de espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="2e485-127">A sparse file affects user quotas by the nominal size of the file, not the actual allocated amount of disk space.</span></span><br/>                                                                  |



 

 

 




