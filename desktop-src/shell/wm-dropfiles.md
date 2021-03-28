---
description: Enviado quando o usuário remove um arquivo na janela de um aplicativo que se registrou como um destinatário dos arquivos soltos.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: Mensagem de WM_DROPFILES (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967879"
---
# <a name="wm_dropfiles-message"></a><span data-ttu-id="2a978-103">Mensagem do WM \_ DropFiles</span><span class="sxs-lookup"><span data-stu-id="2a978-103">WM\_DROPFILES message</span></span>

<span data-ttu-id="2a978-104">Enviado quando o usuário remove um arquivo na janela de um aplicativo que se registrou como um destinatário dos arquivos soltos.</span><span class="sxs-lookup"><span data-stu-id="2a978-104">Sent when the user drops a file on the window of an application that has registered itself as a recipient of dropped files.</span></span>


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a><span data-ttu-id="2a978-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a978-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a978-106">*hDrop*</span><span class="sxs-lookup"><span data-stu-id="2a978-106">*hDrop*</span></span> 
</dt> <dd>

<span data-ttu-id="2a978-107">Um identificador para uma estrutura interna que descreve os arquivos descartados.</span><span class="sxs-lookup"><span data-stu-id="2a978-107">A handle to an internal structure describing the dropped files.</span></span> <span data-ttu-id="2a978-108">Passe esse identificador [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)ou [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) para recuperar informações sobre os arquivos ignorados.</span><span class="sxs-lookup"><span data-stu-id="2a978-108">Pass this handle [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea), or [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) to retrieve information about the dropped files.</span></span>

</dd> <dt>

<span data-ttu-id="2a978-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a978-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a978-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2a978-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a978-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2a978-111">Return value</span></span>

<span data-ttu-id="2a978-112">Um aplicativo deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="2a978-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a978-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a978-113">Remarks</span></span>

<span data-ttu-id="2a978-114">O identificador HDROP é declarado em shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="2a978-114">The HDROP handle is declared in Shellapi.h.</span></span> <span data-ttu-id="2a978-115">Você deve incluir esse cabeçalho em sua compilação para usar o **WM \_ DropFiles**.</span><span class="sxs-lookup"><span data-stu-id="2a978-115">You must include this header in your build to use **WM\_DROPFILES**.</span></span> <span data-ttu-id="2a978-116">Para obter mais informações sobre como usar o recurso de arrastar e soltar para transferir dados do Shell, consulte [transferindo dados do shell usando o recurso de arrastar e soltar ou a área de transferência](dragdrop.md).</span><span class="sxs-lookup"><span data-stu-id="2a978-116">For further discussion of how to use drag-and-drop to transfer Shell data, see [Transferring Shell Data Using Drag-and-Drop or the Clipboard](dragdrop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a978-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a978-117">Requirements</span></span>



| <span data-ttu-id="2a978-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a978-118">Requirement</span></span> | <span data-ttu-id="2a978-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2a978-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2a978-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a978-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2a978-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2a978-121">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="2a978-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a978-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2a978-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2a978-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2a978-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2a978-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a978-125"><dt>WinUser. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a978-125"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a978-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a978-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a978-127">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="2a978-127">**PostMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="2a978-128">**DragAcceptFiles**</span><span class="sxs-lookup"><span data-stu-id="2a978-128">**DragAcceptFiles**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
