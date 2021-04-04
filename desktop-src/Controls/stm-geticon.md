---
title: Mensagem de STM_GETICON (WinUser. h)
description: Um aplicativo envia a \_ mensagem de GETICON STM para recuperar um identificador para o ícone associado a um controle estático que tem o \_ estilo de ícone SS.
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- Controles de STM_GETICON de mensagens do Windows
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085286"
---
# <a name="stm_geticon-message"></a><span data-ttu-id="a9f00-104">\_Mensagem de GETICON STM</span><span class="sxs-lookup"><span data-stu-id="a9f00-104">STM\_GETICON message</span></span>

<span data-ttu-id="a9f00-105">Um aplicativo envia a mensagem de **\_ GetIcon STM** para recuperar um identificador para o ícone associado a um controle estático que tem o \_ estilo de ícone SS.</span><span class="sxs-lookup"><span data-stu-id="a9f00-105">An application sends the **STM\_GETICON** message to retrieve a handle to the icon associated with a static control that has the SS\_ICON style.</span></span>

## <a name="parameters"></a><span data-ttu-id="a9f00-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9f00-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9f00-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a9f00-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9f00-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a9f00-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="a9f00-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9f00-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9f00-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a9f00-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9f00-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9f00-111">Return value</span></span>

<span data-ttu-id="a9f00-112">O valor de retorno é um identificador para o ícone, ou **NULL** se o controle estático não tiver nenhum ícone associado ou se ocorreu um erro.</span><span class="sxs-lookup"><span data-stu-id="a9f00-112">The return value is a handle to the icon, or **NULL** if either the static control has no associated icon or if an error occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9f00-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9f00-113">Requirements</span></span>



| <span data-ttu-id="a9f00-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9f00-114">Requirement</span></span> | <span data-ttu-id="a9f00-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a9f00-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f00-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9f00-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a9f00-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a9f00-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a9f00-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9f00-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a9f00-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a9f00-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a9f00-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9f00-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9f00-121"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9f00-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9f00-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9f00-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9f00-123">**\_ícone STM**</span><span class="sxs-lookup"><span data-stu-id="a9f00-123">**STM\_SETICON**</span></span>](stm-seticon.md)
</dt> </dl>

 

 





