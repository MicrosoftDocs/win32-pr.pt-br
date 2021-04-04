---
title: Mensagem de LVM_CANCELEDITLABEL (commctrl. h)
description: Cancela uma operação de edição de texto de item.
ms.assetid: 73e9c922-3223-4c49-a33c-df7c09443ccc
keywords:
- Controles de LVM_CANCELEDITLABEL de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_CANCELEDITLABEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfed26fb3c38d91f7a5b07683079d29ecd4597d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085177"
---
# <a name="lvm_canceleditlabel-message"></a><span data-ttu-id="49d91-104">\_Mensagem CANCELEDITLABEL LVM</span><span class="sxs-lookup"><span data-stu-id="49d91-104">LVM\_CANCELEDITLABEL message</span></span>

<span data-ttu-id="49d91-105">Cancela uma operação de edição de texto de item.</span><span class="sxs-lookup"><span data-stu-id="49d91-105">Cancels an item text editing operation.</span></span>

## <a name="parameters"></a><span data-ttu-id="49d91-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49d91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49d91-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="49d91-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="49d91-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="49d91-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="49d91-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="49d91-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="49d91-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="49d91-110">Must be zero.</span></span></dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49d91-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="49d91-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="49d91-112">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="49d91-112">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="49d91-113">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="49d91-113">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

<span data-ttu-id="49d91-114">Essa mensagem faz com que uma notificação [LVN \_ ENDLABELEDIT](lvn-endlabeledit.md) seja enviada.</span><span class="sxs-lookup"><span data-stu-id="49d91-114">This message causes a an [LVN\_ENDLABELEDIT](lvn-endlabeledit.md) notification to be sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="49d91-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49d91-115">Requirements</span></span>



| <span data-ttu-id="49d91-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="49d91-116">Requirement</span></span> | <span data-ttu-id="49d91-117">Valor</span><span class="sxs-lookup"><span data-stu-id="49d91-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="49d91-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49d91-118">Minimum supported client</span></span><br/> | <span data-ttu-id="49d91-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49d91-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="49d91-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49d91-120">Minimum supported server</span></span><br/> | <span data-ttu-id="49d91-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="49d91-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="49d91-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="49d91-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="49d91-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="49d91-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





