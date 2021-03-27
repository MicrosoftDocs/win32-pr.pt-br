---
description: 'Permite que o objeto de retorno de chamada especifique uma cadeia de texto de dica de ferramenta para itens de menu ou botões da barra de ferramentas Usado por IShellFolderViewCB:: MessageSFVCB.'
ms.assetid: 29849218-0d30-4412-86c8-5d320bc5dd26
title: Mensagem de SFVM_GETTOOLTIPTEXT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ffea70f6051ec435e14640ac70d2e9617b11305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922748"
---
# <a name="sfvm_gettooltiptext-message"></a><span data-ttu-id="46dfc-104">\_Mensagem SFVM GETtooltiptext</span><span class="sxs-lookup"><span data-stu-id="46dfc-104">SFVM\_GETTOOLTIPTEXT message</span></span>

<span data-ttu-id="46dfc-105">Permite que o objeto de retorno de chamada especifique uma cadeia de texto de dica de ferramenta para itens de menu ou botões da barra de ferramentas</span><span class="sxs-lookup"><span data-stu-id="46dfc-105">Allows the callback object to specify a tooltip text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="46dfc-106">Usado por [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="46dfc-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETTOOLTIPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="46dfc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="46dfc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46dfc-108">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="46dfc-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46dfc-109">A palavra de ordem inferior desse parâmetro contém a ID de comando.</span><span class="sxs-lookup"><span data-stu-id="46dfc-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="46dfc-110">A palavra de ordem superior contém o número de caracteres no buffer *pszText* .</span><span class="sxs-lookup"><span data-stu-id="46dfc-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="46dfc-111">*pszText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="46dfc-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46dfc-112">Uma cadeia de caracteres terminada em nulo que contém o texto de ajuda.</span><span class="sxs-lookup"><span data-stu-id="46dfc-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46dfc-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46dfc-113">Requirements</span></span>



| <span data-ttu-id="46dfc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="46dfc-114">Requirement</span></span> | <span data-ttu-id="46dfc-115">Valor</span><span class="sxs-lookup"><span data-stu-id="46dfc-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="46dfc-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46dfc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="46dfc-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46dfc-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="46dfc-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46dfc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="46dfc-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="46dfc-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="46dfc-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="46dfc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="46dfc-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="46dfc-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
