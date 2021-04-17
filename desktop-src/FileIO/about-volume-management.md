---
description: Os volumes são implementados por um driver de dispositivo chamado Gerenciador de volumes.
ms.assetid: 424ddbd9-5692-45ef-95fb-7b00b09e3205
title: Sobre o gerenciamento de volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0767d137eeecaa4ded060382b689b5ea3780dcbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759421"
---
# <a name="about-volume-management"></a><span data-ttu-id="22f42-103">Sobre o gerenciamento de volume</span><span class="sxs-lookup"><span data-stu-id="22f42-103">About Volume Management</span></span>

<span data-ttu-id="22f42-104">Os volumes são implementados por um driver de dispositivo chamado Gerenciador de volumes.</span><span class="sxs-lookup"><span data-stu-id="22f42-104">Volumes are implemented by a device driver called a volume manager.</span></span> <span data-ttu-id="22f42-105">Os exemplos incluem o Gerenciador de FtDisk, o Gerenciador de discos lógicos (LDM) e o Gerenciador de volumes lógicos (LVM) da VERITAS.</span><span class="sxs-lookup"><span data-stu-id="22f42-105">Examples include the FtDisk Manager, the Logical Disk Manager (LDM), and the VERITAS Logical Volume Manager (LVM).</span></span> <span data-ttu-id="22f42-106">Os gerenciadores de volumes fornecem uma camada de abstração física, proteção de dados (usando alguma forma de RAID) e desempenho.</span><span class="sxs-lookup"><span data-stu-id="22f42-106">Volume managers provide a layer of physical abstraction, data protection (using some form of RAID), and performance.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="22f42-107">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="22f42-107">In this section</span></span>



| <span data-ttu-id="22f42-108">Tópico</span><span class="sxs-lookup"><span data-stu-id="22f42-108">Topic</span></span>                                                                       | <span data-ttu-id="22f42-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="22f42-109">Description</span></span>                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22f42-110">Reconhecimento do sistema de arquivos</span><span class="sxs-lookup"><span data-stu-id="22f42-110">File System Recognition</span></span>](file-system-recognition.md)<br/>           | <span data-ttu-id="22f42-111">A meta do reconhecimento do sistema de arquivos é permitir que o sistema operacional Windows tenha uma opção adicional para um sistema de arquivos válido, mas não reconhecido, diferente de "RAW".</span><span class="sxs-lookup"><span data-stu-id="22f42-111">The goal of file system recognition is to allow the Windows operating system to have an additional option for a valid but unrecognized file system other than "RAW".</span></span><br/>                                                                                                         |
| [<span data-ttu-id="22f42-112">Nomeando um volume</span><span class="sxs-lookup"><span data-stu-id="22f42-112">Naming a Volume</span></span>](naming-a-volume.md)<br/>                           | <span data-ttu-id="22f42-113">Um rótulo é um nome amigável que é atribuído a um volume, geralmente por um usuário final, para facilitar o reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="22f42-113">A label is a user-friendly name that is assigned to a volume, usually by an end user, to make it easier to recognize.</span></span> <span data-ttu-id="22f42-114">Um volume pode ter um rótulo, uma letra da unidade, ambos ou nenhum.</span><span class="sxs-lookup"><span data-stu-id="22f42-114">A volume can have a label, a drive letter, both, or neither.</span></span> <span data-ttu-id="22f42-115">Para definir o rótulo de um volume, use a função [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) .</span><span class="sxs-lookup"><span data-stu-id="22f42-115">To set the label for a volume, use the [**SetVolumeLabel**](/windows/desktop/api/WinBase/nf-winbase-setvolumelabela) function.</span></span><br/> |
| [<span data-ttu-id="22f42-116">Enumerando volumes</span><span class="sxs-lookup"><span data-stu-id="22f42-116">Enumerating Volumes</span></span>](enumerating-volumes.md)<br/>                   | <span data-ttu-id="22f42-117">Para fazer uma lista completa dos volumes em um computador ou manipular cada volume por vez, você pode enumerar volumes.</span><span class="sxs-lookup"><span data-stu-id="22f42-117">To make a complete list of the volumes on a computer, or to manipulate each volume in turn, you can enumerate volumes.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="22f42-118">Obtendo informações de volume</span><span class="sxs-lookup"><span data-stu-id="22f42-118">Obtaining Volume Information</span></span>](obtaining-volume-information.md)<br/> | <span data-ttu-id="22f42-119">Antes de acessar arquivos e diretórios em um determinado volume, você deve determinar os recursos do sistema de arquivos usando a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) .</span><span class="sxs-lookup"><span data-stu-id="22f42-119">Before you access files and directories on a given volume, you should determine the capabilities of the file system by using the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function.</span></span><br/>                                                                              |
| [<span data-ttu-id="22f42-120">Diários de alterações</span><span class="sxs-lookup"><span data-stu-id="22f42-120">Change Journals</span></span>](change-journals.md)<br/>                           | <span data-ttu-id="22f42-121">Quando qualquer alteração é feita em um arquivo ou diretório em um volume, o diário de alterações do USN desse volume é atualizado com uma descrição da alteração e o nome do arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="22f42-121">When any change is made to a file or directory in a volume, the USN change journal for that volume is updated with a description of the change and the name of the file or directory.</span></span><br/>                                                                                        |
| [<span data-ttu-id="22f42-122">Pastas montadas</span><span class="sxs-lookup"><span data-stu-id="22f42-122">Mounted Folders</span></span>](volume-mount-points.md)<br/>                       | <span data-ttu-id="22f42-123">Usando pastas montadas, você pode unificar sistemas de arquivos diferentes, como o sistema de arquivos NTFS, um sistema de arquivos FAT de 16 bits e um sistema de arquivos ISO-9660 em uma unidade de CD-ROM em um sistema de arquivos lógico em um único volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="22f42-123">Using mounted folders, you can unify disparate file systems such as the NTFS file system, a 16-bit FAT file system, and an ISO-9660 file system on a CD-ROM drive into one logical file system on a single NTFS volume.</span></span><br/>                                                      |
| [<span data-ttu-id="22f42-124">Tabela de arquivos mestre</span><span class="sxs-lookup"><span data-stu-id="22f42-124">Master File Table</span></span>](master-file-table.md)<br/>                       | <span data-ttu-id="22f42-125">Todas as informações sobre um arquivo, incluindo seu tamanho, carimbos de data e hora, permissões e conteúdo de dados, são armazenadas em entradas de MFT (tabela de arquivos mestre) ou em espaço fora do MFT que é descrito pelas entradas de MFT.</span><span class="sxs-lookup"><span data-stu-id="22f42-125">All information about a file, including its size, time and date stamps, permissions, and data content, is stored either in master file table (MFT) entries, or in space outside the MFT that is described by MFT entries.</span></span><br/>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="22f42-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22f42-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="22f42-127">[Referência técnica de volumes e discos básicos](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="22f42-127">[Basic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc784732(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="22f42-128">[Referência técnica de volumes e discos dinâmicos](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="22f42-128">[Dynamic Disks and Volumes Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc785638(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="22f42-129">Referência de gerenciamento de volume</span><span class="sxs-lookup"><span data-stu-id="22f42-129">Volume Management Reference</span></span>](volume-management-reference.md)
</dt> </dl>

 

