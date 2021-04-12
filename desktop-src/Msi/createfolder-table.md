---
description: A tabela CreateFolder contém referências a pastas que precisam ser criadas explicitamente para um componente específico.
ms.assetid: b17b470b-6971-4124-8ec3-73914fdea95f
title: Tabela CreateFolder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc286b32b48e0db9e5b991ab10af663c51538bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170665"
---
# <a name="createfolder-table"></a><span data-ttu-id="02377-103">Tabela CreateFolder</span><span class="sxs-lookup"><span data-stu-id="02377-103">CreateFolder Table</span></span>

<span data-ttu-id="02377-104">A tabela CreateFolder contém referências a pastas que precisam ser criadas explicitamente para um componente específico.</span><span class="sxs-lookup"><span data-stu-id="02377-104">The CreateFolder table contains references to folders that need to be created explicitly for a particular component.</span></span>

<span data-ttu-id="02377-105">A tabela CreateFolder tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="02377-105">The CreateFolder table has the following columns.</span></span>



| <span data-ttu-id="02377-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="02377-106">Column</span></span>      | <span data-ttu-id="02377-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="02377-107">Type</span></span>                         | <span data-ttu-id="02377-108">Chave</span><span class="sxs-lookup"><span data-stu-id="02377-108">Key</span></span> | <span data-ttu-id="02377-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="02377-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="02377-110">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="02377-110">Directory\_</span></span> | [<span data-ttu-id="02377-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="02377-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="02377-112">S</span><span class="sxs-lookup"><span data-stu-id="02377-112">Y</span></span>   | <span data-ttu-id="02377-113">N</span><span class="sxs-lookup"><span data-stu-id="02377-113">N</span></span>        |
| <span data-ttu-id="02377-114">Componente\_</span><span class="sxs-lookup"><span data-stu-id="02377-114">Component\_</span></span> | [<span data-ttu-id="02377-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="02377-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="02377-116">S</span><span class="sxs-lookup"><span data-stu-id="02377-116">Y</span></span>   | <span data-ttu-id="02377-117">N</span><span class="sxs-lookup"><span data-stu-id="02377-117">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="02377-118">Colunas</span><span class="sxs-lookup"><span data-stu-id="02377-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="02377-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Active\_</span><span class="sxs-lookup"><span data-stu-id="02377-119"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="02377-120">Chave externa na primeira coluna da tabela de [diretórios](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="02377-120">External key into the first column of the [Directory table](directory-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="02377-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="02377-121"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="02377-122">Chave externa na primeira coluna da tabela de [componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="02377-122">External key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="02377-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="02377-123">Remarks</span></span>

<span data-ttu-id="02377-124">As pastas nesta tabela são criadas quando o componente é instalado.</span><span class="sxs-lookup"><span data-stu-id="02377-124">The folders in this table are created when the component is installed.</span></span> <span data-ttu-id="02377-125">É feita uma tentativa de remover essas pastas somente quando o componente é desinstalado ou movido para a execução da fonte.</span><span class="sxs-lookup"><span data-stu-id="02377-125">An attempt is made to remove these folders only when the component is uninstalled or moved to run-from-source.</span></span> <span data-ttu-id="02377-126">Nenhuma remoção automática será disparada se as pastas ficarem vazias.</span><span class="sxs-lookup"><span data-stu-id="02377-126">No automatic removal is triggered if the folders become empty.</span></span> <span data-ttu-id="02377-127">Por outro lado, as pastas criadas pelo instalador, mas não listadas nesta tabela, são removidas quando ficam vazias.</span><span class="sxs-lookup"><span data-stu-id="02377-127">In contrast, folders created by the installer but not listed in this table are removed when they become empty.</span></span>

<span data-ttu-id="02377-128">Como as pastas criadas pelo instalador são excluídas quando se tornam vazias, você deve criar uma entrada na tabela CreateFolder para instalar um componente que consiste em uma pasta vazia.</span><span class="sxs-lookup"><span data-stu-id="02377-128">Because folders created by the installer are deleted when they become empty, you must author an entry into the CreateFolder table to install a component that consists of an empty folder.</span></span>

<span data-ttu-id="02377-129">Essa tabela é referida quando a ação [Createfolders](createfolders-action.md) ou a ação [RemoveFolders](removefolders-action.md) é chamada.</span><span class="sxs-lookup"><span data-stu-id="02377-129">This table is referred to when the [CreateFolders](createfolders-action.md) action or the [RemoveFolders](removefolders-action.md) action is called.</span></span>

<span data-ttu-id="02377-130">Para obter informações sobre como proteger uma pasta, consulte a [tabela MsiLockPermissionsEx](msilockpermissionsex-table.md) e a [Tabela LockPermissions](lockpermissions-table.md).</span><span class="sxs-lookup"><span data-stu-id="02377-130">For information on how to secure a folder see the [MsiLockPermissionsEx Table](msilockpermissionsex-table.md) and [LockPermissions Table](lockpermissions-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="02377-131">Validação</span><span class="sxs-lookup"><span data-stu-id="02377-131">Validation</span></span>

<dl>

[<span data-ttu-id="02377-132">ICE03</span><span class="sxs-lookup"><span data-stu-id="02377-132">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="02377-133">ICE06</span><span class="sxs-lookup"><span data-stu-id="02377-133">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="02377-134">ICE18</span><span class="sxs-lookup"><span data-stu-id="02377-134">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="02377-135">ICE32</span><span class="sxs-lookup"><span data-stu-id="02377-135">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="02377-136">ICE55</span><span class="sxs-lookup"><span data-stu-id="02377-136">ICE55</span></span>](ice55.md)  
</dl>

 

 



