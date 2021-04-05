---
title: LVN_ODCACHEHINT código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista virtual quando o conteúdo de sua área de exibição foi alterado.
ms.assetid: 2fac6a16-f65e-402f-9295-f2beb23db924
keywords:
- LVN_ODCACHEHINT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_ODCACHEHINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ad81b6ebb66a4fbe5c1a3b283175818b99e98
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919239"
---
# <a name="lvn_odcachehint-notification-code"></a><span data-ttu-id="417f5-104">Código de notificação do LVN \_ ODCACHEHINT</span><span class="sxs-lookup"><span data-stu-id="417f5-104">LVN\_ODCACHEHINT notification code</span></span>

<span data-ttu-id="417f5-105">Enviado por um controle de exibição de lista virtual quando o conteúdo de sua área de exibição foi alterado.</span><span class="sxs-lookup"><span data-stu-id="417f5-105">Sent by a virtual list-view control when the contents of its display area have changed.</span></span> <span data-ttu-id="417f5-106">Por exemplo, um controle de exibição de lista envia esse código de notificação quando o usuário rola a exibição do controle.</span><span class="sxs-lookup"><span data-stu-id="417f5-106">For example, a list-view control sends this notification code when the user scrolls the control's display.</span></span> <span data-ttu-id="417f5-107">O \_ código de notificação LVN ODCACHEHINT é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="417f5-107">The LVN\_ODCACHEHINT notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ODCACHEHINT

    pCachehint = (NMLVCACHEHINT *) lParam;
```



## <a name="parameters"></a><span data-ttu-id="417f5-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="417f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="417f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="417f5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="417f5-110">Ponteiro para uma estrutura [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) que contém informações sobre o intervalo de itens a serem armazenados em cache.</span><span class="sxs-lookup"><span data-stu-id="417f5-110">Pointer to an [**NMLVCACHEHINT**](/windows/win32/api/commctrl/ns-commctrl-nmlvcachehint) structure containing information about the range of items to be cached.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="417f5-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="417f5-111">Return value</span></span>

<span data-ttu-id="417f5-112">O aplicativo que recebe esse código de notificação deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="417f5-112">The application receiving this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="417f5-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="417f5-113">Remarks</span></span>

<span data-ttu-id="417f5-114">Manipular essa mensagem permite que o aplicativo atualize as informações do item mantidas no cache para que ele esteja prontamente disponível quando um código de notificação [LVN \_ GETDISPINFO](lvn-getdispinfo.md) é enviado.</span><span class="sxs-lookup"><span data-stu-id="417f5-114">Handling this message allows the application to update the item information held in cache so that it is readily available when an [LVN\_GETDISPINFO](lvn-getdispinfo.md) notification code is sent.</span></span>

<span data-ttu-id="417f5-115">Observe que esse código de notificação nem sempre é uma representação exata dos itens que serão solicitados por [LVN \_ GETDISPINFO](lvn-getdispinfo.md).</span><span class="sxs-lookup"><span data-stu-id="417f5-115">Note that this notification code is not always an exact representation of the items that will be requested by [LVN\_GETDISPINFO](lvn-getdispinfo.md).</span></span> <span data-ttu-id="417f5-116">Portanto, se o item solicitado não for armazenado em cache durante o tratamento de LVN \_ GETDISPINFO, o aplicativo deverá estar preparado para fornecer as informações solicitadas de uma fonte fora do cache.</span><span class="sxs-lookup"><span data-stu-id="417f5-116">Therefore, if the requested item is not cached while handling LVN\_GETDISPINFO, the application must be prepared to supply the requested information from a source outside the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="417f5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="417f5-117">Requirements</span></span>



| <span data-ttu-id="417f5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="417f5-118">Requirement</span></span> | <span data-ttu-id="417f5-119">Valor</span><span class="sxs-lookup"><span data-stu-id="417f5-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="417f5-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="417f5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="417f5-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="417f5-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="417f5-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="417f5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="417f5-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="417f5-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="417f5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="417f5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="417f5-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="417f5-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





