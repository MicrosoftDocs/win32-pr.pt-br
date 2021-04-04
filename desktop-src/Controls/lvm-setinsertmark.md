---
title: Mensagem de LVM_SETINSERTMARK (commctrl. h)
description: Define o ponto de inserção para a posição definida.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- Controles de LVM_SETINSERTMARK de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dab80b1b73b620ce94b75aecab90f6bdd69bf228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085165"
---
# <a name="lvm_setinsertmark-message"></a><span data-ttu-id="3c23e-104">\_Mensagem SETINSERTMARK LVM</span><span class="sxs-lookup"><span data-stu-id="3c23e-104">LVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="3c23e-105">Define o ponto de inserção para a posição definida.</span><span class="sxs-lookup"><span data-stu-id="3c23e-105">Sets the insertion point to the defined position.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c23e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3c23e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c23e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c23e-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3c23e-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3c23e-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3c23e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c23e-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3c23e-110">Ponteiro para uma estrutura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> que especifica onde definir o ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="3c23e-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies where to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c23e-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3c23e-111">Return value</span></span>

<span data-ttu-id="3c23e-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="3c23e-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="3c23e-113">**False** será retornado se o tamanho no membro **CbSize** da estrutura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) não for igual ao tamanho real da estrutura ou quando um ponto de inserção não se aplicar na exibição atual.</span><span class="sxs-lookup"><span data-stu-id="3c23e-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c23e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c23e-114">Remarks</span></span>

<span data-ttu-id="3c23e-115">Um ponto de inserção só poderá aparecer se o controle de exibição de lista estiver na exibição de ícones, na exibição de ícones pequenos ou na exibição de bloco, e não estiver no modo de exibição de grupo.</span><span class="sxs-lookup"><span data-stu-id="3c23e-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="3c23e-116">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="3c23e-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="3c23e-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3c23e-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c23e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c23e-118">Requirements</span></span>



| <span data-ttu-id="3c23e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c23e-119">Requirement</span></span> | <span data-ttu-id="3c23e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3c23e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c23e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c23e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="3c23e-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c23e-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c23e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c23e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="3c23e-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c23e-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c23e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c23e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c23e-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c23e-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





