---
description: Os binários do Windows Server 2003 com Service Pack 1 (SP1) são compatíveis com o Windows Vista e o Windows Server 2008. No entanto, os binários de versões anteriores do Windows devem ser recompilados.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Portando aplicativos de backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505746"
---
# <a name="porting-backup-applications"></a><span data-ttu-id="d85ae-104">Portando aplicativos de backup</span><span class="sxs-lookup"><span data-stu-id="d85ae-104">Porting Backup Applications</span></span>

<span data-ttu-id="d85ae-105">Os binários do Windows Server 2003 com Service Pack 1 (SP1) são compatíveis com o Windows Vista e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d85ae-105">Binaries from Windows Server 2003 with Service Pack 1 (SP1) are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="d85ae-106">No entanto, os binários de versões anteriores do Windows devem ser recompilados.</span><span class="sxs-lookup"><span data-stu-id="d85ae-106">However, binaries from earlier versions of Windows must be recompiled.</span></span>

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a><span data-ttu-id="d85ae-107">Portando aplicativos de backup do Windows XP para o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d85ae-107">Porting Windows XP Backup Applications to Windows Vista</span></span>

<span data-ttu-id="d85ae-108">Várias interfaces VSS foram alteradas desde o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d85ae-108">Several VSS interfaces have changed since Windows XP.</span></span> <span data-ttu-id="d85ae-109">No mínimo, os aplicativos do Windows XP devem ser recompilados usando arquivos de cabeçalho e bibliotecas do SDK do VSS 7,2 ou do SDK do Windows Vista ou do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d85ae-109">At a minimum, Windows XP applications must be recompiled using header files and libraries from the VSS 7.2 SDK or the Windows Vista or Windows Server 2008 SDK.</span></span>

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a><span data-ttu-id="d85ae-110">Portando aplicativos de backup do Windows Server 2003 SP1 para o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d85ae-110">Porting Windows Server 2003 SP1 Backup Applications to Windows Vista</span></span>

<span data-ttu-id="d85ae-111">Os binários do Windows Server 2003 com SP1 são compatíveis com o Windows Vista e o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d85ae-111">Binaries from Windows Server 2003 with SP1 are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="d85ae-112">No entanto, a maioria dos aplicativos de backup do Windows Server 2003 com SP1 deve ser atualizada para considerar novos recursos, que são descritos nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="d85ae-112">However, most Windows Server 2003 with SP1 backup applications must be updated to account for new features, which are described in the following sections.</span></span>

## <a name="compiling-backup-applications-for-windows-vista"></a><span data-ttu-id="d85ae-113">Compilando aplicativos de backup para o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d85ae-113">Compiling Backup Applications for Windows Vista</span></span>

<span data-ttu-id="d85ae-114">Os aplicativos que usam interfaces disponíveis no Windows Server 2003 podem ser compilados usando arquivos de cabeçalho e bibliotecas fornecidas no SDK do VSS 7,2.</span><span class="sxs-lookup"><span data-stu-id="d85ae-114">Applications that use interfaces available in Windows Server 2003 can be compiled using header files and libraries provided in the VSS 7.2 SDK.</span></span> <span data-ttu-id="d85ae-115">Para usar novas interfaces, os aplicativos devem ser recompilados usando os arquivos de cabeçalho e as bibliotecas incluídas no SDK do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d85ae-115">To use new interfaces, applications must be recompiled using the header files and libraries included in the Windows Vista SDK.</span></span>

> [!Note]  
> <span data-ttu-id="d85ae-116">Os binários compilados usando o Windows Vista ou o Windows Server 2008 não são compatíveis com o Windows Server 2003 com SP1 ou versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="d85ae-116">Binaries compiled using Windows Vista or Windows Server 2008 are not compatible with Windows Server 2003 with SP1 or earlier versions of Windows.</span></span>

 

 

 



