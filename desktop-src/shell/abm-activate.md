---
description: Notifica o sistema de que um AppBar foi ativado. Um AppBar deve chamar essa mensagem em resposta à mensagem de \_ ativação do WM.
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: Mensagem de ABM_ACTIVATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090037"
---
# <a name="abm_activate-message"></a><span data-ttu-id="cce9c-104">ABM \_ Ativar mensagem</span><span class="sxs-lookup"><span data-stu-id="cce9c-104">ABM\_ACTIVATE message</span></span>

<span data-ttu-id="cce9c-105">Notifica o sistema de que um AppBar foi ativado.</span><span class="sxs-lookup"><span data-stu-id="cce9c-105">Notifies the system that an appbar has been activated.</span></span> <span data-ttu-id="cce9c-106">Um AppBar deve chamar essa mensagem em resposta à mensagem [**de \_ ativação do WM**](/windows/desktop/inputdev/wm-activate) .</span><span class="sxs-lookup"><span data-stu-id="cce9c-106">An appbar should call this message in response to the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message.</span></span>


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a><span data-ttu-id="cce9c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cce9c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cce9c-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="cce9c-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="cce9c-109">Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) que identifica o AppBar a ser ativado.</span><span class="sxs-lookup"><span data-stu-id="cce9c-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="cce9c-110">Você deve especificar os membros **cbSize** e **HWND** ao enviar esta mensagem; todos os outros membros são ignorados.</span><span class="sxs-lookup"><span data-stu-id="cce9c-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cce9c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cce9c-111">Return value</span></span>

<span data-ttu-id="cce9c-112">Sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="cce9c-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cce9c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cce9c-113">Remarks</span></span>

<span data-ttu-id="cce9c-114">Essa mensagem será ignorada se o membro **HWND** da estrutura apontado por *pabd* identificar uma AutoOcultar AppBar.</span><span class="sxs-lookup"><span data-stu-id="cce9c-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span> <span data-ttu-id="cce9c-115">O sistema define automaticamente a ordem z para o AutoOcultar appbars.</span><span class="sxs-lookup"><span data-stu-id="cce9c-115">The system automatically sets the z-order for autohide appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="cce9c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cce9c-116">Requirements</span></span>



| <span data-ttu-id="cce9c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="cce9c-117">Requirement</span></span> | <span data-ttu-id="cce9c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cce9c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cce9c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cce9c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cce9c-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cce9c-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cce9c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cce9c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cce9c-122">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cce9c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cce9c-123">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cce9c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cce9c-124"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="cce9c-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

