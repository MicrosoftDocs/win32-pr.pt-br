---
title: Mensagem de CB_SHOWDROPDOWN (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de lista suspensa CB para mostrar ou ocultar a caixa de listagem de uma caixa de combinação que tem o \_ estilo de lista suspensa CBS ou CBS \_ .
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- Controles de CB_SHOWDROPDOWN de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb66e9a0ecf3b6680fce9aca7f680fd6e6fd13e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086197"
---
# <a name="cb_showdropdown-message"></a><span data-ttu-id="a1d0b-104">\_Mensagem de lista suspensa CB</span><span class="sxs-lookup"><span data-stu-id="a1d0b-104">CB\_SHOWDROPDOWN message</span></span>

<span data-ttu-id="a1d0b-105">Um aplicativo envia uma mensagem de lista **\_ suspensa CB** para mostrar ou ocultar a caixa de listagem de uma caixa de combinação que tem o estilo de [**\_ lista suspensa CBS**](combo-box-styles.md) ou [**CBS \_**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a1d0b-105">An application sends a **CB\_SHOWDROPDOWN** message to show or hide the list box of a combo box that has the [**CBS\_DROPDOWN**](combo-box-styles.md) or [**CBS\_DROPDOWNLIST**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="a1d0b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1d0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1d0b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a1d0b-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1d0b-108">Um **bool** que especifica se a caixa de listagem suspensa deve ser exibida ou ocultada.</span><span class="sxs-lookup"><span data-stu-id="a1d0b-108">A **BOOL** that specifies whether the drop-down list box is to be shown or hidden.</span></span> <span data-ttu-id="a1d0b-109">Um valor **true** mostra a caixa de listagem; um valor de **false** oculta-o.</span><span class="sxs-lookup"><span data-stu-id="a1d0b-109">A value of **TRUE** shows the list box; a value of **FALSE** hides it.</span></span>

</dd> <dt>

<span data-ttu-id="a1d0b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1d0b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1d0b-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="a1d0b-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1d0b-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a1d0b-112">Return value</span></span>

<span data-ttu-id="a1d0b-113">O valor de retorno é sempre **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="a1d0b-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1d0b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1d0b-114">Remarks</span></span>

<span data-ttu-id="a1d0b-115">Esta mensagem não tem nenhum efeito em uma caixa de combinação criada com o estilo [**\_ simples do CBS**](combo-box-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a1d0b-115">This message has no effect on a combo box created with the [**CBS\_SIMPLE**](combo-box-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1d0b-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1d0b-116">Requirements</span></span>



| <span data-ttu-id="a1d0b-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1d0b-117">Requirement</span></span> | <span data-ttu-id="a1d0b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a1d0b-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1d0b-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1d0b-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a1d0b-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1d0b-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a1d0b-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1d0b-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a1d0b-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a1d0b-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a1d0b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1d0b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1d0b-124"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1d0b-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1d0b-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1d0b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1d0b-126">**CB \_ GETremovestate**</span><span class="sxs-lookup"><span data-stu-id="a1d0b-126">**CB\_GETDROPPEDSTATE**</span></span>](cb-getdroppedstate.md)
</dt> </dl>

 

 





