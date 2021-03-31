---
title: Mensagem de DTM_GETSYSTEMTIME (commctrl. h)
description: Obtém a hora atualmente selecionada de um controle de data e hora (DTP) e o coloca em uma estrutura SYSTEMTIME especificada. Você pode enviar essa mensagem explicitamente ou usar a \_ macro DateTime GetSystemTime.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- Controles de DTM_GETSYSTEMTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085943"
---
# <a name="dtm_getsystemtime-message"></a><span data-ttu-id="6f661-105">DTM \_ mensagem GETsystemtime</span><span class="sxs-lookup"><span data-stu-id="6f661-105">DTM\_GETSYSTEMTIME message</span></span>

<span data-ttu-id="6f661-106">Obtém a hora atualmente selecionada de um controle de data e hora (DTP) e o coloca em uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) especificada.</span><span class="sxs-lookup"><span data-stu-id="6f661-106">Gets the currently selected time from a date and time picker (DTP) control and places it in a specified [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="6f661-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**DateTime \_ GetSystemTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) .</span><span class="sxs-lookup"><span data-stu-id="6f661-107">You can send this message explicitly or use the [**DateTime\_GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f661-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f661-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f661-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6f661-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6f661-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6f661-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6f661-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6f661-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6f661-112">Um ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="6f661-112">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="6f661-113">Se **DTM \_ GetSystemTime** retornar \_ a GDT válida, essa estrutura conterá a hora atualmente selecionada.</span><span class="sxs-lookup"><span data-stu-id="6f661-113">If **DTM\_GETSYSTEMTIME** returns GDT\_VALID, this structure will contain the currently selected time.</span></span> <span data-ttu-id="6f661-114">Caso contrário, ele não conterá informações válidas.</span><span class="sxs-lookup"><span data-stu-id="6f661-114">Otherwise, it will not contain valid information.</span></span> <span data-ttu-id="6f661-115">Esse parâmetro deve ser um ponteiro válido; Não pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6f661-115">This parameter must be a valid pointer; it cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f661-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f661-116">Return value</span></span>

<span data-ttu-id="6f661-117">Retorna \_ a GDT válida se as informações de tempo foram colocadas com êxito em *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6f661-117">Returns GDT\_VALID if the time information was successfully placed in *lParam*.</span></span> <span data-ttu-id="6f661-118">Retorna GDT \_ None se o controle foi definido como o estilo [**DTS não \_ None**](date-and-time-picker-control-styles.md) e a caixa de seleção controle não foi selecionada.</span><span class="sxs-lookup"><span data-stu-id="6f661-118">Returns GDT\_NONE if the control was set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style and the control check box was not selected.</span></span> <span data-ttu-id="6f661-119">Retorna \_ o erro da GDT se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="6f661-119">Returns GDT\_ERROR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f661-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f661-120">Requirements</span></span>



| <span data-ttu-id="6f661-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f661-121">Requirement</span></span> | <span data-ttu-id="6f661-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6f661-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6f661-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f661-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6f661-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6f661-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6f661-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f661-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6f661-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6f661-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6f661-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f661-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f661-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f661-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

