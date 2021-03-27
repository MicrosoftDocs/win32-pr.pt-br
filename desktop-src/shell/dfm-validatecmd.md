---
description: Enviado para verificar a existência de um comando de menu.
title: Mensagem de DFM_VALIDATECMD (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 97ff3cdf-ed0c-4813-8d5a-b5141636d32c
api_name:
- DFM_VALIDATECMD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5aa171f19d4d08c3ba3088676a4ae5364f0826f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090023"
---
# <a name="dfm_validatecmd-message"></a><span data-ttu-id="aa4cc-103">\_Mensagem DFM VALIDATECMD</span><span class="sxs-lookup"><span data-stu-id="aa4cc-103">DFM\_VALIDATECMD message</span></span>

<span data-ttu-id="aa4cc-104">Enviado para verificar a existência de um comando de menu.</span><span class="sxs-lookup"><span data-stu-id="aa4cc-104">Sent to verify the existence of a menu command.</span></span>


```C++
DFM_INVOKECOMMAND

    wParam = (WPARAM)(WPARAM) idCmd;            

    lParam = (LPARAM)(LPARAM) lParam = 0;

            
```



## <a name="parameters"></a><span data-ttu-id="aa4cc-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa4cc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa4cc-106">*idCmd*</span><span class="sxs-lookup"><span data-stu-id="aa4cc-106">*idCmd*</span></span> 
</dt> <dd><span data-ttu-id="aa4cc-107">O deslocamento do identificador de comando do menu.</span><span class="sxs-lookup"><span data-stu-id="aa4cc-107">The menu command identifier offset.</span></span></dd> <dt>

<span data-ttu-id="aa4cc-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="aa4cc-108">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="aa4cc-109">Não usado.</span><span class="sxs-lookup"><span data-stu-id="aa4cc-109">Not used.</span></span> <span data-ttu-id="aa4cc-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="aa4cc-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa4cc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa4cc-111">Return value</span></span>

<span data-ttu-id="aa4cc-112">Retornará S \_ OK se o comando existir, \_ caso contrário, s false.</span><span class="sxs-lookup"><span data-stu-id="aa4cc-112">Returns S\_OK if the command exists, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa4cc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa4cc-113">Remarks</span></span>

<span data-ttu-id="aa4cc-114">Essa mensagem é enviada para a função de retorno de chamada ou para o objeto de retorno de chamada, dependendo de como o objeto de menu de contexto padrão é construído.</span><span class="sxs-lookup"><span data-stu-id="aa4cc-114">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="aa4cc-115">Há duas APIs para sua construção, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="aa4cc-115">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="aa4cc-116">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) é uma versão estendida dessa mensagem e fornece mais informações para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="aa4cc-116">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="aa4cc-117">Use **DFM \_ INVOKECOMMANDEX** se as informações adicionais fornecidas por essa interface forem necessárias em sua implementação.</span><span class="sxs-lookup"><span data-stu-id="aa4cc-117">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa4cc-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa4cc-118">Requirements</span></span>



| <span data-ttu-id="aa4cc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa4cc-119">Requirement</span></span> | <span data-ttu-id="aa4cc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="aa4cc-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aa4cc-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa4cc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="aa4cc-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="aa4cc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="aa4cc-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa4cc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="aa4cc-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aa4cc-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aa4cc-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa4cc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa4cc-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa4cc-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




