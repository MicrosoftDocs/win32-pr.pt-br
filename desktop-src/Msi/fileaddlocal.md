---
description: O valor da propriedade FILEADDLOCAL denota uma lista de chaves de arquivo delimitadas por vírgulas que devem ser instaladas para serem executadas a partir da mídia de origem local.
ms.assetid: 89ae876e-53f0-4c1d-ba16-7513af79ee5e
title: Propriedade FILEADDLOCAL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e3e05a35e5bcd4fc672a2feb6bd2f40619bfcb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758779"
---
# <a name="fileaddlocal-property"></a><span data-ttu-id="b505c-103">Propriedade FILEADDLOCAL</span><span class="sxs-lookup"><span data-stu-id="b505c-103">FILEADDLOCAL property</span></span>

<span data-ttu-id="b505c-104">O valor da propriedade **FILEADDLOCAL** denota uma lista de chaves de arquivo delimitadas por vírgulas que devem ser instaladas para serem executadas a partir da mídia de origem local.</span><span class="sxs-lookup"><span data-stu-id="b505c-104">The value of the **FILEADDLOCAL** property denotes a list of file keys delimited by commas that are to be installed to run from the local source media.</span></span> <span data-ttu-id="b505c-105">Para cada chave de arquivo na lista, o instalador determina o componente que controla esse arquivo e, em seguida, examina todos os recursos vinculados a esse componente pela tabela [FeatureComponents](featurecomponents-table.md) e instala o recurso que requer a quantidade mínima de espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="b505c-105">For each file key in the list, the installer determines the component that controls that file, then examines all features linked to that component by the [FeatureComponents](featurecomponents-table.md) table and installs the feature that requires the least amount of disk space.</span></span> <span data-ttu-id="b505c-106">As chaves de arquivo na lista devem estar presentes na coluna arquivo da tabela de [arquivos](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="b505c-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="b505c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b505c-107">Remarks</span></span>

<span data-ttu-id="b505c-108">Observe que os nomes de chave de arquivo diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="b505c-108">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="b505c-109">Observe também que, se o sinalizador de bit LocalOnly estiver definido na coluna atributos da tabela de [componentes](component-table.md) de um componente, o componente será instalado para ser executado localmente.</span><span class="sxs-lookup"><span data-stu-id="b505c-109">Also note that if the LocalOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run locally.</span></span>

<span data-ttu-id="b505c-110">O instalador sempre avalia as propriedades a seguir na seguinte ordem.</span><span class="sxs-lookup"><span data-stu-id="b505c-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="b505c-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="b505c-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="b505c-112">**EXCLU**</span><span class="sxs-lookup"><span data-stu-id="b505c-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="b505c-113">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="b505c-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="b505c-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b505c-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="b505c-115">**Install**</span><span class="sxs-lookup"><span data-stu-id="b505c-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="b505c-116">**ANUNCI**</span><span class="sxs-lookup"><span data-stu-id="b505c-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="b505c-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="b505c-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="b505c-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="b505c-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="b505c-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b505c-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. <span data-ttu-id="b505c-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="b505c-120">**FILEADDLOCAL**</span></span>
11. [<span data-ttu-id="b505c-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="b505c-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="b505c-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b505c-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="b505c-123">Por exemplo, se a linha de comando especificar: ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e MyFeature será definido como Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="b505c-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="b505c-124">Se a linha de comando for: addsource = todos, ADDLOCAL = MyFeature, primeiro MyFeature estiver definido como Run-local e, quando ADDSOURCE = ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para execução-da-source.</span><span class="sxs-lookup"><span data-stu-id="b505c-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="b505c-125">O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="b505c-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="b505c-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b505c-126">Requirements</span></span>



| <span data-ttu-id="b505c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b505c-127">Requirement</span></span> | <span data-ttu-id="b505c-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b505c-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b505c-129">Versão</span><span class="sxs-lookup"><span data-stu-id="b505c-129">Version</span></span><br/> | <span data-ttu-id="b505c-130">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b505c-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b505c-131">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b505c-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b505c-132">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b505c-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b505c-133">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b505c-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b505c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="b505c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b505c-135">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b505c-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




