---
description: Expõe métodos que são usados para inicializar uma lista de MRU (usada mais recentemente) para um objeto de conclusão automática.
title: Interface IACLCustomMRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU
api_type:
- COM
api_location: ''
ms.assetid: 6ebf64da-9eba-4ea7-91aa-242474097be1
ms.openlocfilehash: 54cda8d6cc3c7f1c46d6bce7736160b0da67a4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988969"
---
# <a name="iaclcustommru-interface"></a><span data-ttu-id="a0dec-103">Interface IACLCustomMRU</span><span class="sxs-lookup"><span data-stu-id="a0dec-103">IACLCustomMRU interface</span></span>

<span data-ttu-id="a0dec-104">Expõe métodos que são usados para inicializar uma lista de MRU (usada mais recentemente) para um objeto de conclusão automática.</span><span class="sxs-lookup"><span data-stu-id="a0dec-104">Exposes methods that are used to initialize a most recently used (MRU) list for an autocompletion object.</span></span>

## <a name="members"></a><span data-ttu-id="a0dec-105">Membros</span><span class="sxs-lookup"><span data-stu-id="a0dec-105">Members</span></span>

<span data-ttu-id="a0dec-106">A interface **IACLCustomMRU** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a0dec-106">The **IACLCustomMRU** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a0dec-107">**IACLCustomMRU** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a0dec-107">**IACLCustomMRU** also has these types of members:</span></span>

-   [<span data-ttu-id="a0dec-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0dec-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a0dec-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0dec-109">Methods</span></span>

<span data-ttu-id="a0dec-110">A interface **IACLCustomMRU** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a0dec-110">The **IACLCustomMRU** interface has these methods.</span></span>



| <span data-ttu-id="a0dec-111">Método</span><span class="sxs-lookup"><span data-stu-id="a0dec-111">Method</span></span>                                             | <span data-ttu-id="a0dec-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0dec-112">Description</span></span>                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="a0dec-113">**AddMRUString**</span><span class="sxs-lookup"><span data-stu-id="a0dec-113">**AddMRUString**</span></span>](iaclcustommru-addmrustring.md) | <span data-ttu-id="a0dec-114">Adiciona uma entrada à lista MRU.</span><span class="sxs-lookup"><span data-stu-id="a0dec-114">Adds an entry to the MRU list.</span></span><br/>                               |
| [<span data-ttu-id="a0dec-115">**Inicializar**</span><span class="sxs-lookup"><span data-stu-id="a0dec-115">**Initialize**</span></span>](iaclcustommru-initialize.md)     | <span data-ttu-id="a0dec-116">Carrega uma lista de cadeias de caracteres na lista MRU do registro.</span><span class="sxs-lookup"><span data-stu-id="a0dec-116">Loads a list of strings into the MRU list from the registry.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a0dec-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0dec-117">Requirements</span></span>



| <span data-ttu-id="a0dec-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0dec-118">Requirement</span></span> | <span data-ttu-id="a0dec-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a0dec-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a0dec-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0dec-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a0dec-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a0dec-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a0dec-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0dec-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a0dec-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a0dec-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
