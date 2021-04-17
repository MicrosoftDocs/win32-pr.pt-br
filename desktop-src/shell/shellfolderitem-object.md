---
description: Estende o objeto FolderItem. Além das propriedades e métodos com suporte do FolderItem, ShellFolderItem tem dois métodos adicionais.
title: Objeto ShellFolderItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0e2f4c91-f9f9-4daa-a801-9c7fea8af738
ms.openlocfilehash: 84e230e295a956f3f83833a577b47be1e46873a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968121"
---
# <a name="shellfolderitem-object"></a><span data-ttu-id="77967-104">Objeto ShellFolderItem</span><span class="sxs-lookup"><span data-stu-id="77967-104">ShellFolderItem object</span></span>

<span data-ttu-id="77967-105">Estende o objeto [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="77967-105">Extends the [**FolderItem**](folderitem.md) object.</span></span> <span data-ttu-id="77967-106">Além das propriedades e métodos com suporte do **FolderItem**, **ShellFolderItem** tem dois métodos adicionais.</span><span class="sxs-lookup"><span data-stu-id="77967-106">In addition to the properties and methods supported by **FolderItem**, **ShellFolderItem** has two additional methods.</span></span>

## <a name="members"></a><span data-ttu-id="77967-107">Membros</span><span class="sxs-lookup"><span data-stu-id="77967-107">Members</span></span>

<span data-ttu-id="77967-108">O objeto **ShellFolderItem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="77967-108">The **ShellFolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="77967-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="77967-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="77967-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="77967-110">Methods</span></span>

<span data-ttu-id="77967-111">O objeto **ShellFolderItem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="77967-111">The **ShellFolderItem** object has these methods.</span></span>



| <span data-ttu-id="77967-112">Método</span><span class="sxs-lookup"><span data-stu-id="77967-112">Method</span></span>                                                       | <span data-ttu-id="77967-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="77967-113">Description</span></span>                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77967-114">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="77967-114">**ExtendedProperty**</span></span>](shellfolderitem-extendedproperty.md) | <span data-ttu-id="77967-115">Obtém o valor de uma propriedade do conjunto de propriedades de um item.</span><span class="sxs-lookup"><span data-stu-id="77967-115">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="77967-116">A propriedade pode ser especificada por nome ou pelo identificador de formato do conjunto de Propriedades (FMTID) e pelo identificador de propriedade (PID).</span><span class="sxs-lookup"><span data-stu-id="77967-116">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span><br/> |
| [<span data-ttu-id="77967-117">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="77967-117">**InvokeVerbEx**</span></span>](invokeverbex.md)                         | <span data-ttu-id="77967-118">Executa um verbo em um item de Shell.</span><span class="sxs-lookup"><span data-stu-id="77967-118">Executes a verb on a Shell item.</span></span><br/>                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="77967-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77967-119">Requirements</span></span>



| <span data-ttu-id="77967-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="77967-120">Requirement</span></span> | <span data-ttu-id="77967-121">Valor</span><span class="sxs-lookup"><span data-stu-id="77967-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77967-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77967-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77967-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="77967-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="77967-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77967-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77967-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="77967-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="77967-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="77967-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="77967-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="77967-127"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="77967-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="77967-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="77967-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="77967-129"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="77967-130">DLL</span><span class="sxs-lookup"><span data-stu-id="77967-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77967-131"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="77967-131"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




