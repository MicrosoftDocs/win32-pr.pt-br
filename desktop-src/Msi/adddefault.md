---
description: O valor da propriedade ADDDEFAULT é uma lista de recursos delimitados por vírgulas, que devem ser instalados em sua configuração padrão.
ms.assetid: 78cec3fc-c653-487a-b41c-a43c42e3a157
title: Propriedade ADDDEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43960b6d70d704337f373031ab4972bcb95dada7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751864"
---
# <a name="adddefault-property"></a><span data-ttu-id="4365e-103">Propriedade ADDDEFAULT</span><span class="sxs-lookup"><span data-stu-id="4365e-103">ADDDEFAULT property</span></span>

<span data-ttu-id="4365e-104">O valor da propriedade **ADDDEFAULT** é uma lista de recursos delimitados por vírgulas, que devem ser instalados em sua configuração padrão.</span><span class="sxs-lookup"><span data-stu-id="4365e-104">The value of the **ADDDEFAULT** property is a list of features delimited by commas, which are to be installed in their default configuration.</span></span> <span data-ttu-id="4365e-105">Os recursos devem estar presentes na coluna recurso da tabela de [recursos.](feature-table.md)</span><span class="sxs-lookup"><span data-stu-id="4365e-105">The features must be present in the Feature column of the [Feature Table.](feature-table.md)</span></span> <span data-ttu-id="4365e-106">Para instalar todos os recursos em suas configurações padrão, use ADDDEFAULT = todos na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4365e-106">To install all features in their default configurations, use ADDDEFAULT=ALL on the command line.</span></span>

<span data-ttu-id="4365e-107">Um recurso listado na propriedade **ADDDEFAULT** é instalado no mesmo estado de instalação como se o usuário solicitasse uma instalação sob demanda do recurso.</span><span class="sxs-lookup"><span data-stu-id="4365e-107">A feature listed in the **ADDDEFAULT** property is installed in the same installation state as if the user requested an installation-on-demand of the feature.</span></span> <span data-ttu-id="4365e-108">O estado é determinado pelos bits que são definidos para o recurso na coluna atributos da [tabela de recursos](feature-table.md)e quais bits são definidos para os componentes de recurso na coluna atributos da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="4365e-108">The state is determined by the bits that are set for the feature in the Attributes column of the [Feature Table](feature-table.md), and which bits are set for the feature components in the Attributes column of the [Component Table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4365e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="4365e-109">Remarks</span></span>

<span data-ttu-id="4365e-110">Os nomes dos recursos diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4365e-110">The feature names are case sensitive.</span></span>

<span data-ttu-id="4365e-111">O instalador sempre avalia as seguintes propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="4365e-111">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="4365e-112">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="4365e-112">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="4365e-113">**EXCLU**</span><span class="sxs-lookup"><span data-stu-id="4365e-113">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="4365e-114">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="4365e-114">**ADDSOURCE**</span></span>](addsource.md)
4.  <span data-ttu-id="4365e-115">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="4365e-115">**ADDDEFAULT**</span></span>
5.  [<span data-ttu-id="4365e-116">**Install**</span><span class="sxs-lookup"><span data-stu-id="4365e-116">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="4365e-117">**ANUNCI**</span><span class="sxs-lookup"><span data-stu-id="4365e-117">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="4365e-118">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="4365e-118">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="4365e-119">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="4365e-119">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="4365e-120">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="4365e-120">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="4365e-121">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="4365e-121">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="4365e-122">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="4365e-122">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="4365e-123">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="4365e-123">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="4365e-124">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="4365e-124">For example:</span></span>

-   <span data-ttu-id="4365e-125">Se a linha de comando especificar: ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e **MyFeature** será definido como Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="4365e-125">If the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then **MyFeature** is set to run-from-source.</span></span>
-   <span data-ttu-id="4365e-126">Se a linha de comando for: addsource = todos, ADDLOCAL = MyFeature, primeiro **MyFeature** estiver definido como Run-local e, quando addsource = All for avaliado, todos os recursos (incluindo **MyFeature**) serão redefinidos para execução-da-source.</span><span class="sxs-lookup"><span data-stu-id="4365e-126">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first **MyFeature** is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including **MyFeature**) are reset to run-from-source.</span></span>

<span data-ttu-id="4365e-127">O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="4365e-127">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation, or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="4365e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4365e-128">Requirements</span></span>



| <span data-ttu-id="4365e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="4365e-129">Requirement</span></span> | <span data-ttu-id="4365e-130">Valor</span><span class="sxs-lookup"><span data-stu-id="4365e-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4365e-131">Versão</span><span class="sxs-lookup"><span data-stu-id="4365e-131">Version</span></span><br/> | <span data-ttu-id="4365e-132">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4365e-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4365e-133">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="4365e-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4365e-134">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4365e-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4365e-135">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="4365e-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4365e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4365e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4365e-137">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4365e-137">Properties</span></span>](properties.md)
</dt> </dl>

 

 




