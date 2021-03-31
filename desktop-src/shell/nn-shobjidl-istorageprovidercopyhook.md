---
description: Define um método que determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.
title: Interface IStorageProviderCopyHook
ms.topic: reference
ms.date: 11/11/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- IStorageProviderCopyHook
api_type:
- COM
api_location:
- shobjidl.h
ms.openlocfilehash: 52f2a7fb7c8d7b37fc27fd1e91c93d716bc92086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369488"
---
# <a name="istorageprovidercopyhook-interface"></a><span data-ttu-id="cd142-103">Interface IStorageProviderCopyHook</span><span class="sxs-lookup"><span data-stu-id="cd142-103">IStorageProviderCopyHook interface</span></span>

<span data-ttu-id="cd142-104">Expõe um método que determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.</span><span class="sxs-lookup"><span data-stu-id="cd142-104">Exposes a method that determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>

## <a name="members"></a><span data-ttu-id="cd142-105">Membros</span><span class="sxs-lookup"><span data-stu-id="cd142-105">Members</span></span>

<span data-ttu-id="cd142-106">A interface **IStorageProviderCopyHook** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="cd142-106">The **IStorageProviderCopyHook** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cd142-107">**IStorageProviderCopyHook** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cd142-107">**IStorageProviderCopyHook** also has these types of members:</span></span>

- [<span data-ttu-id="cd142-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="cd142-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cd142-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="cd142-109">Methods</span></span>

<span data-ttu-id="cd142-110">A interface **IStorageProviderCopyHook** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cd142-110">The **IStorageProviderCopyHook** interface has these methods.</span></span>



| <span data-ttu-id="cd142-111">Método</span><span class="sxs-lookup"><span data-stu-id="cd142-111">Method</span></span>                                           | <span data-ttu-id="cd142-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd142-112">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd142-113">**CopyCallback**</span><span class="sxs-lookup"><span data-stu-id="cd142-113">**CopyCallback**</span></span>](nf-shobjidl-istorageprovidercopyhook-copycallback.md)               |  <span data-ttu-id="cd142-114">Determina se o Shell terá permissão para mover, copiar, excluir ou renomear uma pasta na raiz de sincronização de um provedor de nuvem.</span><span class="sxs-lookup"><span data-stu-id="cd142-114">Determines whether the Shell will be allowed to move, copy, delete, or rename a folder in a cloud provider's sync root.</span></span>                                                           |


## <a name="requirements"></a><span data-ttu-id="cd142-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd142-115">Requirements</span></span>

| <span data-ttu-id="cd142-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd142-116">Requirement</span></span> | <span data-ttu-id="cd142-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cd142-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd142-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd142-118">Minimum supported client</span></span> | <span data-ttu-id="cd142-119">Build 19624 do Windows 10 Insider Preview</span><span class="sxs-lookup"><span data-stu-id="cd142-119">Windows 10 Insider Preview Build 19624</span></span>                                                |
| <span data-ttu-id="cd142-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd142-120">Header</span></span><br/>                   | <span data-ttu-id="cd142-121">ShObjIdl. h</span><span class="sxs-lookup"><span data-stu-id="cd142-121">shobjidl.h</span></span>   |
