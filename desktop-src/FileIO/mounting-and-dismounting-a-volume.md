---
description: A criação de uma pasta montada é um processo de duas etapas.
ms.assetid: 02ecdf93-1133-48af-a6c9-52142256673f
title: Criando pastas montadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5d64630716be6e85ac323c80e89dda0500ba6c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778603"
---
# <a name="creating-mounted-folders"></a><span data-ttu-id="35858-103">Criando pastas montadas</span><span class="sxs-lookup"><span data-stu-id="35858-103">Creating Mounted Folders</span></span>

<span data-ttu-id="35858-104">A criação de uma pasta montada é um processo de duas etapas.</span><span class="sxs-lookup"><span data-stu-id="35858-104">Creating a mounted folder is a two-step process.</span></span> <span data-ttu-id="35858-105">Primeiro, chame [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) com o ponto de montagem (letra da unidade, caminho do GUID do volume ou pasta montada) do volume a ser atribuído à pasta montada.</span><span class="sxs-lookup"><span data-stu-id="35858-105">First, call [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) with the mount point (drive letter, volume GUID path, or mounted folder) of the volume to be assigned to the mounted folder.</span></span> <span data-ttu-id="35858-106">Em seguida, use a função [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) para associar o caminho do GUID do volume retornado ao diretório desejado em outro volume.</span><span class="sxs-lookup"><span data-stu-id="35858-106">Then use the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function to associate the returned volume GUID path with the desired directory on another volume.</span></span> <span data-ttu-id="35858-107">Para obter um exemplo de código, consulte [criando uma pasta montada](mounting-a-volume-at-a-mount-point.md).</span><span class="sxs-lookup"><span data-stu-id="35858-107">For example code, see [Creating a Mounted Folder](mounting-a-volume-at-a-mount-point.md).</span></span>

<span data-ttu-id="35858-108">Seu aplicativo pode designar qualquer diretório vazio em um volume diferente da raiz como uma pasta montada.</span><span class="sxs-lookup"><span data-stu-id="35858-108">Your application can designate any empty directory on a volume other than the root as a mounted folder.</span></span> <span data-ttu-id="35858-109">Quando você chama a função [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , esse diretório se torna a pasta montada.</span><span class="sxs-lookup"><span data-stu-id="35858-109">When you call the [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) function, that directory becomes the mounted folder.</span></span> <span data-ttu-id="35858-110">Você pode atribuir o mesmo volume a várias pastas montadas.</span><span class="sxs-lookup"><span data-stu-id="35858-110">You can assign the same volume to multiple mounted folders.</span></span>

<span data-ttu-id="35858-111">Depois que a pasta montada tiver sido estabelecida, ela será mantida por meio da reinicialização do computador automaticamente.</span><span class="sxs-lookup"><span data-stu-id="35858-111">After the mounted folder has been established, it is maintained through computer restarts automatically.</span></span>

<span data-ttu-id="35858-112">Se um volume falhar, todos os volumes que foram atribuídos a pastas montadas nesse volume não poderão mais ser acessados por meio dessas pastas montadas.</span><span class="sxs-lookup"><span data-stu-id="35858-112">If a volume fails, any volumes that have been assigned to mounted folders on that volume can no longer be accessed through those mounted folders.</span></span> <span data-ttu-id="35858-113">Por exemplo, suponha que você tenha dois volumes, C: e D:, e que D: esteja associado à pasta montada C: montado \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="35858-113">For example, suppose you have two volumes, C: and D:, and that D: is associated with the mounted folder C:\\MountD\\.</span></span> <span data-ttu-id="35858-114">Se o volume C: falhar, o volume D: não poderá mais ser acessado por meio do caminho C: \\ montado \\ .</span><span class="sxs-lookup"><span data-stu-id="35858-114">If volume C: fails, volume D: can no longer be accessed through the path C:\\MountD\\.</span></span>

<span data-ttu-id="35858-115">Somente volumes do sistema de arquivos NTFS podem ter pastas montadas, mas os volumes de destino para as pastas montadas podem ser volumes não NTFS.</span><span class="sxs-lookup"><span data-stu-id="35858-115">Only NTFS file system volumes can have mounted folders, but the target volumes for the mounted folders can be non-NTFS volumes.</span></span>

<span data-ttu-id="35858-116">As pastas montadas são implementadas usando pontos de nova análise e estão sujeitas às suas restrições.</span><span class="sxs-lookup"><span data-stu-id="35858-116">Mounted folders are implemented by using reparse points and are subject to their restrictions.</span></span> <span data-ttu-id="35858-117">Para obter mais informações, consulte [pontos de nova análise](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="35858-117">For more information, see [Reparse Points](reparse-points.md).</span></span> <span data-ttu-id="35858-118">Não é necessário manipular pontos de nova análise para usar pastas montadas; funções como [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) lidam com todos os detalhes do ponto de nova análise para você.</span><span class="sxs-lookup"><span data-stu-id="35858-118">It is not necessary to manipulate reparse points to use mounted folders; functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) handle all the reparse point details for you.</span></span>

<span data-ttu-id="35858-119">Como as pastas montadas são diretórios, você pode renomear, remover, mover e, de outra forma, manipulá-los, como faria com outros diretórios.</span><span class="sxs-lookup"><span data-stu-id="35858-119">Because mounted folders are directories, you can rename, remove, move, and otherwise manipulate them, as you would other directories.</span></span>

<span data-ttu-id="35858-120">(Observação: a documentação do TechNet usa o termo *unidades montadas* para se referir a *pastas montadas*.)</span><span class="sxs-lookup"><span data-stu-id="35858-120">(Note: The TechNet documentation uses the term *mounted drives* to refer to *mounted folders*.)</span></span>

 

 



