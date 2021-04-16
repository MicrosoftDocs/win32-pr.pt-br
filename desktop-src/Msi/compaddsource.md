---
description: O valor da propriedade COMPADDSOURCE é uma lista de GUIDs de componente da coluna ComponentID da tabela de componentes, delimitada por vírgulas, que devem ser instaladas para serem executadas a partir da mídia de origem.
ms.assetid: ee1e0650-674d-4189-8ef7-3d2ece89cc28
title: Propriedade COMPADDSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f59526196a75599dbd2a535db6dcda4fb733936
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752263"
---
# <a name="compaddsource-property"></a><span data-ttu-id="9401d-103">Propriedade COMPADDSOURCE</span><span class="sxs-lookup"><span data-stu-id="9401d-103">COMPADDSOURCE property</span></span>

<span data-ttu-id="9401d-104">O valor da propriedade **COMPADDSOURCE** é uma lista de GUIDs de componente da coluna ComponentID da tabela de [componentes](component-table.md) , delimitada por vírgulas, que devem ser instaladas para serem executadas a partir da mídia de origem.</span><span class="sxs-lookup"><span data-stu-id="9401d-104">The value of the **COMPADDSOURCE** property is a list of component GUIDs from the ComponentId column of the [Component](component-table.md) table, delimited by commas, that are to be installed to run from the source media.</span></span> <span data-ttu-id="9401d-105">O instalador usa esse valor para determinar quais recursos estão definidos para serem executados a partir da origem, com base nos componentes especificados.</span><span class="sxs-lookup"><span data-stu-id="9401d-105">The installer uses this value to determine which features are set to be installed to run from source, based on the specified components.</span></span> <span data-ttu-id="9401d-106">Para cada ID de componente listado, o instalador examina todos os recursos vinculados (por meio da tabela [FeatureComponents](featurecomponents-table.md) ) para esse componente e instala o recurso que requer a quantidade mínima de espaço em disco a ser instalada.</span><span class="sxs-lookup"><span data-stu-id="9401d-106">For each listed component ID, the installer examines all features linked (through the [FeatureComponents](featurecomponents-table.md) table) to that component, and installs the feature that requires the least amount of disk space to install.</span></span> <span data-ttu-id="9401d-107">Os componentes listados devem estar presentes na coluna componente da tabela de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="9401d-107">The components listed must be present in the Component column of the [Component](component-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="9401d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="9401d-108">Remarks</span></span>

<span data-ttu-id="9401d-109">Observe que os nomes de componentes diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9401d-109">Note that the component names are case-sensitive.</span></span> <span data-ttu-id="9401d-110">Observe também que, se o sinalizador de bit LocalOnly estiver definido na coluna atributos da tabela de [componentes](component-table.md) de um componente, o componente será instalado para ser executado localmente.</span><span class="sxs-lookup"><span data-stu-id="9401d-110">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="9401d-111">O instalador sempre avalia as seguintes propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="9401d-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="9401d-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9401d-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="9401d-113">**EXCLU**</span><span class="sxs-lookup"><span data-stu-id="9401d-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="9401d-114">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="9401d-114">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="9401d-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9401d-115">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="9401d-116">**Install**</span><span class="sxs-lookup"><span data-stu-id="9401d-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="9401d-117">**ANUNCI**</span><span class="sxs-lookup"><span data-stu-id="9401d-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="9401d-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9401d-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  <span data-ttu-id="9401d-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9401d-119">**COMPADDSOURCE**</span></span>
9.  [<span data-ttu-id="9401d-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9401d-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="9401d-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="9401d-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="9401d-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="9401d-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="9401d-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="9401d-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="9401d-124">Por exemplo, se a linha de comando especificar: ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e MyFeature será definido como Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="9401d-124">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="9401d-125">Se a linha de comando for: addsource = todos, ADDLOCAL = MyFeature, primeiro MyFeature estiver definido como Run-local e, quando ADDSOURCE = ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para execução-da-source.</span><span class="sxs-lookup"><span data-stu-id="9401d-125">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="9401d-126">O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="9401d-126">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="9401d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9401d-127">Requirements</span></span>



| <span data-ttu-id="9401d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9401d-128">Requirement</span></span> | <span data-ttu-id="9401d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="9401d-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9401d-130">Versão</span><span class="sxs-lookup"><span data-stu-id="9401d-130">Version</span></span><br/> | <span data-ttu-id="9401d-131">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9401d-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9401d-132">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9401d-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9401d-133">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9401d-133">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="9401d-134">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="9401d-134">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9401d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9401d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9401d-136">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9401d-136">Properties</span></span>](properties.md)
</dt> </dl>

 

 




