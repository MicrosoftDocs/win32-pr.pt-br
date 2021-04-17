---
description: Usando pastas montadas, você pode unificar sistemas de arquivos diferentes, como o sistema de arquivos NTFS, um sistema de arquivos FAT de 16 bits e um sistema de arquivos ISO-9660 em uma unidade de CD-ROM em um sistema de arquivos lógico em um único volume NTFS.
ms.assetid: 6de526cd-5537-4411-b43f-3c0bdac70d64
title: Pastas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f0f0c937ded5f7a6b78f19b17b4c098178f254f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812955"
---
# <a name="mounted-folders"></a><span data-ttu-id="58de9-103">Pastas montadas</span><span class="sxs-lookup"><span data-stu-id="58de9-103">Mounted Folders</span></span>

<span data-ttu-id="58de9-104">O sistema de arquivos NTFS dá suporte a pastas montadas.</span><span class="sxs-lookup"><span data-stu-id="58de9-104">The NTFS file system supports mounted folders.</span></span> <span data-ttu-id="58de9-105">Uma *pasta montada* é uma associação entre um volume e um diretório em outro volume.</span><span class="sxs-lookup"><span data-stu-id="58de9-105">A *mounted folder* is an association between a volume and a directory on another volume.</span></span> <span data-ttu-id="58de9-106">Quando uma pasta montada é criada, os usuários e os aplicativos podem acessar o volume de destino usando o caminho para a pasta montada ou usando a letra da unidade do volume.</span><span class="sxs-lookup"><span data-stu-id="58de9-106">When a mounted folder is created, users and applications can access the target volume either by using the path to the mounted folder or by using the volume's drive letter.</span></span> <span data-ttu-id="58de9-107">Por exemplo, um usuário pode criar uma pasta montada para associar a unidade D: com a \\ pasta c: mnt \\ DDrive na unidade C. Depois de criar a pasta montada, o usuário pode usar o caminho "C: \\ mnt \\ DDrive" para acessar a unidade D: como se fosse uma pasta na unidade C:.</span><span class="sxs-lookup"><span data-stu-id="58de9-107">For example, a user can create a mounted folder to associate drive D: with the C:\\Mnt\\DDrive folder on drive C. After creating the mounted folder, the user can use the "C:\\Mnt\\DDrive" path to access drive D: as if it were a folder on drive C:.</span></span>

<span data-ttu-id="58de9-108">Usando pastas montadas, você pode unificar sistemas de arquivos diferentes, como o sistema de arquivos NTFS, um sistema de arquivos FAT de 16 bits e um sistema de arquivos ISO-9660 em uma unidade de CD-ROM em um sistema de arquivos lógico em um único volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="58de9-108">Using mounted folders, you can unify disparate file systems such as the NTFS file system, a 16-bit FAT file system, and an ISO-9660 file system on a CD-ROM drive into one logical file system on a single NTFS volume.</span></span> <span data-ttu-id="58de9-109">Nem os usuários nem aplicativos precisam de informações sobre o volume de destino no qual um arquivo específico está localizado.</span><span class="sxs-lookup"><span data-stu-id="58de9-109">Neither users nor applications need information about the target volume on which a specific file is located.</span></span> <span data-ttu-id="58de9-110">Todas as informações necessárias para localizar um arquivo especificado são um caminho completo usando uma pasta montada no volume NTFS.</span><span class="sxs-lookup"><span data-stu-id="58de9-110">All the information they need to locate a specified file is a complete path using a mounted folder on the NTFS volume.</span></span> <span data-ttu-id="58de9-111">Os volumes podem ser reorganizados, substituídos ou subdivididos em muitos volumes sem que os usuários ou aplicativos precisem alterar as configurações.</span><span class="sxs-lookup"><span data-stu-id="58de9-111">Volumes can be rearranged, substituted, or subdivided into many volumes without users or applications needing to change settings.</span></span>

<span data-ttu-id="58de9-112">Para obter informações sobre pastas montadas, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="58de9-112">For information on mounted folders, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="58de9-113">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="58de9-113">In this section</span></span>



| <span data-ttu-id="58de9-114">Tópico</span><span class="sxs-lookup"><span data-stu-id="58de9-114">Topic</span></span>                                                                                                                         | <span data-ttu-id="58de9-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="58de9-115">Description</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58de9-116">Criando pastas montadas</span><span class="sxs-lookup"><span data-stu-id="58de9-116">Creating Mounted Folders</span></span>](mounting-and-dismounting-a-volume.md)<br/>                                                  | <span data-ttu-id="58de9-117">A criação de uma pasta montada é um processo de duas etapas.</span><span class="sxs-lookup"><span data-stu-id="58de9-117">Creating a mounted folder is a two-step process.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="58de9-118">Enumerando pastas montadas</span><span class="sxs-lookup"><span data-stu-id="58de9-118">Enumerating Mounted Folders</span></span>](enumerating-volume-mount-points.md)<br/>                                                 | <span data-ttu-id="58de9-119">Funções a serem usadas para enumerar pastas montadas em um volume.</span><span class="sxs-lookup"><span data-stu-id="58de9-119">Functions to use to enumerate mounted folders on a volume.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="58de9-120">Determinando se um diretório é uma pasta montada</span><span class="sxs-lookup"><span data-stu-id="58de9-120">Determining Whether a Directory Is a Mounted Folder</span></span>](determining-whether-a-directory-is-a-volume-mount-point.md)<br/> | <span data-ttu-id="58de9-121">Como determinar se um diretório especificado é uma pasta montada.</span><span class="sxs-lookup"><span data-stu-id="58de9-121">How to determine whether a specified directory is a mounted folder.</span></span><br/>                                                                                                                                              |
| [<span data-ttu-id="58de9-122">Atribuindo uma letra de unidade a um volume</span><span class="sxs-lookup"><span data-stu-id="58de9-122">Assigning a Drive Letter to a Volume</span></span>](assigning-a-drive-letter-to-a-volume.md)<br/>                                   | <span data-ttu-id="58de9-123">Você pode atribuir uma letra de unidade (por exemplo, X: \) para um volume local usando a função [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , desde que não haja nenhum volume já atribuído a essa letra de unidade.</span><span class="sxs-lookup"><span data-stu-id="58de9-123">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span><br/> |
| [<span data-ttu-id="58de9-124">Funções de pasta montadas</span><span class="sxs-lookup"><span data-stu-id="58de9-124">Mounted Folder Functions</span></span>](volume-mount-point-functions.md)<br/>                                                       | <span data-ttu-id="58de9-125">Funções usadas para gerenciar pastas montadas.</span><span class="sxs-lookup"><span data-stu-id="58de9-125">Functions used to manage mounted folders.</span></span><br/>                                                                                                                                                                        |



 

<span data-ttu-id="58de9-126">Para obter exemplos, consulte [exemplos de pastas montadas](volume-mount-point-examples.md).</span><span class="sxs-lookup"><span data-stu-id="58de9-126">For examples, see [Mounted Folder Examples](volume-mount-point-examples.md).</span></span>

 

 




