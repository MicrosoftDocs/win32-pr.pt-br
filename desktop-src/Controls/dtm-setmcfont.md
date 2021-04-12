---
title: Mensagem de DTM_SETMCFONT (commctrl. h)
description: Define a fonte a ser usada pelo controle de calendário do mês filho do controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime SetMonthCalFont.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- Controles de DTM_SETMCFONT de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455551"
---
# <a name="dtm_setmcfont-message"></a><span data-ttu-id="27f8a-105">\_Mensagem DTM SETMCFONT</span><span class="sxs-lookup"><span data-stu-id="27f8a-105">DTM\_SETMCFONT message</span></span>

<span data-ttu-id="27f8a-106">Define a fonte a ser usada pelo controle de calendário do mês filho do controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="27f8a-106">Sets the font to be used by the date and time picker (DTP) control's child month calendar control.</span></span> <span data-ttu-id="27f8a-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .</span><span class="sxs-lookup"><span data-stu-id="27f8a-107">You can send this message explicitly or use the [**DateTime\_SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="27f8a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="27f8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27f8a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="27f8a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27f8a-110">Um identificador para a fonte que será definida.</span><span class="sxs-lookup"><span data-stu-id="27f8a-110">A handle to the font that will be set.</span></span>

</dd> <dt>

<span data-ttu-id="27f8a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="27f8a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="27f8a-112">Especifica se o controle deve ser redesenhado imediatamente após a configuração da fonte.</span><span class="sxs-lookup"><span data-stu-id="27f8a-112">Specifies whether the control should be redrawn immediately upon setting the font.</span></span> <span data-ttu-id="27f8a-113">Definir esse parâmetro como **true** faz com que o controle seja redesenhado.</span><span class="sxs-lookup"><span data-stu-id="27f8a-113">Setting this parameter to **TRUE** causes the control to redraw itself.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27f8a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="27f8a-114">Return value</span></span>

<span data-ttu-id="27f8a-115">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="27f8a-115">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="27f8a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27f8a-116">Requirements</span></span>



| <span data-ttu-id="27f8a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="27f8a-117">Requirement</span></span> | <span data-ttu-id="27f8a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="27f8a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27f8a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27f8a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="27f8a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27f8a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="27f8a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="27f8a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="27f8a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="27f8a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="27f8a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="27f8a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="27f8a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="27f8a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





