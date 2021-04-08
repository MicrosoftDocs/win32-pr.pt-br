---
title: MCN_SELECT código de notificação (commctrl. h)
description: Enviado por um controle de calendário mensal quando o usuário faz uma seleção de data explícita dentro de um controle de calendário mensal. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 3cabb4b2-9422-4190-85d3-ab6593891e3d
keywords:
- MCN_SELECT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- MCN_SELECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252133267b9c552542df17ed73caa8c34a69641
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008999"
---
# <a name="mcn_select-notification-code"></a><span data-ttu-id="50acb-105">MCN \_ selecionar código de notificação</span><span class="sxs-lookup"><span data-stu-id="50acb-105">MCN\_SELECT notification code</span></span>

<span data-ttu-id="50acb-106">Enviado por um controle de calendário mensal quando o usuário faz uma seleção de data explícita dentro de um controle de calendário mensal.</span><span class="sxs-lookup"><span data-stu-id="50acb-106">Sent by a month calendar control when the user makes an explicit date selection within a month calendar control.</span></span> <span data-ttu-id="50acb-107">Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="50acb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_SELECT

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="50acb-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50acb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50acb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="50acb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="50acb-110">Ponteiro para uma estrutura [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) que contém informações sobre o intervalo de datas selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="50acb-110">Pointer to an [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) structure that contains information about the currently selected date range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50acb-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="50acb-111">Return value</span></span>

<span data-ttu-id="50acb-112">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="50acb-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="50acb-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="50acb-113">Remarks</span></span>

<span data-ttu-id="50acb-114">O código de notificação **MCN \_ Select** é semelhante a [**MCN \_ SELCHANGE**](mcn-selchange.md), mas **MCN \_ Select** é enviada somente em resposta às seleções de data explícitas de um usuário.</span><span class="sxs-lookup"><span data-stu-id="50acb-114">The **MCN\_SELECT** notification code is similar to [**MCN\_SELCHANGE**](mcn-selchange.md), but **MCN\_SELECT** is sent only in response to a user's explicit date selections.</span></span> <span data-ttu-id="50acb-115">**MCN \_ SELCHANGE** aplica-se a qualquer alteração de seleção.</span><span class="sxs-lookup"><span data-stu-id="50acb-115">**MCN\_SELCHANGE** applies to any selection change.</span></span>

## <a name="requirements"></a><span data-ttu-id="50acb-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="50acb-116">Requirements</span></span>



| <span data-ttu-id="50acb-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="50acb-117">Requirement</span></span> | <span data-ttu-id="50acb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="50acb-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="50acb-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50acb-119">Minimum supported client</span></span><br/> | <span data-ttu-id="50acb-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="50acb-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="50acb-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="50acb-121">Minimum supported server</span></span><br/> | <span data-ttu-id="50acb-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="50acb-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="50acb-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="50acb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="50acb-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="50acb-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





