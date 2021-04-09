---
title: Entradas do registro (COM)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: 'Saiba mais sobre: entradas do registro (COM)'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089581"
---
# <a name="registry-entries-com"></a><span data-ttu-id="2a613-103">Entradas do registro (COM)</span><span class="sxs-lookup"><span data-stu-id="2a613-103">Registry Entries (COM)</span></span>

<span data-ttu-id="2a613-104">Os valores do registro nas chaves do registro a seguir controlam aspectos da funcionalidade do COM:</span><span class="sxs-lookup"><span data-stu-id="2a613-104">Registry values in the following registry keys control aspects of the functionality of COM:</span></span>

-   [<span data-ttu-id="2a613-105">**HKEY \_ local \_ Machine \\ software \\ classes**</span><span class="sxs-lookup"><span data-stu-id="2a613-105">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes**</span></span>](hkey-local-machine-software-classes.md)
-   [<span data-ttu-id="2a613-106">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ OLE**</span><span class="sxs-lookup"><span data-stu-id="2a613-106">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Ole**</span></span>](hkey-local-machine-software-microsoft-ole.md)
-   [<span data-ttu-id="2a613-107">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion**</span><span class="sxs-lookup"><span data-stu-id="2a613-107">**HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows NT\\CurrentVersion**</span></span>](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

<span data-ttu-id="2a613-108">A partir do Windows Server 2003, o COM usa apenas o token de processo atual para decidir qual hive de registro deve acessar, não o token de thread.</span><span class="sxs-lookup"><span data-stu-id="2a613-108">As of Windows Server 2003, COM uses only the current process token to decide which registry hive to access, not the thread token.</span></span> <span data-ttu-id="2a613-109">Se COM não for capaz de acessar o hive do registro de perfil do usuário, ele acessará o hive do **\_ \_ \\ sistema do computador local hKey** .</span><span class="sxs-lookup"><span data-stu-id="2a613-109">If COM is not able to access the user profile registry hive, it will access the **HKEY\_LOCAL\_MACHINE\\System** hive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a613-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2a613-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a613-111">Registro</span><span class="sxs-lookup"><span data-stu-id="2a613-111">Registry</span></span>](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
