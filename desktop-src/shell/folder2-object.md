---
description: Estende o objeto Folder para dar suporte a pastas offline.
title: Objeto Pasta2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.openlocfilehash: c2c630ef36f6e4b2b58f3902c3d5728a31ad1f0d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842057"
---
# <a name="folder2-object"></a><span data-ttu-id="ec50e-103">Objeto Pasta2</span><span class="sxs-lookup"><span data-stu-id="ec50e-103">Folder2 object</span></span>

<span data-ttu-id="ec50e-104">Estende o objeto [**Folder**](folder.md) para dar suporte a pastas offline.</span><span class="sxs-lookup"><span data-stu-id="ec50e-104">Extends the [**Folder**](folder.md) object to support offline folders.</span></span>

## <a name="members"></a><span data-ttu-id="ec50e-105">Membros</span><span class="sxs-lookup"><span data-stu-id="ec50e-105">Members</span></span>

<span data-ttu-id="ec50e-106">O objeto **Pasta2** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ec50e-106">The **Folder2** object has these types of members:</span></span>

-   [<span data-ttu-id="ec50e-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="ec50e-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="ec50e-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ec50e-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ec50e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ec50e-109">Methods</span></span>

<span data-ttu-id="ec50e-110">O objeto **Pasta2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ec50e-110">The **Folder2** object has these methods.</span></span>



| <span data-ttu-id="ec50e-111">Método</span><span class="sxs-lookup"><span data-stu-id="ec50e-111">Method</span></span>                                                                 | <span data-ttu-id="ec50e-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec50e-112">Description</span></span>                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec50e-113">**DismissedWebViewBarricade**</span><span class="sxs-lookup"><span data-stu-id="ec50e-113">**DismissedWebViewBarricade**</span></span>](folder2-dismissedwebviewbarricade.md) | <span data-ttu-id="ec50e-114">Chamado em resposta à exibição da Web Barricade sendo Descartado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="ec50e-114">Called in response to the web view barricade being dismissed by the user.</span></span><br/> |
| [<span data-ttu-id="ec50e-115">**Novamente**</span><span class="sxs-lookup"><span data-stu-id="ec50e-115">**Synchronize**</span></span>](folder2-synchronize.md)                             | <span data-ttu-id="ec50e-116">Sincroniza todos os arquivos offline na pasta.</span><span class="sxs-lookup"><span data-stu-id="ec50e-116">Synchronizes all offline files in the folder.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="ec50e-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ec50e-117">Properties</span></span>

<span data-ttu-id="ec50e-118">O objeto **Pasta2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ec50e-118">The **Folder2** object has these properties.</span></span>



| <span data-ttu-id="ec50e-119">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ec50e-119">Property</span></span>                                                                            | <span data-ttu-id="ec50e-120">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="ec50e-120">Access type</span></span>          | <span data-ttu-id="ec50e-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="ec50e-121">Description</span></span>                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="ec50e-122">**HaveToShowWebViewBarricade**</span><span class="sxs-lookup"><span data-stu-id="ec50e-122">**HaveToShowWebViewBarricade**</span></span>](folder2-havetoshowwebviewbarricade.md)<br/> | <span data-ttu-id="ec50e-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ec50e-123">Read-only</span></span><br/> | <span data-ttu-id="ec50e-124">Não há suporte no momento.</span><span class="sxs-lookup"><span data-stu-id="ec50e-124">Not currently supported.</span></span><br/>                                       |
| [<span data-ttu-id="ec50e-125">**OfflineStatus**</span><span class="sxs-lookup"><span data-stu-id="ec50e-125">**OfflineStatus**</span></span>](folder2-offlinestatus.md)<br/>                           | <span data-ttu-id="ec50e-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ec50e-126">Read-only</span></span><br/> | <span data-ttu-id="ec50e-127">Contém o status offline da pasta.</span><span class="sxs-lookup"><span data-stu-id="ec50e-127">Contains the offline status of the folder.</span></span><br/>                     |
| [<span data-ttu-id="ec50e-128">**Auto-restauração**</span><span class="sxs-lookup"><span data-stu-id="ec50e-128">**Self**</span></span>](folder2-self.md)<br/>                                             | <span data-ttu-id="ec50e-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ec50e-129">Read-only</span></span><br/> | <span data-ttu-id="ec50e-130">Contém o objeto [**FolderItem**](folderitem.md) da pasta.</span><span class="sxs-lookup"><span data-stu-id="ec50e-130">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ec50e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec50e-131">Requirements</span></span>



| <span data-ttu-id="ec50e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec50e-132">Requirement</span></span> | <span data-ttu-id="ec50e-133">Valor</span><span class="sxs-lookup"><span data-stu-id="ec50e-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec50e-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec50e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ec50e-135">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ec50e-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ec50e-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec50e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ec50e-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ec50e-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ec50e-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ec50e-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec50e-139"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec50e-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="ec50e-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="ec50e-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ec50e-141"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="ec50e-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ec50e-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ec50e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec50e-143"><dt>Shell32.dll (versão 5.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ec50e-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec50e-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec50e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec50e-145">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="ec50e-145">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




