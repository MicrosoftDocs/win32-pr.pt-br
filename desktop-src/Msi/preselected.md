---
description: A propriedade selecionada indica que os recursos já foram selecionados e que a caixa de diálogo de seleção não precisa ser mostrada. Expressões condicionais que dependem de se os recursos já estão instalados usam esse valor.
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: Propriedade preselecionada
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750226"
---
# <a name="preselected-property"></a><span data-ttu-id="c772e-103">Propriedade preselecionada</span><span class="sxs-lookup"><span data-stu-id="c772e-103">Preselected property</span></span>

<span data-ttu-id="c772e-104">A propriedade **selecionada** indica que os recursos já foram selecionados e que a caixa de diálogo de seleção não precisa ser mostrada.</span><span class="sxs-lookup"><span data-stu-id="c772e-104">The **Preselected** property indicates that features have already been selected and that the selection dialog need not be shown.</span></span>

<span data-ttu-id="c772e-105">Expressões condicionais que dependem de se os recursos já estão instalados usam esse valor.</span><span class="sxs-lookup"><span data-stu-id="c772e-105">Conditional expressions which depend on whether features are already installed use this value.</span></span> <span data-ttu-id="c772e-106">Por exemplo, a propriedade pode ser usada para suprimir qualquer caixa de diálogo que envolva seleções de recursos durante a retomada de uma instalação suspensa.</span><span class="sxs-lookup"><span data-stu-id="c772e-106">For example, the property can be used to suppress any dialogs involving feature selections during the resumption of a suspended installation.</span></span>

<span data-ttu-id="c772e-107">O instalador define a propriedade **preselecionada** com um valor de "1" durante a retomada de uma instalação suspensa ou quando qualquer uma das propriedades a seguir é especificada na linha de comando.</span><span class="sxs-lookup"><span data-stu-id="c772e-107">The installer sets the **Preselected** property to a value of "1" during the resumption of a suspended installation or when any of the following properties are specified on the command line.</span></span> <span data-ttu-id="c772e-108">Se a propriedade **preselecionada** tiver sido definida como 1, o instalador não usará a [tabela de condição](condition-table.md) para avaliar a seleção de recursos.</span><span class="sxs-lookup"><span data-stu-id="c772e-108">If the **Preselected** property has been set to 1, the installer does not use the [Condition table](condition-table.md) to evaluate the selection of features.</span></span> <span data-ttu-id="c772e-109">Os recursos são instalados com base nas propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="c772e-109">Features are installed based upon the following properties.</span></span> <span data-ttu-id="c772e-110">O instalador sempre avalia essas propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="c772e-110">The installer always evaluates these properties in the following order:</span></span>

1.  [<span data-ttu-id="c772e-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="c772e-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="c772e-112">**EXCLU**</span><span class="sxs-lookup"><span data-stu-id="c772e-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="c772e-113">**Addsource**</span><span class="sxs-lookup"><span data-stu-id="c772e-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="c772e-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c772e-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="c772e-115">**Install**</span><span class="sxs-lookup"><span data-stu-id="c772e-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="c772e-116">**ANUNCI**</span><span class="sxs-lookup"><span data-stu-id="c772e-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="c772e-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="c772e-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="c772e-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="c772e-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="c772e-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c772e-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="c772e-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="c772e-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="c772e-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="c772e-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="c772e-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="c772e-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

## <a name="requirements"></a><span data-ttu-id="c772e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c772e-123">Requirements</span></span>



| <span data-ttu-id="c772e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c772e-124">Requirement</span></span> | <span data-ttu-id="c772e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c772e-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c772e-126">Versão</span><span class="sxs-lookup"><span data-stu-id="c772e-126">Version</span></span><br/> | <span data-ttu-id="c772e-127">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c772e-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c772e-128">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c772e-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c772e-129">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c772e-129">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c772e-130">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c772e-130">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c772e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c772e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c772e-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c772e-132">Properties</span></span>](properties.md)
</dt> </dl>

 

 




