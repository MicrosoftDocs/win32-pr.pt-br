---
title: Mensagem de LVM_GETINSERTMARK (commctrl. h)
description: Recupera a posição do ponto de inserção.
ms.assetid: ad00df4c-4b4b-48f1-8821-7849a216df2e
keywords:
- Controles de LVM_GETINSERTMARK de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8cba96ae7d357e3e1f5a007fa41f6b7e9e3b64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824298"
---
# <a name="lvm_getinsertmark-message"></a><span data-ttu-id="bd0fe-104">\_Mensagem GETINSERTMARK LVM</span><span class="sxs-lookup"><span data-stu-id="bd0fe-104">LVM\_GETINSERTMARK message</span></span>

<span data-ttu-id="bd0fe-105">Recupera a posição do ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="bd0fe-105">Retrieves the position of the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="bd0fe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd0fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd0fe-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bd0fe-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bd0fe-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bd0fe-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bd0fe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bd0fe-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bd0fe-110">Ponteiro para uma estrutura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> que recebe a posição do ponto de inserção.</span><span class="sxs-lookup"><span data-stu-id="bd0fe-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that receives the position of the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd0fe-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bd0fe-111">Return value</span></span>

<span data-ttu-id="bd0fe-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="bd0fe-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="bd0fe-113">**False** será retornado se o tamanho no membro **CbSize** da estrutura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) não for igual ao tamanho real da estrutura.</span><span class="sxs-lookup"><span data-stu-id="bd0fe-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd0fe-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd0fe-114">Remarks</span></span>

<span data-ttu-id="bd0fe-115">Um ponto de inserção só poderá aparecer se o controle de exibição de lista estiver na exibição de ícones, na exibição de ícones pequenos ou na exibição de bloco, e não estiver no modo de exibição de grupo.</span><span class="sxs-lookup"><span data-stu-id="bd0fe-115">An insertion point can appear only if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="bd0fe-116">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="bd0fe-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="bd0fe-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bd0fe-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bd0fe-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd0fe-118">Requirements</span></span>



| <span data-ttu-id="bd0fe-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd0fe-119">Requirement</span></span> | <span data-ttu-id="bd0fe-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bd0fe-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bd0fe-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd0fe-121">Minimum supported client</span></span><br/> | <span data-ttu-id="bd0fe-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd0fe-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bd0fe-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bd0fe-123">Minimum supported server</span></span><br/> | <span data-ttu-id="bd0fe-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bd0fe-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bd0fe-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bd0fe-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd0fe-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd0fe-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





