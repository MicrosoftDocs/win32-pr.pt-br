---
title: PGN_CALCSIZE código de notificação (commctrl. h)
description: Enviado por um controle de pager para obter as dimensões roláveis da janela contida.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- PGN_CALCSIZE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee6de1c45402f8bdc154f9f10be00140d7c766c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644579"
---
# <a name="pgn_calcsize-notification-code"></a><span data-ttu-id="3fd2c-104">Código de notificação do PGN \_ CALCSIZE</span><span class="sxs-lookup"><span data-stu-id="3fd2c-104">PGN\_CALCSIZE notification code</span></span>

<span data-ttu-id="3fd2c-105">Enviado por um controle de pager para obter as dimensões roláveis da janela contida.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-105">Sent by a pager control to obtain the scrollable dimensions of the contained window.</span></span> <span data-ttu-id="3fd2c-106">Essas dimensões são usadas pelo controle de pager para determinar o tamanho rolável da janela contida.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-106">These dimensions are used by the pager control to determine the scrollable size of the contained window.</span></span> <span data-ttu-id="3fd2c-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="3fd2c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3fd2c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fd2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fd2c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3fd2c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3fd2c-110">Ponteiro para uma estrutura [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) que contém e recebe informações sobre o código de notificação.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-110">Pointer to an [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="3fd2c-111">O membro **dwFlag** dessa estrutura indica qual dimensão está sendo calculada.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-111">The **dwFlag** member of this structure indicates which dimension is being calculated.</span></span> <span data-ttu-id="3fd2c-112">Dependendo do valor de **dwFlag**, você deve posicionar a dimensão desejada no membro **iWidth** ou **iHeight** dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-112">Depending on the value of **dwFlag**, you should place the desired dimension in the **iWidth** or **iHeight** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fd2c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3fd2c-113">Return value</span></span>

<span data-ttu-id="3fd2c-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fd2c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fd2c-115">Requirements</span></span>



| <span data-ttu-id="3fd2c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fd2c-116">Requirement</span></span> | <span data-ttu-id="3fd2c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="3fd2c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3fd2c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fd2c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3fd2c-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3fd2c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3fd2c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fd2c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3fd2c-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3fd2c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3fd2c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fd2c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fd2c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fd2c-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





