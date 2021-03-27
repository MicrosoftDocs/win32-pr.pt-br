---
description: 'Notifica o objeto de retorno de chamada de que um de seus comandos de menu ou de barra de ferramentas foi invocado pelo usuário. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 6b9e4a4d-ec45-489c-bbff-d123d5756b75
title: Mensagem de SFVM_INVOKECOMMAND (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5fc9709827250e5cf8060400bbecb714ae5998
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837227"
---
# <a name="sfvm_invokecommand-message"></a><span data-ttu-id="6e943-104">\_Mensagem SFVM INVOKECOMMAND</span><span class="sxs-lookup"><span data-stu-id="6e943-104">SFVM\_INVOKECOMMAND message</span></span>

<span data-ttu-id="6e943-105">Notifica o objeto de retorno de chamada de que um de seus comandos de menu ou de barra de ferramentas foi invocado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="6e943-105">Notifies the callback object that one of its toolbar or menu commands has been invoked by the user.</span></span> <span data-ttu-id="6e943-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="6e943-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_INVOKECOMMAND 

    wParam = (WPARAM)(UINT) idCmd;

            
```



## <a name="parameters"></a><span data-ttu-id="6e943-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6e943-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e943-108">*idCmd* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="6e943-108">*idCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e943-109">A ID de comando da barra de ferramentas ou do item de menu selecionado.</span><span class="sxs-lookup"><span data-stu-id="6e943-109">The command ID of the selected toolbar or menu item.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e943-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e943-110">Remarks</span></span>

<span data-ttu-id="6e943-111">Essa mensagem serve essencialmente a mesma função que uma mensagem de [**\_ comando do WM**](../menurc/wm-command.md) em um procedimento de janela convencional.</span><span class="sxs-lookup"><span data-stu-id="6e943-111">This message serves essentially the same function as a [**WM\_COMMAND**](../menurc/wm-command.md) message in a conventional window procedure.</span></span> <span data-ttu-id="6e943-112">Ele permite que o objeto de retorno de chamada manipule quaisquer itens que tenham sido adicionados à ferramenta ou à barra de menus do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="6e943-112">It allows the callback object to handle any items that it has added to the Windows Explorer tool or menu bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e943-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e943-113">Requirements</span></span>



| <span data-ttu-id="6e943-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e943-114">Requirement</span></span> | <span data-ttu-id="6e943-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6e943-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6e943-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e943-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6e943-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e943-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6e943-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6e943-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6e943-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6e943-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6e943-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6e943-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e943-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e943-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
