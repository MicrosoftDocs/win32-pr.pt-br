---
description: O instalador definirá a propriedade OutOfDiskSpace como TRUE se qualquer volume que for um destino da instalação atual não tiver espaço em disco suficiente para acomodar a instalação.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Propriedade OutOfDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760835"
---
# <a name="outofdiskspace-property"></a><span data-ttu-id="a5526-103">Propriedade OutOfDiskSpace</span><span class="sxs-lookup"><span data-stu-id="a5526-103">OutOfDiskSpace property</span></span>

<span data-ttu-id="a5526-104">O instalador definirá a propriedade **OutOfDiskSpace** como true se qualquer volume que for um destino da instalação atual não tiver espaço em disco suficiente para acomodar a instalação.</span><span class="sxs-lookup"><span data-stu-id="a5526-104">The installer sets the **OutOfDiskSpace** property to TRUE if any volume that is a target of the current installation has insufficient disk space to accommodate the installation.</span></span> <span data-ttu-id="a5526-105">Se todos os volumes tiverem espaço suficiente, o valor será FALSE.</span><span class="sxs-lookup"><span data-stu-id="a5526-105">If all volumes have sufficient space, the value is FALSE.</span></span> <span data-ttu-id="a5526-106">As ações de resolução de seleção usam esse valor para cancelar uma instalação e gerar uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a5526-106">Selection resolution actions use this value to cancel an installation and generate a dialog box.</span></span>

<span data-ttu-id="a5526-107">Essa propriedade é válida a qualquer momento após a execução da [ação CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="a5526-107">This property is valid at any time after the [CostFinalize action](costfinalize-action.md) is executed.</span></span> <span data-ttu-id="a5526-108">O status da propriedade [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) é atualizado dinamicamente sempre que o custo total da instalação é recalculado (por exemplo, sempre que o estado da instalação de qualquer recurso é alterado por meio da caixa de diálogo de [seleção](selection-dialog.md) ).</span><span class="sxs-lookup"><span data-stu-id="a5526-108">The [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) property status is dynamically updated any time the total installation cost is recalculated (for example, any time the installation state of any feature is changed through the [Selection](selection-dialog.md) dialog).</span></span>

## <a name="remarks"></a><span data-ttu-id="a5526-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5526-109">Remarks</span></span>

<span data-ttu-id="a5526-110">Qualquer caixa de diálogo que dependa da propriedade **OutOfDiskSpace** para determinar se uma caixa de diálogo deve ser exibida, defina o [bit do estilo da caixa](trackdiskspace-dialog-style-bit.md) de diálogo TrackDiskSpace para que a caixa de diálogo atualize dinamicamente o espaço nos volumes de destino.</span><span class="sxs-lookup"><span data-stu-id="a5526-110">Any dialog relying on the **OutOfDiskSpace** property to determine whether to bring up a dialog must set the [TrackDiskSpace Dialog Style Bit](trackdiskspace-dialog-style-bit.md) for the dialog to dynamically update space on the target volumes.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5526-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5526-111">Requirements</span></span>



| <span data-ttu-id="a5526-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5526-112">Requirement</span></span> | <span data-ttu-id="a5526-113">Valor</span><span class="sxs-lookup"><span data-stu-id="a5526-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5526-114">Versão</span><span class="sxs-lookup"><span data-stu-id="a5526-114">Version</span></span><br/> | <span data-ttu-id="a5526-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a5526-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="a5526-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a5526-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="a5526-117">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a5526-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="a5526-118">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="a5526-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5526-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5526-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5526-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a5526-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




