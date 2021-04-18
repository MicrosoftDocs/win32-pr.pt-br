---
description: O valor da propriedade addsource é uma lista de recursos delimitados por vírgulas e que devem ser instalados para serem executados da origem.
ms.assetid: 7bc38b49-72d8-4b0c-bd71-284a638e7860
title: Propriedade addsource
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd51d6f86060def1a7536134a0041f1e15178a91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755091"
---
# <a name="addsource-property"></a><span data-ttu-id="9e6f7-103">Propriedade addsource</span><span class="sxs-lookup"><span data-stu-id="9e6f7-103">ADDSOURCE property</span></span>

<span data-ttu-id="9e6f7-104">O valor da propriedade **addsource** é uma lista de recursos delimitados por vírgulas e que devem ser instalados para serem executados da origem.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-104">The value of the **ADDSOURCE** property is a list of features that are delimited by commas, and are to be installed to run from the source.</span></span> <span data-ttu-id="9e6f7-105">Os recursos devem estar presentes na coluna recurso da tabela de [recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="9e6f7-105">The features must be present in the Feature column of the [Feature Table](feature-table.md).</span></span> <span data-ttu-id="9e6f7-106">Para instalar todos os recursos como executar da origem, use addsource = todos na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-106">To install all features as run from source, use ADDSOURCE=ALL on the command line.</span></span> <span data-ttu-id="9e6f7-107">Não insira addsource = todos na tabela de [Propriedades](property-table.md), pois isso gera um pacote de execução do código-fonte que não pode ser removido corretamente.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-107">Do not enter ADDSOURCE=ALL into the [Property Table](property-table.md), because this generates a run-from-source package that cannot be correctly removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e6f7-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e6f7-108">Remarks</span></span>

<span data-ttu-id="9e6f7-109">Os nomes dos recursos diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-109">The feature names are case sensitive.</span></span> <span data-ttu-id="9e6f7-110">Se o sinalizador de bit LocalOnly for definido na coluna atributos da [tabela de componentes](component-table.md) para um componente de um recurso na lista, esse componente será instalado para ser executado localmente.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-110">If the LocalOnly bit flag is set in the Attributes column of the [Component Table](component-table.md) for a component of a feature in the list, that component is installed to run locally.</span></span>

<span data-ttu-id="9e6f7-111">O instalador sempre avalia as seguintes propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="9e6f7-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="9e6f7-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="9e6f7-113">**EXCLU**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-113">**REMOVE**</span></span>](remove.md)
3.  <span data-ttu-id="9e6f7-114">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-114">**ADDSOURCE**</span></span>
4.  [<span data-ttu-id="9e6f7-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="9e6f7-116">**Install**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="9e6f7-117">**ANUNCI**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="9e6f7-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="9e6f7-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="9e6f7-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="9e6f7-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="9e6f7-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="9e6f7-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9e6f7-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="9e6f7-124">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9e6f7-124">For example:</span></span>

-   <span data-ttu-id="9e6f7-125">Se a linha de comando especificar: ADDLOCAL = todos, addsource = **MyFeature**, todos os recursos serão definidos primeiro como Run-local e **MyFeature** será definido como Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = **MyFeature**, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="9e6f7-126">Se a linha de comando for: addsource = todos, ADDLOCAL =**MyFeature**, primeiro **MyFeature** estiver definido como Run-local e, quando addsource = All for avaliado, todos os recursos (incluindo **MyFeature**) serão redefinidos para execução-da-source.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=**MyFeature**, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="9e6f7-127">O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-127">The installer sets the [**Preselected**](preselected.md) Property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e6f7-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e6f7-128">Requirements</span></span>



| <span data-ttu-id="9e6f7-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e6f7-129">Requirement</span></span> | <span data-ttu-id="9e6f7-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9e6f7-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e6f7-131">Versão</span><span class="sxs-lookup"><span data-stu-id="9e6f7-131">Version</span></span><br/> | <span data-ttu-id="9e6f7-132">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9e6f7-133">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9e6f7-134">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9e6f7-135">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9e6f7-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e6f7-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e6f7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e6f7-137">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9e6f7-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




