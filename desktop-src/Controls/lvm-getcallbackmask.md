---
title: Mensagem de LVM_GETCALLBACKMASK (commctrl. h)
description: Obtém a máscara de retorno de chamada para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetCallbackMask do ListView.
ms.assetid: fb05593d-14b9-4e53-acb3-d5ac61e517ec
keywords:
- Controles de LVM_GETCALLBACKMASK de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETCALLBACKMASK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68438b748f5260bb7cc6e43702442aa4cbe3a84e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454633"
---
# <a name="lvm_getcallbackmask-message"></a><span data-ttu-id="5d525-105">\_Mensagem GETCALLBACKMASK LVM</span><span class="sxs-lookup"><span data-stu-id="5d525-105">LVM\_GETCALLBACKMASK message</span></span>

<span data-ttu-id="5d525-106">Obtém a máscara de retorno de chamada para um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="5d525-106">Gets the callback mask for a list-view control.</span></span> <span data-ttu-id="5d525-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetCallbackMask do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) .</span><span class="sxs-lookup"><span data-stu-id="5d525-107">You can send this message explicitly or by using the [**ListView\_GetCallbackMask**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcallbackmask) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d525-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5d525-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d525-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d525-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5d525-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5d525-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5d525-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d525-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5d525-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5d525-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d525-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5d525-113">Return value</span></span>

<span data-ttu-id="5d525-114">Retorna a máscara de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="5d525-114">Returns the callback mask.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d525-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d525-115">Requirements</span></span>



| <span data-ttu-id="5d525-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d525-116">Requirement</span></span> | <span data-ttu-id="5d525-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5d525-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d525-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d525-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5d525-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d525-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d525-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5d525-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5d525-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5d525-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d525-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5d525-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d525-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d525-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





