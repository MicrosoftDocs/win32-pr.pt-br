---
description: A ação removidas remove os arquivos instalados anteriormente pela ação InstallFiles.
ms.assetid: 1079be89-515c-443e-8927-46ddf7891a59
title: Ação de RemoveFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 174e477d512401c8ff6f1ff091b7c67f26e86f16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756892"
---
# <a name="removefiles-action"></a><span data-ttu-id="bbed9-103">Ação de RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="bbed9-103">RemoveFiles Action</span></span>

<span data-ttu-id="bbed9-104">A ação removidas remove os arquivos instalados anteriormente pela ação [InstallFiles](installfiles-action.md) .</span><span class="sxs-lookup"><span data-stu-id="bbed9-104">The RemoveFiles action removes files previously installed by the [InstallFiles](installfiles-action.md) action.</span></span> <span data-ttu-id="bbed9-105">Cada um desses arquivos é restringido por um link para uma entrada na tabela de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bbed9-105">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="bbed9-106">Somente os arquivos com componentes resolvidos para o estado *msiInstallStateAbsent* ou *msiInstallStateLocal* , se o componente for instalado localmente, serão removidos.</span><span class="sxs-lookup"><span data-stu-id="bbed9-106">Only those files with components resolved to either the *msiInstallStateAbsent* state or the *msiInstallStateLocal* state if the component is installed locally, are removed.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="bbed9-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="bbed9-107">Sequence Restrictions</span></span>

<span data-ttu-id="bbed9-108">A ação [InstallValidate](installvalidate-action.md) deve ser chamada antes de chamar RemoveFiles.</span><span class="sxs-lookup"><span data-stu-id="bbed9-108">The [InstallValidate](installvalidate-action.md) action must be called before calling RemoveFiles.</span></span> <span data-ttu-id="bbed9-109">Se uma ação [InstallFiles](installfiles-action.md) for usada, ela deverá aparecer após removes.</span><span class="sxs-lookup"><span data-stu-id="bbed9-109">If an [InstallFiles](installfiles-action.md) action is used, it must appear after RemoveFiles.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="bbed9-110">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="bbed9-110">ActionData Messages</span></span>



| <span data-ttu-id="bbed9-111">Campo</span><span class="sxs-lookup"><span data-stu-id="bbed9-111">Field</span></span> | <span data-ttu-id="bbed9-112">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="bbed9-112">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="bbed9-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="bbed9-113">\[1\]</span></span> | <span data-ttu-id="bbed9-114">Identificador do arquivo removido.</span><span class="sxs-lookup"><span data-stu-id="bbed9-114">Identifier of removed file.</span></span>                   |
| <span data-ttu-id="bbed9-115">\[9\]</span><span class="sxs-lookup"><span data-stu-id="bbed9-115">\[9\]</span></span> | <span data-ttu-id="bbed9-116">Identificador do diretório que contém o arquivo removido.</span><span class="sxs-lookup"><span data-stu-id="bbed9-116">Identifier of directory holding removed file.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="bbed9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bbed9-117">Remarks</span></span>

<span data-ttu-id="bbed9-118">A tabela [RemoveFile](removefile-table.md) pode ser omitida do banco de dados do instalador se não houver arquivos diversos a serem removidos.</span><span class="sxs-lookup"><span data-stu-id="bbed9-118">The [RemoveFile](removefile-table.md) table can be omitted from the installer database if there are no miscellaneous files to remove.</span></span>

<span data-ttu-id="bbed9-119">A ação removidas também pode remover arquivos especificados pelo autor que não estão instalados pela ação InstallFiles.</span><span class="sxs-lookup"><span data-stu-id="bbed9-119">The RemoveFiles action can also remove author-specified files that are not installed by the InstallFiles action.</span></span> <span data-ttu-id="bbed9-120">Esses arquivos são especificados na tabela [RemoveFile](removefile-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bbed9-120">These files are specified in the [RemoveFile](removefile-table.md) table.</span></span> <span data-ttu-id="bbed9-121">Cada um desses arquivos é restringido por um link para uma entrada na tabela de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="bbed9-121">Each of these files is gated by a link to an entry in the [Component](component-table.md) table.</span></span> <span data-ttu-id="bbed9-122">Esses arquivos cujos componentes são resolvidos para qualquer estado de ação ativo (ou seja, não no estado desativado ou nulo) são removidos se o arquivo existir no diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="bbed9-122">Those files whose components are resolved to any active Action state (that is, not in the Off or Null state) are removed if the file exists in the specified directory.</span></span> <span data-ttu-id="bbed9-123">A remoção de arquivos especificados na tabela RemoveFile é tentada quando o componente vinculado é instalado pela primeira vez, durante uma reinstalação do e novamente quando o componente vinculado é removido.</span><span class="sxs-lookup"><span data-stu-id="bbed9-123">The removal of files specified in the RemoveFile table is attempted when the linked component is first installed, during a reinstall, and again when the linked component is removed.</span></span>

<span data-ttu-id="bbed9-124">A ação removidas também pode remover pastas.</span><span class="sxs-lookup"><span data-stu-id="bbed9-124">The RemoveFiles action can also remove folders.</span></span> <span data-ttu-id="bbed9-125">Uma pasta vazia será removida se o valor na coluna FileName da tabela RemoveFile for NULL.</span><span class="sxs-lookup"><span data-stu-id="bbed9-125">An empty folder is removed if the value in the FileName column of the RemoveFile table is null.</span></span>

<span data-ttu-id="bbed9-126">Ao remover arquivos instalados anteriormente, a ação removidas consulta os mesmos campos nas mesmas tabelas que aqueles consultados pela ação [InstallFiles](installfiles-action.md) com a exceção de que a [tabela de mídia](media-table.md) não é usada pela ação removidas.</span><span class="sxs-lookup"><span data-stu-id="bbed9-126">When removing previously installed files, the RemoveFiles action queries the same fields in the same tables as those queried by the [InstallFiles](installfiles-action.md) action with the exception that the [Media table](media-table.md) is not used by the RemoveFiles action.</span></span>

<span data-ttu-id="bbed9-127">O nome do arquivo de destino pode ser especificado no texto localizado na coluna FileName da tabela RemoveFile.</span><span class="sxs-lookup"><span data-stu-id="bbed9-127">The target file name can be specified in localized text in the FileName column of the RemoveFile table.</span></span>

 

 



