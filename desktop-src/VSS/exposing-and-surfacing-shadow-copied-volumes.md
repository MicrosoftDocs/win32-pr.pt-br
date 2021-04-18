---
description: Além de serem acessados por meio da interface IVssBackupComponents por meio do objeto de dispositivo da sua cópia, um solicitante pode disponibilizar uma cópia de sombra para outros processos como um dispositivo somente leitura montado.
ms.assetid: 0898c2dc-992a-411b-81df-4f5e129f6a80
title: Expondo e Identificandondo volumes copiados de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d684aa9b696facaf1caa3aa3102c6b1d7fc37409
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781486"
---
# <a name="exposing-and-surfacing-shadow-copied-volumes"></a><span data-ttu-id="b67c1-103">Expondo e Identificandondo volumes copiados de sombra</span><span class="sxs-lookup"><span data-stu-id="b67c1-103">Exposing and Surfacing Shadow Copied Volumes</span></span>

<span data-ttu-id="b67c1-104">Além de serem acessados por meio da interface [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) por meio do [*objeto de dispositivo*](vssgloss-d.md)da sua cópia, um solicitante pode disponibilizar uma cópia de sombra para outros processos como um dispositivo somente leitura montado.</span><span class="sxs-lookup"><span data-stu-id="b67c1-104">In addition to being accessed through the [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) interface by means of its copy's [*device object*](vssgloss-d.md), a requester can make a shadow copy available to other processes as a mounted read-only device.</span></span>

<span data-ttu-id="b67c1-105">Esse processo é conhecido como [*expor uma cópia de sombra*](vssgloss-e.md)e é executado usando o método [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) .</span><span class="sxs-lookup"><span data-stu-id="b67c1-105">This process is known as [*exposing a shadow copy*](vssgloss-e.md), and is performed using the [**IVssBackupComponents::ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot) method.</span></span>

<span data-ttu-id="b67c1-106">Uma cópia de sombra pode ser exposta como um volume local, atribuída uma letra de unidade ou associada a uma pasta montada — ou como um compartilhamento de arquivos.</span><span class="sxs-lookup"><span data-stu-id="b67c1-106">A shadow copy can be exposed as a local volume—assigned a drive letter or associated with a mounted folder—or as a file share.</span></span>

<span data-ttu-id="b67c1-107">Para ilustrar, considere uma cópia de sombra feita de um volume no sistema exposedSys montada em F: \\ on cuja raiz são os diretórios dirOne e dirTwo e o arquivo FileOne.</span><span class="sxs-lookup"><span data-stu-id="b67c1-107">To illustrate, consider a shadow copy made of a volume on the system exposedSys mounted at F:\\ on whose root are the directories dirOne and dirTwo, and the file FileOne.</span></span>

## <a name="exposing-a-shadow-copy-locally"></a><span data-ttu-id="b67c1-108">Expondo uma cópia de sombra localmente</span><span class="sxs-lookup"><span data-stu-id="b67c1-108">Exposing a Shadow Copy Locally</span></span>

<span data-ttu-id="b67c1-109">Quando montado como um volume local, a raiz da cópia de sombra fica sempre visível no ponto de montagem (letra da unidade ou pasta montada) e todos os arquivos copiados por sombra são visíveis.</span><span class="sxs-lookup"><span data-stu-id="b67c1-109">When mounted as a local volume, the shadow copy's root is always visible at the mount point (drive letter or mounted folder) and all the shadow-copied files are visible.</span></span>

