---
title: Mensagem de DTM_SETFORMAT (commctrl. h)
description: Define a exibição de um controle DTP (data e hora) com base em uma determinada cadeia de caracteres de formato. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetFormat de DateTime.
ms.assetid: a89fa3ad-9894-4c52-ab56-fb62208e39b3
keywords:
- Controles de DTM_SETFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_SETFORMAT
- DTM_SETFORMATA
- DTM_SETFORMATW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17669ed2e1ed23e3b090b77701bbe05d23a5ccb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009569"
---
# <a name="dtm_setformat-message"></a><span data-ttu-id="ea79a-105">\_Mensagem DTM SETformat</span><span class="sxs-lookup"><span data-stu-id="ea79a-105">DTM\_SETFORMAT message</span></span>

<span data-ttu-id="ea79a-106">Define a exibição de um controle DTP (data e hora) com base em uma determinada cadeia de caracteres de formato.</span><span class="sxs-lookup"><span data-stu-id="ea79a-106">Sets the display of a date and time picker (DTP) control based on a given format string.</span></span> <span data-ttu-id="ea79a-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetFormat de DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) .</span><span class="sxs-lookup"><span data-stu-id="ea79a-107">You can send this message explicitly or use the [**DateTime\_SetFormat**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea79a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea79a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea79a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea79a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ea79a-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ea79a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ea79a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea79a-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea79a-112">Um ponteiro para uma [cadeia de caracteres de formato](date-and-time-picker-controls.md) terminada em zero que define a exibição desejada.</span><span class="sxs-lookup"><span data-stu-id="ea79a-112">A pointer to a zero-terminated [format string](date-and-time-picker-controls.md) that defines the desired display.</span></span> <span data-ttu-id="ea79a-113">Definir esse parâmetro como **NULL** redefinirá o controle para a cadeia de caracteres de formato padrão para o estilo atual.</span><span class="sxs-lookup"><span data-stu-id="ea79a-113">Setting this parameter to **NULL** will reset the control to the default format string for the current style.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea79a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea79a-114">Return value</span></span>

<span data-ttu-id="ea79a-115">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="ea79a-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea79a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea79a-116">Remarks</span></span>

<span data-ttu-id="ea79a-117">É aceitável incluir caracteres extras na cadeia de caracteres de formato para produzir uma exibição mais rica.</span><span class="sxs-lookup"><span data-stu-id="ea79a-117">It is acceptable to include extra characters within the format string to produce a more rich display.</span></span> <span data-ttu-id="ea79a-118">No entanto, todos os caracteres não formatados devem ser colocados entre aspas simples.</span><span class="sxs-lookup"><span data-stu-id="ea79a-118">However, any nonformat characters must be enclosed within single quotes.</span></span> <span data-ttu-id="ea79a-119">Por exemplo, a cadeia de caracteres de formato "' hoje é: ' hh ': ' M' ' s ddddMMMdd ', ' YYY ' produziria uma saída como" hoje é: 04:22:31 terça-feira, 23 de março, 1996 ".</span><span class="sxs-lookup"><span data-stu-id="ea79a-119">For example, the format string "'Today is: 'hh':'m':'s ddddMMMdd', 'yyy" would produce output like "Today is: 04:22:31 Tuesday Mar 23, 1996".</span></span>

> [!Note]  
> <span data-ttu-id="ea79a-120">Um controle DTP controla as alterações de localidade quando está usando a cadeia de caracteres de formato padrão.</span><span class="sxs-lookup"><span data-stu-id="ea79a-120">A DTP control tracks locale changes when it is using the default format string.</span></span> <span data-ttu-id="ea79a-121">Se você definir uma cadeia de caracteres de formato personalizado, ela não será atualizada em resposta às alterações de localidade.</span><span class="sxs-lookup"><span data-stu-id="ea79a-121">If you set a custom format string, it will not be updated in response to locale changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea79a-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea79a-122">Requirements</span></span>



| <span data-ttu-id="ea79a-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea79a-123">Requirement</span></span> | <span data-ttu-id="ea79a-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ea79a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea79a-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea79a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ea79a-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea79a-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea79a-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea79a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ea79a-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea79a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea79a-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea79a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea79a-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea79a-130"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="ea79a-131">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="ea79a-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ea79a-132">**DTM \_ SETFORMATW** (Unicode) e **DTM \_ setformaa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="ea79a-132">**DTM\_SETFORMATW** (Unicode) and **DTM\_SETFORMATA** (ANSI)</span></span><br/>               |



 

 





