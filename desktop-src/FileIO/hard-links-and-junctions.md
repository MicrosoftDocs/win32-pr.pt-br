---
description: Descreve links e junções difíceis.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Links físicos e junções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760076"
---
# <a name="hard-links-and-junctions"></a><span data-ttu-id="81107-103">Links físicos e junções</span><span class="sxs-lookup"><span data-stu-id="81107-103">Hard Links and Junctions</span></span>

<span data-ttu-id="81107-104">Há três tipos de links de arquivo com suporte no sistema de arquivos NTFS: links físicos, junções e links simbólicos.</span><span class="sxs-lookup"><span data-stu-id="81107-104">There are three types of file links supported in the NTFS file system: hard links, junctions, and symbolic links.</span></span> <span data-ttu-id="81107-105">Este tópico é uma visão geral dos links e junções difíceis.</span><span class="sxs-lookup"><span data-stu-id="81107-105">This topic is an overview of hard links and junctions.</span></span> <span data-ttu-id="81107-106">Para obter informações sobre links simbólicos, consulte [criando links simbólicos](creating-symbolic-links.md).</span><span class="sxs-lookup"><span data-stu-id="81107-106">For information about symbolic links, see [Creating Symbolic Links](creating-symbolic-links.md).</span></span>

## <a name="hard-links"></a><span data-ttu-id="81107-107">Links físicos</span><span class="sxs-lookup"><span data-stu-id="81107-107">Hard Links</span></span>

<span data-ttu-id="81107-108">Um *vínculo físico* é a representação do sistema de arquivos de um arquivo pelo qual mais de um caminho faz referência a um único arquivo no mesmo volume.</span><span class="sxs-lookup"><span data-stu-id="81107-108">A *hard link* is the file system representation of a file by which more than one path references a single file in the same volume.</span></span> <span data-ttu-id="81107-109">Para criar um link físico, use a função [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) .</span><span class="sxs-lookup"><span data-stu-id="81107-109">To create a hard link, use the [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) function.</span></span> <span data-ttu-id="81107-110">Qualquer alteração no arquivo é imediatamente visível para aplicativos que o acessam por meio de links físicos que fazem referência a ele.</span><span class="sxs-lookup"><span data-stu-id="81107-110">Any changes to that file are instantly visible to applications that access it through the hard links that reference it.</span></span> <span data-ttu-id="81107-111">No entanto, as informações de tamanho e atributo de entrada de diretório são atualizadas somente para o link pelo qual a alteração foi feita.</span><span class="sxs-lookup"><span data-stu-id="81107-111">However, the directory entry size and attribute information is updated only for the link through which the change was made.</span></span> <span data-ttu-id="81107-112">Observe que os atributos no arquivo são refletidos em cada link físico para esse arquivo e as alterações nos atributos desse arquivo se propagam para todos os links físicos.</span><span class="sxs-lookup"><span data-stu-id="81107-112">Note that the attributes on the file are reflected in every hard link to that file, and changes to that file's attributes propagate to all the hard links.</span></span> <span data-ttu-id="81107-113">Por exemplo, se você redefinir o atributo READONLY em um link físico para excluir esse link físico específico e houver vários links físicos para o arquivo real, será necessário redefinir o bit READONLY no arquivo de um dos links físicos restantes para trazer o arquivo e todos os links físicos restantes de volta para o estado READONLY.</span><span class="sxs-lookup"><span data-stu-id="81107-113">For example if you reset the READONLY attribute on a hard link to delete that particular hard link, and there are multiple hard links to the actual file, then you will need to reset the READONLY bit on the file from one of the remaining hard links to bring the file and all remaining hard links back to the READONLY state.</span></span>

<span data-ttu-id="81107-114">Por exemplo, em um sistema em que C: e D: são unidades locais e Z: é uma unidade de rede mapeada para \\ \\ Fred \\ share, as seguintes referências são permitidas como um link físico:</span><span class="sxs-lookup"><span data-stu-id="81107-114">For example, in a system where C: and D: are local drives and Z: is a network drive mapped to \\\\fred\\share, the following references are permitted as a hard link:</span></span>

-   <span data-ttu-id="81107-115">C: \\ dira \\ethel.txt vinculado a C: \\ dirb \\ dirc \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="81107-115">C:\\dira\\ethel.txt linked to C:\\dirb\\dirc\\lucy.txt</span></span>
-   <span data-ttu-id="81107-116">D: \\ dir1 \\tinker.txt a D: \\ dir2 \\ Dirx \\bell.txt</span><span class="sxs-lookup"><span data-stu-id="81107-116">D:\\dir1\\tinker.txt to D:\\dir2\\dirx\\bell.txt</span></span>
-   <span data-ttu-id="81107-117">C: \\ diry \\ Bob. bak vinculado a C: \\ dir2 \\mina.txt</span><span class="sxs-lookup"><span data-stu-id="81107-117">C:\\diry\\bob.bak linked to C:\\dir2\\mina.txt</span></span>

