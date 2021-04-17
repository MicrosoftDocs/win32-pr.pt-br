---
title: Mensagem de LVM_MAPIDTOINDEX (commctrl. h)
description: Mapeia a ID de um item para um índice.
ms.assetid: vs|controls|~\controls\listview\messages\lvm_mapidtoindex.htm
keywords:
- Controles de LVM_MAPIDTOINDEX de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_MAPIDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb4cb8aa49b37186ef689ed8cb319bbb92b62d75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748256"
---
# <a name="lvm_mapidtoindex-message"></a><span data-ttu-id="7bd60-104">\_Mensagem MAPIDTOINDEX LVM</span><span class="sxs-lookup"><span data-stu-id="7bd60-104">LVM\_MAPIDTOINDEX message</span></span>

<span data-ttu-id="7bd60-105">Mapeia a ID de um item para um índice.</span><span class="sxs-lookup"><span data-stu-id="7bd60-105">Maps the ID of an item to an index.</span></span>

## <a name="parameters"></a><span data-ttu-id="7bd60-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bd60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bd60-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7bd60-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7bd60-108">A ID exclusiva de um item.</span><span class="sxs-lookup"><span data-stu-id="7bd60-108">The unique ID of an item.</span></span>

</dd> <dt>

<span data-ttu-id="7bd60-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7bd60-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7bd60-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7bd60-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bd60-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7bd60-111">Return value</span></span>

<span data-ttu-id="7bd60-112">Retorna o índice mais atual.</span><span class="sxs-lookup"><span data-stu-id="7bd60-112">Returns the most current index.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bd60-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7bd60-113">Remarks</span></span>

<span data-ttu-id="7bd60-114">Controles de exibição de lista controlam internamente os itens por índice.</span><span class="sxs-lookup"><span data-stu-id="7bd60-114">List-view controls internally track items by index.</span></span> <span data-ttu-id="7bd60-115">Isso pode apresentar problemas porque os índices podem ser alterados durante o tempo de vida do controle.</span><span class="sxs-lookup"><span data-stu-id="7bd60-115">This can present problems because indexes can change during the control's lifetime.</span></span>

<span data-ttu-id="7bd60-116">O controle de exibição de lista pode marcar um item com uma ID quando o item é criado.</span><span class="sxs-lookup"><span data-stu-id="7bd60-116">The list-view control can tag an item with an ID when the item is created.</span></span> <span data-ttu-id="7bd60-117">Você pode usar essa ID para garantir a exclusividade durante o tempo de vida do controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="7bd60-117">You can use this ID to guarantee uniqueness during the lifetime of the list-view control.</span></span>

<span data-ttu-id="7bd60-118">Para identificar exclusivamente um item, pegue o índice que é retornado de uma chamada como [**IComponent:: GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) e chame o [**LVM \_ MAPINDEXTOID**](lvm-mapindextoid.md).</span><span class="sxs-lookup"><span data-stu-id="7bd60-118">To uniquely identify an item, take the index that is returned from a call such as [**IComponent::GetDisplayInfo**](/windows/desktop/api/mmc/nf-mmc-icomponent-getdisplayinfo) and call [**LVM\_MAPINDEXTOID**](lvm-mapindextoid.md).</span></span> <span data-ttu-id="7bd60-119">O valor de retorno é uma ID exclusiva.</span><span class="sxs-lookup"><span data-stu-id="7bd60-119">The return value is a unique ID.</span></span>

<span data-ttu-id="7bd60-120">Se você precisar do índice de um item depois que uma ID for criada, poderá chamar o **LVM \_ MAPIDTOINDEX** com a ID exclusiva e ele retornará o índice mais atual.</span><span class="sxs-lookup"><span data-stu-id="7bd60-120">If you need the index of an item after an ID is created you can call **LVM\_MAPIDTOINDEX** with the unique ID and it returns the most current index.</span></span>

<span data-ttu-id="7bd60-121">**LVM \_** Não há suporte para MAPIDTOINDEX no estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7bd60-121">**LVM\_MAPIDTOINDEX** is not supported under the [**LVS\_OWNERDATA**](list-view-window-styles.md) style.</span></span>

> [!Note]  
> <span data-ttu-id="7bd60-122">Em um ambiente multi-threaded, o índice só é garantido no thread que hospeda o controle de exibição de lista, não em threads em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7bd60-122">In a multithreaded environment, the index is only guaranteed on the thread that hosts the list-view control, not on background threads.</span></span>

 

> [!Note]  
> <span data-ttu-id="7bd60-123">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="7bd60-123">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="7bd60-124">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7bd60-124">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7bd60-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bd60-125">Requirements</span></span>



| <span data-ttu-id="7bd60-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bd60-126">Requirement</span></span> | <span data-ttu-id="7bd60-127">Valor</span><span class="sxs-lookup"><span data-stu-id="7bd60-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7bd60-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7bd60-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7bd60-129">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7bd60-129">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7bd60-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7bd60-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7bd60-131">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7bd60-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7bd60-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7bd60-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bd60-133"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bd60-133"><dt>Commctrl.h</dt></span></span> </dl> |



 

