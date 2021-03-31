---
title: Mensagem de PGM_SETPOS (commctrl. h)
description: Define a posição de rolagem atual para o controle de pager. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetPos do pager.
ms.assetid: b882ea2d-9dab-4d36-9201-29522141f779
keywords:
- Controles de PGM_SETPOS de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_SETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5af4497e97a8263fa9ec8e454d367bb57e830c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644580"
---
# <a name="pgm_setpos-message"></a><span data-ttu-id="695ba-105">\_Mensagem SETPOS do PGM</span><span class="sxs-lookup"><span data-stu-id="695ba-105">PGM\_SETPOS message</span></span>

<span data-ttu-id="695ba-106">Define a posição de rolagem atual para o controle de pager.</span><span class="sxs-lookup"><span data-stu-id="695ba-106">Sets the current scroll position for the pager control.</span></span> <span data-ttu-id="695ba-107">Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetPos do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) .</span><span class="sxs-lookup"><span data-stu-id="695ba-107">You can send this message explicitly or use the [**Pager\_SetPos**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setpos) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="695ba-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="695ba-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="695ba-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="695ba-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="695ba-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="695ba-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="695ba-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="695ba-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="695ba-112">Valor do tipo **int** que contém a nova posição de rolagem, em pixels.</span><span class="sxs-lookup"><span data-stu-id="695ba-112">Value of type **int** that contains the new scroll position, in pixels.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="695ba-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="695ba-113">Return value</span></span>

<span data-ttu-id="695ba-114">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="695ba-114">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="695ba-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="695ba-115">Requirements</span></span>



| <span data-ttu-id="695ba-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="695ba-116">Requirement</span></span> | <span data-ttu-id="695ba-117">Valor</span><span class="sxs-lookup"><span data-stu-id="695ba-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="695ba-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="695ba-118">Minimum supported client</span></span><br/> | <span data-ttu-id="695ba-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="695ba-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="695ba-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="695ba-120">Minimum supported server</span></span><br/> | <span data-ttu-id="695ba-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="695ba-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="695ba-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="695ba-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="695ba-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="695ba-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





