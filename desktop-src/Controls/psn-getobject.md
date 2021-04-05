---
title: PSN_GETOBJECT código de notificação (Prsht. h)
description: Enviado por uma folha de propriedades para solicitar um objeto de destino de soltar quando o cursor passa sobre um dos botões do controle de guia. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0a039cf97dee1d1f1168894bb167c06de10d38d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009072"
---
# <a name="psn_getobject-notification-code"></a><span data-ttu-id="9f428-105">\_Código de notificação GETobject do PSN</span><span class="sxs-lookup"><span data-stu-id="9f428-105">PSN\_GETOBJECT notification code</span></span>

<span data-ttu-id="9f428-106">Enviado por uma folha de propriedades para solicitar um objeto de destino de soltar quando o cursor passa sobre um dos botões do controle de guia.</span><span class="sxs-lookup"><span data-stu-id="9f428-106">Sent by a property sheet to request a drop target object when the cursor passes over one of the tab control's buttons.</span></span> <span data-ttu-id="9f428-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9f428-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9f428-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f428-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f428-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f428-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f428-110">Ponteiro para uma estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que, na entrada, contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="9f428-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that, on entry, contains information about the notification code.</span></span> <span data-ttu-id="9f428-111">Se esse código de notificação for processado, você deverá inserir informações de objeto nessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="9f428-111">If this notification code is processed, you must insert object information into this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f428-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f428-112">Return value</span></span>

<span data-ttu-id="9f428-113">O aplicativo que processa esse código de notificação deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="9f428-113">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f428-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f428-114">Remarks</span></span>

<span data-ttu-id="9f428-115">Para fornecer um objeto, um aplicativo deve definir valores em alguns membros da estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="9f428-115">To provide an object, an application must set values in some members of the [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure at *lParam*.</span></span> <span data-ttu-id="9f428-116">O membro **pObject** deve ser definido como um ponteiro de objeto válido e o membro **HRESULT** deve ser definido como um sinalizador de êxito.</span><span class="sxs-lookup"><span data-stu-id="9f428-116">The **pObject** member must be set to a valid object pointer, and the **hResult** member must be set to a success flag.</span></span> <span data-ttu-id="9f428-117">Para obedecer aos padrões de Component Object Model (COM), sempre aumente a contagem de referência do objeto ao fornecer um ponteiro de objeto.</span><span class="sxs-lookup"><span data-stu-id="9f428-117">To comply with Component Object Model (COM) standards, always increment the object's reference count when providing an object pointer.</span></span>

<span data-ttu-id="9f428-118">Se um aplicativo não fornecer um objeto, ele deverá definir **pObject** como **nulo** e **HRESULT** como um sinalizador de falha.</span><span class="sxs-lookup"><span data-stu-id="9f428-118">If an application does not provide an object, it must set **pObject** to **NULL** and **hResult** to a failure flag.</span></span>

> [!Note]  
> <span data-ttu-id="9f428-119">Não há suporte para este código de notificação ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="9f428-119">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9f428-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f428-120">Requirements</span></span>



| <span data-ttu-id="9f428-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f428-121">Requirement</span></span> | <span data-ttu-id="9f428-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9f428-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9f428-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f428-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9f428-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f428-124">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9f428-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9f428-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9f428-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f428-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9f428-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f428-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f428-128"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f428-128"><dt>Prsht.h</dt></span></span> </dl> |



 

 





