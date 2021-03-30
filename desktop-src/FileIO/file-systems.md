---
description: Gerenciar diretórios com tabela de entrada de diretório, identificadores de diretório, pontos de nova análise.
title: Sistemas de arquivos locais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92f624ef1999b81adb63ba1d5b7e349259cabd53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661796"
---
# <a name="local-file-systems"></a><span data-ttu-id="5700f-103">Sistemas de arquivos locais</span><span class="sxs-lookup"><span data-stu-id="5700f-103">Local File Systems</span></span>

<span data-ttu-id="5700f-104">Um *sistema de arquivos* permite que os aplicativos armazenem e recuperem arquivos em dispositivos de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5700f-104">A *file system* enables applications to store and retrieve files on storage devices.</span></span> <span data-ttu-id="5700f-105">Os arquivos são colocados em uma estrutura hierárquica.</span><span class="sxs-lookup"><span data-stu-id="5700f-105">Files are placed in a hierarchical structure.</span></span> <span data-ttu-id="5700f-106">O sistema de arquivos especifica convenções de nomenclatura para arquivos e o formato para especificar o caminho para um arquivo na estrutura de árvore.</span><span class="sxs-lookup"><span data-stu-id="5700f-106">The file system specifies naming conventions for files and the format for specifying the path to a file in the tree structure.</span></span>

<span data-ttu-id="5700f-107">Cada sistema de arquivos consiste em um ou mais drivers e bibliotecas de vínculo dinâmico que definem os formatos de dados e os recursos do sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="5700f-107">Each file system consists of one or more drivers and dynamic-link libraries that define the data formats and features of the file system.</span></span> <span data-ttu-id="5700f-108">Os sistemas de arquivos podem existir em vários tipos diferentes de dispositivos de armazenamento, incluindo discos rígidos, jukeboxes, discos ópticos removíveis, unidades de backup de fita e cartões de memória.</span><span class="sxs-lookup"><span data-stu-id="5700f-108">File systems can exist on many different types of storage devices, including hard disks, jukeboxes, removable optical disks, tape back-up units, and memory cards.</span></span>

<span data-ttu-id="5700f-109">Todos os sistemas de arquivos com suporte do Windows têm os seguintes componentes de armazenamento:</span><span class="sxs-lookup"><span data-stu-id="5700f-109">All file systems supported by Windows have the following storage components:</span></span>

-   <span data-ttu-id="5700f-110">Volumes.</span><span class="sxs-lookup"><span data-stu-id="5700f-110">Volumes.</span></span> <span data-ttu-id="5700f-111">Um *volume* é uma coleção de diretórios e arquivos.</span><span class="sxs-lookup"><span data-stu-id="5700f-111">A *volume* is a collection of directories and files.</span></span>
-   <span data-ttu-id="5700f-112">Listas.</span><span class="sxs-lookup"><span data-stu-id="5700f-112">Directories.</span></span> <span data-ttu-id="5700f-113">Um *diretório* é uma coleção hierárquica de diretórios e arquivos.</span><span class="sxs-lookup"><span data-stu-id="5700f-113">A *directory* is a hierarchical collection of directories and files.</span></span>
-   <span data-ttu-id="5700f-114">Arquivos.</span><span class="sxs-lookup"><span data-stu-id="5700f-114">Files.</span></span> <span data-ttu-id="5700f-115">Um *arquivo* é um agrupamento lógico de dados relacionados.</span><span class="sxs-lookup"><span data-stu-id="5700f-115">A *file* is a logical grouping of related data.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5700f-116">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="5700f-116">In this section</span></span>



