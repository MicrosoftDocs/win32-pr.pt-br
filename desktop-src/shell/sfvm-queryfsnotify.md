---
description: SFVM \_ QUERYFSNOTIFY pode ser alterado ou indisponível.
ms.assetid: 5d777115-bae3-47c4-9edc-c99c40a4f926
title: Mensagem de SFVM_QUERYFSNOTIFY (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a4416bda249e3ec0f2a0c0f2d45ac353961e180
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172074"
---
# <a name="sfvm_queryfsnotify-message"></a><span data-ttu-id="5b77d-103">\_Mensagem SFVM QUERYFSNOTIFY</span><span class="sxs-lookup"><span data-stu-id="5b77d-103">SFVM\_QUERYFSNOTIFY message</span></span>

<span data-ttu-id="5b77d-104">\[**SFVM \_ O QUERYFSNOTIFY** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="5b77d-104">\[**SFVM\_QUERYFSNOTIFY** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5b77d-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="5b77d-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="5b77d-106">Permite que o objeto de retorno de chamada registre uma pasta para que as alterações na exibição dessa pasta gerem notificações.</span><span class="sxs-lookup"><span data-stu-id="5b77d-106">Allows the callback object to register a folder so that changes to that folder's view will generate notifications.</span></span> <span data-ttu-id="5b77d-107">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="5b77d-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_QUERYFSNOTIFY 
    lParam = (LPARAM)(SHChangeNotifyEntry*) shcne;
            
```



## <a name="parameters"></a><span data-ttu-id="5b77d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5b77d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b77d-109">*shcne* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="5b77d-109">*shcne* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b77d-110">Uma estrutura para manter o PIDL do item para observar eventos e uma indicação se as subpastas desse item também devem ser observadas.</span><span class="sxs-lookup"><span data-stu-id="5b77d-110">A structure to hold the PIDL of the item to watch for events and an indication whether subfolders of that item should also be watched.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b77d-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b77d-111">Requirements</span></span>



| <span data-ttu-id="5b77d-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b77d-112">Requirement</span></span> | <span data-ttu-id="5b77d-113">Valor</span><span class="sxs-lookup"><span data-stu-id="5b77d-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5b77d-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b77d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5b77d-115">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5b77d-115">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5b77d-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b77d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5b77d-117">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5b77d-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5b77d-118">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="5b77d-118">End of client support</span></span><br/>    | <span data-ttu-id="5b77d-119">Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="5b77d-119">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="5b77d-120">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="5b77d-120">End of server support</span></span><br/>    | <span data-ttu-id="5b77d-121">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5b77d-121">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="5b77d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b77d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b77d-123"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b77d-123"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
