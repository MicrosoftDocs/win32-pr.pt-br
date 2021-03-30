---
title: Mensagem de LVM_MAPINDEXTOID (commctrl. h)
description: Mapeia o índice de um item para uma ID exclusiva.
ms.assetid: d0486e21-2703-4289-abb0-f5f9c7b60b40
keywords:
- Controles de LVM_MAPINDEXTOID de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_MAPINDEXTOID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a2a5de558b025e61bef26fd20278f125372769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454937"
---
# <a name="lvm_mapindextoid-message"></a><span data-ttu-id="52137-104">\_Mensagem MAPINDEXTOID LVM</span><span class="sxs-lookup"><span data-stu-id="52137-104">LVM\_MAPINDEXTOID message</span></span>

<span data-ttu-id="52137-105">Mapeia o índice de um item para uma ID exclusiva.</span><span class="sxs-lookup"><span data-stu-id="52137-105">Maps the index of an item to a unique ID.</span></span>

## <a name="parameters"></a><span data-ttu-id="52137-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="52137-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52137-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="52137-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52137-108">O índice de um item.</span><span class="sxs-lookup"><span data-stu-id="52137-108">The index of an item.</span></span>

</dd> <dt>

<span data-ttu-id="52137-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="52137-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="52137-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="52137-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52137-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="52137-111">Return value</span></span>

<span data-ttu-id="52137-112">Retorna uma ID exclusiva.</span><span class="sxs-lookup"><span data-stu-id="52137-112">Returns a unique ID.</span></span>

## <a name="remarks"></a><span data-ttu-id="52137-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="52137-113">Remarks</span></span>

<span data-ttu-id="52137-114">Controles de exibição de lista controlam internamente os itens por índice.</span><span class="sxs-lookup"><span data-stu-id="52137-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="52137-115">Isso pode apresentar problemas porque os índices podem ser alterados durante o tempo de vida do controle.</span><span class="sxs-lookup"><span data-stu-id="52137-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="52137-116">O controle de exibição de lista pode marcar um item com uma ID quando o item é criado.</span><span class="sxs-lookup"><span data-stu-id="52137-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="52137-117">Você pode usar essa ID para garantir a exclusividade durante o tempo de vida do controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="52137-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="52137-118">Para identificar exclusivamente um item, pegue o índice que é retornado de uma chamada como [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) e chame o **LVM \_ MAPINDEXTOID**.</span><span class="sxs-lookup"><span data-stu-id="52137-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call **LVM\_MAPINDEXTOID**.</span></span> <span data-ttu-id="52137-119">O valor de retorno é uma ID exclusiva.</span><span class="sxs-lookup"><span data-stu-id="52137-119">The return value is a unique ID.</span></span>

> [!Note]  
> <span data-ttu-id="52137-120">Em um ambiente multi-threaded, o índice só é garantido no thread que hospeda o controle de exibição de lista, não em threads em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="52137-120">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="52137-121">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="52137-121">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="52137-122">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="52137-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="52137-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52137-123">Requirements</span></span>



| <span data-ttu-id="52137-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="52137-124">Requirement</span></span> | <span data-ttu-id="52137-125">Valor</span><span class="sxs-lookup"><span data-stu-id="52137-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52137-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52137-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52137-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="52137-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="52137-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52137-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52137-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="52137-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="52137-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="52137-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="52137-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="52137-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

