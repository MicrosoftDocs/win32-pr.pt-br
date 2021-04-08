---
title: Mensagem de LVM_SETTEXTBKCOLOR (commctrl. h)
description: Define a cor da tela de fundo do texto em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetTextBkColor do ListView.
ms.assetid: e51d6914-0e98-47f8-b2d8-4c2404b98242
keywords:
- Controles de LVM_SETTEXTBKCOLOR de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2247dfd04d90c2b9eacadcb1c38608f519540fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009200"
---
# <a name="lvm_settextbkcolor-message"></a><span data-ttu-id="32c3d-105">\_Mensagem SETTEXTBKCOLOR LVM</span><span class="sxs-lookup"><span data-stu-id="32c3d-105">LVM\_SETTEXTBKCOLOR message</span></span>

<span data-ttu-id="32c3d-106">Define a cor da tela de fundo do texto em um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="32c3d-106">Sets the background color of text in a list-view control.</span></span> <span data-ttu-id="32c3d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetTextBkColor do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="32c3d-107">You can send this message explicitly or by using the [**ListView\_SetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="32c3d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32c3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32c3d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="32c3d-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="32c3d-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="32c3d-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="32c3d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="32c3d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="32c3d-112">Nova cor do plano de fundo do texto.</span><span class="sxs-lookup"><span data-stu-id="32c3d-112">New text background color.</span></span> <span data-ttu-id="32c3d-113">Isso pode ser \_ nenhum CLR para nenhuma cor do plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="32c3d-113">This can be CLR\_NONE for no background color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32c3d-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32c3d-114">Return value</span></span>

<span data-ttu-id="32c3d-115">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="32c3d-115">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="32c3d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32c3d-116">Requirements</span></span>



| <span data-ttu-id="32c3d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="32c3d-117">Requirement</span></span> | <span data-ttu-id="32c3d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="32c3d-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32c3d-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32c3d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="32c3d-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="32c3d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="32c3d-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32c3d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="32c3d-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="32c3d-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32c3d-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32c3d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="32c3d-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="32c3d-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





