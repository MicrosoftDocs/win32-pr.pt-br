---
description: O instalador definirá o valor da propriedade MsiSystemRebootPending como 1 se houver uma operação pendente para renomear um arquivo.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Propriedade MsiSystemRebootPending
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759649"
---
# <a name="msisystemrebootpending-property"></a><span data-ttu-id="2ab8b-103">Propriedade MsiSystemRebootPending</span><span class="sxs-lookup"><span data-stu-id="2ab8b-103">MsiSystemRebootPending property</span></span>

<span data-ttu-id="2ab8b-104">O instalador definirá o valor da propriedade **MsiSystemRebootPending** como 1 se houver uma operação pendente para renomear um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2ab8b-104">The installer sets the value of the **MsiSystemRebootPending** property to 1 if there is an operation pending to rename a file.</span></span>

<span data-ttu-id="2ab8b-105">Os autores de pacote podem basear uma condição na [tabela LaunchCondition](launchcondition-table.md) nessa propriedade para evitar a instalação do pacote nos casos em que há uma operação pendente para renomear um arquivo.</span><span class="sxs-lookup"><span data-stu-id="2ab8b-105">Package authors can base a condition in the [LaunchCondition table](launchcondition-table.md) on this property to prevent the installation of their package in cases where there is an operation pending to rename a file.</span></span> <span data-ttu-id="2ab8b-106">Isso pode ser feito para evitar uma reinicialização do sistema operacional causado pela renomeação do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2ab8b-106">This may be done to prevent a restart of the operating system caused by the renaming of the file.</span></span> <span data-ttu-id="2ab8b-107">O instalador não define a propriedade **MsiSystemRebootPending** em todos os casos que exijam uma reinicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="2ab8b-107">The installer does not set the **MsiSystemRebootPending** property in all cases that require a restart of the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ab8b-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ab8b-108">Requirements</span></span>



| <span data-ttu-id="2ab8b-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ab8b-109">Requirement</span></span> | <span data-ttu-id="2ab8b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2ab8b-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ab8b-111">Versão</span><span class="sxs-lookup"><span data-stu-id="2ab8b-111">Version</span></span><br/> | <span data-ttu-id="2ab8b-112">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2ab8b-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2ab8b-113">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2ab8b-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2ab8b-114">Windows Installer 4,5 no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2ab8b-114">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2ab8b-115">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="2ab8b-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ab8b-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ab8b-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ab8b-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2ab8b-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="2ab8b-118">Reinicializações do sistema</span><span class="sxs-lookup"><span data-stu-id="2ab8b-118">System Reboots</span></span>](system-reboots.md)
</dt> <dt>

[<span data-ttu-id="2ab8b-119">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="2ab8b-119">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




