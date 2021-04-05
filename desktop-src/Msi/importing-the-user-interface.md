---
description: Além das informações discutidas nas seções anteriores, uisample.msi também contém dados para uma interface do usuário de exemplo.
ms.assetid: 7e4ae4b8-e7b2-49b3-97b7-374b69006a2f
title: Importando a interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2957dbec645bb85121c9748de83bc5c96ad04b05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827349"
---
# <a name="importing-the-user-interface"></a><span data-ttu-id="86531-103">Importando a interface do usuário</span><span class="sxs-lookup"><span data-stu-id="86531-103">Importing the User Interface</span></span>

<span data-ttu-id="86531-104">Além das informações discutidas nas seções anteriores, uisample.msi também contém dados para uma interface do usuário de exemplo.</span><span class="sxs-lookup"><span data-stu-id="86531-104">In addition to information discussed in previous sections, uisample.msi also contains data for a sample user interface.</span></span> <span data-ttu-id="86531-105">Se você mesclou uisample.msi em MNP2000.msi na seção [importando um banco de dados em branco](importing-a-blank-database.md), essas informações também estão presentes no MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="86531-105">If you merged uisample.msi into MNP2000.msi in the section [Importing a Blank Database](importing-a-blank-database.md), then this information is present in MNP2000.msi as well.</span></span> <span data-ttu-id="86531-106">As informações para a interface do usuário de exemplo estão nas tabelas a seguir.</span><span class="sxs-lookup"><span data-stu-id="86531-106">The information for the sample user interface is in the following tables.</span></span>

-   [<span data-ttu-id="86531-107">Tabela ActionText</span><span class="sxs-lookup"><span data-stu-id="86531-107">ActionText table</span></span>](actiontext-table.md)
-   [<span data-ttu-id="86531-108">Tabela binária</span><span class="sxs-lookup"><span data-stu-id="86531-108">Binary table</span></span>](binary-table.md)
-   [<span data-ttu-id="86531-109">Tabela de controle</span><span class="sxs-lookup"><span data-stu-id="86531-109">Control table</span></span>](control-table.md)
-   [<span data-ttu-id="86531-110">Tabela ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="86531-110">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="86531-111">Tabela de diálogo</span><span class="sxs-lookup"><span data-stu-id="86531-111">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="86531-112">Tabela de erros</span><span class="sxs-lookup"><span data-stu-id="86531-112">Error table</span></span>](error-table.md)
-   [<span data-ttu-id="86531-113">Tabela EventMappings</span><span class="sxs-lookup"><span data-stu-id="86531-113">EventMapping table</span></span>](eventmapping-table.md)
-   [<span data-ttu-id="86531-114">Tabela de botões de opção</span><span class="sxs-lookup"><span data-stu-id="86531-114">RadioButton table</span></span>](radiobutton-table.md)
-   [<span data-ttu-id="86531-115">Tabela TextStyle</span><span class="sxs-lookup"><span data-stu-id="86531-115">TextStyle table</span></span>](textstyle-table.md)
-   [<span data-ttu-id="86531-116">Tabela UIText</span><span class="sxs-lookup"><span data-stu-id="86531-116">UIText table</span></span>](uitext-table.md)

<span data-ttu-id="86531-117">O editor de banco de dados Orca fornecido com o instalador inclui uma opção de visualização de diálogo que você pode usar para visualizar as caixas de diálogo da interface do usuário que é especificada pelos dados nas tabelas acima.</span><span class="sxs-lookup"><span data-stu-id="86531-117">The database editor Orca provided with the installer includes a dialog preview option that you can use to preview the dialogs of the user interface that is specified by the data in the above tables.</span></span>

<span data-ttu-id="86531-118">O pacote de instalação de exemplo MNP2000.msi agora está pronto para a validação do pacote.</span><span class="sxs-lookup"><span data-stu-id="86531-118">The sample installation package MNP2000.msi is now ready for package validation.</span></span> <span data-ttu-id="86531-119">Sempre execute a validação em um novo pacote antes de tentar instalar o pacote pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="86531-119">Always run validation on a new package before attempting to install the package for the first time.</span></span> <span data-ttu-id="86531-120">Isso é discutido na validação do exemplo de instalação.</span><span class="sxs-lookup"><span data-stu-id="86531-120">This is discussed in Validating the Installation Sample.</span></span>

