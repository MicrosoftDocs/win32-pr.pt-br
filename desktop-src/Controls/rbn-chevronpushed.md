---
title: RBN_CHEVRONPUSHED código de notificação (commctrl. h)
description: Enviado por um controle rebar quando uma divisa é enviada por push. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 58aa2c9d-8ab6-46ee-b32f-5c04fb7afa84
keywords:
- RBN_CHEVRONPUSHED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_CHEVRONPUSHED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab28d992b6d4a617b7aa7ee144eb50aef3b0e834
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009348"
---
# <a name="rbn_chevronpushed-notification-code"></a><span data-ttu-id="c7e92-105">Código de notificação do RBN \_ CHEVRONPUSHED</span><span class="sxs-lookup"><span data-stu-id="c7e92-105">RBN\_CHEVRONPUSHED notification code</span></span>

<span data-ttu-id="c7e92-106">Enviado por um controle rebar quando uma divisa é enviada por push.</span><span class="sxs-lookup"><span data-stu-id="c7e92-106">Sent by a rebar control when a chevron is pushed.</span></span> <span data-ttu-id="c7e92-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="c7e92-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_CHEVRONPUSHED

    lpnm = (NMREBARCHEVRON) lParam;
```



## <a name="parameters"></a><span data-ttu-id="c7e92-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7e92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7e92-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7e92-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7e92-110">Ponteiro para a estrutura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) da banda.</span><span class="sxs-lookup"><span data-stu-id="c7e92-110">Pointer to the band's [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7e92-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c7e92-111">Return value</span></span>

<span data-ttu-id="c7e92-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="c7e92-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7e92-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7e92-113">Remarks</span></span>

<span data-ttu-id="c7e92-114">Quando um aplicativo recebe esse código de notificação, ele é responsável por exibir um menu pop-up com itens para cada ferramenta oculta.</span><span class="sxs-lookup"><span data-stu-id="c7e92-114">When an application receives this notification code, it is responsible for displaying a popup menu with items for each hidden tool.</span></span> <span data-ttu-id="c7e92-115">Use o membro **RC** da estrutura [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) para localizar a posição correta para o menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="c7e92-115">Use the **rc** member of the [**NMREBARCHEVRON**](/windows/win32/api/commctrl/ns-commctrl-nmrebarchevron) structure to find the correct position for the popup menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7e92-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7e92-116">Requirements</span></span>



| <span data-ttu-id="c7e92-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7e92-117">Requirement</span></span> | <span data-ttu-id="c7e92-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c7e92-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7e92-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7e92-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c7e92-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7e92-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7e92-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7e92-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c7e92-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7e92-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7e92-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7e92-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7e92-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7e92-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





