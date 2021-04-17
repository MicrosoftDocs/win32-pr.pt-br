---
description: O instalador definirá a propriedade OutOfNoRbDiskSpace como true se qualquer volume que for um destino da instalação não tiver espaço em disco suficiente para acomodar a instalação.
ms.assetid: 910d6c1d-38d3-4680-b256-2bf30689ce11
title: Propriedade OutOfNoRbDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa9cdd7c1d444e141103ca148344dd26ea1d2a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748763"
---
# <a name="outofnorbdiskspace-property"></a><span data-ttu-id="09514-103">Propriedade OutOfNoRbDiskSpace</span><span class="sxs-lookup"><span data-stu-id="09514-103">OutOfNoRbDiskSpace property</span></span>

<span data-ttu-id="09514-104">O instalador definirá a propriedade **OutOfNoRbDiskSpace** como true se qualquer volume que for um destino da instalação não tiver espaço em disco suficiente para acomodar a instalação.</span><span class="sxs-lookup"><span data-stu-id="09514-104">The installer sets the **OutOfNoRbDiskSpace** property to True if any volume that is a target of the installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="09514-105">Nesse caso, a propriedade **OutOfNoRbDiskSpace** é definida como true mesmo que a reversão tenha sido desabilitada.</span><span class="sxs-lookup"><span data-stu-id="09514-105">In this case, the **OutOfNoRbDiskSpace** property is set to True even if rollback has been disabled.</span></span> <span data-ttu-id="09514-106">Se todos os volumes tiverem espaço suficiente, o valor será false.</span><span class="sxs-lookup"><span data-stu-id="09514-106">If all volumes have sufficient space, the value is False.</span></span>

<span data-ttu-id="09514-107">Um desenvolvedor de um pacote de instalação pode lidar com a situação em que a propriedade [**OutOfDiskSpace**](outofdiskspace.md) é verdadeira e a propriedade **OutOfNoRbDiskSpace** é false, criando uma interface do usuário que apresenta ao usuário uma opção para desabilitar a reversão e continuar a instalação.</span><span class="sxs-lookup"><span data-stu-id="09514-107">A developer of an installation package can handle the situation when the [**OutOfDiskSpace**](outofdiskspace.md) property is True and the **OutOfNoRbDiskSpace** property is False by authoring a user interface that presents the user with an option to disable rollback and continue the installation.</span></span> <span data-ttu-id="09514-108">Para obter informações sobre como exibir condicionalmente uma caixa de diálogo, consulte [visão geral do ControlEvent,](controlevent-overview.md).</span><span class="sxs-lookup"><span data-stu-id="09514-108">For information about conditionally displaying a dialog box, see [ControlEvent Overview](controlevent-overview.md).</span></span> <span data-ttu-id="09514-109">Para obter informações sobre como desabilitar a reversão, consulte [EnableRollback ControlEvent,](enablerollback-controlevent.md).</span><span class="sxs-lookup"><span data-stu-id="09514-109">For information about disabling rollback, see [EnableRollback ControlEvent](enablerollback-controlevent.md).</span></span>

<span data-ttu-id="09514-110">A propriedade **OutOfNoRbDiskSpace** é válida a qualquer momento após a execução da [ação CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="09514-110">The **OutOfNoRbDiskSpace** property is valid at any time after the [CostFinalize action](costfinalize-action.md) has been executed.</span></span> <span data-ttu-id="09514-111">O status da propriedade **OutOfNoRbDiskSpace** é atualizado dinamicamente sempre que o custo total da instalação é recalculado (por exemplo, sempre que o estado da instalação de qualquer recurso é alterado por meio da [caixa de diálogo de seleção](selection-dialog.md)).</span><span class="sxs-lookup"><span data-stu-id="09514-111">The **OutOfNoRbDiskSpace** property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection dialog](selection-dialog.md)).</span></span> <span data-ttu-id="09514-112">As ações de resolução de seleção usam esse valor para cancelar uma instalação e gerar uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="09514-112">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="09514-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09514-113">Requirements</span></span>



| <span data-ttu-id="09514-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="09514-114">Requirement</span></span> | <span data-ttu-id="09514-115">Valor</span><span class="sxs-lookup"><span data-stu-id="09514-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09514-116">Versão</span><span class="sxs-lookup"><span data-stu-id="09514-116">Version</span></span><br/> | <span data-ttu-id="09514-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="09514-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="09514-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="09514-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="09514-119">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="09514-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="09514-120">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="09514-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09514-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="09514-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09514-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="09514-122">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="09514-123">Visão geral do ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="09514-123">ControlEvent Overview</span></span>](controlevent-overview.md)
</dt> <dt>

[<span data-ttu-id="09514-124">**Propriedade OutOfDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="09514-124">**OutOfDiskSpace property**</span></span>](outofdiskspace.md)
</dt> <dt>

[<span data-ttu-id="09514-125">EnableRollback ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="09514-125">EnableRollback ControlEvent</span></span>](enablerollback-controlevent.md)
</dt> <dt>

[<span data-ttu-id="09514-126">Ação CostFinalize</span><span class="sxs-lookup"><span data-stu-id="09514-126">CostFinalize action</span></span>](costfinalize-action.md)
</dt> <dt>

[<span data-ttu-id="09514-127">Caixa de diálogo de seleção</span><span class="sxs-lookup"><span data-stu-id="09514-127">Selection dialog</span></span>](selection-dialog.md)
</dt> </dl>

 

 