<span data-ttu-id="86531-121">Se você não quiser incluir a interface do usuário no pacote de exemplo, omita ou remova todas as informações nas tabelas mostradas acima, exceto a [tabela TextStyle](textstyle-table.md) (que é necessária para definir a propriedade [**DefaultUIFont**](defaultuifont.md) ).</span><span class="sxs-lookup"><span data-stu-id="86531-121">If you do not want to include the user interface in the sample package, omit or remove the all information in the tables shown above except for the [TextStyle table](textstyle-table.md) (which is needed to define the [**DefaultUIFont**](defaultuifont.md) property).</span></span> <span data-ttu-id="86531-122">Você também deve remover as propriedades da interface do usuário da [tabela de propriedades](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="86531-122">You should also remove user interface properties from the [Property Table](property-table.md).</span></span> <span data-ttu-id="86531-123">Uma tabela de propriedades de exemplo para o exemplo do bloco de notas, sem uma interface do usuário, é mostrada abaixo.</span><span class="sxs-lookup"><span data-stu-id="86531-123">An example Property table for the Notepad sample, without a UI, is shown below.</span></span> <span data-ttu-id="86531-124">Não reutilize os GUIDs mostrados na tabela se você copiar este exemplo.</span><span class="sxs-lookup"><span data-stu-id="86531-124">Do not reuse the GUIDs shown in the table if you copy this example.</span></span>

[<span data-ttu-id="86531-125">Tabela de propriedades</span><span class="sxs-lookup"><span data-stu-id="86531-125">Property Table</span></span>](property-table.md)



| <span data-ttu-id="86531-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="86531-126">Property</span></span>                                   | <span data-ttu-id="86531-127">Valor</span><span class="sxs-lookup"><span data-stu-id="86531-127">Value</span></span>                                  |
|--------------------------------------------|----------------------------------------|
| [<span data-ttu-id="86531-128">**DefaultUIFont**</span><span class="sxs-lookup"><span data-stu-id="86531-128">**DefaultUIFont**</span></span>](defaultuifont.md)     | <span data-ttu-id="86531-129">DlgFont8</span><span class="sxs-lookup"><span data-stu-id="86531-129">DlgFont8</span></span>                               |
| [<span data-ttu-id="86531-130">**INSTALLLEVEL**</span><span class="sxs-lookup"><span data-stu-id="86531-130">**INSTALLLEVEL**</span></span>](installlevel.md)       | <span data-ttu-id="86531-131">3</span><span class="sxs-lookup"><span data-stu-id="86531-131">3</span></span>                                      |
| [<span data-ttu-id="86531-132">**LIMITUI**</span><span class="sxs-lookup"><span data-stu-id="86531-132">**LIMITUI**</span></span>](limitui.md)                 | <span data-ttu-id="86531-133">1</span><span class="sxs-lookup"><span data-stu-id="86531-133">1</span></span>                                      |
| [<span data-ttu-id="86531-134">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="86531-134">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="86531-135">Microsoft</span><span class="sxs-lookup"><span data-stu-id="86531-135">Microsoft</span></span>                              |
| [<span data-ttu-id="86531-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="86531-136">**ProductCode**</span></span>](productcode.md)         | <span data-ttu-id="86531-137">{18A9233C-0B34-4127-A966-C257386270BC}</span><span class="sxs-lookup"><span data-stu-id="86531-137">{18A9233C-0B34-4127-A966-C257386270BC}</span></span> |
| [<span data-ttu-id="86531-138">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="86531-138">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="86531-139">1046</span><span class="sxs-lookup"><span data-stu-id="86531-139">1033</span></span>                                   |
| [<span data-ttu-id="86531-140">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="86531-140">**ProductName**</span></span>](productname.md)         | <span data-ttu-id="86531-141">MNP2000</span><span class="sxs-lookup"><span data-stu-id="86531-141">MNP2000</span></span>                                |
| [<span data-ttu-id="86531-142">**ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="86531-142">**ProductVersion**</span></span>](productversion.md)   | <span data-ttu-id="86531-143">01.40.0000</span><span class="sxs-lookup"><span data-stu-id="86531-143">01.40.0000</span></span>                             |
| [<span data-ttu-id="86531-144">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="86531-144">**UpgradeCode**</span></span>](upgradecode.md)         | <span data-ttu-id="86531-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span><span class="sxs-lookup"><span data-stu-id="86531-145">{908E378A-9551-4772-BF1D-5CFAF6FD9CB4}</span></span> |



 

<span data-ttu-id="86531-146">Um pacote sem uma interface do usuário pode ser instalado a partir da linha de comando ou de um programa.</span><span class="sxs-lookup"><span data-stu-id="86531-146">A package without a user interface can be installed from the command line or from a program.</span></span> <span data-ttu-id="86531-147">Para instalar um pacote da linha de comando, use os métodos descritos em [Opções de linha de comando](command-line-options.md).</span><span class="sxs-lookup"><span data-stu-id="86531-147">To install a package from the command line use the methods described in [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="86531-148">Para instalar um pacote de um programa, use os métodos descritos em [usando as funções do instalador](using-installer-functions.md).</span><span class="sxs-lookup"><span data-stu-id="86531-148">To install a package from a program use the methods described in [Using Installer Functions](using-installer-functions.md).</span></span> <span data-ttu-id="86531-149">Sempre execute a validação em um novo pacote antes de tentar instalar um novo pacote pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="86531-149">Always run validation on a new package before attempting to install a new package for the first time.</span></span>

[<span data-ttu-id="86531-150">Continuar</span><span class="sxs-lookup"><span data-stu-id="86531-150">Continue</span></span>](validating-an-installation-database.md)

 

 