<span data-ttu-id="81107-118">Os itens a seguir não são:</span><span class="sxs-lookup"><span data-stu-id="81107-118">The following are not:</span></span>

-   <span data-ttu-id="81107-119">C: \\ dira vinculado a C: \\ dirb</span><span class="sxs-lookup"><span data-stu-id="81107-119">C:\\dira linked to C:\\dirb</span></span>
-   <span data-ttu-id="81107-120">C: \\ dira \\ethel.txt vinculado a D: \\ dirb \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="81107-120">C:\\dira\\ethel.txt linked to D:\\dirb\\lucy.txt</span></span>
-   <span data-ttu-id="81107-121">C: \\ dira \\ethel.txt vinculado a Z: \\ dirb \\lucy.txt</span><span class="sxs-lookup"><span data-stu-id="81107-121">C:\\dira\\ethel.txt linked to Z:\\dirb\\lucy.txt</span></span>

<span data-ttu-id="81107-122">Para excluir um link físico, use a função [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) .</span><span class="sxs-lookup"><span data-stu-id="81107-122">To delete a hard link, use the [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) function.</span></span> <span data-ttu-id="81107-123">Você pode excluir links físicos em qualquer ordem, independentemente da ordem em que eles são criados.</span><span class="sxs-lookup"><span data-stu-id="81107-123">You can delete hard links in any order regardless of the order in which they are created.</span></span>

## <a name="junctions"></a><span data-ttu-id="81107-124">Junções</span><span class="sxs-lookup"><span data-stu-id="81107-124">Junctions</span></span>

<span data-ttu-id="81107-125">Uma *junção* (também chamada de *link suave*) difere de um link físico no qual os objetos de armazenamento referenciados são diretórios separados e uma junção pode vincular diretórios localizados em diferentes volumes locais no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="81107-125">A *junction* (also called a *soft link*) differs from a hard link in that the storage objects it references are separate directories, and a junction can link directories located on different local volumes on the same computer.</span></span> <span data-ttu-id="81107-126">Caso contrário, as junções operam de forma idêntica a links físicos.</span><span class="sxs-lookup"><span data-stu-id="81107-126">Otherwise, junctions operate identically to hard links.</span></span> <span data-ttu-id="81107-127">As junções são implementadas por meio de [pontos de nova análise](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="81107-127">Junctions are implemented through [reparse points](reparse-points.md).</span></span>

<span data-ttu-id="81107-128">Supondo que as mesmas condições na seção de links físicos, as referências a seguir são permitidas como junções:</span><span class="sxs-lookup"><span data-stu-id="81107-128">Assuming the same conditions in the Hard Links section, the following references are permitted as junctions:</span></span>

-   <span data-ttu-id="81107-129">C: \\ dira vinculado a C: \\ dirb \\ dirc</span><span class="sxs-lookup"><span data-stu-id="81107-129">C:\\dira linked to C:\\dirb\\dirc</span></span>
-   <span data-ttu-id="81107-130">C: \\ Dirx vinculado a D: \\ diry</span><span class="sxs-lookup"><span data-stu-id="81107-130">C:\\dirx linked to D:\\diry</span></span>

<span data-ttu-id="81107-131">Os itens a seguir não são:</span><span class="sxs-lookup"><span data-stu-id="81107-131">The following are not:</span></span>

-   <span data-ttu-id="81107-132">C: \\ dira \\one.txt vinculados a C \\ : \\ dirbtwo.txt</span><span class="sxs-lookup"><span data-stu-id="81107-132">C:\\dira\\one.txt linked to C:\\dirb\\two.txt</span></span>
-   <span data-ttu-id="81107-133">C: \\ dir1 vinculado a Z: \\ dir2</span><span class="sxs-lookup"><span data-stu-id="81107-133">C:\\dir1 linked to Z:\\dir2</span></span>

## <a name="related-topics"></a><span data-ttu-id="81107-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="81107-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81107-135">Criando links simbólicos</span><span class="sxs-lookup"><span data-stu-id="81107-135">Creating Symbolic Links</span></span>](creating-symbolic-links.md)
</dt> </dl>

 

 



