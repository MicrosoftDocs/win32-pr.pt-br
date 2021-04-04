---
description: A ação RemoveDuplicateFiles exclui os arquivos instalados pela ação DuplicateFiles.
ms.assetid: 3d8ba4c5-775f-471e-a479-32fa6f7a1bf0
title: Ação RemoveDuplicateFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 555379f3810770abc9f91fd449e71434e9fa6244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647055"
---
# <a name="removeduplicatefiles-action"></a><span data-ttu-id="35221-103">Ação RemoveDuplicateFiles</span><span class="sxs-lookup"><span data-stu-id="35221-103">RemoveDuplicateFiles Action</span></span>

<span data-ttu-id="35221-104">A ação RemoveDuplicateFiles exclui os arquivos instalados pela ação [DuplicateFiles](duplicatefiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="35221-104">The RemoveDuplicateFiles action deletes files installed by the [DuplicateFiles](duplicatefiles-action.md) action.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="35221-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="35221-105">Sequence Restrictions</span></span>

<span data-ttu-id="35221-106">A ação RemoveDuplicateFiles deve ocorrer após a ação [InstallValidate](installvalidate-action.md) e antes da ação [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="35221-106">The RemoveDuplicateFiles action must occur after the [InstallValidate](installvalidate-action.md) action and before the [InstallFiles](installfiles-action.md) action.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="35221-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="35221-107">ActionData Messages</span></span>



| <span data-ttu-id="35221-108">Campo</span><span class="sxs-lookup"><span data-stu-id="35221-108">Field</span></span> | <span data-ttu-id="35221-109">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="35221-109">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="35221-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="35221-110">\[1\]</span></span> | <span data-ttu-id="35221-111">Identificador do arquivo removido.</span><span class="sxs-lookup"><span data-stu-id="35221-111">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="35221-112">\[9\]</span><span class="sxs-lookup"><span data-stu-id="35221-112">\[9\]</span></span> | <span data-ttu-id="35221-113">Identificador do diretório que contém o arquivo removido.</span><span class="sxs-lookup"><span data-stu-id="35221-113">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="35221-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="35221-114">Remarks</span></span>

<span data-ttu-id="35221-115">Para excluir um arquivo duplicado com a [ação DuplicateFiles](duplicatefiles-action.md) usando a ação RemoveDuplicateFiles, o componente associado à entrada do arquivo na tabela duplicatafile deve ser selecionado para remoção.</span><span class="sxs-lookup"><span data-stu-id="35221-115">To delete a file duplicated with the [DuplicateFiles action](duplicatefiles-action.md) using the RemoveDuplicateFiles action, the component associated with the file's entry in the DuplicateFile table must be selected for removal.</span></span>

<span data-ttu-id="35221-116">Use a coluna DestFolder da [tabela duplicatefile](duplicatefile-table.md) para especificar o nome da propriedade cujo valor identifica a pasta de destino.</span><span class="sxs-lookup"><span data-stu-id="35221-116">Use the DestFolder column of the [DuplicateFile table](duplicatefile-table.md) to specify the property name whose value identifies the destination folder.</span></span>

 

 