<span data-ttu-id="b67c1-110">Se a cópia de sombra tiver sido exposta localmente por meio da pasta montada C: \\ ShadowOfF, você encontrará todos os arquivos presentes no disco montado em F: \\ no momento da cópia de sombra disponível em C: \\ ShadowOfF.</span><span class="sxs-lookup"><span data-stu-id="b67c1-110">If the shadow copy was locally exposed through the mounted folder C:\\ShadowOfF, you would find all files present on disk mounted at F:\\ at the time of the shadow copy available under C:\\ShadowOfF.</span></span> <span data-ttu-id="b67c1-111">Examinar C: \\ ShadowOfF revelaria dois diretórios, dirOne e dirTwo, e um arquivo, fileone, em C: \\ ShadowOfF.</span><span class="sxs-lookup"><span data-stu-id="b67c1-111">Examining C:\\ShadowOfF would reveal two directories, dirOne and dirTwo, and one file, fileOne, under C:\\ShadowOfF.</span></span>

<span data-ttu-id="b67c1-112">Uma chamada para expor localmente a cópia de sombra pode ser:</span><span class="sxs-lookup"><span data-stu-id="b67c1-112">A call to locally expose the shadow copy might be:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  PWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
         snapID,                           // VSS_ID SnapshotId,
         NULL,                             // VSS_PWSZ wszPathFromRoot
         VSS_VOLSNAP_ATTR_EXPOSED_LOCALLY, // LONG lAttributes
         L"C:\ShadowOfF",                  // VSS_PWSZ wszExpose
         LPWSTR &wszExposed,               // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="b67c1-113">Se a cópia de sombra tiver sido exposta com êxito localmente, *wszExposed* deverá conter a cadeia de caracteres larga "C: \\ ShadowOfF".</span><span class="sxs-lookup"><span data-stu-id="b67c1-113">If the shadow copy was successfully exposed locally, *wszExposed* should contain the wide character string "C:\\ShadowOfF."</span></span>

