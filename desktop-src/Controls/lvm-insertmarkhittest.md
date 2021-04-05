---
title: Mensagem de LVM_INSERTMARKHITTEST (commctrl. h)
description: Recupera o ponto de inserção mais próximo de um ponto especificado.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- Controles de LVM_INSERTMARKHITTEST de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086155"
---
# <a name="lvm_insertmarkhittest-message"></a><span data-ttu-id="ea761-104">\_Mensagem INSERTMARKHITTEST LVM</span><span class="sxs-lookup"><span data-stu-id="ea761-104">LVM\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="ea761-105">Recupera o ponto de inserção mais próximo de um ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="ea761-105">Retrieves the insertion point closest to a specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea761-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea761-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea761-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea761-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ea761-108">Ponteiro para uma estrutura de **ponto** que contém as coordenadas de teste de clique.</span><span class="sxs-lookup"><span data-stu-id="ea761-108">Pointer to a **POINT** structure that contains the hit test coordinates.</span></span></dd> <dt>

<span data-ttu-id="ea761-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea761-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="ea761-110">Ponteiro para uma estrutura <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> que especifica o ponto de inserção mais próximo das coordenadas definidas pelo parâmetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="ea761-110">Pointer to an <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies the insertion point closest to the coordinates defined by the *wParam* parameter.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea761-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea761-111">Return value</span></span>

<span data-ttu-id="ea761-112">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="ea761-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="ea761-113">**False** será retornado se o tamanho no membro **CbSize** da estrutura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) não for igual ao tamanho real da estrutura ou quando um ponto de inserção não se aplicar na exibição atual.</span><span class="sxs-lookup"><span data-stu-id="ea761-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea761-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea761-114">Remarks</span></span>

<span data-ttu-id="ea761-115">Um ponto de inserção só poderá aparecer se o controle de exibição de lista estiver na exibição de ícones, na exibição de ícones pequenos ou na exibição de bloco e não estiver no modo de exibição de grupo.</span><span class="sxs-lookup"><span data-stu-id="ea761-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view and is not in group-view mode.</span></span>

<span data-ttu-id="ea761-116">Se os pontos de inserção não se aplicarem à exibição, a estrutura [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) conterá um-1 no membro **iItem** .</span><span class="sxs-lookup"><span data-stu-id="ea761-116">If insertion points do not apply for the view, the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure contains a -1 in the **iItem** member.</span></span>

> [!Note]  
> <span data-ttu-id="ea761-117">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="ea761-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="ea761-118">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ea761-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ea761-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea761-119">Requirements</span></span>



| <span data-ttu-id="ea761-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea761-120">Requirement</span></span> | <span data-ttu-id="ea761-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ea761-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea761-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea761-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea761-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ea761-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ea761-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ea761-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea761-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ea761-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ea761-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea761-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea761-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea761-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





