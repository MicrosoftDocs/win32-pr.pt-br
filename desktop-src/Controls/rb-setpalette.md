---
title: Mensagem de RB_SETPALETTE (commctrl. h)
description: Define a paleta atual do controle rebar.
ms.assetid: 85f0726a-21fd-41b3-aa52-6a0a0c1947fa
keywords:
- Controles de RB_SETPALETTE de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_SETPALETTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7ee47985c05bcd8a857620e7fe501bddf53bdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918778"
---
# <a name="rb_setpalette-message"></a><span data-ttu-id="b4a04-104">\_Mensagem de SETpalette de RB</span><span class="sxs-lookup"><span data-stu-id="b4a04-104">RB\_SETPALETTE message</span></span>

<span data-ttu-id="b4a04-105">Define a paleta atual do controle rebar.</span><span class="sxs-lookup"><span data-stu-id="b4a04-105">Sets the rebar control's current palette.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4a04-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4a04-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4a04-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4a04-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b4a04-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b4a04-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b4a04-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b4a04-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b4a04-110">Um **HPALETTE** que especifica a nova paleta que será usada pelo controle rebar.</span><span class="sxs-lookup"><span data-stu-id="b4a04-110">An **HPALETTE** that specifies the new palette that the rebar control will use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4a04-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4a04-111">Return value</span></span>

<span data-ttu-id="b4a04-112">Retorna um **HPALETTE** que especifica a paleta anterior do controle rebar.</span><span class="sxs-lookup"><span data-stu-id="b4a04-112">Returns an **HPALETTE** that specifies the rebar control's previous palette.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4a04-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4a04-113">Remarks</span></span>

<span data-ttu-id="b4a04-114">É responsabilidade do aplicativo enviar essa mensagem para excluir o **HPALETTE** passado nesta mensagem (consulte [**DeleteId**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span><span class="sxs-lookup"><span data-stu-id="b4a04-114">It is the responsibility of the application sending this message to delete the **HPALETTE** passed in this message (see [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)).</span></span> <span data-ttu-id="b4a04-115">O controle rebar não excluirá um conjunto de **HPALETTE** com essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="b4a04-115">The rebar control will not delete an **HPALETTE** set with this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4a04-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4a04-116">Requirements</span></span>



| <span data-ttu-id="b4a04-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4a04-117">Requirement</span></span> | <span data-ttu-id="b4a04-118">Valor</span><span class="sxs-lookup"><span data-stu-id="b4a04-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a04-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4a04-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b4a04-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4a04-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b4a04-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b4a04-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b4a04-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b4a04-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4a04-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4a04-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4a04-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4a04-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4a04-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4a04-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4a04-126">**GetPalette RB \_**</span><span class="sxs-lookup"><span data-stu-id="b4a04-126">**RB\_GETPALETTE**</span></span>](rb-getpalette.md)
</dt> </dl>

 

