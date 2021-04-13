---
title: LVN_GETINFOTIP código de notificação (commctrl. h)
description: Enviado por um ícone grande exibir lista-exibir controle que tem o \_ \_ estilo estendido LVS ex INFOTIP.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b4552456a575e2f03e02b2bfb78f7fcc1d8ca1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499868"
---
# <a name="lvn_getinfotip-notification-code"></a><span data-ttu-id="9bbb2-104">Código de notificação do LVN \_ GETINFOTIP</span><span class="sxs-lookup"><span data-stu-id="9bbb2-104">LVN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="9bbb2-105">Enviado por um ícone grande exibir lista-exibir controle que tem o estilo estendido [**LVS \_ ex \_ INFOTIP**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9bbb2-105">Sent by a large icon view list-view control that has the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="9bbb2-106">Esse código de notificação é enviado quando o controle de exibição de lista está solicitando informações de texto adicionais a serem exibidas em uma dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="9bbb2-106">This notification code is sent when the list-view control is requesting additional text information to be displayed in a tooltip.</span></span> <span data-ttu-id="9bbb2-107">Ele é enviado na forma de uma mensagem [**de \_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9bbb2-107">It is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a><span data-ttu-id="9bbb2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bbb2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bbb2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9bbb2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9bbb2-110">Ponteiro para uma estrutura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) que contém informações sobre este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="9bbb2-110">Pointer to an [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bbb2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9bbb2-111">Return value</span></span>

<span data-ttu-id="9bbb2-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="9bbb2-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="9bbb2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bbb2-113">Remarks</span></span>

<span data-ttu-id="9bbb2-114">Esse código de notificação é enviado somente por controles de exibição de lista que têm o estilo estendido [**LVS \_ ex \_ INFOTIP**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9bbb2-114">This notification code is only sent by list-view controls that have the [**LVS\_EX\_INFOTIP**](extended-list-view-styles.md) extended style.</span></span> <span data-ttu-id="9bbb2-115">O \_ código de notificação LVN GETINFOTIP é enviado somente para o subitem 0.</span><span class="sxs-lookup"><span data-stu-id="9bbb2-115">The LVN\_GETINFOTIP notification code is sent only for subitem 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bbb2-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bbb2-116">Requirements</span></span>



| <span data-ttu-id="9bbb2-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bbb2-117">Requirement</span></span> | <span data-ttu-id="9bbb2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9bbb2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9bbb2-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bbb2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9bbb2-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9bbb2-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9bbb2-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bbb2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9bbb2-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9bbb2-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9bbb2-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9bbb2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bbb2-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bbb2-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="9bbb2-125">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="9bbb2-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="9bbb2-126">**LVN \_ GETINFOTIPW** (Unicode) e **LVN \_ GETINFOTIPA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="9bbb2-126">**LVN\_GETINFOTIPW** (Unicode) and **LVN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