| <span data-ttu-id="5700f-117">Tópico</span><span class="sxs-lookup"><span data-stu-id="5700f-117">Topic</span></span>                                                                | <span data-ttu-id="5700f-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="5700f-118">Description</span></span>                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5700f-119">Gerenciamento de diretórios</span><span class="sxs-lookup"><span data-stu-id="5700f-119">Directory Management</span></span>](directory-management.md)<br/>          | <span data-ttu-id="5700f-120">Um *diretório* é uma coleção hierárquica de diretórios e arquivos.</span><span class="sxs-lookup"><span data-stu-id="5700f-120">A *directory* is a hierarchical collection of directories and files.</span></span> <span data-ttu-id="5700f-121">A única restrição no número de arquivos que podem estar contidos em um único diretório é o tamanho físico do disco no qual o diretório está localizado.</span><span class="sxs-lookup"><span data-stu-id="5700f-121">The only constraint on the number of files that can be contained in a single directory is the physical size of the disk on which the directory is located.</span></span><br/> |
| [<span data-ttu-id="5700f-122">Gerenciamento de disco</span><span class="sxs-lookup"><span data-stu-id="5700f-122">Disk Management</span></span>](disk-management.md)<br/>                    | <span data-ttu-id="5700f-123">Um *disco rígido* é uma unidade rígida dentro de um computador que armazena e fornece acesso relativamente rápido a grandes quantidades de dados.</span><span class="sxs-lookup"><span data-stu-id="5700f-123">A *hard disk* is a rigid disk inside a computer that stores and provides relatively quick access to large amounts of data.</span></span> <span data-ttu-id="5700f-124">É o tipo de armazenamento usado com mais frequência com o Windows.</span><span class="sxs-lookup"><span data-stu-id="5700f-124">It is the type of storage most often used with Windows.</span></span> <span data-ttu-id="5700f-125">O sistema também dá suporte a mídia removível.</span><span class="sxs-lookup"><span data-stu-id="5700f-125">The system also supports removable media.</span></span><br/>    |
| [<span data-ttu-id="5700f-126">Gerenciamento de Arquivos</span><span class="sxs-lookup"><span data-stu-id="5700f-126">File Management</span></span>](file-management.md)<br/>                    | <span data-ttu-id="5700f-127">Um *objeto File* fornece uma representação de um recurso (um dispositivo físico ou um recurso localizado em um dispositivo físico) que pode ser gerenciado pelo sistema de e/s.</span><span class="sxs-lookup"><span data-stu-id="5700f-127">A *file object* provides a representation of a resource (either a physical device or a resource located on a physical device) that can be managed by the I/O system.</span></span><br/>                                                            |
| [<span data-ttu-id="5700f-128">NTFS Transacional (TxF)</span><span class="sxs-lookup"><span data-stu-id="5700f-128">Transactional NTFS (TxF)</span></span>](transactional-ntfs-portal.md)<br/> | <span data-ttu-id="5700f-129">O NTFS Transacional (TxF) permite que as operações de arquivo em um volume do sistema de arquivos NTFS sejam executadas em uma transação.</span><span class="sxs-lookup"><span data-stu-id="5700f-129">Transactional NTFS (TxF) allows file operations on an NTFS file system volume to be performed in a transaction.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="5700f-130">Gerenciamento de volume</span><span class="sxs-lookup"><span data-stu-id="5700f-130">Volume Management</span></span>](volume-management.md)<br/>                | <span data-ttu-id="5700f-131">O nível mais alto de organização no sistema de arquivos é o *volume*.</span><span class="sxs-lookup"><span data-stu-id="5700f-131">The highest level of organization in the file system is the *volume*.</span></span> <span data-ttu-id="5700f-132">Um sistema de arquivos reside em um volume.</span><span class="sxs-lookup"><span data-stu-id="5700f-132">A file system resides on a volume.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="5700f-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5700f-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5700f-134">[Referência técnica de FAT](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="5700f-134">[FAT Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758586(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="5700f-135">[Tecnologias de sistemas de arquivos](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="5700f-135">[File Systems Technologies](/previous-versions/windows/it-pro/windows-server-2003/cc778296(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="5700f-136">[Referência técnica do NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="5700f-136">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

