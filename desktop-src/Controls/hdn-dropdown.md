---
title: HDN_DROPDOWN código de notificação (commctrl. h)
description: Enviado por um controle de cabeçalho para seu pai quando a seta suspensa no controle de cabeçalho é clicada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: cacf5cb9-0593-42ff-868d-b098481f565f
keywords:
- HDN_DROPDOWN de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- HDN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c0ae7f2e2ee31feab1d8a2293913ac875a03718
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824866"
---
# <a name="hdn_dropdown-notification-code"></a><span data-ttu-id="6c42e-105">\_Código de notificação da lista suspensa HDN</span><span class="sxs-lookup"><span data-stu-id="6c42e-105">HDN\_DROPDOWN notification code</span></span>

<span data-ttu-id="6c42e-106">Enviado por um controle de cabeçalho para seu pai quando a seta suspensa no controle de cabeçalho é clicada.</span><span class="sxs-lookup"><span data-stu-id="6c42e-106">Sent by a header control to its parent when the drop-down arrow on the header control is clicked.</span></span> <span data-ttu-id="6c42e-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="6c42e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_DROPDOWN
        
    pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6c42e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6c42e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c42e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6c42e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6c42e-110">Um ponteiro para uma estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) que contém informações sobre o controle de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6c42e-110">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure that contains information on the header control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c42e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6c42e-111">Return value</span></span>

<span data-ttu-id="6c42e-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="6c42e-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c42e-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c42e-113">Remarks</span></span>

<span data-ttu-id="6c42e-114">O exemplo na seção sintaxe mostra como o receptor de notificação converte **lParam** para recuperar a estrutura [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) .</span><span class="sxs-lookup"><span data-stu-id="6c42e-114">The example in the Syntax section shows how the notification receiver casts **LPARAM** to retrieve the [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure.</span></span> <span data-ttu-id="6c42e-115">**WParam** contém a ID do controle que envia essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="6c42e-115">**WPARAM** contains the ID of the control that sends this message.</span></span>

<span data-ttu-id="6c42e-116">Essa mensagem será enviada somente se o estilo HDF \_ SPLITBUTTON estiver definido no item de cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="6c42e-116">This message is sent only if style HDF\_SPLITBUTTON is set on the header item.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c42e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c42e-117">Requirements</span></span>



| <span data-ttu-id="6c42e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c42e-118">Requirement</span></span> | <span data-ttu-id="6c42e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6c42e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c42e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c42e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c42e-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c42e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6c42e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6c42e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c42e-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c42e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6c42e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6c42e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c42e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c42e-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





