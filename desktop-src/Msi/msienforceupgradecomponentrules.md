---
description: Defina a propriedade MSIENFORCEUPGRADECOMPONENTRULES como 1 na linha de comando ou na tabela de propriedades para aplicar as regras de atualização de componente durante pequenas atualizações e pequenas atualizações de um produto específico.
ms.assetid: 0c8424c7-ab9b-4a09-aaa8-6a3f44c2789f
title: Propriedade MSIENFORCEUPGRADECOMPONENTRULES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85d5946ba3a0001c988ddfe76eeaf95c008205b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811838"
---
# <a name="msienforceupgradecomponentrules-property"></a><span data-ttu-id="531ff-103">Propriedade MSIENFORCEUPGRADECOMPONENTRULES</span><span class="sxs-lookup"><span data-stu-id="531ff-103">MSIENFORCEUPGRADECOMPONENTRULES property</span></span>

<span data-ttu-id="531ff-104">Defina a propriedade **MSIENFORCEUPGRADECOMPONENTRULES** como 1 na linha de comando ou na [tabela de propriedades](property-table.md) para aplicar as regras de atualização de componente durante [pequenas atualizações](small-updates.md) e pequenas [atualizações](minor-upgrades.md) de um produto específico.</span><span class="sxs-lookup"><span data-stu-id="531ff-104">Set the **MSIENFORCEUPGRADECOMPONENTRULES** property to 1 on the command line or in the [Property table](property-table.md) to apply the upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of a particular product.</span></span> <span data-ttu-id="531ff-105">Para aplicar as regras durante pequenas atualizações e pequenas atualizações de todos os produtos no computador, defina a política [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) como 1.</span><span class="sxs-lookup"><span data-stu-id="531ff-105">To apply the rules during small updates and minor upgrades of all products on the computer, set the [EnforceUpgradeComponentRules](enforceupgradecomponentrules.md) policy to 1.</span></span>

<span data-ttu-id="531ff-106">Quando a propriedade ou a política é definida como 1, [as pequenas atualizações](small-updates.md) e atualizações [secundárias](minor-upgrades.md) podem falhar porque a atualização tenta fazer o seguinte que viola as regras de componente de atualização:</span><span class="sxs-lookup"><span data-stu-id="531ff-106">When the property or policy is set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update tries to do the following that violates the upgrade component rules:</span></span>

-   <span data-ttu-id="531ff-107">Adicione um novo recurso à parte superior ou central de uma árvore de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="531ff-107">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="531ff-108">O novo recurso deve ser adicionado como um novo recurso folha a uma árvore de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="531ff-108">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="531ff-109">Nesse caso, o [**ProductCode**](productcode.md) do produto pode ser alterado e a atualização pode ser tratada como uma [atualização principal](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="531ff-109">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="531ff-110">Remover um componente de um recurso.</span><span class="sxs-lookup"><span data-stu-id="531ff-110">Remove a component from a feature.</span></span>

    <span data-ttu-id="531ff-111">Isso também pode ocorrer se você alterar o GUID de um componente.</span><span class="sxs-lookup"><span data-stu-id="531ff-111">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="531ff-112">O componente identificado pelo GUID original parece ser removido e o componente, conforme identificado pelo novo GUID, aparece como um novo componente.</span><span class="sxs-lookup"><span data-stu-id="531ff-112">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="531ff-113">**Windows Installer 4,5 e posterior:** O componente pode ser removido corretamente usando Windows Installer 4,5 e posterior definindo o atributo **msidbComponentAttributesUninstallOnSupersedence** na tabela de [componentes](component-table.md) ou definindo a propriedade [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .</span><span class="sxs-lookup"><span data-stu-id="531ff-113">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 and later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component Table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="531ff-114">Como alternativa, o [**ProductCode**](productcode.md) do produto pode ser alterado e a atualização pode ser tratada como uma [atualização principal](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="531ff-114">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the update can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="531ff-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="531ff-115">Requirements</span></span>



| <span data-ttu-id="531ff-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="531ff-116">Requirement</span></span> | <span data-ttu-id="531ff-117">Valor</span><span class="sxs-lookup"><span data-stu-id="531ff-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="531ff-118">Versão</span><span class="sxs-lookup"><span data-stu-id="531ff-118">Version</span></span><br/> | <span data-ttu-id="531ff-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="531ff-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="531ff-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="531ff-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="531ff-121">Windows Installer 3,0 ou posterior no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="531ff-121">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="531ff-122">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="531ff-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="531ff-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="531ff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="531ff-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="531ff-124">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="531ff-125">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="531ff-125">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




