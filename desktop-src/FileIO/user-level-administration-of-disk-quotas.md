---
description: Como obter mais espaço livre em disco depois de exceder a concessão de cota.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Administração em nível de usuário de cotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc130cf925899ccf0a86af20ff6772689ecdfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758994"
---
# <a name="user-level-administration-of-disk-quotas"></a><span data-ttu-id="ab66e-103">Administração em nível de usuário de cotas de disco</span><span class="sxs-lookup"><span data-stu-id="ab66e-103">User-level Administration of Disk Quotas</span></span>

<span data-ttu-id="ab66e-104">As cotas de disco são transparentes para o usuário.</span><span class="sxs-lookup"><span data-stu-id="ab66e-104">Disk quotas are transparent to the user.</span></span> <span data-ttu-id="ab66e-105">Quando um usuário solicita a quantidade de espaço livre em um disco, o sistema relata apenas a concessão de cota disponível que o usuário disponibilizou.</span><span class="sxs-lookup"><span data-stu-id="ab66e-105">When a user asks how much space is free on a disk, the system reports only the available quota allowance the user has available.</span></span> <span data-ttu-id="ab66e-106">Se o usuário exceder essa concessão, o sistema retornará o erro de **disco de erro \_ \_ cheio** , assim como seria para indicar que o disco estava cheio.</span><span class="sxs-lookup"><span data-stu-id="ab66e-106">If the user exceeds this allowance, the system returns the **ERROR\_DISK\_FULL** error, just as it would to indicate that the disk was full.</span></span>

<span data-ttu-id="ab66e-107">Para obter mais espaço livre em disco depois de exceder a concessão de cota, o usuário deve seguir um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="ab66e-107">To obtain more free disk space after exceeding the quota allowance, the user must do one of the following:</span></span>

-   <span data-ttu-id="ab66e-108">Exclua alguns arquivos.</span><span class="sxs-lookup"><span data-stu-id="ab66e-108">Delete some files.</span></span>
-   <span data-ttu-id="ab66e-109">Fazer com que outro usuário solicite a propriedade de alguns arquivos.</span><span class="sxs-lookup"><span data-stu-id="ab66e-109">Have another user claim ownership of some files.</span></span>
-   <span data-ttu-id="ab66e-110">Fazer com que o administrador aumente a concessão de cota.</span><span class="sxs-lookup"><span data-stu-id="ab66e-110">Have the administrator increase the quota allowance.</span></span>

<span data-ttu-id="ab66e-111">Os programas que precisam recuperar a quantidade real de espaço livre em disco podem chamar a função [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) e examinar o parâmetro *TotalNumberOfFreeBytes* .</span><span class="sxs-lookup"><span data-stu-id="ab66e-111">Programs that need to retrieve the actual amount of free disk space can call the [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) function and look at the *TotalNumberOfFreeBytes* parameter.</span></span>

 

 



