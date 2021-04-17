---
description: O valor da propriedade reinstalar é uma lista de recursos delimitados por vírgulas que devem ser reinstaladas. Os recursos listados devem estar presentes na coluna recurso da tabela de recursos. Para reinstalar todos os recursos, use REINSTALL = ALL na linha de comando.
ms.assetid: 14346fef-7923-4f30-bca8-96a29c0f820d
title: Reinstalar Propriedade
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147b4120968991aa3cb6caf438b7565281fc6f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749577"
---
# <a name="reinstall-property"></a><span data-ttu-id="6c8b2-105">Reinstalar Propriedade</span><span class="sxs-lookup"><span data-stu-id="6c8b2-105">REINSTALL property</span></span>

<span data-ttu-id="6c8b2-106">O valor da propriedade **reinstalar** é uma lista de recursos delimitados por vírgulas que devem ser reinstaladas.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-106">The value of the **REINSTALL** property is a list of features delimited by commas that are to be reinstalled.</span></span> <span data-ttu-id="6c8b2-107">Os recursos listados devem estar presentes na coluna recurso da tabela de [recursos](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="6c8b2-107">The features listed must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="6c8b2-108">Para reinstalar todos os recursos, use REINSTALL = ALL na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-108">To reinstall all features use REINSTALL=ALL on the command line.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c8b2-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c8b2-109">Remarks</span></span>

<span data-ttu-id="6c8b2-110">Observe que os nomes dos recursos diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-110">Note that the feature names are case-sensitive.</span></span>

<span data-ttu-id="6c8b2-111">Se a propriedade **reinstalar** for definida, a propriedade [**REINSTALLMODE**](reinstallmode.md) também deverá ser definida para indicar o tipo de reinstalação a ser executada.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-111">If the **REINSTALL** property is set, the [**REINSTALLMODE**](reinstallmode.md) property should also be set, to indicate the type of reinstall to be performed.</span></span> <span data-ttu-id="6c8b2-112">Se a propriedade **REinstallmode** não estiver definida, por padrão, todos os arquivos que estão instalados no momento serão reinstalados, se o arquivo atualmente instalado for uma versão menor (ou não estiver presente).</span><span class="sxs-lookup"><span data-stu-id="6c8b2-112">If the **REINSTALLMODE** property is not set, then by default all files that are currently installed are reinstalled, IF the currently installed file is a lesser version (or is not present).</span></span> <span data-ttu-id="6c8b2-113">Por padrão, nenhuma entrada de registro é reescrita.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-113">By default, no registry entries are rewritten.</span></span>

<span data-ttu-id="6c8b2-114">Observe que, mesmo se a **reinstalação** for definida como todos, somente os recursos que já foram instalados anteriormente serão reinstalados.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-114">Note that even if **REINSTALL** is set to ALL, only those features that were already installed previously are reinstalled.</span></span> <span data-ttu-id="6c8b2-115">Assim, se a **reinstalação** for definida para um produto que ainda está instalado, nenhuma ação de instalação ocorrerá.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-115">Thus, if **REINSTALL** is set for a product that is yet to be installed, no installation action will take place at all.</span></span>

<span data-ttu-id="6c8b2-116">O instalador sempre avalia as seguintes propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="6c8b2-116">The installer always evaluates the following properties in the following order:</span></span>

1.  [<span data-ttu-id="6c8b2-117">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="6c8b2-117">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="6c8b2-118">**EXCLU**</span><span class="sxs-lookup"><span data-stu-id="6c8b2-118">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="6c8b2-119">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="6c8b2-119">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="6c8b2-120">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="6c8b2-120">**ADDDEFAULT**</span></span>](adddefault.md)
5.  <span data-ttu-id="6c8b2-121">**Install**</span><span class="sxs-lookup"><span data-stu-id="6c8b2-121">**REINSTALL**</span></span>
6.  [<span data-ttu-id="6c8b2-122">**ANUNCI**</span><span class="sxs-lookup"><span data-stu-id="6c8b2-122">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="6c8b2-123">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="6c8b2-123">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="6c8b2-124">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="6c8b2-124">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="6c8b2-125">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="6c8b2-125">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
10. [<span data-ttu-id="6c8b2-126">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="6c8b2-126">**FILEADDSOURCE**</span></span>](fileaddsource.md)
11. [<span data-ttu-id="6c8b2-127">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="6c8b2-127">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="6c8b2-128">Por exemplo, se a linha de comando especificar: ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e MyFeature será definido como Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-128">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="6c8b2-129">Se a linha de comando for: addsource = todos, ADDLOCAL = MyFeature, primeiro MyFeature estiver definido como Run-local e, quando ADDSOURCE = ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para execução-da-source.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-129">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="6c8b2-130">O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-130">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c8b2-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c8b2-131">Requirements</span></span>



| <span data-ttu-id="6c8b2-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c8b2-132">Requirement</span></span> | <span data-ttu-id="6c8b2-133">Valor</span><span class="sxs-lookup"><span data-stu-id="6c8b2-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8b2-134">Versão</span><span class="sxs-lookup"><span data-stu-id="6c8b2-134">Version</span></span><br/> | <span data-ttu-id="6c8b2-135">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-135">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6c8b2-136">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-136">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6c8b2-137">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-137">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6c8b2-138">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="6c8b2-138">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c8b2-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="6c8b2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8b2-140">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6c8b2-140">Properties</span></span>](properties.md)
</dt> </dl>

 

 




