---
description: SFVM \_ THISIDLIST pode ser alterado ou indisponível.
ms.assetid: 488f696d-aa71-4727-bbd2-c99e7d245d85
title: Mensagem de SFVM_THISIDLIST (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86e24199e5adbb895c8d1d5fc36bfff0c109bc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663387"
---
# <a name="sfvm_thisidlist-message"></a><span data-ttu-id="2dd0a-103">\_Mensagem SFVM THISIDLIST</span><span class="sxs-lookup"><span data-stu-id="2dd0a-103">SFVM\_THISIDLIST message</span></span>

<span data-ttu-id="2dd0a-104">\[**SFVM \_ O THISIDLIST** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="2dd0a-104">\[**SFVM\_THISIDLIST** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2dd0a-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="2dd0a-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="2dd0a-106">Permite que o objeto de retorno de chamada especifique o ponteiro da exibição para uma lista de identificadores de item (PIDL).</span><span class="sxs-lookup"><span data-stu-id="2dd0a-106">Allows the callback object to specify the view's pointer to an item identifier list (PIDL).</span></span> <span data-ttu-id="2dd0a-107">Isso é usado somente quando [**IPersistIDList:: SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) e [**IPersistFolder2:: GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) falharam.</span><span class="sxs-lookup"><span data-stu-id="2dd0a-107">This is used only when [**IPersistIDList::SetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistidlist-setidlist) and [**IPersistFolder2::GetCurFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder2-getcurfolder) have failed.</span></span> <span data-ttu-id="2dd0a-108">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="2dd0a-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_THISIDLIST
    lParam = (LPARAM)(LPITEMIDLIST*) pidl;
            
```



## <a name="parameters"></a><span data-ttu-id="2dd0a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2dd0a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dd0a-110">*PIDL* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2dd0a-110">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dd0a-111">O endereço do PIDL da exibição.</span><span class="sxs-lookup"><span data-stu-id="2dd0a-111">The address of the view's PIDL.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2dd0a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2dd0a-112">Requirements</span></span>



| <span data-ttu-id="2dd0a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dd0a-113">Requirement</span></span> | <span data-ttu-id="2dd0a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2dd0a-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd0a-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dd0a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2dd0a-116">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2dd0a-116">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2dd0a-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2dd0a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2dd0a-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2dd0a-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2dd0a-119">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="2dd0a-119">End of client support</span></span><br/>    | <span data-ttu-id="2dd0a-120">Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="2dd0a-120">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="2dd0a-121">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="2dd0a-121">End of server support</span></span><br/>    | <span data-ttu-id="2dd0a-122">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="2dd0a-122">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="2dd0a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2dd0a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dd0a-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dd0a-124"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
