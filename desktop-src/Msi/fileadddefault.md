---
description: O valor da propriedade FILEADDDEFAULT é uma lista de chaves de arquivo delimitadas por vírgulas que são instaladas em sua configuração padrão.
ms.assetid: 089b8dd9-1841-4b6d-8da8-d5aa5de85a68
title: Propriedade FILEADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c1afc9658c58b048c4e75232d7e550acb36e57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789779"
---
# <a name="fileadddefault-property"></a><span data-ttu-id="f5f70-103">Propriedade FILEADDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="f5f70-103">FILEADDDEFAULT property</span></span>

<span data-ttu-id="f5f70-104">O valor da propriedade **FILEADDDEFAULT** é uma lista de chaves de arquivo delimitadas por vírgulas que são instaladas em sua configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="f5f70-104">The value of the **FILEADDDEFAULT** property is a list of file keys delimited by commas that are installed in their default configuration.</span></span> <span data-ttu-id="f5f70-105">Para cada chave de arquivo na lista, o instalador determina o componente que controla esse arquivo e instala o recurso que requer o menor espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="f5f70-105">For each file key in the list, the installer determines the component that controls that file and installs the feature that requires the least disk space.</span></span> <span data-ttu-id="f5f70-106">As chaves de arquivo na lista devem estar presentes na coluna arquivo da tabela de [arquivos](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="f5f70-106">The file keys in the list must be present in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="f5f70-107">Um recurso é instalado no mesmo estado de instalação como se o usuário tivesse solicitado uma instalação sob demanda do recurso.</span><span class="sxs-lookup"><span data-stu-id="f5f70-107">A feature is installed in the same installation state as if the user had requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="f5f70-108">O estado é determinado pelo qual os bits são definidos para o recurso na coluna atributos da [tabela de recursos](feature-table.md)e quais bits são definidos para os componentes do recurso na coluna atributos da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f5f70-108">The state is determined by which bits are set for the feature in the Attributes column of the [Feature table](feature-table.md), and which bits are set for the feature's components in the Attributes column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f5f70-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5f70-109">Remarks</span></span>

<span data-ttu-id="f5f70-110">Observe que os nomes de chave de arquivo diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="f5f70-110">Note that the file key names are case-sensitive.</span></span> <span data-ttu-id="f5f70-111">Observe também que, se o sinalizador de bit SourceOnly for definido na coluna atributos da tabela de [componentes](component-table.md) de um componente, o componente será instalado para ser executado da origem.</span><span class="sxs-lookup"><span data-stu-id="f5f70-111">Also note that if the SourceOnly bit flag is set in the Attributes column of the [Component](component-table.md) table for a component, then the component is installed to run from source.</span></span>

<span data-ttu-id="f5f70-112">O instalador sempre avalia as propriedades a seguir na seguinte ordem.</span><span class="sxs-lookup"><span data-stu-id="f5f70-112">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="f5f70-113">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="f5f70-113">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="f5f70-114">**EXCLU**</span><span class="sxs-lookup"><span data-stu-id="f5f70-114">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="f5f70-115">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="f5f70-115">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="f5f70-116">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f5f70-116">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="f5f70-117">**Install**</span><span class="sxs-lookup"><span data-stu-id="f5f70-117">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="f5f70-118">**ANUNCI**</span><span class="sxs-lookup"><span data-stu-id="f5f70-118">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="f5f70-119">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="f5f70-119">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="f5f70-120">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="f5f70-120">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="f5f70-121">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f5f70-121">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="f5f70-122">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="f5f70-122">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="f5f70-123">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="f5f70-123">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. <span data-ttu-id="f5f70-124">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="f5f70-124">**FILEADDDEFAULT**</span></span>

<span data-ttu-id="f5f70-125">Por exemplo, se a linha de comando especificar: ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e MyFeature será definido como Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="f5f70-125">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="f5f70-126">Se a linha de comando for: addsource = todos, ADDLOCAL = MyFeature, primeiro MyFeature estiver definido como Run-local e, quando ADDSOURCE = ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para execução-da-source.</span><span class="sxs-lookup"><span data-stu-id="f5f70-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="f5f70-127">O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="f5f70-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5f70-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5f70-128">Requirements</span></span>



| <span data-ttu-id="f5f70-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5f70-129">Requirement</span></span> | <span data-ttu-id="f5f70-130">Valor</span><span class="sxs-lookup"><span data-stu-id="f5f70-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5f70-131">Versão</span><span class="sxs-lookup"><span data-stu-id="f5f70-131">Version</span></span><br/> | <span data-ttu-id="f5f70-132">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f5f70-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f5f70-133">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f5f70-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f5f70-134">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f5f70-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f5f70-135">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f5f70-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f5f70-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5f70-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5f70-137">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f5f70-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




