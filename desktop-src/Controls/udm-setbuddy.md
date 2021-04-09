---
title: Mensagem de UDM_SETBUDDY (commctrl. h)
description: Define a janela Buddy para um controle de cima para baixo.
ms.assetid: 66e35acc-95f6-4bc5-b654-690abf2188ba
keywords:
- Controles de UDM_SETBUDDY de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_SETBUDDY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0e8bd57727d730c67fe09a52c0bedf121eac982
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085917"
---
# <a name="udm_setbuddy-message"></a><span data-ttu-id="b978c-104">\_Mensagem UDM SETbuddy</span><span class="sxs-lookup"><span data-stu-id="b978c-104">UDM\_SETBUDDY message</span></span>

<span data-ttu-id="b978c-105">Define a janela Buddy para um controle de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="b978c-105">Sets the buddy window for an up-down control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b978c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b978c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b978c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b978c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b978c-108">Manipule a nova janela Buddy.</span><span class="sxs-lookup"><span data-stu-id="b978c-108">Handle to the new buddy window.</span></span>

</dd> <dt>

<span data-ttu-id="b978c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b978c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b978c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b978c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b978c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b978c-111">Return value</span></span>

<span data-ttu-id="b978c-112">O valor de retorno é o identificador para a janela do Buddy anterior.</span><span class="sxs-lookup"><span data-stu-id="b978c-112">The return value is the handle to the previous buddy window.</span></span>

## <a name="requirements"></a><span data-ttu-id="b978c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b978c-113">Requirements</span></span>



| <span data-ttu-id="b978c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b978c-114">Requirement</span></span> | <span data-ttu-id="b978c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b978c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b978c-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b978c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b978c-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b978c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b978c-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b978c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b978c-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b978c-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b978c-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b978c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b978c-121"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b978c-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





