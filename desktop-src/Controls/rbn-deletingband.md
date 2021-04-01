---
title: RBN_DELETINGBAND código de notificação (commctrl. h)
description: Enviado por um controle rebar quando uma banda está prestes a ser excluída. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 92840cb1-375e-4c37-bde4-7ba02a1ff4f1
keywords:
- RBN_DELETINGBAND de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_DELETINGBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf810fd8800d7774a0dbf9a65cdf08c2d53d92ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918776"
---
# <a name="rbn_deletingband-notification-code"></a><span data-ttu-id="44ab3-105">Código de notificação do RBN \_ DELETINGBAND</span><span class="sxs-lookup"><span data-stu-id="44ab3-105">RBN\_DELETINGBAND notification code</span></span>

<span data-ttu-id="44ab3-106">Enviado por um controle rebar quando uma banda está prestes a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="44ab3-106">Sent by a rebar control when a band is about to be deleted.</span></span> <span data-ttu-id="44ab3-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="44ab3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_DELETINGBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="44ab3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44ab3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44ab3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="44ab3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="44ab3-110">Ponteiro para uma estrutura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contém informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="44ab3-110">Pointer to an [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44ab3-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="44ab3-111">Return value</span></span>

<span data-ttu-id="44ab3-112">O valor de retorno para essa notificação não é usado.</span><span class="sxs-lookup"><span data-stu-id="44ab3-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="44ab3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44ab3-113">Requirements</span></span>



| <span data-ttu-id="44ab3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="44ab3-114">Requirement</span></span> | <span data-ttu-id="44ab3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="44ab3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="44ab3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44ab3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="44ab3-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="44ab3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="44ab3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44ab3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="44ab3-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="44ab3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="44ab3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="44ab3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="44ab3-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="44ab3-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





