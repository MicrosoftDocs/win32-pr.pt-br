---
description: A propriedade ReplacedInUseFiles será definida se o instalador gravar em um arquivo que está sendo mantido em uso.
ms.assetid: cef7d36e-c721-4d47-beaa-53e6749334b6
title: Propriedade ReplacedInUseFiles
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d6826f1db2ec1844234cf32f1137e43c89528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747948"
---
# <a name="replacedinusefiles-property"></a><span data-ttu-id="c5d79-103">Propriedade ReplacedInUseFiles</span><span class="sxs-lookup"><span data-stu-id="c5d79-103">ReplacedInUseFiles property</span></span>

<span data-ttu-id="c5d79-104">A propriedade **ReplacedInUseFiles** será definida se o instalador gravar em um arquivo que está sendo mantido em uso.</span><span class="sxs-lookup"><span data-stu-id="c5d79-104">The **ReplacedInUseFiles** property is set if the installer writes over a file that is being held in use.</span></span> <span data-ttu-id="c5d79-105">Essa propriedade é usada por ações personalizadas para detectar que uma reinicialização é necessária para concluir a instalação.</span><span class="sxs-lookup"><span data-stu-id="c5d79-105">This property is used by custom actions to detect that a reboot is required to complete the installation.</span></span>

<span data-ttu-id="c5d79-106">Definido durante as ações [InstallExecute](installexecute-action.md) e [InstallFinalize](installfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c5d79-106">Set during the [InstallExecute](installexecute-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5d79-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5d79-107">Requirements</span></span>



| <span data-ttu-id="c5d79-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5d79-108">Requirement</span></span> | <span data-ttu-id="c5d79-109">Valor</span><span class="sxs-lookup"><span data-stu-id="c5d79-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5d79-110">Versão</span><span class="sxs-lookup"><span data-stu-id="c5d79-110">Version</span></span><br/> | <span data-ttu-id="c5d79-111">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c5d79-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c5d79-112">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c5d79-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c5d79-113">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c5d79-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c5d79-114">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c5d79-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c5d79-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5d79-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5d79-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c5d79-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




