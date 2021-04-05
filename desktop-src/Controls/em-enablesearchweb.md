---
title: Mensagem de EM_ENABLESEARCHWEB (CommCtrl. h)
description: Habilita ou desabilita o recurso "Pesquisar na Web" e a entrada do menu de contexto.
ms.assetid: 9393f03e-0719-458b-8122-616df738c417
keywords:
- Controles de EM_ENABLESEARCHWEB de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_ENABLESEARCHWEB
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb2638476027f0a7fe2bb1a66a3a00a330e28c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918707"
---
# <a name="em_enablesearchweb-message"></a><span data-ttu-id="1855c-104">\_Mensagem em ENABLESEARCHWEB</span><span class="sxs-lookup"><span data-stu-id="1855c-104">EM\_ENABLESEARCHWEB message</span></span>

<span data-ttu-id="1855c-105">Habilita ou desabilita o recurso "Pesquisar na Web" e a entrada do menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="1855c-105">Enables or disables the "Search the web" feature and context menu entry.</span></span>

## <a name="parameters"></a><span data-ttu-id="1855c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1855c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1855c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1855c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1855c-108">Um valor **true** indica que o recurso "Pesquisar na Web" está habilitado e um valor **false** indica que ele está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1855c-108">A value of **TRUE** indicates the "Search the web" feature is enabled, and a value of **FALSE** indicates it is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="1855c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1855c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1855c-110">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="1855c-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1855c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1855c-111">Return value</span></span>

<span data-ttu-id="1855c-112">Essa mensagem não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1855c-112">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1855c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="1855c-113">Remarks</span></span>

<span data-ttu-id="1855c-114">Se você desabilitar "Pesquisar na Web" usando essa mensagem, a mensagem em [**\_ SEARCHWEB**](em-searchweb.md) não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="1855c-114">If you disable "Search the web" using this message, the [**EM\_SEARCHWEB**](em-searchweb.md) message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="1855c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1855c-115">Requirements</span></span>



| <span data-ttu-id="1855c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1855c-116">Requirement</span></span> | <span data-ttu-id="1855c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1855c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1855c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1855c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1855c-119">\[Somente aplicativos de área de trabalho do Windows 10, 1809\]</span><span class="sxs-lookup"><span data-stu-id="1855c-119">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1855c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1855c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1855c-121">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="1855c-121">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1855c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1855c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1855c-123"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1855c-123"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1855c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1855c-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="1855c-125">**Referência**</span><span class="sxs-lookup"><span data-stu-id="1855c-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1855c-126">**em \_ SEARCHWEB**</span><span class="sxs-lookup"><span data-stu-id="1855c-126">**EM\_SEARCHWEB**</span></span>](em-searchweb.md)
</dt> </dl>

 

 





