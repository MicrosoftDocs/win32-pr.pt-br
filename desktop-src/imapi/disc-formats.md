---
title: Formatos de disco
description: O IMAPi dá suporte a três formatos de sistema de arquivos ISO 9660, Joliet e UDF.
ms.assetid: 9cd782c0-203b-452c-9d04-3464d39453b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9b4d4c5c5b6aa3e0c4c96598486a531c297b61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292211"
---
# <a name="disc-formats"></a><span data-ttu-id="a108a-103">Formatos de disco</span><span class="sxs-lookup"><span data-stu-id="a108a-103">Disc Formats</span></span>

<span data-ttu-id="a108a-104">O IMAPi dá suporte a três formatos de sistema de arquivos: [ISO 9660](#iso-9660), [Joliet](#joliet)e [UDF](#universal-disk-format-udf).</span><span class="sxs-lookup"><span data-stu-id="a108a-104">IMAPI supports three file system formats: [ISO 9660](#iso-9660), [Joliet](#joliet), and [UDF](#universal-disk-format-udf).</span></span>

## <a name="iso-9660"></a><span data-ttu-id="a108a-105">ISO 9660</span><span class="sxs-lookup"><span data-stu-id="a108a-105">ISO 9660</span></span>

<span data-ttu-id="a108a-106">O formato ISO 9660 é o sistema de arquivos padrão original para os discos de dados do CD.</span><span class="sxs-lookup"><span data-stu-id="a108a-106">The ISO 9660 format is the original standard file system for CD data discs.</span></span> <span data-ttu-id="a108a-107">O formato é reconhecido em vários sistemas operacionais, incluindo o MSDOS, o Mac OS, o UNIX e o sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="a108a-107">The format is recognized on several operating systems, including MSDOS, the Mac OS, UNIX, and the Windows operating system.</span></span> <span data-ttu-id="a108a-108">O formato ISO 9660 é publicado pelo Organização Internacional de Normalização (ISO).</span><span class="sxs-lookup"><span data-stu-id="a108a-108">The ISO 9660 format is published by the International Organization for Standardization (ISO).</span></span>

<span data-ttu-id="a108a-109">O formato começa no setor 16 com o cabeçalho do volume, CD0001; segue o restante do cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="a108a-109">The format begins at sector 16 with the volume header, CD0001; the remainder of the header follows.</span></span> <span data-ttu-id="a108a-110">Outros formatos derivados também começam no setor 16, mas usam outra cadeia de caracteres para o cabeçalho do volume.</span><span class="sxs-lookup"><span data-stu-id="a108a-110">Other derived formats also begin at sector 16, but use another string for the volume header.</span></span> <span data-ttu-id="a108a-111">Por exemplo, discos de alta serra usam a cadeia de caracteres CD-ROM0001 e o formato interativo do CD Interactive usam o CD-I0001.</span><span class="sxs-lookup"><span data-stu-id="a108a-111">For example, High Sierra discs use the string CD-ROM0001 and Compact Disc Interactive format uses CD-I0001.</span></span>

<span data-ttu-id="a108a-112">O cabeçalho aponta para áreas do disco que armazenam os nomes de arquivo no formato ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="a108a-112">The header points to areas of the disc that store the file names in ISO 9660 format.</span></span> <span data-ttu-id="a108a-113">A Convenção de nomenclatura de arquivo e diretório consiste em 8 caracteres, um ponto e mais três caracteres.</span><span class="sxs-lookup"><span data-stu-id="a108a-113">The file and directory naming convention consists of 8 characters, a period, and 3 more characters.</span></span> <span data-ttu-id="a108a-114">Essa é a mesma convenção de nomenclatura usada pelo sistema operacional MSDOS.</span><span class="sxs-lookup"><span data-stu-id="a108a-114">This is the same naming convention used by the MSDOS operating system.</span></span>

<span data-ttu-id="a108a-115">Cabeçalhos de sistema de arquivos adicionais, para formatos como Joliet e UDF, podem coexistir em um disco sem afetar a legibilidade do formato ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="a108a-115">Additional file system headers, for formats such as Joliet and UDF, can co-exist on a disc without affecting the readability of the ISO 9660 format.</span></span> <span data-ttu-id="a108a-116">Depois dos índices, um conjunto de arquivos de dados ocupa o disco. Os índices para cada sistema de arquivos referenciam arquivos de dados de forma independente no disco.</span><span class="sxs-lookup"><span data-stu-id="a108a-116">After the indexes, a set of data files occupy the disc. The indexes for each file system independently reference data files on the disc.</span></span>

<span data-ttu-id="a108a-117">A especificação ISO 9660 define três níveis do formato:</span><span class="sxs-lookup"><span data-stu-id="a108a-117">The ISO 9660 specification defines three levels of the format:</span></span>

-   <span data-ttu-id="a108a-118">O nível 1 define os nomes de arquivo para usar o formato de caractere 8,3.</span><span class="sxs-lookup"><span data-stu-id="a108a-118">Level 1 defines file names to use the 8.3 character format.</span></span>
-   <span data-ttu-id="a108a-119">O nível 2 permite nomes de arquivo mais longos, conforme encontrado em plataformas DOS 6. XX, MacIntosh e UNIX.</span><span class="sxs-lookup"><span data-stu-id="a108a-119">Level 2 permits longer file names, as found on DOS 6.xx, MacIntosh, and UNIX platforms.</span></span>
-   <span data-ttu-id="a108a-120">O nível 3 permite dados intercalados e arquivos de áudio para melhorar o desempenho da recuperação (reprodução).</span><span class="sxs-lookup"><span data-stu-id="a108a-120">Level 3 allows interleaved data and audio files to improve retrieval (playback) performance.</span></span> <span data-ttu-id="a108a-121">Esse nível também remove o limite de arquivos de 2GB.</span><span class="sxs-lookup"><span data-stu-id="a108a-121">This level also removes the 2GB file limit.</span></span> <span data-ttu-id="a108a-122">**Não** há suporte para esse nível na API de mestre de imagem.</span><span class="sxs-lookup"><span data-stu-id="a108a-122">This level is **not** supported by the Image Mastering API.</span></span>

<span data-ttu-id="a108a-123">Os discos de DVD também podem usar o ISO 9660; no entanto, o sistema de arquivos UDF é o sistema de arquivos mais predominante usado com mídia de DVD.</span><span class="sxs-lookup"><span data-stu-id="a108a-123">DVD discs can also use ISO 9660; however, the UDF file system is the most prevalent file system used with DVD media.</span></span>

## <a name="joliet"></a><span data-ttu-id="a108a-124">Joliet</span><span class="sxs-lookup"><span data-stu-id="a108a-124">Joliet</span></span>

<span data-ttu-id="a108a-125">O formato Joliet é um derivativo do ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="a108a-125">The Joliet format is a derivative of ISO 9660.</span></span> <span data-ttu-id="a108a-126">Esse formato grava o índice do sistema de arquivos Joliet na imagem do disco, além do índice do sistema de arquivos ISO 9660.</span><span class="sxs-lookup"><span data-stu-id="a108a-126">This format writes the Joliet file system index to the disc image in addition to the ISO 9660 file system index.</span></span>

<span data-ttu-id="a108a-127">O índice Joliet fornece os seguintes aprimoramentos para o índice do sistema de arquivos:</span><span class="sxs-lookup"><span data-stu-id="a108a-127">The Joliet index provides the following improvements to the file system index:</span></span>

-   <span data-ttu-id="a108a-128">Reconhece nomes de arquivo longos de até 32 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a108a-128">Recognizes long file names up to 32 characters.</span></span>
-   <span data-ttu-id="a108a-129">Distingue entre letras maiúsculas e minúsculas nos nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a108a-129">Distinguishes between upper and lower case letters in the file names.</span></span>
-   <span data-ttu-id="a108a-130">Dá suporte a caracteres Unicode no nome do arquivo.</span><span class="sxs-lookup"><span data-stu-id="a108a-130">Supports Unicode characters in the filename.</span></span>

<span data-ttu-id="a108a-131">O cabeçalho de formato Joliet começa no setor 17 do disco.</span><span class="sxs-lookup"><span data-stu-id="a108a-131">The Joliet format header begins at sector 17 of the disc.</span></span>

<span data-ttu-id="a108a-132">Como o formato Joliet preserva o sistema de arquivos ISO 9660 em um disco, a compatibilidade com dispositivos ISO 9660 em conformidade é mantida.</span><span class="sxs-lookup"><span data-stu-id="a108a-132">Because the Joliet format preserves the ISO 9660 file system on a disc, compatibility with ISO 9660-compliant devices is retained.</span></span>

## <a name="universal-disk-format-udf"></a><span data-ttu-id="a108a-133">UDF (Formato de Disco Universal)</span><span class="sxs-lookup"><span data-stu-id="a108a-133">Universal Disk Format (UDF)</span></span>

<span data-ttu-id="a108a-134">O UDF (formato de disco universal) é um sistema de arquivos mais recente desenvolvido para mídia óptica pela OSTA (Associação de tecnologia de armazenamento óptico).</span><span class="sxs-lookup"><span data-stu-id="a108a-134">The Universal Disk Format (UDF) is a newer file system developed for optical media by the Optical Storage Technology Association (OSTA).</span></span> <span data-ttu-id="a108a-135">UDF é um formato portátil que é reconhecido por vários sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="a108a-135">UDF is a portable format that is recognized by several operating systems.</span></span> <span data-ttu-id="a108a-136">O UDF está substituindo o ISO 9660 como o novo padrão, especialmente com mídia de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a108a-136">UDF is replacing ISO 9660 as the new standard, especially with read/write media.</span></span>

<span data-ttu-id="a108a-137">Os recursos do UDF incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a108a-137">Features of UDF include the following:</span></span>

-   <span data-ttu-id="a108a-138">Dá suporte à mídia de até 2TB de tamanho.</span><span class="sxs-lookup"><span data-stu-id="a108a-138">Supports media up to 2TB in size.</span></span>
-   <span data-ttu-id="a108a-139">Dá suporte a Flash Media, discos Iomega REV e discos CD-MRW.</span><span class="sxs-lookup"><span data-stu-id="a108a-139">Supports flash media, Iomega REV discs, and CD-MRW discs.</span></span>
-   <span data-ttu-id="a108a-140">Armazena arquivos com menos de 2 KB de comprimento no bloco de entrada de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a108a-140">Stores files less than 2 KB in length in the File Entry block.</span></span>
-   <span data-ttu-id="a108a-141">Dá suporte a arquivos de até 2TB com nomes de arquivo, desde 255 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a108a-141">Supports files up to 2TB with filenames as long as 255 characters.</span></span>
-   <span data-ttu-id="a108a-142">O oferece suporte a um conjunto avançado de atributos de arquivo que atendam a vários sistemas operacionais.</span><span class="sxs-lookup"><span data-stu-id="a108a-142">Supports a rich set of file attributes that suit various operating systems.</span></span>
-   <span data-ttu-id="a108a-143">Dá suporte a um formato de ponte em que os formatos ISO 9660, Joliet e UDF residem no mesmo disco. Isso é usado em aplicativos de vídeo, como DVD-Video, DVD + VR e DVD-VR.</span><span class="sxs-lookup"><span data-stu-id="a108a-143">Supports a bridge format where ISO 9660, Joliet, and UDF formats all reside on the same disc. This is used in video applications, such as DVD-Video, DVD+VR, and DVD-VR.</span></span>
-   <span data-ttu-id="a108a-144">Dá suporte a fluxos nomeados e arquivos ' em tempo real '.</span><span class="sxs-lookup"><span data-stu-id="a108a-144">Supports named streams and 'Real-Time' files.</span></span>

 

 




