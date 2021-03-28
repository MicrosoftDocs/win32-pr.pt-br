---
description: Remove um objeto da exibição do Shell. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_REMOVEOBJECT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5b493cea-dfbd-4aee-8126-b118c058bb4c
api_name:
- SFVM_REMOVEOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99eaf6b1e8ca49403e0003d6cd60a6769778233a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968234"
---
# <a name="sfvm_removeobject-message"></a><span data-ttu-id="f3b21-104">\_Mensagem de REmovimentaçãoobject do SFVM</span><span class="sxs-lookup"><span data-stu-id="f3b21-104">SFVM\_REMOVEOBJECT message</span></span>

<span data-ttu-id="f3b21-105">Remove um objeto da exibição do Shell.</span><span class="sxs-lookup"><span data-stu-id="f3b21-105">Removes an object from the shell view.</span></span> <span data-ttu-id="f3b21-106">Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="f3b21-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REMOVEOBJECT 
    lParam = (LPARAM) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="f3b21-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f3b21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3b21-108">*PIDL* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f3b21-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="f3b21-109">PIDL do objeto a ser removido.</span><span class="sxs-lookup"><span data-stu-id="f3b21-109">PIDL of the object to remove.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3b21-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f3b21-110">Return value</span></span>

<span data-ttu-id="f3b21-111">Retorna o índice do item que foi removido se um item correspondente ao PIDL especificado foi encontrado; caso contrário, retornará-1.</span><span class="sxs-lookup"><span data-stu-id="f3b21-111">Returns the index of the item that was removed if an item matching the specified PIDL was found; otherwise, returns -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3b21-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f3b21-112">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="f3b21-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3b21-113">Requirements</span></span>



| <span data-ttu-id="f3b21-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3b21-114">Requirement</span></span> | <span data-ttu-id="f3b21-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f3b21-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f3b21-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3b21-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b21-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3b21-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f3b21-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3b21-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b21-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3b21-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f3b21-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f3b21-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3b21-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3b21-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




