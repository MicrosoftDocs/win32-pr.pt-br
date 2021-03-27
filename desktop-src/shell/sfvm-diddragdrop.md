---
description: SFVM \_ DIDDRAGDROP pode ser alterado ou indisponível.
ms.assetid: 5d37cf61-d8a7-4afa-9159-fea13d2b1d59
title: Mensagem de SFVM_DIDDRAGDROP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 025bcf6320b014ff31b0819f394dd8b76fa90e59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989042"
---
# <a name="sfvm_diddragdrop-message"></a><span data-ttu-id="db66d-103">\_Mensagem SFVM DIDDRAGDROP</span><span class="sxs-lookup"><span data-stu-id="db66d-103">SFVM\_DIDDRAGDROP message</span></span>

<span data-ttu-id="db66d-104">\[**SFVM \_ O DIDDRAGDROP** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="db66d-104">\[**SFVM\_DIDDRAGDROP** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="db66d-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="db66d-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="db66d-106">Notifica a função de retorno de chamada que uma operação de arrastar e soltar começou.</span><span class="sxs-lookup"><span data-stu-id="db66d-106">Notifies the callback function that a drag-and-drop operation has begun.</span></span> <span data-ttu-id="db66d-107">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="db66d-107">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DIDDRAGDROP 
    wParam = (WPARAM)(DWORD) dwEffect;
    lParam = (LPARAM)(IDataObject*) pIdo;
            
```



## <a name="parameters"></a><span data-ttu-id="db66d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db66d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db66d-109">*dwEffect* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db66d-109">*dwEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db66d-110">Um especificador de efeito de soltar da enumeração [**DROPEFFECT**](../com/dropeffect-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="db66d-110">A drop effect specifier from the [**DROPEFFECT**](../com/dropeffect-constants.md) enumeration.</span></span> <span data-ttu-id="db66d-111">Isso é obtido chamando [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span><span class="sxs-lookup"><span data-stu-id="db66d-111">This is obtained by calling [**SHDoDragDrop**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shdodragdrop).</span></span>

</dd> <dt>

<span data-ttu-id="db66d-112">*pIdo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="db66d-112">*pIdo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db66d-113">Um ponteiro para a instância [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) .</span><span class="sxs-lookup"><span data-stu-id="db66d-113">A pointer to the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="db66d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="db66d-114">Requirements</span></span>



| <span data-ttu-id="db66d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="db66d-115">Requirement</span></span> | <span data-ttu-id="db66d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="db66d-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="db66d-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db66d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="db66d-118">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="db66d-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="db66d-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="db66d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="db66d-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db66d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="db66d-121">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="db66d-121">End of client support</span></span><br/>    | <span data-ttu-id="db66d-122">Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="db66d-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="db66d-123">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="db66d-123">End of server support</span></span><br/>    | <span data-ttu-id="db66d-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db66d-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="db66d-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="db66d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="db66d-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="db66d-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
