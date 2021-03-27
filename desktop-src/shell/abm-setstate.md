---
description: Define os Estados de ocultar automaticamente e sempre visível da barra de tarefas do Windows.
title: Mensagem de ABM_SETSTATE (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967373"
---
# <a name="abm_setstate-message"></a><span data-ttu-id="14795-103">\_Mensagem ABM SETstate</span><span class="sxs-lookup"><span data-stu-id="14795-103">ABM\_SETSTATE message</span></span>

<span data-ttu-id="14795-104">Define os Estados de ocultar automaticamente e sempre visível da barra de tarefas do Windows.</span><span class="sxs-lookup"><span data-stu-id="14795-104">Sets the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="14795-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="14795-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14795-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="14795-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="14795-107">Um ponteiro para uma estrutura [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) .</span><span class="sxs-lookup"><span data-stu-id="14795-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="14795-108">Você deve especificar os membros **cbSize** e **HWND** ao enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="14795-108">You must specify the **cbSize** and **hWnd** members when sending this message.</span></span> <span data-ttu-id="14795-109">Os dados para o estado desejado são enviados no membro **lParam** usando um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="14795-109">Data for the desired state is sent in the **lParam** member using one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="14795-110"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="14795-110"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="14795-111">Ocultar automaticamente e sempre ativo-superior</span><span class="sxs-lookup"><span data-stu-id="14795-111">Autohide and always-on-top both off</span></span>

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span data-ttu-id="14795-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ALWAYSONTOP de ABS \_**</span><span class="sxs-lookup"><span data-stu-id="14795-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="14795-113">Sempre visível, ocultar automaticamente</span><span class="sxs-lookup"><span data-stu-id="14795-113">Always-on-top on, autohide off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span data-ttu-id="14795-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**AutoOcultar do ABS \_**</span><span class="sxs-lookup"><span data-stu-id="14795-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS\_AUTOHIDE**</span></span>


</dt> <dd>

<span data-ttu-id="14795-115">Ocultar automaticamente, sempre visível</span><span class="sxs-lookup"><span data-stu-id="14795-115">Autohide on, always-on-top off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span data-ttu-id="14795-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS \_ ocultar \| ABS \_ ALWAYSONTOP**</span><span class="sxs-lookup"><span data-stu-id="14795-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS\_AUTOHIDE \| ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="14795-117">Ocultar automaticamente e sempre em cima</span><span class="sxs-lookup"><span data-stu-id="14795-117">Autohide and always-on-top both on</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14795-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="14795-118">Return value</span></span>

<span data-ttu-id="14795-119">Sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="14795-119">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="14795-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="14795-120">Requirements</span></span>



| <span data-ttu-id="14795-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="14795-121">Requirement</span></span> | <span data-ttu-id="14795-122">Valor</span><span class="sxs-lookup"><span data-stu-id="14795-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="14795-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14795-123">Minimum supported client</span></span><br/> | <span data-ttu-id="14795-124">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="14795-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="14795-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="14795-125">Minimum supported server</span></span><br/> | <span data-ttu-id="14795-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="14795-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="14795-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="14795-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="14795-128"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="14795-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




