---
description: 'Notifica o objeto de retorno de chamada que a janela de exibição de pasta está sendo criada. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_WINDOWCREATED (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b57eb1d8-a897-4358-a855-89e152035eff
api_name:
- SFVM_WINDOWCREATED
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9d545feadecdaadbf776f94e653df8b71150ac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968229"
---
# <a name="sfvm_windowcreated-message"></a><span data-ttu-id="5eda7-104">\_Mensagem SFVM WINDOWCREATED</span><span class="sxs-lookup"><span data-stu-id="5eda7-104">SFVM\_WINDOWCREATED message</span></span>

<span data-ttu-id="5eda7-105">Notifica o objeto de retorno de chamada que a janela de exibição de pasta está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="5eda7-105">Notifies the callback object that the folder view window is being created.</span></span> <span data-ttu-id="5eda7-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="5eda7-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_WINDOWCREATED 

    wParam = (WPARAM)(HWND) hwndView;

            
```



## <a name="parameters"></a><span data-ttu-id="5eda7-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5eda7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5eda7-108">*hwndView* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5eda7-108">*hwndView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5eda7-109">O identificador da janela da exibição de pasta.</span><span class="sxs-lookup"><span data-stu-id="5eda7-109">The folder view's window handle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5eda7-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5eda7-110">Requirements</span></span>



| <span data-ttu-id="5eda7-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eda7-111">Requirement</span></span> | <span data-ttu-id="5eda7-112">Valor</span><span class="sxs-lookup"><span data-stu-id="5eda7-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5eda7-113">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5eda7-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5eda7-114">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5eda7-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5eda7-115">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5eda7-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5eda7-116">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5eda7-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5eda7-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5eda7-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5eda7-118"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eda7-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
