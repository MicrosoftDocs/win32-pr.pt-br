---
description: Registra um novo AppBar e especifica o identificador da mensagem que o sistema deve usar para enviar mensagens de notificação. Um AppBar deve enviar essa mensagem antes de enviar qualquer outra mensagem AppBar.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: Mensagem de ABM_NEW (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646852"
---
# <a name="abm_new-message"></a><span data-ttu-id="80883-104">ABM \_ nova mensagem</span><span class="sxs-lookup"><span data-stu-id="80883-104">ABM\_NEW message</span></span>

<span data-ttu-id="80883-105">Registra um novo AppBar e especifica o identificador da mensagem que o sistema deve usar para enviar mensagens de notificação.</span><span class="sxs-lookup"><span data-stu-id="80883-105">Registers a new appbar and specifies the message identifier that the system should use to send it notification messages.</span></span> <span data-ttu-id="80883-106">Um AppBar deve enviar essa mensagem antes de enviar qualquer outra mensagem AppBar.</span><span class="sxs-lookup"><span data-stu-id="80883-106">An appbar should send this message before sending any other appbar messages.</span></span>


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="80883-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="80883-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80883-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="80883-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="80883-109">Um ponteiro para uma estrutura de [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que contém o identificador de janela e a identificação de mensagem do novo AppBar.</span><span class="sxs-lookup"><span data-stu-id="80883-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the new appbar's window handle and message identifier.</span></span> <span data-ttu-id="80883-110">Você deve especificar os membros **cbSize**, **HWND** e **uCallbackMessage** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="80883-110">You must specify the **cbSize**, **hWnd**, and **uCallbackMessage** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80883-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="80883-111">Return value</span></span>

<span data-ttu-id="80883-112">Retornará **true** se for bem-sucedido ou **false** se ocorrer um erro ou se o AppBar já estiver registrado.</span><span class="sxs-lookup"><span data-stu-id="80883-112">Returns **TRUE** if successful, or **FALSE** if an error occurs or if the appbar is already registered.</span></span>

## <a name="requirements"></a><span data-ttu-id="80883-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80883-113">Requirements</span></span>



| <span data-ttu-id="80883-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="80883-114">Requirement</span></span> | <span data-ttu-id="80883-115">Valor</span><span class="sxs-lookup"><span data-stu-id="80883-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="80883-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80883-116">Minimum supported client</span></span><br/> | <span data-ttu-id="80883-117">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="80883-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="80883-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="80883-118">Minimum supported server</span></span><br/> | <span data-ttu-id="80883-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="80883-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="80883-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="80883-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="80883-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="80883-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




