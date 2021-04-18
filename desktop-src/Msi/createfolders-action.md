---
description: A ação createfolders cria pastas vazias para componentes que estão definidos para serem instalados.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Ação createfolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780962"
---
# <a name="createfolders-action"></a><span data-ttu-id="50fa5-103">Ação createfolders</span><span class="sxs-lookup"><span data-stu-id="50fa5-103">CreateFolders Action</span></span>

<span data-ttu-id="50fa5-104">A ação createfolders cria pastas vazias para componentes que estão definidos para serem instalados.</span><span class="sxs-lookup"><span data-stu-id="50fa5-104">The CreateFolders action creates empty folders for components that are set to be installed.</span></span> <span data-ttu-id="50fa5-105">O instalador cria pastas para componentes que são executados localmente e executados a partir da origem.</span><span class="sxs-lookup"><span data-stu-id="50fa5-105">The installer creates folders both for components that run locally and run from source.</span></span> <span data-ttu-id="50fa5-106">As pastas recém-criadas são registradas com o identificador de componente apropriado.</span><span class="sxs-lookup"><span data-stu-id="50fa5-106">Newly created folders are registered with the appropriate component identifier.</span></span>

<span data-ttu-id="50fa5-107">A ação createfolders consulta a [tabela CreateFolder](createfolder-table.md) e a [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="50fa5-107">The CreateFolders action queries the [CreateFolder table](createfolder-table.md) and the [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="50fa5-108">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="50fa5-108">Sequence Restrictions</span></span>

<span data-ttu-id="50fa5-109">A ação createfolders deve ser executada antes da ação [InstallFiles](installfiles-action.md) ou antes de qualquer ação que adicione arquivos a pastas.</span><span class="sxs-lookup"><span data-stu-id="50fa5-109">The CreateFolders action must be executed either before the [InstallFiles](installfiles-action.md) action or before any action that adds files to folders.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="50fa5-110">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="50fa5-110">ActionData Messages</span></span>



| <span data-ttu-id="50fa5-111">Campo</span><span class="sxs-lookup"><span data-stu-id="50fa5-111">Field</span></span> | <span data-ttu-id="50fa5-112">Descrição da descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="50fa5-112">Description of action data description</span></span> |
|-------|----------------------------------------|
| <span data-ttu-id="50fa5-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="50fa5-113">\[1\]</span></span> | <span data-ttu-id="50fa5-114">Identificador de diretório da pasta.</span><span class="sxs-lookup"><span data-stu-id="50fa5-114">Directory identifier of folder.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="50fa5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="50fa5-115">Remarks</span></span>

<span data-ttu-id="50fa5-116">O instalador não remove automaticamente as pastas criadas pela ação createfolders durante uma desinstalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50fa5-116">The installer does not automatically remove folders created by the CreateFolders action during an uninstallation of the application.</span></span> <span data-ttu-id="50fa5-117">O instalador só removerá pastas se a [ação RemoveFolders](removefolders-action.md) estiver incluída na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="50fa5-117">The installer only removes folders if the [RemoveFolders action](removefolders-action.md) is included in the action sequence.</span></span>

 

 



