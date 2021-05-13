---
description: Enviado a um procedimento de DLL de extensão do Gerenciador de arquivos quando o usuário pressiona F1 em um menu ou item de comando de barra de ferramentas. A extensão deve chamar WinHelp, com o parâmetro hWnd da função definido como o valor do parâmetro hWnd da extensão.
title: Mensagem de FMEVENT_HELPMENUITEM (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPMENUITEM
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 6298061d-7e24-45ab-8bc4-96b28e071080
ms.openlocfilehash: 46cb246e91f9901204432527ba36fd8ac72beba4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842307"
---
# <a name="fmevent_helpmenuitem-message"></a><span data-ttu-id="4565c-104">\_Mensagem FMEVENT HELPMENUITEM</span><span class="sxs-lookup"><span data-stu-id="4565c-104">FMEVENT\_HELPMENUITEM message</span></span>

<span data-ttu-id="4565c-105">Enviado a um procedimento de DLL de extensão do Gerenciador de arquivos quando o usuário pressiona F1 em um menu ou item de comando de barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="4565c-105">Sent to a File Manager extension DLL procedure when the user presses F1 on a menu or toolbar command item.</span></span> <span data-ttu-id="4565c-106">A extensão deve chamar [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), com o parâmetro *HWND* da função definido como o valor do parâmetro *hWnd* da extensão.</span><span class="sxs-lookup"><span data-stu-id="4565c-106">The extension should call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa), with that function's *hwnd* parameter set to the value of the extension's *hwnd* parameter.</span></span>

## <a name="parameters"></a><span data-ttu-id="4565c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4565c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4565c-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4565c-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4565c-109">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4565c-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4565c-110">*uItem*</span><span class="sxs-lookup"><span data-stu-id="4565c-110">*uItem*</span></span> 
</dt> <dd>

<span data-ttu-id="4565c-111">Um valor que identifica o menu ou o item de comando da barra de ferramentas para o qual a ajuda é desejada.</span><span class="sxs-lookup"><span data-stu-id="4565c-111">A value that identifies the menu or toolbar command item for which Help is desired.</span></span> <span data-ttu-id="4565c-112">O procedimento de extensão usa esse valor para determinar a melhor maneira de chamar o [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span><span class="sxs-lookup"><span data-stu-id="4565c-112">The extension procedure uses this value to determine how best to call [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4565c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4565c-113">Return value</span></span>

<span data-ttu-id="4565c-114">Um procedimento de DLL de extensão deve retornar zero se ele processar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="4565c-114">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4565c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4565c-115">Requirements</span></span>



| <span data-ttu-id="4565c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="4565c-116">Requirement</span></span> | <span data-ttu-id="4565c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="4565c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4565c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4565c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4565c-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4565c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="4565c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4565c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4565c-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4565c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4565c-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4565c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4565c-123"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="4565c-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4565c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4565c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4565c-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="4565c-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="4565c-126">**FMEVENT \_ HelpString**</span><span class="sxs-lookup"><span data-stu-id="4565c-126">**FMEVENT\_HELPSTRING**</span></span>](fmevent-helpstring.md)
</dt> </dl>

 

 




