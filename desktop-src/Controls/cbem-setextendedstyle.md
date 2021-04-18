---
title: Mensagem de CBEM_SETEXTENDEDSTYLE (commctrl. h)
description: Define os estilos estendidos dentro de um controle ComboBoxEx.
ms.assetid: 00848bd0-5a2f-4bfb-ae1f-ee3aa88ac57a
keywords:
- Controles de CBEM_SETEXTENDEDSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- CBEM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0a60518d2f6130c2c89e379125308fc2e647c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752946"
---
# <a name="cbem_setextendedstyle-message"></a><span data-ttu-id="b03a9-104">\_Mensagem CBEM SETextendedattribute</span><span class="sxs-lookup"><span data-stu-id="b03a9-104">CBEM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="b03a9-105">Define os estilos estendidos dentro de um controle ComboBoxEx.</span><span class="sxs-lookup"><span data-stu-id="b03a9-105">Sets extended styles within a ComboBoxEx control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b03a9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b03a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b03a9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b03a9-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b03a9-108">Um valor **DWORD** que indica quais estilos em *lParam* devem ser afetados.</span><span class="sxs-lookup"><span data-stu-id="b03a9-108">A **DWORD** value that indicates which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="b03a9-109">Somente os estilos estendidos em *wParam* serão alterados.</span><span class="sxs-lookup"><span data-stu-id="b03a9-109">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="b03a9-110">Se esse parâmetro for zero, todos os estilos em *lParam* serão afetados.</span><span class="sxs-lookup"><span data-stu-id="b03a9-110">If this parameter is zero, then all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="b03a9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b03a9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b03a9-112">Um valor **DWORD** que contém os [estilos estendidos do controle ComboBoxEx](comboboxex-control-extended-styles.md) a serem definidos para o controle.</span><span class="sxs-lookup"><span data-stu-id="b03a9-112">A **DWORD** value that contains the [ComboBoxEx Control Extended Styles](comboboxex-control-extended-styles.md) to set for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b03a9-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b03a9-113">Return value</span></span>

<span data-ttu-id="b03a9-114">Retorna um valor **DWORD** que contém os estilos estendidos usados anteriormente para o controle.</span><span class="sxs-lookup"><span data-stu-id="b03a9-114">Returns a **DWORD** value that contains the extended styles previously used for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="b03a9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="b03a9-115">Remarks</span></span>

<span data-ttu-id="b03a9-116">*wParam* permite modificar um ou mais estilos estendidos sem precisar recuperar os estilos existentes primeiro.</span><span class="sxs-lookup"><span data-stu-id="b03a9-116">*wParam* enables you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="b03a9-117">Por exemplo, se você passar [**CBES \_ ex \_ NOEDITIMAGE**](comboboxex-control-extended-styles.md) para *wParam* e 0 para *lParam*, o estilo **CBES \_ ex \_ NOEDITIMAGE** será limpo, mas todos os outros estilos permanecerão os mesmos.</span><span class="sxs-lookup"><span data-stu-id="b03a9-117">For example, if you pass [**CBES\_EX\_NOEDITIMAGE**](comboboxex-control-extended-styles.md) for *wParam* and 0 for *lParam*, the **CBES\_EX\_NOEDITIMAGE** style will be cleared, but all other styles will remain the same.</span></span>

<span data-ttu-id="b03a9-118">Se você tentar definir um estilo estendido para um controle ComboBoxEx criado com o [**estilo \_ simples do CBS**](combo-box-styles.md) , ele poderá não ser redesenhado corretamente.</span><span class="sxs-lookup"><span data-stu-id="b03a9-118">If you try to set an extended style for a ComboBoxEx control created with the [**CBS\_SIMPLE**](combo-box-styles.md) style, it may not repaint properly.</span></span>

## <a name="requirements"></a><span data-ttu-id="b03a9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b03a9-119">Requirements</span></span>



| <span data-ttu-id="b03a9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b03a9-120">Requirement</span></span> | <span data-ttu-id="b03a9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="b03a9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b03a9-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b03a9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b03a9-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b03a9-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b03a9-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b03a9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b03a9-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b03a9-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b03a9-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b03a9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b03a9-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b03a9-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





