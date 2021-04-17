---
description: 'Você pode atribuir uma letra de unidade (por exemplo, X: \) para um volume local usando a função SetVolumeMountPoint, desde que não haja nenhum volume já atribuído a essa letra de unidade.'
ms.assetid: 8c78b2e8-199a-4934-a9c4-6f3913f44efe
title: Atribuindo uma letra de unidade a um volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f31b9446cc41ad26f14a34874c59e153e1db8ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789817"
---
# <a name="assigning-a-drive-letter-to-a-volume"></a><span data-ttu-id="dffb1-103">Atribuindo uma letra de unidade a um volume</span><span class="sxs-lookup"><span data-stu-id="dffb1-103">Assigning a Drive Letter to a Volume</span></span>

<span data-ttu-id="dffb1-104">Você pode atribuir uma letra de unidade (por exemplo, X: \) para um volume local usando a função [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , desde que não haja nenhum volume já atribuído a essa letra de unidade.</span><span class="sxs-lookup"><span data-stu-id="dffb1-104">You can assign a drive letter (for example, X:\) to a local volume by using the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, provided there is no volume already assigned to that drive letter.</span></span> <span data-ttu-id="dffb1-105">Se o volume local já tiver uma letra de unidade.</span><span class="sxs-lookup"><span data-stu-id="dffb1-105">If the local volume already has a drive letter.</span></span> <span data-ttu-id="dffb1-106">em seguida, [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) falhará.</span><span class="sxs-lookup"><span data-stu-id="dffb1-106">then [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) will fail.</span></span> <span data-ttu-id="dffb1-107">Para lidar com isso, primeiro exclua a letra da unidade usando a função [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="dffb1-107">To handle this, first delete the drive letter by using the [**DeleteVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-deletevolumemountpointw) function.</span></span> <span data-ttu-id="dffb1-108">Para obter um exemplo de código, consulte [editando as atribuições de letra da unidade](editing-drive-letter-assignments.md).</span><span class="sxs-lookup"><span data-stu-id="dffb1-108">For example code, see [Editing Drive Letter Assignments](editing-drive-letter-assignments.md).</span></span>

<span data-ttu-id="dffb1-109">O sistema dá suporte a no máximo uma letra de unidade por volume.</span><span class="sxs-lookup"><span data-stu-id="dffb1-109">The system supports at most one drive letter per volume.</span></span> <span data-ttu-id="dffb1-110">Portanto, você não pode ter C: \\ e F: \\ representar o mesmo volume.</span><span class="sxs-lookup"><span data-stu-id="dffb1-110">Therefore, you cannot have C:\\ and F:\\ represent the same volume.</span></span>

> [!Caution]
>
> <span data-ttu-id="dffb1-111">A exclusão de uma letra de unidade existente e a atribuição de uma nova pode interromper os caminhos existentes, como aqueles em atalhos de área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dffb1-111">Deleting an existing drive letter and assigning a new one may break existing paths, such as those in desktop shortcuts.</span></span> <span data-ttu-id="dffb1-112">Ele também pode quebrar o caminho para o programa que faz com que a letra da unidade seja alterada.</span><span class="sxs-lookup"><span data-stu-id="dffb1-112">It may also break the path to the program making the drive letter changes.</span></span> <span data-ttu-id="dffb1-113">Com o gerenciamento de memória virtual do Windows, isso pode interromper o aplicativo, deixando o sistema em um estado instável e possivelmente inutilizável.</span><span class="sxs-lookup"><span data-stu-id="dffb1-113">With Windows virtual memory management, this may break the application, leaving the system in an unstable and possibly unusable state.</span></span> <span data-ttu-id="dffb1-114">É responsabilidade do designer de programa evitar essas possíveis catástrofes.</span><span class="sxs-lookup"><span data-stu-id="dffb1-114">It is the program designer's responsibility to avoid such potential catastrophes.</span></span>

 

 

 



