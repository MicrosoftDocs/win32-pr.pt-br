---
description: O valor da propriedade REMOVE é uma lista de recursos delimitados por vírgulas que devem ser removidas.
ms.assetid: 39f4609a-7bf8-42b3-b23e-0d6a40b69fd3
title: propriedade REMOVE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8f46bcd5547abdefd67f98dff312bfdf1dff41e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747323"
---
# <a name="remove-property"></a><span data-ttu-id="8c6b6-103">propriedade REMOVE</span><span class="sxs-lookup"><span data-stu-id="8c6b6-103">REMOVE property</span></span>

<span data-ttu-id="8c6b6-104">O valor da propriedade **Remove** é uma lista de recursos delimitados por vírgulas que devem ser removidas.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-104">The value of the **REMOVE** property is a list of features delimited by commas that are to be removed.</span></span> <span data-ttu-id="8c6b6-105">Os recursos devem estar presentes na coluna recurso da tabela de [recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c6b6-105">The features must be present in the Feature column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="8c6b6-106">Observe que se você usar REMOVE = ALL na linha de comando, o instalador removerá todos os recursos que têm um nível de instalação maior que 0.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-106">Note that if you use REMOVE=ALL on the command line, the installer removes all features having an install level greater than 0.</span></span> <span data-ttu-id="8c6b6-107">Nesse caso, o instalador não remove os recursos que têm um nível de instalação de 0.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-107">In this case, the installer does not remove features having an install level of 0.</span></span> <span data-ttu-id="8c6b6-108">Para obter mais informações sobre o nível de instalação dos recursos, consulte [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="8c6b6-108">For more information about the install level of features see [Feature table](feature-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8c6b6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c6b6-109">Remarks</span></span>

<span data-ttu-id="8c6b6-110">Para determinar se um produto foi definido para ser completamente desinstalado, um autor de pacote pode usar uma expressão condicional para verificar se REMOVE = ALL.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-110">To determine whether a product has been set to be completely uninstalled, a package author may use a conditional expression to check whether REMOVE=ALL.</span></span> <span data-ttu-id="8c6b6-111">Observe que, se o produto for removido definindo seu principal recurso como ausente, a propriedade **Remove** poderá não ser igual a All após a [ação InstallValidate](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="8c6b6-111">Note that if the product is removed by setting its top feature to absent, the **REMOVE** property may not equal ALL until after the [InstallValidate action](installvalidate-action.md).</span></span> <span data-ttu-id="8c6b6-112">Isso significa que qualquer ação personalizada que dependa de REMOVE = ALL deve ser sequenciada após o InstallValidate.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-112">This means that any custom action that depends upon REMOVE=ALL must be sequenced after the InstallValidate.</span></span> <span data-ttu-id="8c6b6-113">Para obter mais informações, consulte também [ações de condicionamento a serem executadas durante a remoção](conditioning-actions-to-run-during-removal.md).</span><span class="sxs-lookup"><span data-stu-id="8c6b6-113">For more information see also [Conditioning Actions to Run During Removal](conditioning-actions-to-run-during-removal.md).</span></span> <span data-ttu-id="8c6b6-114">Observe que os nomes dos recursos diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-114">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="8c6b6-115">O instalador sempre avalia as seguintes propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="8c6b6-115">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="8c6b6-116">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-116">**ADDLOCAL**</span></span>](addlocal.md)
2.  <span data-ttu-id="8c6b6-117">**EXCLU**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-117">**REMOVE**</span></span>
3.  [<span data-ttu-id="8c6b6-118">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-118">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="8c6b6-119">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-119">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="8c6b6-120">**Install**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-120">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="8c6b6-121">**ANUNCI**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-121">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="8c6b6-122">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-122">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="8c6b6-123">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-123">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="8c6b6-124">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-124">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="8c6b6-125">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="8c6b6-126">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="8c6b6-127">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8c6b6-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="8c6b6-128">Por exemplo, se a linha de comando especificar ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e MyFeature será definido como Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-128">For example, if the command line specifies ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="8c6b6-129">Se a linha de comando for addsource = todos, ADDLOCAL = MyFeature, primeiro MyFeature estiver definido como Run-local, quando ADDSOURCE = ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para executar-de-source.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-129">If the command line is ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="8c6b6-130">O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c6b6-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c6b6-131">Requirements</span></span>



| <span data-ttu-id="8c6b6-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c6b6-132">Requirement</span></span> | <span data-ttu-id="8c6b6-133">Valor</span><span class="sxs-lookup"><span data-stu-id="8c6b6-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c6b6-134">Versão</span><span class="sxs-lookup"><span data-stu-id="8c6b6-134">Version</span></span><br/> | <span data-ttu-id="8c6b6-135">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8c6b6-136">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8c6b6-137">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8c6b6-138">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="8c6b6-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c6b6-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c6b6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c6b6-140">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8c6b6-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




