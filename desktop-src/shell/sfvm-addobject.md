---
description: Adiciona um objeto à exibição do Shell. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_ADDOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0e5b3f0a5b1aed634ab8929b0501d2e23ba40352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989035"
---
# <a name="sfvm_addobject-message"></a><span data-ttu-id="f391b-104">\_Mensagem SFVM ADDobject</span><span class="sxs-lookup"><span data-stu-id="f391b-104">SFVM\_ADDOBJECT message</span></span>

<span data-ttu-id="f391b-105">Adiciona um objeto à exibição do Shell.</span><span class="sxs-lookup"><span data-stu-id="f391b-105">Adds an object to the Shell view.</span></span> <span data-ttu-id="f391b-106">Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="f391b-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a><span data-ttu-id="f391b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f391b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f391b-108">*PIDL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f391b-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="f391b-109">Um ponteiro para o objeto de interesse a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="f391b-109">A pointer to the object of interest to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f391b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f391b-110">Return value</span></span>

<span data-ttu-id="f391b-111">Retorna a nova ID de item ListView do objeto adicionado se o processo foi bem-sucedido; caso contrário, retornará-1.</span><span class="sxs-lookup"><span data-stu-id="f391b-111">Returns the new listview item ID of the added object if the process was successful; otherwise, returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="f391b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f391b-112">Requirements</span></span>



| <span data-ttu-id="f391b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f391b-113">Requirement</span></span> | <span data-ttu-id="f391b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f391b-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f391b-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f391b-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f391b-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f391b-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f391b-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f391b-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f391b-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f391b-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f391b-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f391b-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f391b-120"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="f391b-120"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




