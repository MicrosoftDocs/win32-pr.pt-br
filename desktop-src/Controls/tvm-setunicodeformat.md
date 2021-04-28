---
title: Mensagem de TVM_SETUNICODEFORMAT (commctrl. h)
description: TVM_SETUNICODEFORMAT mensagem – define o sinalizador de formato de caractere Unicode para o controle.
ms.assetid: e4b58ae5-6217-4a2e-80e5-3ba9e578859a
keywords:
- Controles de TVM_SETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b49fcdd22cff0ac91885ef8f54d49922f9c677e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116544"
---
# <a name="tvm_setunicodeformat-message"></a><span data-ttu-id="bd6b2-104">\_Mensagem TVM SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="bd6b2-104">TVM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="bd6b2-105">Define o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="bd6b2-105">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="bd6b2-106">Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.</span><span class="sxs-lookup"><span data-stu-id="bd6b2-106">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span> <span data-ttu-id="bd6b2-107">Você pode enviar essa mensagem explicitamente ou usar a macro [**TreeView \_ SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat) .</span><span class="sxs-lookup"><span data-stu-id="bd6b2-107">You can send this message explicitly or use the [**TreeView\_SetUnicodeFormat**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_setunicodeformat) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd6b2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd6b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd6b2-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd6b2-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bd6b2-110">Determina o conjunto de caracteres que é usado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="bd6b2-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="bd6b2-111">Se esse valor for diferente de zero, o controle usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="bd6b2-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="bd6b2-112">Se esse valor for zero, o controle usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="bd6b2-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="bd6b2-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd6b2-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bd6b2-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bd6b2-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd6b2-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bd6b2-115">Return value</span></span>

<span data-ttu-id="bd6b2-116">Retorna o sinalizador de formato Unicode anterior para o controle.</span><span class="sxs-lookup"><span data-stu-id="bd6b2-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd6b2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd6b2-117">Remarks</span></span>

<span data-ttu-id="bd6b2-118">Consulte os comentários para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="bd6b2-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd6b2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd6b2-119">Requirements</span></span>



| <span data-ttu-id="bd6b2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd6b2-120">Requirement</span></span> | <span data-ttu-id="bd6b2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bd6b2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd6b2-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd6b2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bd6b2-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd6b2-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd6b2-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd6b2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bd6b2-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd6b2-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd6b2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd6b2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd6b2-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd6b2-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd6b2-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bd6b2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd6b2-129">**TVM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="bd6b2-129">**TVM\_GETUNICODEFORMAT**</span></span>](tvm-getunicodeformat.md)
</dt> </dl>

 

 





