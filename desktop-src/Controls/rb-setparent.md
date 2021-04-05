---
title: Mensagem de RB_SETPARENT (commctrl. h)
description: Define a janela pai do controle rebar.
ms.assetid: bb8036d4-cab8-4887-86c6-66460bdbe64b
keywords:
- Controles de RB_SETPARENT de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETPARENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6fafd054d9438b6aedd268620097847b42f3d60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824581"
---
# <a name="rb_setparent-message"></a><span data-ttu-id="b0f1a-104">Mensagem de "RB \_ SETpai"</span><span class="sxs-lookup"><span data-stu-id="b0f1a-104">RB\_SETPARENT message</span></span>

<span data-ttu-id="b0f1a-105">Define a janela pai do controle rebar.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-105">Sets a rebar control's parent window.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0f1a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0f1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f1a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0f1a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f1a-108">Identificador para a janela pai a ser definida.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-108">Handle to the parent window to be set.</span></span>

</dd> <dt>

<span data-ttu-id="b0f1a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0f1a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b0f1a-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0f1a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0f1a-111">Return value</span></span>

<span data-ttu-id="b0f1a-112">Retorna o identificador para a janela pai anterior ou **NULL** se não houver nenhum pai anterior.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-112">Returns the handle to the previous parent window, or **NULL** if there is no previous parent.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0f1a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0f1a-113">Remarks</span></span>

<span data-ttu-id="b0f1a-114">O controle rebar envia mensagens de notificação para a janela que você especifica com essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-114">The rebar control sends notification messages to the window you specify with this message.</span></span> <span data-ttu-id="b0f1a-115">Essa mensagem não altera realmente o pai do controle rebar.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-115">This message does not actually change the parent of the rebar control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f1a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0f1a-116">Requirements</span></span>



| <span data-ttu-id="b0f1a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0f1a-117">Requirement</span></span> | <span data-ttu-id="b0f1a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b0f1a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f1a-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0f1a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0f1a-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0f1a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0f1a-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0f1a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0f1a-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b0f1a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0f1a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0f1a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0f1a-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0f1a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





