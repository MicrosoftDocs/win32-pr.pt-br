---
description: Se a ação InstallValidate detectar a instalação de um arquivo em uso, ela exibirá a caixa de diálogo FilesInUse e registrará as informações a seguir.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Registro em log de solicitações de reinicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506254"
---
# <a name="logging-of-reboot-requests"></a><span data-ttu-id="2d10a-103">Registro em log de solicitações de reinicialização</span><span class="sxs-lookup"><span data-stu-id="2d10a-103">Logging of Reboot Requests</span></span>

<span data-ttu-id="2d10a-104">Se a [ação InstallValidate](installvalidate-action.md) detectar a instalação de um arquivo em uso, ela exibirá a [caixa de diálogo FilesInUse](filesinuse-dialog.md) e registrará as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d10a-104">If the [InstallValidate action](installvalidate-action.md) detects the installation of a file in use it displays the [FilesInUse Dialog](filesinuse-dialog.md) and logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

<span data-ttu-id="2d10a-105">Se o instalador detectar que está prestes a substituir um arquivo que está em uso, ele registrará as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d10a-105">If the installer detects that it is about to overwrite a file that is in use, it logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

<span data-ttu-id="2d10a-106">O \[ token de nome de arquivo \] pode realmente conter um caminho para um arquivo com uma extensão. RBF.</span><span class="sxs-lookup"><span data-stu-id="2d10a-106">The \[filename\] token may actually contain a path to a file with an .rbf extension.</span></span> <span data-ttu-id="2d10a-107">Nesse caso, o arquivo. RBF é, na verdade, o arquivo original registrado pela mensagem 1603 que foi renomeada para o arquivo. RBF.</span><span class="sxs-lookup"><span data-stu-id="2d10a-107">In this case the .rbf file is actually the original file logged by the 1603 message which has been renamed to the .rbf file.</span></span> <span data-ttu-id="2d10a-108">O arquivo em uso é renomeado primeiro com uma extensão. RBF e, em seguida, excluído.</span><span class="sxs-lookup"><span data-stu-id="2d10a-108">The file that's in use is first renamed with an .rbf extension and then deleted.</span></span>

<span data-ttu-id="2d10a-109">Para obter mais informações sobre por que o instalador está tentando substituir esse arquivo específico, você pode usar a opção de log detalhado.</span><span class="sxs-lookup"><span data-stu-id="2d10a-109">To obtain more information about why the installer is attempting to overwrite this particular file, you can use the verbose logging option.</span></span> <span data-ttu-id="2d10a-110">Use o \_ valor Verbose INSTALLLOGMODE em uma chamada para [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) ou use a opção de saída detalhada das opções de [linha de comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="2d10a-110">Use the INSTALLLOGMODE\_VERBOSE value in a call to [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) or use the verbose output option of the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="2d10a-111">Isso registra as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d10a-111">This logs the following information.</span></span>

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

<span data-ttu-id="2d10a-112">O log incluirá uma mensagem como "o arquivo existente é uma versão inferior" ou "o arquivo existente está corrompido (soma de verificação inválida)"</span><span class="sxs-lookup"><span data-stu-id="2d10a-112">The log will include a message such as "Existing file is a lower version" or "Existing file is corrupt (invalid checksum)"</span></span>

 

 



