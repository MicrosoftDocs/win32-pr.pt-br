---
title: Mensagem de TCM_GETCURSEL (commctrl. h)
description: Determina a guia selecionada no momento em um controle guia. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Getcurseal TabCtrl.
ms.assetid: 1caa7fad-da5a-4b26-8e78-12110c126691
keywords:
- Controles de TCM_GETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- TCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3103931e29d150412192a745f8dde7681cff0e94
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105749670"
---
# <a name="tcm_getcursel-message"></a><span data-ttu-id="6a459-105">Mensagem do TCM \_ GETcurseal</span><span class="sxs-lookup"><span data-stu-id="6a459-105">TCM\_GETCURSEL message</span></span>

<span data-ttu-id="6a459-106">Determina a guia selecionada no momento em um controle guia.</span><span class="sxs-lookup"><span data-stu-id="6a459-106">Determines the currently selected tab in a tab control.</span></span> <span data-ttu-id="6a459-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ getcurseal TabCtrl**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .</span><span class="sxs-lookup"><span data-stu-id="6a459-107">You can send this message explicitly or by using the [**TabCtrl\_GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6a459-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6a459-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a459-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6a459-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6a459-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6a459-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6a459-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a459-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6a459-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6a459-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a459-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6a459-113">Return value</span></span>

<span data-ttu-id="6a459-114">Retorna o índice da guia selecionada, se for bem-sucedido, ou-1 se nenhuma guia for selecionada.</span><span class="sxs-lookup"><span data-stu-id="6a459-114">Returns the index of the selected tab if successful, or -1 if no tab is selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a459-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a459-115">Requirements</span></span>



| <span data-ttu-id="6a459-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a459-116">Requirement</span></span> | <span data-ttu-id="6a459-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6a459-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a459-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a459-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6a459-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6a459-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a459-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a459-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6a459-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6a459-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a459-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a459-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a459-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a459-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





