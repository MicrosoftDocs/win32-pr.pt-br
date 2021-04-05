---
title: Mensagem de LVM_GETFOOTERRECT (commctrl. h)
description: Recupera as coordenadas do rodapé de um controle de exibição de lista. Envie essa mensagem explicitamente ou usando a \_ macro GetFooterRect do ListView.
ms.assetid: f8816f35-c1d2-4072-81d3-0a9a3df53d64
keywords:
- Controles de LVM_GETFOOTERRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31df3a1b7b29e5ad9191da9e990e04daec99e948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085170"
---
# <a name="lvm_getfooterrect-message"></a><span data-ttu-id="652bf-105">\_Mensagem GETFOOTERRECT LVM</span><span class="sxs-lookup"><span data-stu-id="652bf-105">LVM\_GETFOOTERRECT message</span></span>

<span data-ttu-id="652bf-106">Recupera as coordenadas do rodapé de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="652bf-106">Retrieves the coordinates of the footer for a list-view control.</span></span> <span data-ttu-id="652bf-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetFooterRect do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) .</span><span class="sxs-lookup"><span data-stu-id="652bf-107">Send this message explicitly or by using the [**ListView\_GetFooterRect**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="652bf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="652bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="652bf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="652bf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="652bf-110">Não usado.</span><span class="sxs-lookup"><span data-stu-id="652bf-110">Not used.</span></span> <span data-ttu-id="652bf-111">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="652bf-111">Must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="652bf-112">*lParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="652bf-112">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="652bf-113">Um ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) para receber as coordenadas.</span><span class="sxs-lookup"><span data-stu-id="652bf-113">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure to receive the coordinates.</span></span> <span data-ttu-id="652bf-114">O processo de chamada é responsável por alocar essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="652bf-114">The calling process is responsible for allocating this structure.</span></span> <span data-ttu-id="652bf-115">As coordenadas recebidas são expressas como coordenadas do cliente.</span><span class="sxs-lookup"><span data-stu-id="652bf-115">The coordinates received are expressed as client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="652bf-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="652bf-116">Return value</span></span>

<span data-ttu-id="652bf-117">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="652bf-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="652bf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="652bf-118">Requirements</span></span>



| <span data-ttu-id="652bf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="652bf-119">Requirement</span></span> | <span data-ttu-id="652bf-120">Valor</span><span class="sxs-lookup"><span data-stu-id="652bf-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="652bf-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="652bf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="652bf-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="652bf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="652bf-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="652bf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="652bf-124">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="652bf-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="652bf-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="652bf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="652bf-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="652bf-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

