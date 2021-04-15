---
title: Mensagem de DTM_GETDATETIMEPICKERINFO (commctrl. h)
description: Obtém informações sobre um controle do seletor de data e hora (DTP).
ms.assetid: 04847b68-ac45-4b28-8f62-2cd68ffe48d4
keywords:
- Controles de DTM_GETDATETIMEPICKERINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETDATETIMEPICKERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398a2543caa6d7104339fb8debd83fcee3ac71f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454709"
---
# <a name="dtm_getdatetimepickerinfo-message"></a><span data-ttu-id="ba63d-104">\_Mensagem DTM GETDATETIMEPICKERINFO</span><span class="sxs-lookup"><span data-stu-id="ba63d-104">DTM\_GETDATETIMEPICKERINFO message</span></span>

<span data-ttu-id="ba63d-105">Obtém informações sobre um controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="ba63d-105">Gets information on a date and time picker (DTP) control.</span></span>

## <a name="parameters"></a><span data-ttu-id="ba63d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba63d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba63d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ba63d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ba63d-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ba63d-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ba63d-109">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba63d-109">*lParam* \[in\]</span></span>
</dt> <dd> <span data-ttu-id="ba63d-110">Um ponteiro para <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> para receber as informações.</span><span class="sxs-lookup"><span data-stu-id="ba63d-110">A pointer to <a href="/windows/win32/api/commctrl/ns-commctrl-datetimepickerinfo">**DATETIMEPICKERINFO**</a> to receive the information.</span></span> <span data-ttu-id="ba63d-111">O chamador é responsável por alocar a memória para essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="ba63d-111">The caller is responsible for allocating the memory for this structure.</span></span> <span data-ttu-id="ba63d-112">Defina o membro **cbSize** da estrutura como sizeof (DATETIMEPICKERINFO) antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="ba63d-112">Set the **cbSize** member of the structure to sizeof(DATETIMEPICKERINFO) before sending this message.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba63d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba63d-113">Return value</span></span>

<span data-ttu-id="ba63d-114">O valor de retorno é ignorado.</span><span class="sxs-lookup"><span data-stu-id="ba63d-114">Return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba63d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba63d-115">Requirements</span></span>



| <span data-ttu-id="ba63d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba63d-116">Requirement</span></span> | <span data-ttu-id="ba63d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ba63d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba63d-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba63d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ba63d-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba63d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ba63d-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba63d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ba63d-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba63d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ba63d-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba63d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba63d-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba63d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





