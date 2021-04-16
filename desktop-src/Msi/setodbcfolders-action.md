---
description: A ação SetODBCFolders verifica os drivers ODBC existentes no sistema e define o diretório de destino de cada novo driver para o local de um driver existente.
ms.assetid: d1739b37-d89b-400e-a4ac-b417e0fb9918
title: Ação SetODBCFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b229d127e976ddb37096c5f3a21605ba8d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758763"
---
# <a name="setodbcfolders-action"></a><span data-ttu-id="566ee-103">Ação SetODBCFolders</span><span class="sxs-lookup"><span data-stu-id="566ee-103">SetODBCFolders Action</span></span>

<span data-ttu-id="566ee-104">A ação SetODBCFolders verifica os drivers ODBC existentes no sistema e define o diretório de destino de cada novo driver para o local de um driver existente.</span><span class="sxs-lookup"><span data-stu-id="566ee-104">The SetODBCFolders action checks for existing ODBC drivers on the system and sets the target directory of each new driver to the location of an existing driver.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="566ee-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="566ee-105">Sequence Restrictions</span></span>

<span data-ttu-id="566ee-106">A ação SetODBCFolders deve vir após a [ação CostFinalize](costfinalize-action.md) e antes da [ação InstallValidate](installvalidate-action.md).</span><span class="sxs-lookup"><span data-stu-id="566ee-106">The SetODBCFolders action must come after the [CostFinalize action](costfinalize-action.md) and before the [InstallValidate action](installvalidate-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="566ee-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="566ee-107">ActionData Messages</span></span>



| <span data-ttu-id="566ee-108">Campo</span><span class="sxs-lookup"><span data-stu-id="566ee-108">Field</span></span> | <span data-ttu-id="566ee-109">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="566ee-109">Description of action data</span></span>                                                          |
|-------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="566ee-110">\[1\]</span><span class="sxs-lookup"><span data-stu-id="566ee-110">\[1\]</span></span> | <span data-ttu-id="566ee-111">Descrição do driver.</span><span class="sxs-lookup"><span data-stu-id="566ee-111">Driver description.</span></span> <span data-ttu-id="566ee-112">A chave do driver ODBC.</span><span class="sxs-lookup"><span data-stu-id="566ee-112">The ODBC driver key.</span></span>                                            |
| <span data-ttu-id="566ee-113">\[2\]</span><span class="sxs-lookup"><span data-stu-id="566ee-113">\[2\]</span></span> | <span data-ttu-id="566ee-114">Local da pasta original do novo driver.</span><span class="sxs-lookup"><span data-stu-id="566ee-114">Original folder location of the new driver.</span></span>                                         |
| <span data-ttu-id="566ee-115">\[3\]</span><span class="sxs-lookup"><span data-stu-id="566ee-115">\[3\]</span></span> | <span data-ttu-id="566ee-116">Novo local da pasta para o novo driver.</span><span class="sxs-lookup"><span data-stu-id="566ee-116">New folder location for the new driver.</span></span> <span data-ttu-id="566ee-117">Este é o local de um driver existente.</span><span class="sxs-lookup"><span data-stu-id="566ee-117">This is the location of an existing driver.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="566ee-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="566ee-118">Remarks</span></span>

<span data-ttu-id="566ee-119">Essa ação coloca um novo driver no mesmo diretório que o driver existente que está sendo substituído.</span><span class="sxs-lookup"><span data-stu-id="566ee-119">This action places a new driver into the same directory as the existing driver being replaced.</span></span> <span data-ttu-id="566ee-120">A ação SetODBCFolders usa a [tabela de diretórios](directory-table.md) para definir os locais dos drivers existentes que serão substituídos.</span><span class="sxs-lookup"><span data-stu-id="566ee-120">The SetODBCFolders action uses the [Directory table](directory-table.md) to set the locations of existing drivers that are to be replaced.</span></span>

 

 



