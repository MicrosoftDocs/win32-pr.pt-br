---
description: Enviado pela implementação do menu de contexto padrão para obter o verbo para a ID de comando fornecida no menu de contexto.
title: Mensagem de DFM_GETVERB (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd12a38e-4d50-43ad-9d1f-8fefa90b44f9
api_name:
- DFM_GETVERB
- DFM_GETVERBA
- DFM_GETVERBW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbb1b2fb54aa2b0e4b66cf8fc559c56eb279504d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164307"
---
# <a name="dfm_getverb-message"></a><span data-ttu-id="19336-103">\_Mensagem GETVERBS DFM</span><span class="sxs-lookup"><span data-stu-id="19336-103">DFM\_GETVERB message</span></span>

<span data-ttu-id="19336-104">Enviado pela implementação do menu de contexto padrão para obter o verbo para a ID de comando fornecida no menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="19336-104">Sent by the default context menu implementation to get the verb for the given command ID in the context menu.</span></span>


```C++

                DFM_GETVERB 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="19336-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="19336-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19336-106">*idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="19336-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19336-107">A palavra de ordem inferior desse parâmetro contém a ID de comando.</span><span class="sxs-lookup"><span data-stu-id="19336-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="19336-108">A palavra de ordem superior contém o número de caracteres no buffer *pszText* .</span><span class="sxs-lookup"><span data-stu-id="19336-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="19336-109">*pszText* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="19336-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19336-110">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o texto do verbo.</span><span class="sxs-lookup"><span data-stu-id="19336-110">A pointer to a null-terminated string that contains the verb text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="19336-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="19336-111">Remarks</span></span>

<span data-ttu-id="19336-112">Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é construído.</span><span class="sxs-lookup"><span data-stu-id="19336-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="19336-113">Há duas APIs para sua construção, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="19336-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="19336-114">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="19336-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="19336-115">Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="19336-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="19336-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19336-116">Requirements</span></span>



| <span data-ttu-id="19336-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="19336-117">Requirement</span></span> | <span data-ttu-id="19336-118">Valor</span><span class="sxs-lookup"><span data-stu-id="19336-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="19336-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19336-119">Minimum supported client</span></span><br/> | <span data-ttu-id="19336-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="19336-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="19336-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="19336-121">Minimum supported server</span></span><br/> | <span data-ttu-id="19336-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="19336-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="19336-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="19336-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="19336-124"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="19336-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="19336-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="19336-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="19336-126">**DFM \_ GETVERBW** (Unicode) e **DFM \_ getverbs** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="19336-126">**DFM\_GETVERBW** (Unicode) and **DFM\_GETVERBA** (ANSI)</span></span><br/>                 |



 

 




