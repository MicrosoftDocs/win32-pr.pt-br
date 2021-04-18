---
description: A ação RemoveExistingProducts passa pelos códigos de produto listados na coluna Actionproperty da tabela de atualização e remove os produtos em sequência invocando instalações simultâneas.
ms.assetid: 3e96283b-1085-4ace-b004-2fd94310eeb2
title: Ação RemoveExistingProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea3b792b02352277e8f29fa422b093fe876b560
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756720"
---
# <a name="removeexistingproducts-action"></a><span data-ttu-id="9de11-103">Ação RemoveExistingProducts</span><span class="sxs-lookup"><span data-stu-id="9de11-103">RemoveExistingProducts Action</span></span>

<span data-ttu-id="9de11-104">A ação RemoveExistingProducts passa pelos códigos de produto listados na coluna Actionproperty da tabela de [atualização](upgrade-table.md) e remove os produtos em sequência invocando instalações simultâneas.</span><span class="sxs-lookup"><span data-stu-id="9de11-104">The RemoveExistingProducts action goes through the product codes listed in the ActionProperty column of the [Upgrade table](upgrade-table.md) and removes the products in sequence by invoking concurrent installations.</span></span> <span data-ttu-id="9de11-105">Para cada instalação simultânea, o instalador define a propriedade [**ProductCode**](productcode.md) para o código do produto e define a propriedade [**Remove**](remove.md) como o valor no campo remove da tabela de atualização.</span><span class="sxs-lookup"><span data-stu-id="9de11-105">For each concurrent installation the installer sets the [**ProductCode**](productcode.md) property to the product code and sets the [**REMOVE**](remove.md) property to the value in the Remove field of the Upgrade table.</span></span> <span data-ttu-id="9de11-106">Se o campo remover estiver em branco, seu valor padrão será todos e o instalador removerá o produto inteiro.</span><span class="sxs-lookup"><span data-stu-id="9de11-106">If the Remove field is blank, its value defaults to ALL and the installer removes the entire product.</span></span>

<span data-ttu-id="9de11-107">O instalador executa apenas a ação RemoveExistingProducts na primeira vez que instala um produto.</span><span class="sxs-lookup"><span data-stu-id="9de11-107">The installer only runs the RemoveExistingProducts action the first time it installs a product.</span></span> <span data-ttu-id="9de11-108">Ele não executa a ação durante uma instalação ou desinstalação de [manutenção](maintenance-installation.md) .</span><span class="sxs-lookup"><span data-stu-id="9de11-108">It does not run the action during a [maintenance installation](maintenance-installation.md) or uninstallation.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="9de11-109">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="9de11-109">Sequence Restrictions</span></span>

<span data-ttu-id="9de11-110">A ação RemoveExistingProducts deve ser agendada na sequência de ações em um dos locais a seguir.</span><span class="sxs-lookup"><span data-stu-id="9de11-110">The RemoveExistingProducts action must be scheduled in the action sequence in one of the following locations.</span></span>

-   <span data-ttu-id="9de11-111">Entre a [ação InstallValidate](installvalidate-action.md) e a [ação InstallInitialize](installinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9de11-111">Between the [InstallValidate action](installvalidate-action.md) and the [InstallInitialize action](installinitialize-action.md).</span></span> <span data-ttu-id="9de11-112">Nesse caso, o instalador remove totalmente os aplicativos antigos antes de instalar os novos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9de11-112">In this case, the installer removes the old applications entirely before installing the new applications.</span></span> <span data-ttu-id="9de11-113">Esse é um posicionamento ineficiente para a ação porque todos os arquivos reutilizados precisam ser copiados novamente.</span><span class="sxs-lookup"><span data-stu-id="9de11-113">This is an inefficient placement for the action because all reused files have to be recopied.</span></span>
-   <span data-ttu-id="9de11-114">Após a [ação InstallInitialize](installinitialize-action.md) e antes de qualquer ação que gere o script de execução.</span><span class="sxs-lookup"><span data-stu-id="9de11-114">After the [InstallInitialize action](installinitialize-action.md) and before any actions that generate execution script.</span></span>
-   <span data-ttu-id="9de11-115">Entre a [ação InstallExecute](installexecute-action.md), ou a [ação InstallExecuteAgain](installexecuteagain-action.md), e a [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9de11-115">Between the [InstallExecute action](installexecute-action.md), or the [InstallExecuteAgain action](installexecuteagain-action.md), and the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="9de11-116">Geralmente, as três últimas ações são agendadas logo após uma outra: InstallExecute, RemoveExistingProducts e InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="9de11-116">Generally the last three actions are scheduled right after one another: InstallExecute, RemoveExistingProducts, and InstallFinalize.</span></span> <span data-ttu-id="9de11-117">Nesse caso, os arquivos atualizados são instalados primeiro e, em seguida, os arquivos antigos são removidos.</span><span class="sxs-lookup"><span data-stu-id="9de11-117">In this case the updated files are installed first and then the old files are removed.</span></span> <span data-ttu-id="9de11-118">No entanto, se a remoção do aplicativo antigo falhar, o instalador reverterá a remoção do aplicativo antigo e a instalação do novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9de11-118">However, if the removal of the old application fails, then the installer rolls back both the removal of the old application and the install of the new application.</span></span>
-   <span data-ttu-id="9de11-119">Após a [ação InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="9de11-119">After the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="9de11-120">Esse é o posicionamento mais eficiente para a ação.</span><span class="sxs-lookup"><span data-stu-id="9de11-120">This is the most efficient placement for the action.</span></span> <span data-ttu-id="9de11-121">Nesse caso, o instalador atualiza os arquivos antes de remover os aplicativos antigos.</span><span class="sxs-lookup"><span data-stu-id="9de11-121">In this case, the installer updates files before removing the old applications.</span></span> <span data-ttu-id="9de11-122">Somente os arquivos que estão sendo atualizados são instalados durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="9de11-122">Only the files being updated get installed during the installation.</span></span> <span data-ttu-id="9de11-123">Se a remoção do aplicativo antigo falhar, o instalador apenas reverterá a desinstalação do aplicativo antigo.</span><span class="sxs-lookup"><span data-stu-id="9de11-123">If the removal of the old application fails, then the installer only rolls back the uninstallation of the old application.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="9de11-124">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="9de11-124">ActionData Messages</span></span>



| <span data-ttu-id="9de11-125">Campo</span><span class="sxs-lookup"><span data-stu-id="9de11-125">Field</span></span> | <span data-ttu-id="9de11-126">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="9de11-126">Description of action data</span></span> |
|-------|----------------------------|
| <span data-ttu-id="9de11-127">\[1\]</span><span class="sxs-lookup"><span data-stu-id="9de11-127">\[1\]</span></span> | <span data-ttu-id="9de11-128">Produto removido.</span><span class="sxs-lookup"><span data-stu-id="9de11-128">Removed product.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="9de11-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="9de11-129">Remarks</span></span>

<span data-ttu-id="9de11-130">Windows Installer define a propriedade [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) quando ela executa essa ação.</span><span class="sxs-lookup"><span data-stu-id="9de11-130">Windows Installer sets the [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) Property when it runs this action.</span></span>

 

 



