---
title: CBEN_GETDISPINFO código de notificação (commctrl. h)
description: Enviado para recuperar informações de exibição sobre um item de retorno de chamada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: a181be28-0001-4953-8e59-77aff2dc40be
keywords:
- CBEN_GETDISPINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBEN_GETDISPINFO
- CBEN_GETDISPINFOA
- CBEN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3121d15b1482bdedf19a814a42e3309265909f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499243"
---
# <a name="cben_getdispinfo-notification-code"></a><span data-ttu-id="a2ecf-105">Código de notificação do CBEN \_ GETDISPINFO</span><span class="sxs-lookup"><span data-stu-id="a2ecf-105">CBEN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="a2ecf-106">Enviado para recuperar informações de exibição sobre um item de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="a2ecf-106">Sent to retrieve display information about a callback item.</span></span> <span data-ttu-id="a2ecf-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a2ecf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_GETDISPINFO

    pDispInfo = (PNMCOMBOBOXEX) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a2ecf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2ecf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ecf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a2ecf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a2ecf-110">Um ponteiro para uma estrutura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="a2ecf-110">A pointer to an [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ecf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a2ecf-111">Return value</span></span>

<span data-ttu-id="a2ecf-112">O aplicativo que processa esse código de notificação deve retornar zero.</span><span class="sxs-lookup"><span data-stu-id="a2ecf-112">The application processing this notification code must return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2ecf-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2ecf-113">Remarks</span></span>

<span data-ttu-id="a2ecf-114">A estrutura [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) contém uma estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) .</span><span class="sxs-lookup"><span data-stu-id="a2ecf-114">The [**NMCOMBOBOXEX**](/windows/desktop/api/Commctrl/ns-commctrl-nmcomboboxexa) structure contains a [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure.</span></span> <span data-ttu-id="a2ecf-115">O membro **Mask** especifica as informações que estão sendo solicitadas pelo controle.</span><span class="sxs-lookup"><span data-stu-id="a2ecf-115">The **mask** member specifies the information being requested by the control.</span></span>

<span data-ttu-id="a2ecf-116">Preencha os membros apropriados da estrutura para retornar as informações solicitadas ao controle.</span><span class="sxs-lookup"><span data-stu-id="a2ecf-116">Fill the appropriate members of the structure to return the requested information to the control.</span></span> <span data-ttu-id="a2ecf-117">Se o manipulador de mensagens definir o membro **Mask** da estrutura [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) para CBEIF \_ di \_ SETITEM, o controle armazenará as informações e não a solicitará novamente.</span><span class="sxs-lookup"><span data-stu-id="a2ecf-117">If your message handler sets the **mask** member of the [**COMBOBOXEXITEM**](/windows/win32/api/commctrl/ns-commctrl-comboboxexitema) structure to CBEIF\_DI\_SETITEM, the control stores the information and will not request it again.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ecf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2ecf-118">Requirements</span></span>



| <span data-ttu-id="a2ecf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2ecf-119">Requirement</span></span> | <span data-ttu-id="a2ecf-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a2ecf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ecf-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2ecf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ecf-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2ecf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a2ecf-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a2ecf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ecf-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2ecf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2ecf-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2ecf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2ecf-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ecf-126"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a2ecf-127">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="a2ecf-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a2ecf-128">**CBEN \_ GETDISPINFOW** (Unicode) e **CBEN \_ GETDISPINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a2ecf-128">**CBEN\_GETDISPINFOW** (Unicode) and **CBEN\_GETDISPINFOA** (ANSI)</span></span><br/>         |



 

 





