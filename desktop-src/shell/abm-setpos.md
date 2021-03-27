---
description: Define o tamanho e a posição da tela de um AppBar.
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: Mensagem de ABM_SETPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6886249f42638745ca038aa1f216ddc995f0e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501447"
---
# <a name="abm_setpos-message"></a><span data-ttu-id="44e0e-103">\_Mensagem ABM SETPOS</span><span class="sxs-lookup"><span data-stu-id="44e0e-103">ABM\_SETPOS message</span></span>

<span data-ttu-id="44e0e-104">Define o tamanho e a posição da tela de um AppBar.</span><span class="sxs-lookup"><span data-stu-id="44e0e-104">Sets the size and screen position of an appbar.</span></span> <span data-ttu-id="44e0e-105">A mensagem Especifica uma borda de tela e o retângulo delimitador para o AppBar.</span><span class="sxs-lookup"><span data-stu-id="44e0e-105">The message specifies a screen edge and the bounding rectangle for the appbar.</span></span> <span data-ttu-id="44e0e-106">O sistema pode ajustar o retângulo delimitador para que o AppBar não interfira na barra de tarefas do Windows nem em qualquer outro appbars.</span><span class="sxs-lookup"><span data-stu-id="44e0e-106">The system may adjust the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="44e0e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44e0e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44e0e-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="44e0e-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="44e0e-109">Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="44e0e-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="44e0e-110">O membro **uEdge** especifica uma borda de tela e o membro **RC** contém o retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="44e0e-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the bounding rectangle.</span></span> <span data-ttu-id="44e0e-111">Quando a função [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) retorna, **RC** contém o retângulo delimitador aprovado.</span><span class="sxs-lookup"><span data-stu-id="44e0e-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="44e0e-112">Você deve especificar os membros **cbSize**, **HWND**, **uEdge** e **RC** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="44e0e-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44e0e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44e0e-113">Return value</span></span>

<span data-ttu-id="44e0e-114">Sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="44e0e-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="44e0e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="44e0e-115">Remarks</span></span>

<span data-ttu-id="44e0e-116">Essa mensagem faz com que o sistema envie a mensagem de notificação do [**ABN \_ POSCHANGED**](abn-poschanged.md) para todos os appbars.</span><span class="sxs-lookup"><span data-stu-id="44e0e-116">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="44e0e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44e0e-117">Requirements</span></span>



| <span data-ttu-id="44e0e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="44e0e-118">Requirement</span></span> | <span data-ttu-id="44e0e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="44e0e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44e0e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44e0e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="44e0e-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="44e0e-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="44e0e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44e0e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="44e0e-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="44e0e-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44e0e-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="44e0e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="44e0e-125"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="44e0e-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




