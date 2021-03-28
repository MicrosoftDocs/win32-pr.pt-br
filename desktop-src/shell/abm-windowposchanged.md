---
description: Notifica o sistema quando uma posição de AppBar é alterada. Um AppBar deve chamar essa mensagem em resposta à mensagem do WM \_ WINDOWPOSCHANGED.
ms.assetid: 8ca51f5f-b6cf-4f2c-98f4-69c992679320
title: Mensagem de ABM_WINDOWPOSCHANGED (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29c8ea6fab6960678ad030a0c1817ad5f8aaae29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460978"
---
# <a name="abm_windowposchanged-message"></a><span data-ttu-id="61f9b-104">\_Mensagem ABM WINDOWPOSCHANGED</span><span class="sxs-lookup"><span data-stu-id="61f9b-104">ABM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="61f9b-105">Notifica o sistema quando uma posição de AppBar é alterada.</span><span class="sxs-lookup"><span data-stu-id="61f9b-105">Notifies the system when an appbar's position has changed.</span></span> <span data-ttu-id="61f9b-106">Um AppBar deve chamar essa mensagem em resposta à mensagem do [**WM \_ WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) .</span><span class="sxs-lookup"><span data-stu-id="61f9b-106">An appbar should call this message in response to the [**WM\_WINDOWPOSCHANGED**](/windows/desktop/winmsg/wm-windowposchanged) message.</span></span>


```C++
SHAppBarMessage(ABM_WINDOWPOSCHANGED, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="61f9b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="61f9b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61f9b-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="61f9b-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="61f9b-109">Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que identifica o AppBar a ser ativado.</span><span class="sxs-lookup"><span data-stu-id="61f9b-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="61f9b-110">Você deve especificar os membros **cbSize** e **HWND** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="61f9b-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61f9b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="61f9b-111">Return value</span></span>

<span data-ttu-id="61f9b-112">Sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="61f9b-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="61f9b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="61f9b-113">Remarks</span></span>

<span data-ttu-id="61f9b-114">Essa mensagem será ignorada se o membro **HWND** da estrutura apontado por *pabd* identificar uma AutoOcultar AppBar.</span><span class="sxs-lookup"><span data-stu-id="61f9b-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span>

## <a name="requirements"></a><span data-ttu-id="61f9b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61f9b-115">Requirements</span></span>



| <span data-ttu-id="61f9b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="61f9b-116">Requirement</span></span> | <span data-ttu-id="61f9b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="61f9b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61f9b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61f9b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="61f9b-119">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="61f9b-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="61f9b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61f9b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="61f9b-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="61f9b-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61f9b-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61f9b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="61f9b-123"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="61f9b-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

