---
description: 'Permite que o objeto de retorno de chamada modifique um menu pop-up do Windows Explorer antes de ser exibido. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_INITMENUPOPUP (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9d7e96e9-c52e-43bd-945b-05db33c8dfd0
api_name:
- SFVM_INITMENUPOPUP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1f9a2a169b232fe3ad16eeee8816536ed81c74dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968221"
---
# <a name="sfvm_initmenupopup-message"></a><span data-ttu-id="926f2-104">\_Mensagem SFVM INITMENUPOPUP</span><span class="sxs-lookup"><span data-stu-id="926f2-104">SFVM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="926f2-105">Permite que o objeto de retorno de chamada modifique um menu pop-up do Windows Explorer antes de ser exibido.</span><span class="sxs-lookup"><span data-stu-id="926f2-105">Allows the callback object to modify a Windows Explorer pop-up menu before it is displayed.</span></span> <span data-ttu-id="926f2-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="926f2-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INITMENUPOPUP 

    wParam = (WPARAM)(int) idCmd,nIndex;

    lParam = (LPARAM)(HMENU) hmenu;

            
```



## <a name="parameters"></a><span data-ttu-id="926f2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="926f2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="926f2-108">*idCmd \_ nIndex* \[\]</span><span class="sxs-lookup"><span data-stu-id="926f2-108">*idCmd\_nIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="926f2-109">A palavra de ordem inferior desse parâmetro contém o valor da primeira ID de comando reservada para comandos de cliente.</span><span class="sxs-lookup"><span data-stu-id="926f2-109">The low-order word of this parameter holds the value of the first command ID reserved for client commands.</span></span> <span data-ttu-id="926f2-110">A palavra de ordem superior contém o índice do menu.</span><span class="sxs-lookup"><span data-stu-id="926f2-110">The high-order word holds the index of the menu.</span></span>

</dd> <dt>

<span data-ttu-id="926f2-111">*HMENU* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="926f2-111">*hmenu* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="926f2-112">A alça do menu.</span><span class="sxs-lookup"><span data-stu-id="926f2-112">The menu's handle.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="926f2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="926f2-113">Remarks</span></span>

<span data-ttu-id="926f2-114">O objeto de exibição da pasta do sistema envia essa mensagem quando um menu é selecionado, mas antes de ser exibido.</span><span class="sxs-lookup"><span data-stu-id="926f2-114">The system folder view object sends this message when a menu is selected, but before it is displayed.</span></span> <span data-ttu-id="926f2-115">Processar esta mensagem se, por exemplo, você precisar habilitar ou desabilitar comandos de menu.</span><span class="sxs-lookup"><span data-stu-id="926f2-115">Process this message if, for instance, you need to enable or disable menu commands.</span></span> <span data-ttu-id="926f2-116">O menu pop-up pode ser:</span><span class="sxs-lookup"><span data-stu-id="926f2-116">The popup menu can be:</span></span>

-   <span data-ttu-id="926f2-117">O menu arquivo, editar ou exibir.</span><span class="sxs-lookup"><span data-stu-id="926f2-117">The File, Edit, or View menu.</span></span>
-   <span data-ttu-id="926f2-118">Um menu de nível superior definido pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="926f2-118">A top-level menu defined by the client.</span></span>
-   <span data-ttu-id="926f2-119">Um submenu definido pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="926f2-119">A client-defined submenu.</span></span>

## <a name="requirements"></a><span data-ttu-id="926f2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="926f2-120">Requirements</span></span>



| <span data-ttu-id="926f2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="926f2-121">Requirement</span></span> | <span data-ttu-id="926f2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="926f2-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="926f2-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="926f2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="926f2-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="926f2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="926f2-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="926f2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="926f2-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="926f2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="926f2-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="926f2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="926f2-128"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="926f2-128"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="926f2-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="926f2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="926f2-130">**SFVM \_ MERGEMENU**</span><span class="sxs-lookup"><span data-stu-id="926f2-130">**SFVM\_MERGEMENU**</span></span>](sfvm-mergemenu.md)
</dt> </dl>

 

 
