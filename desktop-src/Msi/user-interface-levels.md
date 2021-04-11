---
description: O Windows Installer fornece aos desenvolvedores de pacotes a capacidade de criar uma interface de usuário interna que tem vários níveis de funcionalidade.
ms.assetid: 9f5796a7-e244-4fc8-af85-52a147bb2c0b
title: Níveis de interface do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a835d1b11a4db4393041e83c1b1dc885018610f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172004"
---
# <a name="user-interface-levels"></a><span data-ttu-id="60ca1-103">Níveis de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="60ca1-103">User Interface Levels</span></span>

<span data-ttu-id="60ca1-104">O Windows Installer fornece aos desenvolvedores de pacotes a capacidade de criar uma interface de usuário interna que tem vários níveis de funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="60ca1-104">Windows Installer provides package developers the capability to author an internal user interface that has multiple levels of functionality.</span></span> <span data-ttu-id="60ca1-105">Como a interface do usuário interna deve ser criada pelo autor do pacote, o comportamento da interface do usuário completa, da interface do usuário reduzida, da interface do usuário básica e de nenhum nível depende do pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="60ca1-105">Because the internal UI must be created by the author of the package, the behavior of the full UI, reduced UI, basic UI, and None levels depends on the installation package.</span></span> <span data-ttu-id="60ca1-106">A tabela a seguir descreve a funcionalidade comumente astranscrita aos níveis de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="60ca1-106">The following table describes the functionality commonly ascribed to UI levels.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="60ca1-107">Nível da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="60ca1-107">UI Level</span></span></th>
<th><span data-ttu-id="60ca1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="60ca1-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="60ca1-109">IU completa</span><span class="sxs-lookup"><span data-stu-id="60ca1-109">Full UI</span></span></td>
<td><span data-ttu-id="60ca1-110">Exibe caixas de diálogo modais e sem janela restrita que foram criadas na interface do usuário interna.</span><span class="sxs-lookup"><span data-stu-id="60ca1-110">Displays modal and modeless dialog boxes that have been authored into the internal UI.</span></span> <span data-ttu-id="60ca1-111">Exibe caixas de <a href="error-dialog.md">diálogo de erro</a> criadas.</span><span class="sxs-lookup"><span data-stu-id="60ca1-111">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="60ca1-112">As caixas de diálogo modais exigem a entrada do usuário para que a instalação possa continuar e é especificada pela configuração do <a href="modal-dialog-style-bit.md">bit do estilo da caixa de diálogo modal</a> na coluna atributos da tabela de <a href="dialog-table.md">diálogo</a> .</span><span class="sxs-lookup"><span data-stu-id="60ca1-112">Modal dialog boxes require user input before the installation can continue and are specified by setting the <a href="modal-dialog-style-bit.md">Modal Dialog Style Bit</a> in the Attributes column of the <a href="dialog-table.md">Dialog</a> table.</span></span> <span data-ttu-id="60ca1-113">Uma caixa de diálogo sem janela restrita não exige a entrada do usuário para que a instalação continue.</span><span class="sxs-lookup"><span data-stu-id="60ca1-113">A modeless dialog box does not require user input for the installation to continue.</span></span>
</blockquote>
<br/> <span data-ttu-id="60ca1-114">Uma interface de usuário completa normalmente exibe o <a href="user-interface-wizard-behavior.md">comportamento do assistente de interface do usuário</a>.</span><span class="sxs-lookup"><span data-stu-id="60ca1-114">A full UI commonly exhibits <a href="user-interface-wizard-behavior.md">User Interface Wizard Behavior</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60ca1-115">Interface do usuário reduzida</span><span class="sxs-lookup"><span data-stu-id="60ca1-115">Reduced UI</span></span></td>
<td><span data-ttu-id="60ca1-116">Exibe qualquer caixa de diálogo sem janela restrita que tenha sido criada na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="60ca1-116">Displays any modeless dialog boxes that have been authored into the UI.</span></span> <span data-ttu-id="60ca1-117">Não exibe nenhuma caixa de diálogo modal criada.</span><span class="sxs-lookup"><span data-stu-id="60ca1-117">Does not display any authored modal dialog boxes.</span></span> <span data-ttu-id="60ca1-118">Exibe caixas de <a href="error-dialog.md">diálogo de erro</a> criadas.</span><span class="sxs-lookup"><span data-stu-id="60ca1-118">Displays authored <a href="error-dialog.md">Error Dialog</a> boxes.</span></span> <span data-ttu-id="60ca1-119">Exibe mensagens de <a href="authoring-disk-prompt-messages.md">prompt de disco</a> .</span><span class="sxs-lookup"><span data-stu-id="60ca1-119">Displays <a href="authoring-disk-prompt-messages.md">Disk Prompt</a> messages.</span></span> <span data-ttu-id="60ca1-120">Exibe caixas de <a href="filesinuse-dialog.md">diálogo FilesInUse</a> .</span><span class="sxs-lookup"><span data-stu-id="60ca1-120">Displays <a href="filesinuse-dialog.md">FilesInUse Dialog</a> boxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60ca1-121">Interface do usuário básica</span><span class="sxs-lookup"><span data-stu-id="60ca1-121">Basic UI</span></span></td>
<td><span data-ttu-id="60ca1-122">Exibe as caixas de diálogo do modelo interno que mostram as mensagens de progresso.</span><span class="sxs-lookup"><span data-stu-id="60ca1-122">Displays the built-in modeless dialog boxes that show progress messages.</span></span> <span data-ttu-id="60ca1-123">Exibe caixas de diálogo de erro internas.</span><span class="sxs-lookup"><span data-stu-id="60ca1-123">Displays built-in error dialog boxes.</span></span> <span data-ttu-id="60ca1-124">Não exibe nenhuma caixa de diálogo criada.</span><span class="sxs-lookup"><span data-stu-id="60ca1-124">Does not display any authored dialog boxes.</span></span> <span data-ttu-id="60ca1-125">Solicita que os usuários insiram um disco exibindo uma caixa de diálogo contendo o valor da propriedade <a href="diskprompt.md"><strong>DiskPrompt</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="60ca1-125">Prompts users to insert a disk by displaying a dialog box containing the <a href="diskprompt.md"><strong>DiskPrompt</strong></a> property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60ca1-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="60ca1-126">None</span></span></td>
<td><span data-ttu-id="60ca1-127">Nenhum significa uma instalação silenciosa que não exibe nenhuma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="60ca1-127">None means a silent installation that displays no UI.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="60ca1-128">O nível da interface do usuário interna pode ser definido usando [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="60ca1-128">The level of the internal UI can be set using [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="60ca1-129">O instalador define a propriedade [**UILevel**](uilevel.md) para o nível atual da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="60ca1-129">The installer sets the [**UILevel**](uilevel.md) property to the current level of the UI.</span></span>

<span data-ttu-id="60ca1-130">Se a propriedade [**LIMITUI**](limitui.md) for definida, o nível da interface do usuário usada ao instalar o pacote será restrito ao básico.</span><span class="sxs-lookup"><span data-stu-id="60ca1-130">If the [**LIMITUI**](limitui.md) property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span>

<span data-ttu-id="60ca1-131">Para obter um exemplo de criação de interface do usuário, consulte [um exemplo de instalação](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="60ca1-131">For an example of UI authoring, see [An Installation Example](an-installation-example.md).</span></span>

 

 




