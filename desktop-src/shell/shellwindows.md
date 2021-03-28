---
description: Representa uma coleção das janelas abertas que pertencem ao shell. Os métodos associados a esses objetos podem controlar e executar comandos no Shell e obter outros objetos relacionados ao shell.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: Objeto ShellWindows (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967965"
---
# <a name="shellwindows-object"></a><span data-ttu-id="2b46d-104">Objeto ShellWindows</span><span class="sxs-lookup"><span data-stu-id="2b46d-104">ShellWindows object</span></span>

<span data-ttu-id="2b46d-105">Representa uma coleção das janelas abertas que pertencem ao shell.</span><span class="sxs-lookup"><span data-stu-id="2b46d-105">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="2b46d-106">Os métodos associados a esses objetos podem controlar e executar comandos no Shell e obter outros objetos relacionados ao shell.</span><span class="sxs-lookup"><span data-stu-id="2b46d-106">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="2b46d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2b46d-107">Members</span></span>

<span data-ttu-id="2b46d-108">O objeto **ShellWindows** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2b46d-108">The **ShellWindows** object has these types of members:</span></span>

-   [<span data-ttu-id="2b46d-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2b46d-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="2b46d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b46d-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2b46d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="2b46d-111">Methods</span></span>

<span data-ttu-id="2b46d-112">O objeto **ShellWindows** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2b46d-112">The **ShellWindows** object has these methods.</span></span>



| <span data-ttu-id="2b46d-113">Método</span><span class="sxs-lookup"><span data-stu-id="2b46d-113">Method</span></span>                                                 | <span data-ttu-id="2b46d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2b46d-114">Description</span></span>                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b46d-115">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="2b46d-115">**\_NewEnum**</span></span>](shellwindows--newenum-method-7ral.md) | <span data-ttu-id="2b46d-116">Cria e retorna um novo objeto **ShellWindows** que é uma cópia desse objeto **ShellWindows** .</span><span class="sxs-lookup"><span data-stu-id="2b46d-116">Creates and returns a new **ShellWindows** object that is a copy of this **ShellWindows** object.</span></span><br/>        |
| [<span data-ttu-id="2b46d-117">**Item**</span><span class="sxs-lookup"><span data-stu-id="2b46d-117">**Item**</span></span>](shellwindows-item.md)                      | <span data-ttu-id="2b46d-118">Recupera um objeto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa a janela do Shell.</span><span class="sxs-lookup"><span data-stu-id="2b46d-118">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2b46d-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2b46d-119">Properties</span></span>

<span data-ttu-id="2b46d-120">O objeto **ShellWindows** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2b46d-120">The **ShellWindows** object has these properties.</span></span>



| <span data-ttu-id="2b46d-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2b46d-121">Property</span></span>                                       | <span data-ttu-id="2b46d-122">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="2b46d-122">Access type</span></span>          | <span data-ttu-id="2b46d-123">Description</span><span class="sxs-lookup"><span data-stu-id="2b46d-123">Description</span></span>                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="2b46d-124">**Contar**</span><span class="sxs-lookup"><span data-stu-id="2b46d-124">**Count**</span></span>](shellwindows-count.md)<br/> | <span data-ttu-id="2b46d-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2b46d-125">Read-only</span></span><br/> | <span data-ttu-id="2b46d-126">Contém o número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="2b46d-126">Contains the number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b46d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b46d-127">Requirements</span></span>



| <span data-ttu-id="2b46d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b46d-128">Requirement</span></span> | <span data-ttu-id="2b46d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2b46d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b46d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b46d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2b46d-131">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2b46d-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2b46d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b46d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2b46d-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2b46d-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b46d-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2b46d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b46d-135"><dt>O textdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b46d-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="2b46d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2b46d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b46d-137"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2b46d-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
