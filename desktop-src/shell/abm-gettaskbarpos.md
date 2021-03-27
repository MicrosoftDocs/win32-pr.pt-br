---
description: Recupera o retângulo delimitador da barra de tarefas do Windows.
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: Mensagem de ABM_GETTASKBARPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501448"
---
# <a name="abm_gettaskbarpos-message"></a><span data-ttu-id="fa19c-103">\_Mensagem ABM GETTASKBARPOS</span><span class="sxs-lookup"><span data-stu-id="fa19c-103">ABM\_GETTASKBARPOS message</span></span>

<span data-ttu-id="fa19c-104">Recupera o retângulo delimitador da barra de tarefas do Windows.</span><span class="sxs-lookup"><span data-stu-id="fa19c-104">Retrieves the bounding rectangle of the Windows taskbar.</span></span>


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a><span data-ttu-id="fa19c-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa19c-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa19c-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="fa19c-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="fa19c-107">Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) cujo membro **RC** recebe o retângulo delimitador, nas coordenadas da tela, da barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="fa19c-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure whose **rc** member receives the bounding rectangle, in screen coordinates, of the taskbar.</span></span> <span data-ttu-id="fa19c-108">Você deve especificar o **cbSize** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="fa19c-108">You must specify the **cbSize** when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa19c-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa19c-109">Return value</span></span>

<span data-ttu-id="fa19c-110">Retornará **true** se for bem-sucedido; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="fa19c-110">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa19c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa19c-111">Remarks</span></span>

<span data-ttu-id="fa19c-112">Observe que isso se aplica somente à barra de tarefas do sistema.</span><span class="sxs-lookup"><span data-stu-id="fa19c-112">Note that this applies only to the system taskbar.</span></span> <span data-ttu-id="fa19c-113">Outros objetos, especialmente barras de ferramentas fornecidas com software de terceiros, também podem estar presentes.</span><span class="sxs-lookup"><span data-stu-id="fa19c-113">Other objects, particularly toolbars supplied with third-party software, also can be present.</span></span> <span data-ttu-id="fa19c-114">Como resultado, parte da área de tela não coberta pela barra de tarefas do Windows pode não estar visível para o usuário.</span><span class="sxs-lookup"><span data-stu-id="fa19c-114">As a result, some of the screen area not covered by the Windows taskbar might not be visible to the user.</span></span> <span data-ttu-id="fa19c-115">Para recuperar a área da tela não coberta pela barra de tarefas e por outras barras de aplicativo a área de trabalho disponível para seu aplicativo, use a função [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) .</span><span class="sxs-lookup"><span data-stu-id="fa19c-115">To retrieve the area of the screen not covered by both the taskbar and other app bars the working area available to your application , use the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa19c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa19c-116">Requirements</span></span>



| <span data-ttu-id="fa19c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa19c-117">Requirement</span></span> | <span data-ttu-id="fa19c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fa19c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa19c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa19c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fa19c-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fa19c-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fa19c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fa19c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fa19c-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fa19c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fa19c-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fa19c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa19c-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa19c-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

