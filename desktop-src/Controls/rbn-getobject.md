---
title: RBN_GETOBJECT código de notificação (commctrl. h)
description: Enviado por um controle rebar criado com o \_ estilo RBS REGISTERDROP quando um objeto é arrastado sobre uma banda no controle. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 057474c1-5f65-4290-973e-4366b760365a
keywords:
- RBN_GETOBJECT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a390bc5c5f74a577805ca8ae1128fbb24e6b10b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085921"
---
# <a name="rbn_getobject-notification-code"></a><span data-ttu-id="07cfc-105">\_Código de notificação GETobject do RBN</span><span class="sxs-lookup"><span data-stu-id="07cfc-105">RBN\_GETOBJECT notification code</span></span>

<span data-ttu-id="07cfc-106">Enviado por um controle rebar criado com o estilo [**RBS \_ REGISTERDROP**](rebar-control-styles.md) quando um objeto é arrastado sobre uma banda no controle.</span><span class="sxs-lookup"><span data-stu-id="07cfc-106">Sent by a rebar control created with the [**RBS\_REGISTERDROP**](rebar-control-styles.md) style when an object is dragged over a band in the control.</span></span> <span data-ttu-id="07cfc-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="07cfc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="07cfc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07cfc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07cfc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07cfc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07cfc-110">Ponteiro para uma estrutura [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) que contém informações sobre a faixa em que o objeto é arrastado e também recebe os dados fornecidos pelo aplicativo de recebimento em resposta a esse código de notificação.</span><span class="sxs-lookup"><span data-stu-id="07cfc-110">Pointer to an [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) structure that contains information about the band that the object is dragged over and also receives the data provided by the receiving application in response to this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07cfc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="07cfc-111">Return value</span></span>

<span data-ttu-id="07cfc-112">O valor de retorno para este código de notificação deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="07cfc-112">The return value for this notification code must be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="07cfc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="07cfc-113">Remarks</span></span>

<span data-ttu-id="07cfc-114">Para receber o \_ código de notificação GetObject do RBN, inicialize o OLE com uma chamada para [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) ou [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span><span class="sxs-lookup"><span data-stu-id="07cfc-114">To receive the RBN\_GETOBJECT notification code, initialize OLE with a call to [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) or [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span></span>

## <a name="requirements"></a><span data-ttu-id="07cfc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07cfc-115">Requirements</span></span>



| <span data-ttu-id="07cfc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="07cfc-116">Requirement</span></span> | <span data-ttu-id="07cfc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="07cfc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07cfc-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07cfc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="07cfc-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="07cfc-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07cfc-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="07cfc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="07cfc-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="07cfc-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07cfc-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="07cfc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="07cfc-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="07cfc-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

