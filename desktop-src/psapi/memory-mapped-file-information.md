---
title: Informações do arquivo de Memory-Mapped
description: Um arquivo mapeado para memória (ou mapeamento de arquivo) é o resultado da Associação de um conteúdo de arquivo com uma parte do espaço de endereço virtual de um processo. Ele pode ser usado para compartilhar um arquivo ou memória entre dois ou mais processos.
ms.assetid: b6ec2bc4-c504-4d0b-87f0-39bb1949accd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc6d33e7f3fe6bef36ea6e5a7f355b780d89b7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084804"
---
# <a name="memory-mapped-file-information"></a><span data-ttu-id="fef0c-104">Informações do arquivo de Memory-Mapped</span><span class="sxs-lookup"><span data-stu-id="fef0c-104">Memory-Mapped File Information</span></span>

<span data-ttu-id="fef0c-105">Um *arquivo mapeado para memória* (ou *mapeamento de arquivo*) é o resultado da Associação de um conteúdo de arquivo com uma parte do espaço de endereço virtual de um processo.</span><span class="sxs-lookup"><span data-stu-id="fef0c-105">A *memory-mapped file* (or *file mapping*) is the result of associating a file's contents with a portion of the virtual address space of a process.</span></span> <span data-ttu-id="fef0c-106">Ele pode ser usado para compartilhar um arquivo ou memória entre dois ou mais processos.</span><span class="sxs-lookup"><span data-stu-id="fef0c-106">It can be used to share a file or memory between two or more processes.</span></span>

<span data-ttu-id="fef0c-107">A função [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) recebe um identificador de processo e um ponteiro para um endereço como entrada.</span><span class="sxs-lookup"><span data-stu-id="fef0c-107">The [**GetMappedFileName**](/windows/desktop/api/Psapi/nf-psapi-getmappedfilenamea) function receives a process handle and a pointer to an address as input.</span></span> <span data-ttu-id="fef0c-108">Se o endereço estiver dentro de um arquivo mapeado por memória no espaço de endereço virtual do processo, a função retornará o nome do arquivo mapeado para a memória.</span><span class="sxs-lookup"><span data-stu-id="fef0c-108">If the address is within a memory-mapped file in the virtual address space of the process, the function returns the name of the memory-mapped file.</span></span> <span data-ttu-id="fef0c-109">Os nomes de arquivo retornados por **GetMappedFileName** usam o formulário de dispositivo, em vez de letras de unidade.</span><span class="sxs-lookup"><span data-stu-id="fef0c-109">The file names returned by **GetMappedFileName** use device form, rather than drive letters.</span></span> <span data-ttu-id="fef0c-110">Por exemplo, o nome do arquivo c: \\ WinNT \\ System32 \\ CType. NLS teria esta aparência no formato do dispositivo:</span><span class="sxs-lookup"><span data-stu-id="fef0c-110">For example, the file name c:\\winnt\\system32\\ctype.nls would look like this in device form:</span></span>

<span data-ttu-id="fef0c-111">\\Device \\ Harddisk0 \\ Partition1 \\ WinNT \\ System32 \\ CType. NLS</span><span class="sxs-lookup"><span data-stu-id="fef0c-111">\\Device\\Harddisk0\\Partition1\\WINNT\\System32\\ctype.nls</span></span>

<span data-ttu-id="fef0c-112">Para obter mais informações sobre arquivos mapeados para memória, consulte [mapeamento de arquivo](/windows/desktop/Memory/file-mapping).</span><span class="sxs-lookup"><span data-stu-id="fef0c-112">For more information about memory-mapped files, see [File Mapping](/windows/desktop/Memory/file-mapping).</span></span> <span data-ttu-id="fef0c-113">Para obter um exemplo que converte nomes de arquivo em formato de dispositivo em letras de unidade, consulte [obtendo um nome de arquivo de um identificador de arquivo](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span><span class="sxs-lookup"><span data-stu-id="fef0c-113">For an example that converts file names in device form to drive letters, see [Obtaining a File Name From a File Handle](/windows/desktop/Memory/obtaining-a-file-name-from-a-file-handle).</span></span>

 

 