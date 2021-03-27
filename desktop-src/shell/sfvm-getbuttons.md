---
description: 'Permite que o objeto de retorno de chamada especifique os botões a serem adicionados à barra de ferramentas. Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: Mensagem de SFVM_GETBUTTONS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ad4ced86909c37ec77bf0470b46a40954f5b61c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829220"
---
# <a name="sfvm_getbuttons-message"></a><span data-ttu-id="e2bd1-104">\_Mensagem de GETbotãors do SFVM</span><span class="sxs-lookup"><span data-stu-id="e2bd1-104">SFVM\_GETBUTTONS message</span></span>

<span data-ttu-id="e2bd1-105">Permite que o objeto de retorno de chamada especifique os botões a serem adicionados à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="e2bd1-105">Allows the callback object to specify the buttons to be added to the toolbar.</span></span> <span data-ttu-id="e2bd1-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="e2bd1-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a><span data-ttu-id="e2bd1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2bd1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2bd1-108">*idCmdFirst \_ cbtnMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="e2bd1-108">*idCmdFirst\_cbtnMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2bd1-109">Contém valores de 2 16 bits incluídos no parâmetro com a macro [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) .</span><span class="sxs-lookup"><span data-stu-id="e2bd1-109">Contains two 16-bit values packed into the parameter with the [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) macro.</span></span> <span data-ttu-id="e2bd1-110">A palavra de ordem inferior contém a ID de comando inicial.</span><span class="sxs-lookup"><span data-stu-id="e2bd1-110">The low-order word contains the initial command ID.</span></span> <span data-ttu-id="e2bd1-111">A palavra de ordem superior contém o número de botões a serem adicionados, conforme especificado na mensagem [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="e2bd1-111">The high-order word contains the number of buttons to be added, as specified in the preceding [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="e2bd1-112">*pbtn* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="e2bd1-112">*pbtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e2bd1-113">O endereço de uma matriz de estruturas [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) , uma para cada botão a ser adicionado à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="e2bd1-113">The address of an array of [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) structures, one for each button to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e2bd1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2bd1-114">Remarks</span></span>

<span data-ttu-id="e2bd1-115">Essa mensagem é precedida por uma mensagem [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="e2bd1-115">This message is preceded by a [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span> <span data-ttu-id="e2bd1-116">O objeto de retorno de chamada deve lidar com essa mensagem para especificar o número de botões e onde eles devem ser colocados na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="e2bd1-116">The callback object must handle that message to specify the number of buttons and where they are to be placed on the toolbar.</span></span> <span data-ttu-id="e2bd1-117">Dependendo de como o objeto de retorno de chamada responde à mensagem **SFVM \_ GETBUTTONINFO** , os botões especificados pelo parâmetro *pbtn* serão acrescentados ou anexados aos botões padrão do objeto de exibição da pasta do sistema ou substituirão o conjunto padrão.</span><span class="sxs-lookup"><span data-stu-id="e2bd1-117">Depending on how the callback object responds to the **SFVM\_GETBUTTONINFO** message, the buttons specified by *pbtn* parameter will be appended or prepended to the system folder view object's standard buttons, or replace the standard set.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2bd1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2bd1-118">Requirements</span></span>



| <span data-ttu-id="e2bd1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2bd1-119">Requirement</span></span> | <span data-ttu-id="e2bd1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e2bd1-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e2bd1-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2bd1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e2bd1-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e2bd1-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e2bd1-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2bd1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e2bd1-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e2bd1-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e2bd1-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e2bd1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2bd1-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2bd1-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
