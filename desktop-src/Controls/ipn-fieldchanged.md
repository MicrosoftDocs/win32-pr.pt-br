---
title: IPN_FIELDCHANGED código de notificação (commctrl. h)
description: Enviado quando o usuário altera um campo no controle ou move de um campo para outro. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: f9ca6435-1715-458e-8d0e-475920ed75bd
keywords:
- IPN_FIELDCHANGED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- IPN_FIELDCHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e283d42d0aba3c237db51fe492a34ec93e8eb73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009615"
---
# <a name="ipn_fieldchanged-notification-code"></a><span data-ttu-id="e0786-105">\_Código de notificação do campo IPN</span><span class="sxs-lookup"><span data-stu-id="e0786-105">IPN\_FIELDCHANGED notification code</span></span>

<span data-ttu-id="e0786-106">Enviado quando o usuário altera um campo no controle ou move de um campo para outro.</span><span class="sxs-lookup"><span data-stu-id="e0786-106">Sent when the user changes a field in the control or moves from one field to another.</span></span> <span data-ttu-id="e0786-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="e0786-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
IPN_FIELDCHANGED

    lpnmipa = (LPNMIPADDRESS) lParam;
```



## <a name="parameters"></a><span data-ttu-id="e0786-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0786-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0786-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0786-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0786-110">Um ponteiro para uma estrutura [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) que contém informações sobre o endereço alterado.</span><span class="sxs-lookup"><span data-stu-id="e0786-110">A pointer to an [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) structure that contains information about the changed address.</span></span> <span data-ttu-id="e0786-111">O membro **iValue** dessa estrutura conterá o valor inserido, mesmo que esteja fora do intervalo do campo.</span><span class="sxs-lookup"><span data-stu-id="e0786-111">The **iValue** member of this structure will contain the entered value, even if it is out of the range of the field.</span></span> <span data-ttu-id="e0786-112">Você pode modificar esse membro para qualquer valor que esteja dentro do intervalo do campo em resposta a este código de notificação.</span><span class="sxs-lookup"><span data-stu-id="e0786-112">You can modify this member to any value that is within the range for the field in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0786-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0786-113">Return value</span></span>

<span data-ttu-id="e0786-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="e0786-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0786-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0786-115">Remarks</span></span>

<span data-ttu-id="e0786-116">Esse código de notificação não é enviado em resposta a uma mensagem de [**\_ SetAddress IPM**](ipm-setaddress.md) .</span><span class="sxs-lookup"><span data-stu-id="e0786-116">This notification code is not sent in response to a [**IPM\_SETADDRESS**](ipm-setaddress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0786-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0786-117">Requirements</span></span>



| <span data-ttu-id="e0786-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0786-118">Requirement</span></span> | <span data-ttu-id="e0786-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e0786-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e0786-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0786-120">Minimum supported client</span></span><br/> | <span data-ttu-id="e0786-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0786-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e0786-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0786-122">Minimum supported server</span></span><br/> | <span data-ttu-id="e0786-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e0786-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e0786-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0786-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0786-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0786-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





