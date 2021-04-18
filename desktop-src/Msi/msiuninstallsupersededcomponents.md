---
description: Defina a propriedade MSIUNINSTALLSUPERSEDEDCOMPONENTS como 1 na tabela de propriedades ou em uma linha de comando.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: Propriedade MSIUNINSTALLSUPERSEDEDCOMPONENTS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757385"
---
# <a name="msiuninstallsupersededcomponents-property"></a><span data-ttu-id="9d269-103">Propriedade MSIUNINSTALLSUPERSEDEDCOMPONENTS</span><span class="sxs-lookup"><span data-stu-id="9d269-103">MSIUNINSTALLSUPERSEDEDCOMPONENTS property</span></span>

<span data-ttu-id="9d269-104">Defina a propriedade **MSIUNINSTALLSUPERSEDEDCOMPONENTS** como 1 na [tabela de propriedades](property-table.md) ou em uma linha de comando.</span><span class="sxs-lookup"><span data-stu-id="9d269-104">Set the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** property to 1 in the [Property table](property-table.md) or on a command line.</span></span> <span data-ttu-id="9d269-105">Quando essa propriedade tiver sido definida como 1, o instalador determinará se os componentes em quaisquer patches substituídos estão se tornando redundantes.</span><span class="sxs-lookup"><span data-stu-id="9d269-105">When this property has been set to 1, the installer determines whether the components in any superseded patches are becoming redundant.</span></span> <span data-ttu-id="9d269-106">O instalador pode cancelar o registro e desinstalar componentes redundantes para evitar deixar por trás componentes órfãos no computador.</span><span class="sxs-lookup"><span data-stu-id="9d269-106">The installer can unregister and uninstall redundant components to prevent leaving behind orphan components on the computer.</span></span>

<span data-ttu-id="9d269-107">A definição dessa propriedade afeta os componentes em todos os patches que estão sendo substituídos.</span><span class="sxs-lookup"><span data-stu-id="9d269-107">Setting this property affects the components in all patches being superseded.</span></span> <span data-ttu-id="9d269-108">Para habilitar essa funcionalidade para componentes únicos, use o atributo **msidbComponentAttributesUninstallOnSupersedence** na [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="9d269-108">To enable this functionality for single components, use the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md).</span></span>

<span data-ttu-id="9d269-109">**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="9d269-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="9d269-110">Versões anteriores a Windows Installer 4,5 ignoram a propriedade **MSIUNINSTALLSUPERSEDEDCOMPONENTS** .</span><span class="sxs-lookup"><span data-stu-id="9d269-110">Versions earlier than Windows Installer 4.5 ignore the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** Property.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d269-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d269-111">Requirements</span></span>



| <span data-ttu-id="9d269-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d269-112">Requirement</span></span> | <span data-ttu-id="9d269-113">Valor</span><span class="sxs-lookup"><span data-stu-id="9d269-113">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d269-114">Versão</span><span class="sxs-lookup"><span data-stu-id="9d269-114">Version</span></span><br/> | <span data-ttu-id="9d269-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9d269-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9d269-116">Windows Installer 4,5 ou Windows Installer 4,5 no Windows Vista, no Windows XP, no Windows Server 2003 e no Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="9d269-116">Windows Installer 4.5 or Windows Installer 4.5 on Windows Vista, Windows XP, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="9d269-117">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9d269-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9d269-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d269-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d269-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d269-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




