---
description: 'Permite que o objeto de retorno de chamada adicione botões à barra de ferramentas. Usado por IShellFolderViewCB:: MessageSFVCB.'
title: Mensagem de SFVM_GETBUTTONINFO (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968069"
---
# <a name="sfvm_getbuttoninfo-message"></a><span data-ttu-id="ef0f4-104">\_Mensagem SFVM GETBUTTONINFO</span><span class="sxs-lookup"><span data-stu-id="ef0f4-104">SFVM\_GETBUTTONINFO message</span></span>

<span data-ttu-id="ef0f4-105">Permite que o objeto de retorno de chamada adicione botões à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="ef0f4-105">Allows the callback object to add buttons to the toolbar.</span></span> <span data-ttu-id="ef0f4-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="ef0f4-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a><span data-ttu-id="ef0f4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ef0f4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef0f4-108">*ptbinfo* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ef0f4-108">*ptbinfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef0f4-109">O endereço de uma estrutura [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) que especifica o número de botões e como eles devem ser adicionados à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="ef0f4-109">The address of a [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) structure that specifies the number of buttons and how they are to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ef0f4-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="ef0f4-110">Remarks</span></span>

<span data-ttu-id="ef0f4-111">Os botões podem ser acrescentados ou anexados aos botões de objeto de exibição da pasta do sistema padrão ou ser exibidos no lugar dos botões padrão.</span><span class="sxs-lookup"><span data-stu-id="ef0f4-111">Buttons can be appended or prepended to the standard system folder view object buttons, or be displayed in place of the standard buttons.</span></span> <span data-ttu-id="ef0f4-112">Essa mensagem é seguida por uma mensagem [**SFVM \_ getbuttons**](sfvm-getbuttons.md) que recupera as informações relacionadas às especificações do botão.</span><span class="sxs-lookup"><span data-stu-id="ef0f4-112">This message is followed by a [**SFVM\_GETBUTTONS**](sfvm-getbuttons.md) message that retrieves the information concerning the button specifics.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef0f4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef0f4-113">Requirements</span></span>



| <span data-ttu-id="ef0f4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef0f4-114">Requirement</span></span> | <span data-ttu-id="ef0f4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ef0f4-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ef0f4-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef0f4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ef0f4-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ef0f4-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ef0f4-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ef0f4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ef0f4-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ef0f4-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ef0f4-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ef0f4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef0f4-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef0f4-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
