---
description: Essa é uma política de sistema por máquina que pode ser usada para aplicar as regras de componente de atualização durante pequenas atualizações e atualizações secundárias.
ms.assetid: 0d39c059-d936-454c-aed8-efedd3da7473
title: EnforceUpgradeComponentRules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a2fc093c2f0beb4167374f93447d978bbca8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921912"
---
# <a name="enforceupgradecomponentrules"></a><span data-ttu-id="d1fd5-103">EnforceUpgradeComponentRules</span><span class="sxs-lookup"><span data-stu-id="d1fd5-103">EnforceUpgradeComponentRules</span></span>

<span data-ttu-id="d1fd5-104">Essa é uma [política de sistema](system-policy.md) por máquina que pode ser usada para aplicar as regras de componente de atualização durante [pequenas atualizações](small-updates.md) e atualizações [secundárias](minor-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="d1fd5-104">This is a per-machine [system policy](system-policy.md) that can be used to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md).</span></span>

<span data-ttu-id="d1fd5-105">Defina a política EnforceUpgradeComponentRules como 1 para aplicar as regras de componente de atualização durante [pequenas atualizações](small-updates.md) [e pequenas atualizações de](minor-upgrades.md) todos os produtos no computador.</span><span class="sxs-lookup"><span data-stu-id="d1fd5-105">Set the EnforceUpgradeComponentRules policy to 1 to apply upgrade component rules during [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) of all products on the computer.</span></span> <span data-ttu-id="d1fd5-106">Para aplicar as regras durante pequenas atualizações e pequenas atualizações de um produto específico, defina a propriedade [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) como 1 na linha de comando ou na [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="d1fd5-106">To apply the rules during small updates and minor upgrades of a particular product, set the [**MSIENFORCEUPGRADECOMPONENTRULES**](msienforceupgradecomponentrules.md) property to 1 on the command line or in the [Property table](property-table.md).</span></span>

<span data-ttu-id="d1fd5-107">Quando a propriedade ou a política foi definida como 1, [as pequenas atualizações](small-updates.md) e atualizações [secundárias](minor-upgrades.md) podem falhar porque a atualização tenta fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d1fd5-107">When the property or policy has been set to 1, [small updates](small-updates.md) and [minor upgrades](minor-upgrades.md) can fail because the update attempts to do the following:</span></span>

-   <span data-ttu-id="d1fd5-108">Adicione um novo recurso à parte superior ou central de uma árvore de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="d1fd5-108">Add a new feature to the top or middle of an existing feature tree.</span></span>

    <span data-ttu-id="d1fd5-109">O novo recurso deve ser adicionado como um novo recurso folha a uma árvore de recursos existente.</span><span class="sxs-lookup"><span data-stu-id="d1fd5-109">The new feature must be added as a new leaf feature to an existing feature tree.</span></span>

    <span data-ttu-id="d1fd5-110">Nesse caso, o [**ProductCode**](productcode.md) do produto pode ser alterado e as atualizações podem ser tratadas como uma [atualização principal](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="d1fd5-110">In this case, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

-   <span data-ttu-id="d1fd5-111">Remover um componente de um recurso.</span><span class="sxs-lookup"><span data-stu-id="d1fd5-111">Remove a component from a feature.</span></span>

    <span data-ttu-id="d1fd5-112">Isso também pode ocorrer se você alterar o GUID de um componente.</span><span class="sxs-lookup"><span data-stu-id="d1fd5-112">This can also occur if you change the GUID of a component.</span></span> <span data-ttu-id="d1fd5-113">O componente identificado pelo GUID original parece ser removido e o componente, conforme identificado pelo novo GUID, aparece como um novo componente.</span><span class="sxs-lookup"><span data-stu-id="d1fd5-113">The component identified by the original GUID appears to be removed and the component as identified by the new GUID appears as a new component.</span></span>

    <span data-ttu-id="d1fd5-114">**Windows Installer 4,5 e posterior:** O componente pode ser removido corretamente usando Windows Installer 4,5 ou posterior definindo o atributo **msidbComponentAttributesUninstallOnSupersedence** na tabela de [componentes](component-table.md) ou definindo a propriedade [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) .</span><span class="sxs-lookup"><span data-stu-id="d1fd5-114">**Windows Installer 4.5 and later:** The component can be removed correctly using Windows Installer 4.5 or later by setting the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md) or by setting the [**MSIUNINSTALLSUPERSEDEDCOMPONENTS**](msiuninstallsupersededcomponents.md) property.</span></span>

    <span data-ttu-id="d1fd5-115">Como alternativa, o [**ProductCode**](productcode.md) do produto pode ser alterado e as atualizações podem ser tratadas como uma [atualização principal](major-upgrades.md).</span><span class="sxs-lookup"><span data-stu-id="d1fd5-115">Alternatively, the [**ProductCode**](productcode.md) of the product can be changed and the updates can be treated as a [major upgrade](major-upgrades.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="d1fd5-116">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="d1fd5-116">Registry Key</span></span>

<span data-ttu-id="d1fd5-117">**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="d1fd5-117">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="d1fd5-118">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="d1fd5-118">Data Type</span></span>

<span data-ttu-id="d1fd5-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="d1fd5-119">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1fd5-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1fd5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1fd5-121">Sem suporte no Windows Installer 2,0 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="d1fd5-121">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



