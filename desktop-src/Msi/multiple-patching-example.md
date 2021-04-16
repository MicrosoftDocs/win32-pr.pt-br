---
description: O exemplo a seguir mostra como Windows Installer 3,0 e posterior podem ser usados para aplicar patches na ordem em que são criados.
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: Exemplo de vários patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754351"
---
# <a name="multiple-patching-example"></a><span data-ttu-id="4751f-103">Exemplo de vários patches</span><span class="sxs-lookup"><span data-stu-id="4751f-103">Multiple Patching Example</span></span>

<span data-ttu-id="4751f-104">O exemplo a seguir mostra como Windows Installer 3,0 e posterior podem ser usados para aplicar patches na ordem em que são criados.</span><span class="sxs-lookup"><span data-stu-id="4751f-104">The following example shows how Windows Installer 3.0 and later can be used to apply patches in the order in which they are authored.</span></span>

## <a name="example"></a><span data-ttu-id="4751f-105">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4751f-105">Example</span></span>

<span data-ttu-id="4751f-106">Neste exemplo, há três patches, QFE1, QFE2 e ServicePack1, e cada um deles tem uma tabela [MsiPatchSequence](msipatchsequence-table.md) .</span><span class="sxs-lookup"><span data-stu-id="4751f-106">In this example there are three patches, QFE1, QFE2, and ServicePack1, and they each have a [MsiPatchSequence](msipatchsequence-table.md) table.</span></span> <span data-ttu-id="4751f-107">Esses patches foram criados para serem aplicados à versão 1,0 do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4751f-107">These patches have been authored to be applied to version 1.0 of the application.</span></span>



| <span data-ttu-id="4751f-108">Nome do patch</span><span class="sxs-lookup"><span data-stu-id="4751f-108">Patch Name</span></span>   | <span data-ttu-id="4751f-109">Tipo de patch</span><span class="sxs-lookup"><span data-stu-id="4751f-109">Patch Type</span></span>    | <span data-ttu-id="4751f-110">Número de Sequência</span><span class="sxs-lookup"><span data-stu-id="4751f-110">Sequence Number</span></span> |
|--------------|---------------|-----------------|
| <span data-ttu-id="4751f-111">QFE1</span><span class="sxs-lookup"><span data-stu-id="4751f-111">QFE1</span></span>         | <span data-ttu-id="4751f-112">Pequena atualização</span><span class="sxs-lookup"><span data-stu-id="4751f-112">Small Update</span></span>  | <span data-ttu-id="4751f-113">1.1.0</span><span class="sxs-lookup"><span data-stu-id="4751f-113">1.1.0</span></span>           |
| <span data-ttu-id="4751f-114">QFE2</span><span class="sxs-lookup"><span data-stu-id="4751f-114">QFE2</span></span>         | <span data-ttu-id="4751f-115">Pequena atualização</span><span class="sxs-lookup"><span data-stu-id="4751f-115">Small Update</span></span>  | <span data-ttu-id="4751f-116">1.2.0</span><span class="sxs-lookup"><span data-stu-id="4751f-116">1.2.0</span></span>           |
| <span data-ttu-id="4751f-117">ServicePack1</span><span class="sxs-lookup"><span data-stu-id="4751f-117">ServicePack1</span></span> | <span data-ttu-id="4751f-118">Atualização secundária</span><span class="sxs-lookup"><span data-stu-id="4751f-118">Minor Upgrade</span></span> | <span data-ttu-id="4751f-119">1.3.0</span><span class="sxs-lookup"><span data-stu-id="4751f-119">1.3.0</span></span>           |



 