<span data-ttu-id="b67c1-114">A cópia de sombra pode ser desexposta posteriormente chamando [**IVssBackupComponentsEx2:: UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span><span class="sxs-lookup"><span data-stu-id="b67c1-114">The shadow copy can later be unexposed by calling [**IVssBackupComponentsEx2::UnexposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-unexposesnapshot).</span></span>

<span data-ttu-id="b67c1-115">Somente as cópias de sombra persistentes, ou seja, cópias de sombra criadas com a \_ reversão do VSS CTX \_ nas \_ Rollback ou a \_ reversão do aplicativo CTX do VSS \_ \_ , podem ser expostas localmente.</span><span class="sxs-lookup"><span data-stu-id="b67c1-115">Only persistent shadow copies—that is, shadow copies created with either VSS\_CTX\_NAS\_ROLLBACK or VSS\_CTX\_APP\_ROLLBACK—can be exposed locally.</span></span>

## <a name="exposing-a-shadow-copy-as-a-remote-share"></a><span data-ttu-id="b67c1-116">Expondo uma cópia de sombra como um compartilhamento remoto</span><span class="sxs-lookup"><span data-stu-id="b67c1-116">Exposing a Shadow Copy as a Remote Share</span></span>

<span data-ttu-id="b67c1-117">Como alternativa, você pode optar por fazer a cópia de sombra do disco montado em F: \\ disponível como um compartilhamento de arquivos remoto e expor apenas os dados em dirTwo como o compartilhamento de arquivos dirTwoOfF.</span><span class="sxs-lookup"><span data-stu-id="b67c1-117">Alternatively, you could choose to make the shadow copy of the disk mounted at F:\\ available as a remote file share, and expose only data under dirTwo as the file share dirTwoOfF.</span></span>

<span data-ttu-id="b67c1-118">Nesse caso, os sistemas podiam acessar a cópia de sombra dos arquivos em F: \\ dirTwo mapeando \\ \\ exposedSys \\ dirTwoOfF como uma unidade de rede.</span><span class="sxs-lookup"><span data-stu-id="b67c1-118">In this case, systems could access the shadow copy of files under F:\\dirTwo by mapping \\\\exposedSys\\dirTwoOfF as a network drive.</span></span>

<span data-ttu-id="b67c1-119">Uma chamada para implementar a exposição remota da cópia de sombra como um compartilhamento pode ser a seguinte:</span><span class="sxs-lookup"><span data-stu-id="b67c1-119">A call to implement remote exposing the shadow copy as a share might be the following:</span></span>

``` syntax
  IVssBackupComponents *pReq;
  VSS_ID snapID;
  LPWSTR wszExposed;
  //    .
  //    .
  hr = pReg->ExposeSnapshot(
               snapID,                            // VSS_ID SnapshotId,
               L"\dirTwo",                        // VSS_PWSZ wszPathFromRoot
               VSS_VOLSNAP_ATTR_EXPOSED_REMOTELY, // LONG lAttributes
               L"dirTwoOfF",                      // VSS_PWSZ wszExpose
               LPWSTR &wszExposed,                // VSS_PWSZ* pwszExposed
       );
```

<span data-ttu-id="b67c1-120">Se a cópia de sombra tiver sido exposta com êxito remotamente, *wszExposed* deverá conter a cadeia de caracteres largo "dirTwoOfF".</span><span class="sxs-lookup"><span data-stu-id="b67c1-120">If the shadow copy was successfully exposed remotely, *wszExposed* should contain the wide character string "dirTwoOfF."</span></span>

<span data-ttu-id="b67c1-121">Qualquer sistema que atualmente mapeie o compartilhamento de rede do dirTwoOfF poderia se desconectar dele, assim como ele pode se desconectar de qualquer compartilhamento comum.</span><span class="sxs-lookup"><span data-stu-id="b67c1-121">Any system currently mapping the network share of dirTwoOfF could disconnect from it, just as it might disconnect from any ordinary share.</span></span>

## <a name="surfacing-a-shadow-copy"></a><span data-ttu-id="b67c1-122">Identificando uma cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="b67c1-122">Surfacing a Shadow Copy</span></span>

<span data-ttu-id="b67c1-123">Uma [*cópia de sombra na superfície*](vssgloss-s.md) é aquela em que a cópia de sombra é conhecida por um namespace do Gerenciador de montagem do sistema.</span><span class="sxs-lookup"><span data-stu-id="b67c1-123">A [*surfaced shadow copy*](vssgloss-s.md) is one in which the shadow copy is known to a system's Mount Manager namespace.</span></span>

<span data-ttu-id="b67c1-124">Isso significa que você pode localizar essas cópias de sombra assim como você localizaria qualquer outro volume disponível, mas ainda não montado, usando **FindFirstVolume** e **FindNextVolume**, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="b67c1-124">This means that you can locate such shadow copies just as you would locate any other available but not-yet-mounted volume—by using **FindFirstVolume** and **FindNextVolume**, for example.</span></span>

<span data-ttu-id="b67c1-125">Claramente, as cópias de sombra expostas também são cópias de sombra em superfície.</span><span class="sxs-lookup"><span data-stu-id="b67c1-125">Clearly, then, exposed shadow copies are also surfaced shadow copies.</span></span> <span data-ttu-id="b67c1-126">No entanto, o inverso não é necessariamente verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="b67c1-126">However, the reverse is not necessarily true.</span></span>

<span data-ttu-id="b67c1-127">Se uma cópia de sombra exposta localmente foi desmontada ou um sistema optou por desconectar uma cópia de sombra exposta remotamente, essa cópia de sombra não seria mais exposta.</span><span class="sxs-lookup"><span data-stu-id="b67c1-127">If a locally exposed shadow copy was dismounted, or a system chose to disconnect a remotely exposed shadow copy, that shadow copy would no longer be exposed.</span></span> <span data-ttu-id="b67c1-128">No entanto, desde que a cópia de sombra persista, os volumes seriam exibidos.</span><span class="sxs-lookup"><span data-stu-id="b67c1-128">However, as long as the shadow copy persisted, the volumes would be surfaced.</span></span> <span data-ttu-id="b67c1-129">Isso significa que eles podem ser montados como qualquer outro volume somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b67c1-129">This means they could be mounted like any other read-only volume.</span></span>

 

 



