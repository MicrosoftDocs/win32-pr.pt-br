---
description: Antes de adicionar ou remover operações de arquivo da lista de espaço em disco, você deve criá-la usando a função SetupCreateDiskSpaceList.
ms.assetid: 287fd84a-dc8c-4a5c-b998-db5f2fbee5f1
title: Usando a lista de Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a19f100fd5190472f5f6bfebaf74affe1a789cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769179"
---
# <a name="using-the-disk-space-list"></a><span data-ttu-id="29e50-103">Usando a lista de Disk-Space</span><span class="sxs-lookup"><span data-stu-id="29e50-103">Using the Disk-Space List</span></span>

<span data-ttu-id="29e50-104">Antes de adicionar ou remover operações de arquivo da lista de espaço em disco, você deve criá-la usando a função [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="29e50-104">Before you can add or remove file operations from the disk-space list, you must create it by using the [**SetupCreateDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupcreatediskspacelista) function.</span></span>

<span data-ttu-id="29e50-105">Depois de criar uma lista de espaço em disco, você pode adicionar operações individuais de cópia de arquivo ou exclusão à lista usando [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span><span class="sxs-lookup"><span data-stu-id="29e50-105">After you create a disk-space list you can add individual file copy or delete operations to the list by using [**SetupAddToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddtodiskspacelista).</span></span> <span data-ttu-id="29e50-106">Para adicionar todas as operações de cópia ou exclusão de arquivo em uma seção INF inteira, use a função [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) ou [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="29e50-106">To add all the file copy or delete operations in an entire INF section, use either the [**SetupAddSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddsectiontodiskspacelista) or [**SetupAddInstallSectionToDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupaddinstallsectiontodiskspacelista) function.</span></span>

<span data-ttu-id="29e50-107">Depois de adicionar todas as operações de instalação à lista de espaço em disco, você pode consultá-las para descobrir quanto espaço em disco é necessário para a instalação especificada usando a função [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) .</span><span class="sxs-lookup"><span data-stu-id="29e50-107">After you add all the installation operations to the disk-space list, you can query it to find out how much disk space is required for the specified installation by using the [**SetupQuerySpaceRequiredOnDrive**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryspacerequiredondrivea) function.</span></span>

<span data-ttu-id="29e50-108">A função [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) retorna as especificações de unidade para cada unidade de destino referenciada nas operações de arquivo na lista de espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="29e50-108">The [**SetupQueryDrivesInDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupquerydrivesindiskspacelista) function returns the drive specifications for each target drive referenced in the file operations on the disk-space list.</span></span> <span data-ttu-id="29e50-109">Você pode usar essas informações para comparar programaticamente o espaço disponível nessas unidades com o espaço exigido pela instalação.</span><span class="sxs-lookup"><span data-stu-id="29e50-109">You can use this information to programmatically compare the available space on these drives with the space required by the installation.</span></span>

<span data-ttu-id="29e50-110">Para remover uma operação de arquivo da lista de espaço em disco, use a função [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="29e50-110">To remove a file operation from the disk-space list, use the [**SetupRemoveFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefromdiskspacelista) function.</span></span> <span data-ttu-id="29e50-111">Para remover todas as operações de cópia ou exclusão de arquivo de uma seção de INF inteira, use a função [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) ou [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) .</span><span class="sxs-lookup"><span data-stu-id="29e50-111">To remove all file copy or delete operations from an entire INF section, use the [**SetupRemoveSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovesectionfromdiskspacelista) or [**SetupRemoveInstallSectionFromDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupremoveinstallsectionfromdiskspacelista) function.</span></span>

<span data-ttu-id="29e50-112">Depois que a lista de espaço em disco não for mais necessária, você poderá liberar os recursos alocados a ela chamando a função [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) .</span><span class="sxs-lookup"><span data-stu-id="29e50-112">After the disk-space list is no longer required, you can release the resources allocated to it by calling the [**SetupDestroyDiskSpaceList**](/windows/desktop/api/Setupapi/nf-setupapi-setupdestroydiskspacelist) function.</span></span>

 

 



