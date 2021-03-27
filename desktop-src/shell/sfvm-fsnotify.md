---
description: 'Notifica o objeto de retorno de chamada que um evento executou que afeta um de seus itens. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_FSNOTIFY (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: ff159c35-afdf-4147-8dd6-7febd9519b18
api_name:
- SFVM_FSNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 74c17f9d4b8c8c1979fa7da2d6f0ff63dff74a9b
ms.sourcegitcommit: cd9672511263d04c0e4bc41758dd1d9e89ea92b4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2021
ms.locfileid: "104989118"
---
# <a name="sfvm_fsnotify-message"></a><span data-ttu-id="3b4c7-104">\_Mensagem SFVM FSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="3b4c7-104">SFVM\_FSNOTIFY message</span></span>

<span data-ttu-id="3b4c7-105">Notifica o objeto de retorno de chamada que um evento executou que afeta um de seus itens.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-105">Notifies the callback object that an event has taken place that affects one of its items.</span></span> <span data-ttu-id="3b4c7-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="3b4c7-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_FSNOTIFY 

    wParam = (WPARAM)(LPCITEMIDLIST*) ppidl;

    lParam = (LPARAM)(DWORD) lEvent;

            
```



## <a name="parameters"></a><span data-ttu-id="3b4c7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b4c7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b4c7-108">*ppidl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b4c7-108">*ppidl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b4c7-109">O ponteiro de PIDL do item afetado.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-109">The pointer of PIDL of the affected item.</span></span>

</dd> <dt>

<span data-ttu-id="3b4c7-110">*Levent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b4c7-110">*lEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b4c7-111">Um valor SHCNE que indica qual evento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="3b4c7-111">A SHCNE value that indicates which event occurred.</span></span> <span data-ttu-id="3b4c7-112">Para obter uma lista de valores possíveis, consulte [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span><span class="sxs-lookup"><span data-stu-id="3b4c7-112">For a list of possible values, see [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3b4c7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b4c7-113">Requirements</span></span>



| <span data-ttu-id="3b4c7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b4c7-114">Requirement</span></span> | <span data-ttu-id="3b4c7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3b4c7-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3b4c7-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b4c7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3b4c7-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3b4c7-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3b4c7-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b4c7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3b4c7-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3b4c7-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3b4c7-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3b4c7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b4c7-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b4c7-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
