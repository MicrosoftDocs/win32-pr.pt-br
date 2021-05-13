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
ms.openlocfilehash: a9e6d6b3f954f0c8ee4b13fb651a9ea04274deb6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840767"
---
# <a name="shellfolderitem-object"></a><span data-ttu-id="481df-104">Objeto ShellFolderItem</span><span class="sxs-lookup"><span data-stu-id="481df-104">ShellFolderItem object</span></span>

<span data-ttu-id="481df-105">Estende o objeto [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="481df-105">Extends the [**FolderItem**](folderitem.md) object.</span></span> <span data-ttu-id="481df-106">Além das propriedades e métodos com suporte do **FolderItem**, **ShellFolderItem** tem dois métodos adicionais.</span><span class="sxs-lookup"><span data-stu-id="481df-106">In addition to the properties and methods supported by **FolderItem**, **ShellFolderItem** has two additional methods.</span></span>

## <a name="members"></a><span data-ttu-id="481df-107">Membros</span><span class="sxs-lookup"><span data-stu-id="481df-107">Members</span></span>

<span data-ttu-id="481df-108">O objeto **ShellFolderItem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="481df-108">The **ShellFolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="481df-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="481df-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="481df-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="481df-110">Methods</span></span>

<span data-ttu-id="481df-111">O objeto **ShellFolderItem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="481df-111">The **ShellFolderItem** object has these methods.</span></span>



| <span data-ttu-id="481df-112">Método</span><span class="sxs-lookup"><span data-stu-id="481df-112">Method</span></span>                                                       | <span data-ttu-id="481df-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="481df-113">Description</span></span>                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="481df-114">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="481df-114">**ExtendedProperty**</span></span>](shellfolderitem-extendedproperty.md) | <span data-ttu-id="481df-115">Obtém o valor de uma propriedade do conjunto de propriedades de um item.</span><span class="sxs-lookup"><span data-stu-id="481df-115">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="481df-116">A propriedade pode ser especificada por nome ou pelo identificador de formato do conjunto de Propriedades (FMTID) e pelo identificador de propriedade (PID).</span><span class="sxs-lookup"><span data-stu-id="481df-116">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span><br/> |
| [<span data-ttu-id="481df-117">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="481df-117">**InvokeVerbEx**</span></span>](invokeverbex.md)                         | <span data-ttu-id="481df-118">Executa um verbo em um item de Shell.</span><span class="sxs-lookup"><span data-stu-id="481df-118">Executes a verb on a Shell item.</span></span><br/>                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="481df-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="481df-119">Requirements</span></span>



| <span data-ttu-id="481df-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="481df-120">Requirement</span></span> | <span data-ttu-id="481df-121">Valor</span><span class="sxs-lookup"><span data-stu-id="481df-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="481df-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="481df-122">Minimum supported client</span></span><br/> | <span data-ttu-id="481df-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="481df-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="481df-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="481df-124">Minimum supported server</span></span><br/> | <span data-ttu-id="481df-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="481df-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="481df-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="481df-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="481df-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="481df-127"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="481df-128">INSERI</span><span class="sxs-lookup"><span data-stu-id="481df-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="481df-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="481df-129"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="481df-130">DLL</span><span class="sxs-lookup"><span data-stu-id="481df-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="481df-131"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="481df-131"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




