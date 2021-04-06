---
title: Mensagem de DTM_GETMCFONT (commctrl. h)
description: Obtém a fonte em que o controle de calendário do mês filho do controle de data e hora (DTP) está sendo usado no momento. Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime GetMonthCalFont.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- Controles de DTM_GETMCFONT de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824692"
---
# <a name="dtm_getmcfont-message"></a><span data-ttu-id="5dc8d-105">\_Mensagem DTM GETMCFONT</span><span class="sxs-lookup"><span data-stu-id="5dc8d-105">DTM\_GETMCFONT message</span></span>

<span data-ttu-id="5dc8d-106">Obtém a fonte em que o controle de calendário do mês filho do controle de data e hora (DTP) está sendo usado no momento.</span><span class="sxs-lookup"><span data-stu-id="5dc8d-106">Gets the font that the date and time picker (DTP) control's child month calendar control is currently using.</span></span> <span data-ttu-id="5dc8d-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) .</span><span class="sxs-lookup"><span data-stu-id="5dc8d-107">You can send this message explicitly or use the [**DateTime\_GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5dc8d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5dc8d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dc8d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5dc8d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5dc8d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5dc8d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5dc8d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5dc8d-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5dc8d-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5dc8d-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5dc8d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5dc8d-113">Return value</span></span>

<span data-ttu-id="5dc8d-114">Retorna um valor HFONT que é o identificador para a fonte atual.</span><span class="sxs-lookup"><span data-stu-id="5dc8d-114">Returns an HFONT value that is the handle to the current font.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dc8d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5dc8d-115">Requirements</span></span>



| <span data-ttu-id="5dc8d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5dc8d-116">Requirement</span></span> | <span data-ttu-id="5dc8d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5dc8d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5dc8d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dc8d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5dc8d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5dc8d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5dc8d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5dc8d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5dc8d-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5dc8d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5dc8d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5dc8d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5dc8d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5dc8d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





