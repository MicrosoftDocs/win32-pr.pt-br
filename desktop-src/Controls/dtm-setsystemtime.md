---
title: Mensagem de DTM_SETSYSTEMTIME (commctrl. h)
description: Define a hora em um controle DTP (data and time Picker). Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetSystemTime DateTime.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- Controles de DTM_SETSYSTEMTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b2a3c625ad4ff02bed138a8086ca0da984de35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918921"
---
# <a name="dtm_setsystemtime-message"></a><span data-ttu-id="96fe7-105">DTM de \_ mensagens</span><span class="sxs-lookup"><span data-stu-id="96fe7-105">DTM\_SETSYSTEMTIME message</span></span>

<span data-ttu-id="96fe7-106">Define a hora em um controle DTP (data and time Picker).</span><span class="sxs-lookup"><span data-stu-id="96fe7-106">Sets the time in a date and time picker (DTP) control.</span></span> <span data-ttu-id="96fe7-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetSystemTime DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) .</span><span class="sxs-lookup"><span data-stu-id="96fe7-107">You can send this message explicitly or use the [**DateTime\_SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="96fe7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96fe7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96fe7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96fe7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96fe7-110">Um valor que especifica a ação que deve ser executada.</span><span class="sxs-lookup"><span data-stu-id="96fe7-110">A value specifying the action that should be performed.</span></span> <span data-ttu-id="96fe7-111">Esse valor deve ser definido como um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="96fe7-111">This value must be set to one of the following:</span></span>



| <span data-ttu-id="96fe7-112">Valor</span><span class="sxs-lookup"><span data-stu-id="96fe7-112">Value</span></span>                                                                                                                                             | <span data-ttu-id="96fe7-113">Significado</span><span class="sxs-lookup"><span data-stu-id="96fe7-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <span data-ttu-id="96fe7-114"><dt>**GDT \_ válida**</dt></span><span class="sxs-lookup"><span data-stu-id="96fe7-114"><dt>**GDT\_VALID**</dt></span></span> </dl> | <span data-ttu-id="96fe7-115">Defina o controle DTP de acordo com os dados dentro da estrutura que os *lParam* apontam.</span><span class="sxs-lookup"><span data-stu-id="96fe7-115">Set the DTP control according to the data within the structure that *lParam* points to.</span></span> <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <span data-ttu-id="96fe7-116"><dt>**GDT \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="96fe7-116"><dt>**GDT\_NONE**</dt></span></span> </dl>    | <span data-ttu-id="96fe7-117">Defina o controle DTP como "sem data" e desmarque sua caixa de seleção.</span><span class="sxs-lookup"><span data-stu-id="96fe7-117">Set the DTP control to "no date" and clear its check box.</span></span> <span data-ttu-id="96fe7-118">Quando esse sinalizador é especificado, *lParam* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="96fe7-118">When this flag is specified, *lParam* is ignored.</span></span> <span data-ttu-id="96fe7-119">Esse sinalizador se aplica somente a controles DTP que são definidos para o estilo [**DTS \_ All None**](date-and-time-picker-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="96fe7-119">This flag applies only to DTP controls that are set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="96fe7-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="96fe7-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="96fe7-121">Um ponteiro para uma estrutura [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que contém a hora do sistema usada para definir o controle DTP.</span><span class="sxs-lookup"><span data-stu-id="96fe7-121">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure containing the system time used to set the DTP control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96fe7-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="96fe7-122">Return value</span></span>

<span data-ttu-id="96fe7-123">Retornará zero se for bem-sucedido ou nenhum outro.</span><span class="sxs-lookup"><span data-stu-id="96fe7-123">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="96fe7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96fe7-124">Requirements</span></span>



| <span data-ttu-id="96fe7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="96fe7-125">Requirement</span></span> | <span data-ttu-id="96fe7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="96fe7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96fe7-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96fe7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="96fe7-128">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96fe7-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="96fe7-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96fe7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="96fe7-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="96fe7-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="96fe7-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96fe7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="96fe7-132"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="96fe7-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

