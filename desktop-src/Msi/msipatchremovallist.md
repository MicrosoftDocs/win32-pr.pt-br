---
description: O instalador define o valor da propriedade MsiPatchRemovalList como uma lista de patches que estão sendo removidos durante a instalação.
ms.assetid: 6e0b391a-d840-4f01-af12-4708ce6c9ce8
title: Propriedade MsiPatchRemovalList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2af522d9570297f2ff911b501bc543cf4b5971c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758952"
---
# <a name="msipatchremovallist-property"></a><span data-ttu-id="92926-103">Propriedade MsiPatchRemovalList</span><span class="sxs-lookup"><span data-stu-id="92926-103">MsiPatchRemovalList property</span></span>

<span data-ttu-id="92926-104">O instalador define o valor da propriedade **MsiPatchRemovalList** como uma lista de patches que estão sendo removidos durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="92926-104">The installer sets the value of the **MsiPatchRemovalList** property to a list of patches that are being removed during the installation.</span></span> <span data-ttu-id="92926-105">Os patches são representados na lista por seus GUIDs de código de patch separados por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="92926-105">The patches are represented in the list by their patch code GUIDs separated by semicolons.</span></span>

<span data-ttu-id="92926-106">Os desenvolvedores podem usar a propriedade **MsiPatchRemovalList** para criar um pacote Windows Installer ou patch que executa [ações personalizadas](custom-actions.md) sobre a remoção de um patch.</span><span class="sxs-lookup"><span data-stu-id="92926-106">Developers can use the **MsiPatchRemovalList** property to author a Windows Installer package or patch that performs [custom actions](custom-actions.md) on the removal of a patch.</span></span> <span data-ttu-id="92926-107">A ação personalizada pode ser criada no pacote de instalação original, um patch que já foi aplicado ao pacote ou um patch que não é um [patch desinstalável](uninstallable-patches.md).</span><span class="sxs-lookup"><span data-stu-id="92926-107">The custom action can be authored into the original installation package, a patch that has already been applied to the package, or a patch that is not an [uninstallable patch](uninstallable-patches.md).</span></span> <span data-ttu-id="92926-108">A ação personalizada pode ser condicional na propriedade **MsiPatchRemovalList** nas tabelas de sequência.</span><span class="sxs-lookup"><span data-stu-id="92926-108">The custom action can be conditionalized on the **MsiPatchRemovalList** property in the sequence tables.</span></span> <span data-ttu-id="92926-109">Consulte [usando propriedades em instruções condicionais](using-properties-in-conditional-statements.md) para obter mais informações sobre a condicionalização de ações.</span><span class="sxs-lookup"><span data-stu-id="92926-109">See [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md) for more information about conditionalizing actions.</span></span>

<span data-ttu-id="92926-110">A ação personalizada pode obter os GUIDs dos patches que estão sendo removidos do valor da propriedade **MsiPatchRemovalList** .</span><span class="sxs-lookup"><span data-stu-id="92926-110">The custom action can obtain the GUIDs of patches being removed from the value of the **MsiPatchRemovalList** property.</span></span> <span data-ttu-id="92926-111">A ação personalizada pode determinar se o estado de instalação do patch é aplicado, obsoleto ou substituído chamando a função [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) ou a propriedade [**patchproperty**](patch-patchproperty.md) do [objeto patch](patch-object.md).</span><span class="sxs-lookup"><span data-stu-id="92926-111">The custom action can determine whether the installation state of the patch is applied, obsolete, or superseded by calling the [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) function or the [**PatchProperty**](patch-patchproperty.md) property of the [Patch object](patch-object.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="92926-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="92926-112">Remarks</span></span>

<span data-ttu-id="92926-113">Para obter mais informações sobre como remover patches, consulte [removendo patches](removing-patches.md).</span><span class="sxs-lookup"><span data-stu-id="92926-113">For more information about removing patches, see [Removing Patches](removing-patches.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="92926-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92926-114">Requirements</span></span>



| <span data-ttu-id="92926-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="92926-115">Requirement</span></span> | <span data-ttu-id="92926-116">Valor</span><span class="sxs-lookup"><span data-stu-id="92926-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92926-117">Versão</span><span class="sxs-lookup"><span data-stu-id="92926-117">Version</span></span><br/> | <span data-ttu-id="92926-118">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="92926-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="92926-119">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="92926-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="92926-120">Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="92926-120">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="92926-121">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="92926-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92926-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="92926-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92926-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="92926-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="92926-124">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="92926-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




