---
description: Mensagem de DFM_GETHELPTEXT-permite que o objeto de retorno de chamada especifique uma cadeia de texto de ajuda.
title: Mensagem de DFM_GETHELPTEXT (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 40ed981b-6d03-4c4f-9e70-1a01d49edcb0
api_name:
- DFM_GETHELPTEXT
- DFM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2428fe6696ff5949a0b25487437c8f3408b95f65
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097064"
---
# <a name="dfm_gethelptext-message"></a><span data-ttu-id="b6486-103">\_Mensagem DFM GEThelptext</span><span class="sxs-lookup"><span data-stu-id="b6486-103">DFM\_GETHELPTEXT message</span></span>

<span data-ttu-id="b6486-104">Permite que o objeto de retorno de chamada especifique uma cadeia de texto de ajuda.</span><span class="sxs-lookup"><span data-stu-id="b6486-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="b6486-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b6486-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6486-106">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="b6486-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b6486-107">A palavra de ordem inferior desse parâmetro contém a ID de comando.</span><span class="sxs-lookup"><span data-stu-id="b6486-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="b6486-108">A palavra de ordem superior contém o número de caracteres no buffer *pszText* .</span><span class="sxs-lookup"><span data-stu-id="b6486-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b6486-109">*pszText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b6486-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b6486-110">Uma cadeia de caracteres ANSI terminada em nulo que contém o texto de ajuda.</span><span class="sxs-lookup"><span data-stu-id="b6486-110">A null-terminated ANSI string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6486-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6486-111">Remarks</span></span>

<span data-ttu-id="b6486-112">Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é construído.</span><span class="sxs-lookup"><span data-stu-id="b6486-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="b6486-113">Há duas APIs para sua construção, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="b6486-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="b6486-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="b6486-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="b6486-115">Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="b6486-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6486-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6486-116">Requirements</span></span>



| <span data-ttu-id="b6486-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6486-117">Requirement</span></span> | <span data-ttu-id="b6486-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b6486-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b6486-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6486-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b6486-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6486-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="b6486-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b6486-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b6486-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6486-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b6486-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b6486-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6486-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6486-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="b6486-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="b6486-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b6486-126">**DFM \_ GetHelpText** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b6486-126">**DFM\_GETHELPTEXT** (ANSI)</span></span><br/>                                              |



 

 




