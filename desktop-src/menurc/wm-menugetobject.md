---
title: Mensagem de WM_MENUGETOBJECT (WinUser. h)
description: Enviado ao proprietário de um menu de arrastar e soltar quando o cursor do mouse entra em um item de menu ou se move do centro do item para a parte superior ou inferior do item.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499837"
---
# <a name="wm_menugetobject-message"></a><span data-ttu-id="11147-104">Mensagem do WM \_ MENUGETOBJECT</span><span class="sxs-lookup"><span data-stu-id="11147-104">WM\_MENUGETOBJECT message</span></span>

<span data-ttu-id="11147-105">Enviado ao proprietário de um menu de arrastar e soltar quando o cursor do mouse entra em um item de menu ou se move do centro do item para a parte superior ou inferior do item.</span><span class="sxs-lookup"><span data-stu-id="11147-105">Sent to the owner of a drag-and-drop menu when the mouse cursor enters a menu item or moves from the center of the item to the top or bottom of the item.</span></span>


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a><span data-ttu-id="11147-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11147-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11147-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="11147-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11147-108">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="11147-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="11147-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11147-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11147-110">Um ponteiro para uma estrutura [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) .</span><span class="sxs-lookup"><span data-stu-id="11147-110">A pointer to a [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11147-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="11147-111">Return value</span></span>

<span data-ttu-id="11147-112">O aplicativo deve retornar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="11147-112">The application should return one of the following values.</span></span>



| <span data-ttu-id="11147-113">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="11147-113">Return code/value</span></span>                                                                                                                                                | <span data-ttu-id="11147-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="11147-114">Description</span></span>                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="11147-115"><dt>**MNGO \_ NOERROR**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="11147-115"><dt>**MNGO\_NOERROR**</dt> <dt>0x00000001</dt></span></span> </dl>     | <span data-ttu-id="11147-116">Um ponteiro de interface foi retornado no membro **pvObj** de [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)</span><span class="sxs-lookup"><span data-stu-id="11147-116">An interface pointer was returned in the **pvObj** member of [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)</span></span><br/> |
| <dl> <span data-ttu-id="11147-117"><dt>**MNGO \_ Nointerface**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="11147-117"><dt>**MNGO\_NOINTERFACE**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="11147-118">Não há suporte para a interface.</span><span class="sxs-lookup"><span data-stu-id="11147-118">The interface is not supported.</span></span><br/>                                                                             |



 

## <a name="requirements"></a><span data-ttu-id="11147-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11147-119">Requirements</span></span>



| <span data-ttu-id="11147-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="11147-120">Requirement</span></span> | <span data-ttu-id="11147-121">Valor</span><span class="sxs-lookup"><span data-stu-id="11147-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11147-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11147-122">Minimum supported client</span></span><br/> | <span data-ttu-id="11147-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="11147-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="11147-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11147-124">Minimum supported server</span></span><br/> | <span data-ttu-id="11147-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="11147-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="11147-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="11147-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="11147-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="11147-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11147-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="11147-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11147-129">Visão geral dos menus</span><span class="sxs-lookup"><span data-stu-id="11147-129">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

 





