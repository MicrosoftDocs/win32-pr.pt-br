---
title: Mensagem de TTM_GETTOOLINFO (commctrl. h)
description: Recupera as informações que um controle ToolTip mantém sobre uma ferramenta.
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- Controles de TTM_GETTOOLINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_GETTOOLINFO
- TTM_GETTOOLINFOA
- TTM_GETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc0de37b97be3bec495c8777b2ddd1cc6fc1bd42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085573"
---
# <a name="ttm_gettoolinfo-message"></a><span data-ttu-id="ca0d2-104">\_Mensagem TTM GETTOOLINFO</span><span class="sxs-lookup"><span data-stu-id="ca0d2-104">TTM\_GETTOOLINFO message</span></span>

<span data-ttu-id="ca0d2-105">Recupera as informações que um controle ToolTip mantém sobre uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-105">Retrieves the information that a tooltip control maintains about a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="ca0d2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca0d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca0d2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ca0d2-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ca0d2-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ca0d2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca0d2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca0d2-110">Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ca0d2-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span> <span data-ttu-id="ca0d2-111">Ao enviar a mensagem, os membros de **HWND** e **UID** identificam uma ferramenta e o membro **cbSize** deve especificar o tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-111">When sending the message, the **hwnd** and **uId** members identify a tool, and the **cbSize** member must specify the size of the structure.</span></span> <span data-ttu-id="ca0d2-112">Ao usar essa mensagem para recuperar o texto da dica de ferramenta, verifique se o membro **lpszText** da estrutura **TOOLINFO** aponta para um buffer válido de tamanho de adquate</span><span class="sxs-lookup"><span data-stu-id="ca0d2-112">When using this message to retrieve the tooltip text, ensure that the **lpszText** member of the **TOOLINFO** structure points to a valid buffer of adquate size</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca0d2-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca0d2-113">Return value</span></span>

<span data-ttu-id="ca0d2-114">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca0d2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca0d2-115">Remarks</span></span>

<span data-ttu-id="ca0d2-116">Se o controle ToolTip incluir a ferramenta, a estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) receberá informações sobre a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-116">If the tooltip control includes the tool, the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure receives information about the tool.</span></span>

## <a name="examples"></a><span data-ttu-id="ca0d2-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca0d2-117">Examples</span></span>

<span data-ttu-id="ca0d2-118">O exemplo a seguir reposiciona um controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="ca0d2-118">The following example repositions a tooltip control.</span></span>


```C++
HRESULT MyToolTipClass::OffsetTooltip(int xOffset, int yOffset)  
{  
    HRESULT hr = S_OK;   
    DWORD   dwError = 0;  
  
    if (NULL != m_hWndToolTip)  
    {  
        TOOLINFO ti = {0};  
  
        ti.cbSize = sizeof(TOOLINFO);  
        ti.hwnd   = m_hWndToolTipOwner;  
  
        // Get the current tooltip definition.          
        if( SendMessage(m_hWndToolTip, TTM_GETTOOLINFO, 0, (LPARAM)&ti))  
        {  
            // Offset the tooltip rectangle as specified.              
            OffsetRect(&ti.rect, xOffset, yOffset);  
  
            // Apply the new rectangle to the tooltip.
            SendMessage(m_hWndToolTip, TTM_NEWTOOLRECT, 0, (LPARAM)&ti);  
        }  
        else  
        {  
            dwError = GetLastError();  
            hr = HRESULT_FROM_WIN32(dwError);  
            MyErrorHandler(hr);
       }  
    }  
    return hr;  
}  
```



## <a name="requirements"></a><span data-ttu-id="ca0d2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca0d2-119">Requirements</span></span>



| <span data-ttu-id="ca0d2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca0d2-120">Requirement</span></span> | <span data-ttu-id="ca0d2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ca0d2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca0d2-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca0d2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ca0d2-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca0d2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca0d2-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ca0d2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ca0d2-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ca0d2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca0d2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca0d2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca0d2-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca0d2-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ca0d2-128">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ca0d2-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ca0d2-129">**TTM \_ GETTOOLINFOW** (Unicode) e **TTM \_ GETTOOLINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ca0d2-129">**TTM\_GETTOOLINFOW** (Unicode) and **TTM\_GETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





