---
description: Para obter o tamanho compactado de um arquivo, use a função GetCompressedFileSize.
ms.assetid: c6bfd221-f125-48b4-b38b-822a23639c40
title: Obtendo o tamanho de um arquivo compactado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4954a53184e55341838fef7cd70f01639f13bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501987"
---
# <a name="obtaining-the-size-of-a-compressed-file"></a><span data-ttu-id="c04b2-103">Obtendo o tamanho de um arquivo compactado</span><span class="sxs-lookup"><span data-stu-id="c04b2-103">Obtaining the Size of a Compressed File</span></span>

<span data-ttu-id="c04b2-104">Use a função [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) para obter o tamanho compactado de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c04b2-104">Use the [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) function to obtain the compressed size of a file.</span></span> <span data-ttu-id="c04b2-105">Se o arquivo estiver compactado, seu tamanho compactado será menor que seu tamanho descompactado.</span><span class="sxs-lookup"><span data-stu-id="c04b2-105">If the file is compressed, its compressed size will be less than its uncompressed size.</span></span> <span data-ttu-id="c04b2-106">Use a função [**GetFiles**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) para determinar o tamanho descompactado de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="c04b2-106">Use the [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function to determine the uncompressed size of a file.</span></span>

 

 



