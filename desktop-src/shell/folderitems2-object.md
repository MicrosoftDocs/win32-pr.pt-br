---
description: Estende o objeto FolderItems. Ele dá suporte a um método adicional.
title: Objeto FolderItems2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0ca0efb3-6831-4561-9fd1-6d0b62704931
ms.openlocfilehash: b11bc4d1b3cd2bdd71802e79ca959c0a0f84e360
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840967"
---
# <a name="folderitems2-object"></a><span data-ttu-id="fe809-104">Objeto FolderItems2</span><span class="sxs-lookup"><span data-stu-id="fe809-104">FolderItems2 object</span></span>

<span data-ttu-id="fe809-105">Estende o objeto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="fe809-105">Extends the [**FolderItems**](folderitems.md) object.</span></span> <span data-ttu-id="fe809-106">Ele dá suporte a um método adicional.</span><span class="sxs-lookup"><span data-stu-id="fe809-106">It supports one additional method.</span></span>

## <a name="members"></a><span data-ttu-id="fe809-107">Membros</span><span class="sxs-lookup"><span data-stu-id="fe809-107">Members</span></span>

<span data-ttu-id="fe809-108">O objeto **FolderItems2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fe809-108">The **FolderItems2** object has these types of members:</span></span>

-   [<span data-ttu-id="fe809-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe809-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fe809-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="fe809-110">Methods</span></span>

<span data-ttu-id="fe809-111">O objeto **FolderItems2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="fe809-111">The **FolderItems2** object has these methods.</span></span>



| <span data-ttu-id="fe809-112">Método</span><span class="sxs-lookup"><span data-stu-id="fe809-112">Method</span></span>                                            | <span data-ttu-id="fe809-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe809-113">Description</span></span>                                                                                                                                                                                                                                         |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe809-114">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="fe809-114">**InvokeVerbEx**</span></span>](folderitems2-invokeverbex.md) | <span data-ttu-id="fe809-115">Executa um verbo em uma coleção de objetos [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="fe809-115">Executes a verb on a collection of [**FolderItem**](folderitem.md) objects.</span></span> <span data-ttu-id="fe809-116">Esse método é uma extensão do método [**InvokeVerb**](folderitem-invokeverb.md) , permitindo um controle adicional da operação por meio de um conjunto de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="fe809-116">This method is an extension of the [**InvokeVerb**](folderitem-invokeverb.md) method, allowing additional control of the operation through a set of flags.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fe809-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe809-117">Requirements</span></span>



| <span data-ttu-id="fe809-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe809-118">Requirement</span></span> | <span data-ttu-id="fe809-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fe809-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe809-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe809-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fe809-121">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fe809-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fe809-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe809-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fe809-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fe809-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fe809-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe809-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe809-125"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe809-125"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fe809-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="fe809-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fe809-127"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fe809-127"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fe809-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fe809-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe809-129"><dt>Shell32.dll (versão 5,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="fe809-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe809-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe809-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe809-131">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="fe809-131">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[<span data-ttu-id="fe809-132">**ShellExecuteEx**</span><span class="sxs-lookup"><span data-stu-id="fe809-132">**ShellExecuteEx**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa)
</dt> </dl>

 

 




