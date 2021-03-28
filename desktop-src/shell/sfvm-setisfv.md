---
description: 'Notifica o objeto de retorno de chamada do site de contêiner. Isso é usado somente quando IObjectWithSite:: SetSite não tem suporte e SHCreateShellFolderViewEx é usado. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: a4aa40f8-1d98-4686-86e2-87280e470aac
title: Mensagem de SFVM_SETISFV (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83021f1d6d52286f08e8ec7bd51bbaa806c17c7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968232"
---
# <a name="sfvm_setisfv-message"></a><span data-ttu-id="207f0-105">\_Mensagem SFVM SETISFV</span><span class="sxs-lookup"><span data-stu-id="207f0-105">SFVM\_SETISFV message</span></span>

<span data-ttu-id="207f0-106">\[Essa notificação é suportada por meio do Windows XP Service Pack 2 (SP2) e do Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="207f0-106">\[This notification is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="207f0-107">Ele pode não ter suporte em versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="207f0-107">It might be unsupported in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="207f0-108">Notifica o objeto de retorno de chamada do site de contêiner.</span><span class="sxs-lookup"><span data-stu-id="207f0-108">Notifies the callback object of the container site.</span></span> <span data-ttu-id="207f0-109">Isso é usado somente quando [**IObjectWithSite:: SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) não tem suporte e [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) é usado.</span><span class="sxs-lookup"><span data-stu-id="207f0-109">This is used only when [**IObjectWithSite::SetSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768221(v=vs.85)) is not supported and [**SHCreateShellFolderViewEx**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreateshellfolderviewex) is used.</span></span> <span data-ttu-id="207f0-110">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="207f0-110">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_SETISFV
    lParam = (LPARAM)(IUnknown*) site;
            
```



## <a name="parameters"></a><span data-ttu-id="207f0-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="207f0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="207f0-112">*site* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="207f0-112">*site* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="207f0-113">Um ponteiro para a interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do site do contêiner.</span><span class="sxs-lookup"><span data-stu-id="207f0-113">A pointer to the container site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="207f0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="207f0-114">Requirements</span></span>



| <span data-ttu-id="207f0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="207f0-115">Requirement</span></span> | <span data-ttu-id="207f0-116">Valor</span><span class="sxs-lookup"><span data-stu-id="207f0-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="207f0-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="207f0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="207f0-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="207f0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="207f0-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="207f0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="207f0-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="207f0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="207f0-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="207f0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="207f0-122"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="207f0-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
