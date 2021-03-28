---
description: 'Notifica o objeto de retorno de chamada que um menu está sendo removido. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_UNMERGEMENU (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0255a41d-e8b4-48d2-931a-aa76ad83c18c
api_name:
- SFVM_UNMERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6c83df7ca42d66f320339901a176dc9d4d38ff37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968216"
---
# <a name="sfvm_unmergemenu-message"></a><span data-ttu-id="aa1e3-104">\_Mensagem SFVM UNMERGEMENU</span><span class="sxs-lookup"><span data-stu-id="aa1e3-104">SFVM\_UNMERGEMENU message</span></span>

<span data-ttu-id="aa1e3-105">Notifica o objeto de retorno de chamada que um menu está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-105">Notifies the callback object that a menu is being removed.</span></span> <span data-ttu-id="aa1e3-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="aa1e3-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_UNMERGEMENU 

    lParam = (LPARAM)(HMENU) hmenuCurrent;

            
```



## <a name="parameters"></a><span data-ttu-id="aa1e3-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa1e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa1e3-108">*hmenuCurrent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="aa1e3-108">*hmenuCurrent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aa1e3-109">O identificador do menu que está sendo removido.</span><span class="sxs-lookup"><span data-stu-id="aa1e3-109">The handle of the menu that is being removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa1e3-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa1e3-110">Requirements</span></span>



| <span data-ttu-id="aa1e3-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa1e3-111">Requirement</span></span> | <span data-ttu-id="aa1e3-112">Valor</span><span class="sxs-lookup"><span data-stu-id="aa1e3-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aa1e3-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa1e3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="aa1e3-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aa1e3-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="aa1e3-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa1e3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="aa1e3-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="aa1e3-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aa1e3-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="aa1e3-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa1e3-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa1e3-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
