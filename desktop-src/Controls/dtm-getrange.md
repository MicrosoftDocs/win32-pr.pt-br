---
title: Mensagem de DTM_GETRANGE (commctrl. h)
description: Obtém os tempos de sistema mínimo e máximo permitidos no momento para um controle do seletor de data e hora (DTP). Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetRange de DateTime.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- Controles de DTM_GETRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455552"
---
# <a name="dtm_getrange-message"></a><span data-ttu-id="a7dbf-105">DTM \_ mensagem GETrange</span><span class="sxs-lookup"><span data-stu-id="a7dbf-105">DTM\_GETRANGE message</span></span>

<span data-ttu-id="a7dbf-106">Obtém os tempos de sistema mínimo e máximo permitidos no momento para um controle do seletor de data e hora (DTP).</span><span class="sxs-lookup"><span data-stu-id="a7dbf-106">Gets the current minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="a7dbf-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetRange de DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) .</span><span class="sxs-lookup"><span data-stu-id="a7dbf-107">You can send this message explicitly or use the [**DateTime\_GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="a7dbf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7dbf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7dbf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a7dbf-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a7dbf-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a7dbf-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="a7dbf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a7dbf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a7dbf-112">Um ponteiro para uma matriz de dois elementos de estruturas [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="a7dbf-112">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7dbf-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7dbf-113">Return value</span></span>

<span data-ttu-id="a7dbf-114">Retorna um valor **DWORD** que é uma combinação de GDTR \_ min ou GDTR \_ Max.</span><span class="sxs-lookup"><span data-stu-id="a7dbf-114">Returns a **DWORD** value that is a combination of GDTR\_MIN or GDTR\_MAX.</span></span> <span data-ttu-id="a7dbf-115">O primeiro elemento da matriz [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contém o tempo mínimo permitido se GDTR \_ min estiver definido.</span><span class="sxs-lookup"><span data-stu-id="a7dbf-115">The first element of the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) array contains the minimum allowable time if GDTR\_MIN is set.</span></span> <span data-ttu-id="a7dbf-116">O segundo elemento da matriz **SYSTEMTIME** contém o tempo máximo permitido se GDTR \_ Max estiver definido.</span><span class="sxs-lookup"><span data-stu-id="a7dbf-116">The second element of the **SYSTEMTIME** array contains the maximum allowable time if GDTR\_MAX is set.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7dbf-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7dbf-117">Remarks</span></span>

<span data-ttu-id="a7dbf-118">O seletor de data e hora exibe apenas datas/horários que se enquadram no intervalo especificado, impedindo que o usuário selecione uma data e hora que esteja fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="a7dbf-118">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="a7dbf-119">Se a mensagem [**DTM \_ SetSystemTime**](dtm-setsystemtime.md) especificar uma data e hora que esteja fora do intervalo, ela falhará.</span><span class="sxs-lookup"><span data-stu-id="a7dbf-119">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7dbf-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7dbf-120">Requirements</span></span>



| <span data-ttu-id="a7dbf-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7dbf-121">Requirement</span></span> | <span data-ttu-id="a7dbf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a7dbf-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a7dbf-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7dbf-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a7dbf-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a7dbf-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a7dbf-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7dbf-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a7dbf-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a7dbf-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a7dbf-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7dbf-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7dbf-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7dbf-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

