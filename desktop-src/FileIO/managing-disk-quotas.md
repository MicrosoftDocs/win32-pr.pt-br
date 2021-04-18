---
description: Os administradores podem controlar a quantidade de dados que cada usuário pode armazenar em um volume do sistema de arquivos NTFS.
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: Gerenciando cotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812957"
---
# <a name="managing-disk-quotas"></a><span data-ttu-id="fa28d-103">Gerenciando cotas de disco</span><span class="sxs-lookup"><span data-stu-id="fa28d-103">Managing Disk Quotas</span></span>

<span data-ttu-id="fa28d-104">O sistema de arquivos NTFS dá suporte a *cotas de disco*, que permitem que os administradores controlem a quantidade de dados que cada usuário pode armazenar em um volume do sistema de arquivos NTFS.</span><span class="sxs-lookup"><span data-stu-id="fa28d-104">The NTFS file system supports *disk quotas*, which allow administrators to control the amount of data that each user can store on an NTFS file system volume.</span></span> <span data-ttu-id="fa28d-105">Opcionalmente, os administradores podem configurar o sistema para registrar um evento quando os usuários estão próximos de sua cota e para negar mais espaço em disco aos usuários que excederem sua cota.</span><span class="sxs-lookup"><span data-stu-id="fa28d-105">Administrators can optionally configure the system to log an event when users are near their quota, and to deny further disk space to users who exceed their quota.</span></span> <span data-ttu-id="fa28d-106">Os administradores também podem gerar relatórios e usar o monitor de eventos para rastrear problemas de cota.</span><span class="sxs-lookup"><span data-stu-id="fa28d-106">Administrators can also generate reports, and use the event monitor to track quota issues.</span></span>

<span data-ttu-id="fa28d-107">Você pode determinar se um sistema de arquivos dá suporte a cotas de disco chamando a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examinando o sinalizador de bit de **\_ \_ cotas de volume de arquivo** .</span><span class="sxs-lookup"><span data-stu-id="fa28d-107">You can determine whether a file system supports disk quotas by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_VOLUME\_QUOTAS** bit flag.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fa28d-108">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="fa28d-108">In this section</span></span>



| <span data-ttu-id="fa28d-109">Tópico</span><span class="sxs-lookup"><span data-stu-id="fa28d-109">Topic</span></span>                                                                                                   | <span data-ttu-id="fa28d-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="fa28d-110">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa28d-111">Administração em nível de usuário de cotas de disco</span><span class="sxs-lookup"><span data-stu-id="fa28d-111">User-level Administration of Disk Quotas</span></span>](user-level-administration-of-disk-quotas.md)<br/>     | <span data-ttu-id="fa28d-112">Como obter mais espaço livre em disco depois de exceder a concessão de cota.</span><span class="sxs-lookup"><span data-stu-id="fa28d-112">How to get more free disk space after exceeding the quota allowance.</span></span><br/>                                                                  |
| [<span data-ttu-id="fa28d-113">Administração em nível de sistema de cotas de disco</span><span class="sxs-lookup"><span data-stu-id="fa28d-113">System-level Administration of Disk Quotas</span></span>](system-level-administration-of-disk-quotas.md)<br/> | <span data-ttu-id="fa28d-114">O administrador do sistema pode definir cotas para usuários específicos em um volume.</span><span class="sxs-lookup"><span data-stu-id="fa28d-114">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="fa28d-115">O administrador também pode definir as cotas padrão para o volume.</span><span class="sxs-lookup"><span data-stu-id="fa28d-115">The administrator can also set default quotas for the volume.</span></span><br/> |
| [<span data-ttu-id="fa28d-116">Limites de cota de disco</span><span class="sxs-lookup"><span data-stu-id="fa28d-116">Disk Quota Limits</span></span>](disk-quota-limits.md)<br/>                                                   | <span data-ttu-id="fa28d-117">Descreve dois tipos de limites de cota de disco e como os limites de cota de disco são medidos.</span><span class="sxs-lookup"><span data-stu-id="fa28d-117">Describes two types of disk quota limits and how disk quota limits are measured.</span></span><br/>                                                      |
| [<span data-ttu-id="fa28d-118">Interfaces de cota de disco</span><span class="sxs-lookup"><span data-stu-id="fa28d-118">Disk Quota Interfaces</span></span>](disk-quota-interfaces.md)<br/>                                           | <span data-ttu-id="fa28d-119">Interfaces usadas com cotas de disco.</span><span class="sxs-lookup"><span data-stu-id="fa28d-119">Interfaces used with disk quotas.</span></span><br/>                                                                                                     |



 

 

 




