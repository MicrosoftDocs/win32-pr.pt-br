---
description: Mensagem de DFM_GETHELPTEXTW-permite que o objeto de retorno de chamada especifique uma cadeia de texto de ajuda.
title: Mensagem de DFM_GETHELPTEXTW (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6271b150bead5be4715259c68711ee67417f6395
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097034"
---
# <a name="dfm_gethelptextw-message"></a><span data-ttu-id="cdbdf-103">\_Mensagem DFM GETHELPTEXTW</span><span class="sxs-lookup"><span data-stu-id="cdbdf-103">DFM\_GETHELPTEXTW message</span></span>

<span data-ttu-id="cdbdf-104">Permite que o objeto de retorno de chamada especifique uma cadeia de texto de ajuda.</span><span class="sxs-lookup"><span data-stu-id="cdbdf-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="cdbdf-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cdbdf-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdbdf-106">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="cdbdf-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdbdf-107">A palavra de ordem inferior desse parâmetro contém a ID de comando.</span><span class="sxs-lookup"><span data-stu-id="cdbdf-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="cdbdf-108">A palavra de ordem superior contém o número de caracteres no buffer *pszText* .</span><span class="sxs-lookup"><span data-stu-id="cdbdf-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cdbdf-109">*pszText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="cdbdf-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdbdf-110">Uma cadeia de caracteres Unicode terminada em nulo que contém o texto de ajuda.</span><span class="sxs-lookup"><span data-stu-id="cdbdf-110">A null-terminated Unicode string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cdbdf-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cdbdf-111">Remarks</span></span>

<span data-ttu-id="cdbdf-112">Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é construído.</span><span class="sxs-lookup"><span data-stu-id="cdbdf-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="cdbdf-113">Há duas APIs para sua construção, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="cdbdf-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="cdbdf-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="cdbdf-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="cdbdf-115">Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="cdbdf-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdbdf-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdbdf-116">Requirements</span></span>



| <span data-ttu-id="cdbdf-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cdbdf-117">Requirement</span></span> | <span data-ttu-id="cdbdf-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cdbdf-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cdbdf-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdbdf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cdbdf-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cdbdf-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cdbdf-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cdbdf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cdbdf-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cdbdf-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cdbdf-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cdbdf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdbdf-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdbdf-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="cdbdf-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="cdbdf-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cdbdf-126">**DFM \_ GETHELPTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="cdbdf-126">**DFM\_GETHELPTEXTW** (Unicode)</span></span><br/>                                          |



 

 




