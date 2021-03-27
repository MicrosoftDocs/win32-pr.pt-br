---
description: Solicita um tamanho e uma posição de tela para um AppBar.
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: Mensagem de ABM_QUERYPOS (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296222"
---
# <a name="abm_querypos-message"></a><span data-ttu-id="4da27-103">\_Mensagem ABM QUERYPOS</span><span class="sxs-lookup"><span data-stu-id="4da27-103">ABM\_QUERYPOS message</span></span>

<span data-ttu-id="4da27-104">Solicita um tamanho e uma posição de tela para um AppBar.</span><span class="sxs-lookup"><span data-stu-id="4da27-104">Requests a size and screen position for an appbar.</span></span> <span data-ttu-id="4da27-105">Quando a solicitação é feita, a mensagem propõe uma borda de tela e um retângulo delimitador para o AppBar.</span><span class="sxs-lookup"><span data-stu-id="4da27-105">When the request is made, the message proposes a screen edge and a bounding rectangle for the appbar.</span></span> <span data-ttu-id="4da27-106">O sistema ajusta o retângulo delimitador para que o AppBar não interfira na barra de tarefas do Windows ou em qualquer outro appbars.</span><span class="sxs-lookup"><span data-stu-id="4da27-106">The system adjusts the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="4da27-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4da27-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4da27-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="4da27-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="4da27-109">Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="4da27-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="4da27-110">O membro **uEdge** especifica uma borda de tela e o membro **RC** contém o retângulo delimitador proposto.</span><span class="sxs-lookup"><span data-stu-id="4da27-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the proposed bounding rectangle.</span></span> <span data-ttu-id="4da27-111">Quando a função [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) retorna, **RC** contém o retângulo delimitador aprovado.</span><span class="sxs-lookup"><span data-stu-id="4da27-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="4da27-112">Você deve especificar os membros **cbSize**, **HWND**, **uEdge** e **RC** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="4da27-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4da27-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4da27-113">Return value</span></span>

<span data-ttu-id="4da27-114">Sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="4da27-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4da27-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="4da27-115">Remarks</span></span>

<span data-ttu-id="4da27-116">Um AppBar deve enviar essa mensagem antes de enviar a mensagem [**\_ SETPOS do ABM**](abm-setpos.md) .</span><span class="sxs-lookup"><span data-stu-id="4da27-116">An appbar should send this message before sending the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="4da27-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4da27-117">Requirements</span></span>



| <span data-ttu-id="4da27-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4da27-118">Requirement</span></span> | <span data-ttu-id="4da27-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4da27-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4da27-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4da27-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4da27-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4da27-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4da27-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4da27-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4da27-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4da27-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4da27-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4da27-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4da27-125"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4da27-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




