---
description: O valor da propriedade ADVERTISE é uma lista de recursos delimitados por vírgulas que devem ser anunciadas.
ms.assetid: ef97f70b-e4bf-4eb3-b643-046a9c348823
title: Propriedade ADVERTISE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e768f22f86dacf35009ca0e0e3ef9337ef84ab70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783279"
---
# <a name="advertise-property"></a><span data-ttu-id="37dec-103">Propriedade ADVERTISE</span><span class="sxs-lookup"><span data-stu-id="37dec-103">ADVERTISE property</span></span>

<span data-ttu-id="37dec-104">O valor da propriedade **advertise** é uma lista de recursos delimitados por vírgulas que devem ser anunciadas.</span><span class="sxs-lookup"><span data-stu-id="37dec-104">The value of the **ADVERTISE** property is a list of features delimited by commas that are to be advertised.</span></span> <span data-ttu-id="37dec-105">Os recursos devem estar presentes na coluna recurso da tabela de [recursos](feature-table.md) .</span><span class="sxs-lookup"><span data-stu-id="37dec-105">The features must be present in the Feature column of the [Feature](feature-table.md) table.</span></span> <span data-ttu-id="37dec-106">Para instalar todos os recursos como anunciados, use ADVERTISE = ALL na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="37dec-106">To install all features as advertised, use ADVERTISE=ALL on the command line.</span></span> <span data-ttu-id="37dec-107">Não insira ADVERTISE = todos na tabela de [Propriedades](property-table.md) porque isso gera um pacote anunciado que não pode ser instalado ou removido.</span><span class="sxs-lookup"><span data-stu-id="37dec-107">Do not enter ADVERTISE=ALL into the [Property table](property-table.md) because this generates an advertised package that cannot be installed or removed.</span></span>

## <a name="remarks"></a><span data-ttu-id="37dec-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="37dec-108">Remarks</span></span>

<span data-ttu-id="37dec-109">Observe que os nomes de recursos diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="37dec-109">Note that feature names are case-sensitive.</span></span>

<span data-ttu-id="37dec-110">O instalador sempre avalia as propriedades a seguir na seguinte ordem.</span><span class="sxs-lookup"><span data-stu-id="37dec-110">The installer always evaluates the following properties in the following order.</span></span>

1.  [<span data-ttu-id="37dec-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="37dec-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="37dec-112">**EXCLU**</span><span class="sxs-lookup"><span data-stu-id="37dec-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="37dec-113">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="37dec-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="37dec-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="37dec-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="37dec-115">**Install**</span><span class="sxs-lookup"><span data-stu-id="37dec-115">**REINSTALL**</span></span>](reinstall.md)
6.  <span data-ttu-id="37dec-116">**ANUNCI**</span><span class="sxs-lookup"><span data-stu-id="37dec-116">**ADVERTISE**</span></span>
7.  [<span data-ttu-id="37dec-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="37dec-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="37dec-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="37dec-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="37dec-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="37dec-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="37dec-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="37dec-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="37dec-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="37dec-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="37dec-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="37dec-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

<span data-ttu-id="37dec-123">Por exemplo, se a linha de comando especificar: ADDLOCAL = todos, addsource = MyFeature, todos os recursos serão definidos primeiro como Run-local e MyFeature será definido como Run-from-Source.</span><span class="sxs-lookup"><span data-stu-id="37dec-123">For example, if the command line specifies: ADDLOCAL=ALL, ADDSOURCE = MyFeature, all the features are first set to run-local and then MyFeature is set to run-from-source.</span></span> <span data-ttu-id="37dec-124">Se a linha de comando for: addsource = todos, ADDLOCAL = MyFeature, primeiro MyFeature estiver definido como Run-local e, quando ADDSOURCE = ALL for avaliado, todos os recursos (incluindo MyFeature) serão redefinidos para execução-da-source.</span><span class="sxs-lookup"><span data-stu-id="37dec-124">If the command line is: ADDSOURCE=ALL, ADDLOCAL=MyFeature, first MyFeature is set to run-local, and then when ADDSOURCE=ALL is evaluated, all features (including MyFeature) are reset to run-from-source.</span></span>

<span data-ttu-id="37dec-125">O instalador define a propriedade [**preselecionada**](preselected.md) com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades acima é especificada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="37dec-125">The installer sets the [**Preselected**](preselected.md) property to a value of "1" during the resumption of a suspended installation or when any of the above properties are specified on the command line.</span></span>

## <a name="requirements"></a><span data-ttu-id="37dec-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37dec-126">Requirements</span></span>



| <span data-ttu-id="37dec-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="37dec-127">Requirement</span></span> | <span data-ttu-id="37dec-128">Valor</span><span class="sxs-lookup"><span data-stu-id="37dec-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37dec-129">Versão</span><span class="sxs-lookup"><span data-stu-id="37dec-129">Version</span></span><br/> | <span data-ttu-id="37dec-130">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="37dec-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="37dec-131">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="37dec-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="37dec-132">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="37dec-132">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="37dec-133">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="37dec-133">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="37dec-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="37dec-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37dec-135">Propriedades</span><span class="sxs-lookup"><span data-stu-id="37dec-135">Properties</span></span>](properties.md)
</dt> </dl>

 

 




