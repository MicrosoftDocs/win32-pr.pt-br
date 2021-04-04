---
title: TBN_GETOBJECT código de notificação (commctrl. h)
description: Enviado por um controle ToolBar que usa o \_ estilo TBSTYLE REGISTERDROP para solicitar um objeto de destino drop quando o ponteiro passa sobre um de seus botões. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- TBN_GETOBJECT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085153"
---
# <a name="tbn_getobject-notification-code"></a><span data-ttu-id="c1b96-105">\_Código de notificação GETobject do tbn</span><span class="sxs-lookup"><span data-stu-id="c1b96-105">TBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="c1b96-106">Enviado por um controle ToolBar que usa o estilo [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) para solicitar um objeto de destino drop quando o ponteiro passa sobre um de seus botões.</span><span class="sxs-lookup"><span data-stu-id="c1b96-106">Sent by a toolbar control that uses the [**TBSTYLE\_REGISTERDROP**](toolbar-control-and-button-styles.md) style to request a drop target object when the pointer passes over one of its buttons.</span></span> <span data-ttu-id="c1b96-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c1b96-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c1b96-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c1b96-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1b96-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1b96-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1b96-110">Ponteiro para uma estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contém informações sobre o botão passado pelo ponteiro e recebe dados que o aplicativo fornece em resposta a esse código de notificação.</span><span class="sxs-lookup"><span data-stu-id="c1b96-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the button that the pointer passed over and receives data the application provides in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1b96-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c1b96-111">Return value</span></span>

<span data-ttu-id="c1b96-112">O aplicativo que processa esse código de notificação deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="c1b96-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1b96-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1b96-113">Remarks</span></span>

<span data-ttu-id="c1b96-114">Para fornecer um objeto, um aplicativo deve definir valores em alguns membros da estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="c1b96-114">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="c1b96-115">O membro **pObject** deve ser definido como um ponteiro de objeto válido e o membro **HRESULT** deve ser definido como um sinalizador de êxito.</span><span class="sxs-lookup"><span data-stu-id="c1b96-115">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="c1b96-116">Para obedecer aos padrões de Component Object Model (COM), sempre aumente a contagem de referência do objeto ao fornecer um ponteiro de objeto.</span><span class="sxs-lookup"><span data-stu-id="c1b96-116">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="c1b96-117">Se um aplicativo não fornecer um objeto, ele deverá definir **pObject** como **nulo** e **HRESULT** como um sinalizador de falha.</span><span class="sxs-lookup"><span data-stu-id="c1b96-117">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b96-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1b96-118">Requirements</span></span>



| <span data-ttu-id="c1b96-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1b96-119">Requirement</span></span> | <span data-ttu-id="c1b96-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c1b96-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b96-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1b96-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c1b96-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1b96-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1b96-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1b96-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c1b96-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c1b96-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1b96-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1b96-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1b96-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1b96-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





