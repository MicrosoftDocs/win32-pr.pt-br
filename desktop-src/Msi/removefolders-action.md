---
description: A ação RemoveFolders remove todas as pastas vinculadas aos componentes definidos para serem removidas ou executadas da origem. Essas pastas serão removidas somente se estiverem vazias. Se uma pasta for removida, ela não será registrada com o identificador de componente apropriado.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: Ação RemoveFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69648fbae333f0e7b989f2e989f0982d49736317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170423"
---
# <a name="removefolders-action"></a><span data-ttu-id="67519-105">Ação RemoveFolders</span><span class="sxs-lookup"><span data-stu-id="67519-105">RemoveFolders Action</span></span>

<span data-ttu-id="67519-106">A ação RemoveFolders remove todas as pastas vinculadas aos componentes definidos para serem removidas ou executadas da origem.</span><span class="sxs-lookup"><span data-stu-id="67519-106">The RemoveFolders action removes any folders linked to components set to be removed or run from source.</span></span> <span data-ttu-id="67519-107">Essas pastas serão removidas somente se estiverem vazias.</span><span class="sxs-lookup"><span data-stu-id="67519-107">These folders are removed only if they are empty.</span></span> <span data-ttu-id="67519-108">Se uma pasta for removida, ela não será registrada com o identificador de componente apropriado.</span><span class="sxs-lookup"><span data-stu-id="67519-108">If a folder is removed, it is unregistered with the appropriate component identifier.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="67519-109">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="67519-109">Sequence Restrictions</span></span>

<span data-ttu-id="67519-110">A ação RemoveFolders deve vir [após a ação](removefiles-action.md) removidas ou qualquer ação que possa remover arquivos de pastas.</span><span class="sxs-lookup"><span data-stu-id="67519-110">The RemoveFolders action must come after the [RemoveFiles](removefiles-action.md) action or any action that may remove files from folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="67519-111">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="67519-111">ActionData Messages</span></span>



| <span data-ttu-id="67519-112">Campo</span><span class="sxs-lookup"><span data-stu-id="67519-112">Field</span></span> | <span data-ttu-id="67519-113">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="67519-113">Description of action data</span></span>    |
|-------|-------------------------------|
| <span data-ttu-id="67519-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="67519-114">\[1\]</span></span> | <span data-ttu-id="67519-115">Identificador da pasta removida.</span><span class="sxs-lookup"><span data-stu-id="67519-115">Identifier of removed folder.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="67519-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="67519-116">Remarks</span></span>

<span data-ttu-id="67519-117">O instalador não remove automaticamente as pastas criadas pela [ação Createfolders](createfolders-action.md) durante uma desinstalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="67519-117">The installer does not automatically remove the folders created by the [CreateFolders action](createfolders-action.md) during an uninstallation of the application.</span></span> <span data-ttu-id="67519-118">O instalador deve ser instruído para remover essas pastas, criando a ação RemoveFolders na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="67519-118">The installer must be instructed to remove these folders by authoring the RemoveFolders action into the action sequence.</span></span>

<span data-ttu-id="67519-119">Para especificar o nome e o local da pasta, use a \_ coluna Directory da [tabela CreateFolder](createfolder-table.md).</span><span class="sxs-lookup"><span data-stu-id="67519-119">To specify the name and location of the folder, use the Directory\_ column of the [CreateFolder table](createfolder-table.md).</span></span> <span data-ttu-id="67519-120">Supõe-se que cada nome de pasta na tabela CreateFolder seja uma propriedade que define o local da pasta.</span><span class="sxs-lookup"><span data-stu-id="67519-120">Each folder name in the CreateFolder table is assumed to be a property defining the folder location.</span></span>

<span data-ttu-id="67519-121">Para especificar o componente que possui a pasta, use a coluna ComponentID da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="67519-121">To specify the component owning the folder, use the ComponentId column of the [Component table](component-table.md).</span></span>

 

 