<span data-ttu-id="4751f-120">A tabela [MsiPatchSequence](msipatchsequence-table.md) de cada patch tem apenas um registro que contém a família de patches, o código do produto e o número de sequência.</span><span class="sxs-lookup"><span data-stu-id="4751f-120">The [MsiPatchSequence](msipatchsequence-table.md) table of each patch has only one record that contains the patch family, product code, and sequence number.</span></span> <span data-ttu-id="4751f-121">Os três patches são todos aplicados ao mesmo produto e pertencem à mesma família de patches, chamada AppPatch.</span><span class="sxs-lookup"><span data-stu-id="4751f-121">The three patches are all applied to the same product and belong to the same patch family, named AppPatch.</span></span> <span data-ttu-id="4751f-122">Nenhum dos patches tem o atributo **msidbPatchSequenceSupersedeEarlier** .</span><span class="sxs-lookup"><span data-stu-id="4751f-122">None of the patches have the **msidbPatchSequenceSupersedeEarlier** attribute.</span></span>

<span data-ttu-id="4751f-123">[Tabela MsiPatchSequence](msipatchsequence-table.md) para a [atualização pequena](small-updates.md)do QFE1.</span><span class="sxs-lookup"><span data-stu-id="4751f-123">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE1 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="4751f-124">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="4751f-124">PatchFamily</span></span> | <span data-ttu-id="4751f-125">ProductCode</span><span class="sxs-lookup"><span data-stu-id="4751f-125">ProductCode</span></span>                            | <span data-ttu-id="4751f-126">Sequência</span><span class="sxs-lookup"><span data-stu-id="4751f-126">Sequence</span></span> | <span data-ttu-id="4751f-127">Atributos</span><span class="sxs-lookup"><span data-stu-id="4751f-127">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="4751f-128">AppPatch</span><span class="sxs-lookup"><span data-stu-id="4751f-128">AppPatch</span></span>    | <span data-ttu-id="4751f-129">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="4751f-129">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="4751f-130">1.1.0</span><span class="sxs-lookup"><span data-stu-id="4751f-130">1.1.0</span></span>    |            |



 

<span data-ttu-id="4751f-131">[Tabela MsiPatchSequence](msipatchsequence-table.md) para a [atualização pequena](small-updates.md)do QFE2.</span><span class="sxs-lookup"><span data-stu-id="4751f-131">[MsiPatchSequence Table](msipatchsequence-table.md) for the QFE2 [small update](small-updates.md).</span></span> 

| <span data-ttu-id="4751f-132">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="4751f-132">PatchFamily</span></span> | <span data-ttu-id="4751f-133">ProductCode</span><span class="sxs-lookup"><span data-stu-id="4751f-133">ProductCode</span></span>                            | <span data-ttu-id="4751f-134">Sequência</span><span class="sxs-lookup"><span data-stu-id="4751f-134">Sequence</span></span> | <span data-ttu-id="4751f-135">Atributos</span><span class="sxs-lookup"><span data-stu-id="4751f-135">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="4751f-136">AppPatch</span><span class="sxs-lookup"><span data-stu-id="4751f-136">AppPatch</span></span>    | <span data-ttu-id="4751f-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="4751f-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="4751f-138">1.2.0</span><span class="sxs-lookup"><span data-stu-id="4751f-138">1.2.0</span></span>    |            |



 

<span data-ttu-id="4751f-139">[Tabela MsiPatchSequence](msipatchsequence-table.md) para [atualização secundária](minor-upgrades.md)ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="4751f-139">[MsiPatchSequence Table](msipatchsequence-table.md) for ServicePack1 [minor upgrade](minor-upgrades.md).</span></span> 

| <span data-ttu-id="4751f-140">PatchFamily</span><span class="sxs-lookup"><span data-stu-id="4751f-140">PatchFamily</span></span> | <span data-ttu-id="4751f-141">ProductCode</span><span class="sxs-lookup"><span data-stu-id="4751f-141">ProductCode</span></span>                            | <span data-ttu-id="4751f-142">Sequência</span><span class="sxs-lookup"><span data-stu-id="4751f-142">Sequence</span></span> | <span data-ttu-id="4751f-143">Atributos</span><span class="sxs-lookup"><span data-stu-id="4751f-143">Attributes</span></span> |
|-------------|----------------------------------------|----------|------------|
| <span data-ttu-id="4751f-144">AppPatch</span><span class="sxs-lookup"><span data-stu-id="4751f-144">AppPatch</span></span>    | <span data-ttu-id="4751f-145">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="4751f-145">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> | <span data-ttu-id="4751f-146">1.3.0</span><span class="sxs-lookup"><span data-stu-id="4751f-146">1.3.0</span></span>    |            |



 

