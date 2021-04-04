---
title: Mensagem de SBM_GETSCROLLBARINFO (WinUser. h)
description: Enviado por um aplicativo para recuperar informações sobre a barra de rolagem especificada.
ms.assetid: db6f704f-99ee-448c-ae7a-dd5a23399fb6
keywords:
- Controles de SBM_GETSCROLLBARINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- SBM_GETSCROLLBARINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8bdd78eb665bd069d854538bb2bdfae1a946765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644618"
---
# <a name="sbm_getscrollbarinfo-message"></a><span data-ttu-id="532c4-104">\_Mensagem SBM GETSCROLLBARINFO</span><span class="sxs-lookup"><span data-stu-id="532c4-104">SBM\_GETSCROLLBARINFO message</span></span>

<span data-ttu-id="532c4-105">Enviado por um aplicativo para recuperar informações sobre a barra de rolagem especificada.</span><span class="sxs-lookup"><span data-stu-id="532c4-105">Sent by an application to retrieve information about the specified scroll bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="532c4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="532c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="532c4-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="532c4-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="532c4-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="532c4-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="532c4-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="532c4-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="532c4-110">Ponteiro para uma estrutura [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) que recebe as informações.</span><span class="sxs-lookup"><span data-stu-id="532c4-110">Pointer to a [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) structure that receives the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="532c4-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="532c4-111">Return value</span></span>

<span data-ttu-id="532c4-112">Retornará zero, se for bem-sucedido ou zero.</span><span class="sxs-lookup"><span data-stu-id="532c4-112">Returns nonzero if successful or zero otherwise.</span></span>

<span data-ttu-id="532c4-113">Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="532c4-113">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="requirements"></a><span data-ttu-id="532c4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="532c4-114">Requirements</span></span>



| <span data-ttu-id="532c4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="532c4-115">Requirement</span></span> | <span data-ttu-id="532c4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="532c4-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="532c4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="532c4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="532c4-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="532c4-118">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="532c4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="532c4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="532c4-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="532c4-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="532c4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="532c4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="532c4-122"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="532c4-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="532c4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="532c4-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="532c4-124">**Referência**</span><span class="sxs-lookup"><span data-stu-id="532c4-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="532c4-125">**GetScrollBarInfo**</span><span class="sxs-lookup"><span data-stu-id="532c4-125">**GetScrollBarInfo**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo)
</dt> <dt>

[<span data-ttu-id="532c4-126">**SCROLLBARINFO**</span><span class="sxs-lookup"><span data-stu-id="532c4-126">**SCROLLBARINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-scrollbarinfo)
</dt> </dl>

 