<span data-ttu-id="4751f-147">Se um usuário instalar a versão 1,0 do produto e, em seguida, aplicar QFE2 e, em uma data posterior, decidir aplicar QFE1, Windows Installer garantirá que a sequência efetiva do aplicativo de patch para o produto seja QFE1 aplicada à frente do QFE2.</span><span class="sxs-lookup"><span data-stu-id="4751f-147">If a user installs version 1.0 of the product, and then applies QFE2, and then at a later date decides to apply QFE1, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 applied ahead of QFE2.</span></span> <span data-ttu-id="4751f-148">Se o usuário aplicar ServicePack1, o aplicará QFE2 e QFE1 juntos em uma data posterior, Windows Installer garantirá que a sequência efetiva do aplicativo de patch para o produto seja QFE1 à frente de QFE2 e à frente de ServicePack1.</span><span class="sxs-lookup"><span data-stu-id="4751f-148">If the user applies ServicePack1, then applies QFE2 and QFE1 together at a later date, Windows Installer ensures that the effective sequence of patch application to the product is QFE1 ahead of QFE2 and ahead of ServicePack1.</span></span>

<span data-ttu-id="4751f-149">Se ServicePack1 tiver **msidbPatchSequenceSupersedeEarlier** definido na coluna Attributes de sua tabela [MsiPatchSequence](msipatchsequence-table.md) , isso significará que o Service Pack contém todas as alterações em QFE1 e QFE2.</span><span class="sxs-lookup"><span data-stu-id="4751f-149">If ServicePack1 has **msidbPatchSequenceSupersedeEarlier** set in the Attributes column of its [MsiPatchSequence](msipatchsequence-table.md) table, this means that the service pack contains all the changes in QFE1 and QFE2.</span></span> <span data-ttu-id="4751f-150">Nesse caso, QFE1 e QFE2 não são aplicados quando ServicePack1 é aplicado.</span><span class="sxs-lookup"><span data-stu-id="4751f-150">In this case, QFE1 and QFE2 are not applied when ServicePack1 is applied.</span></span>

<span data-ttu-id="4751f-151">**Windows Installer 2,0:** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="4751f-151">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="4751f-152">Versões anteriores a Windows Installer 3,0 podem instalar apenas um patch por transação e os patches são aplicados na sequência em que são fornecidos.</span><span class="sxs-lookup"><span data-stu-id="4751f-152">Versions earlier than Windows Installer 3.0 can install only one patch per transaction and patches are applied in the sequence that they are provided.</span></span> <span data-ttu-id="4751f-153">Para o exemplo anterior, se QFE2 for aplicado primeiro e, em seguida, QFE1 for aplicado, ou seja, duas transações e os patches serão aplicados à versão 1,0 do aplicativo na sequência QFE2 seguida por QFE1.</span><span class="sxs-lookup"><span data-stu-id="4751f-153">For the preceding example, if QFE2 is applied first and then QFE1 is applied, that is two transactions and the patches are applied to version 1.0 of the application in the sequence QFE2 followed by QFE1.</span></span> <span data-ttu-id="4751f-154">Se ServicePack1 for aplicado primeiro, QFE1 ou QFE2 não poderão ser aplicados em uma transação posterior porque ServicePack1 é uma atualização secundária que altera a versão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4751f-154">If ServicePack1 is applied first, then QFE1 or QFE2 cannot be applied in a later transaction because ServicePack1 is a minor upgrade that changes the application version.</span></span> <span data-ttu-id="4751f-155">QFE1 e QFE2 só podem ser aplicados à versão 1,0 do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4751f-155">QFE1 and QFE2 can only be applied to version 1.0 of the application.</span></span>

 

 



