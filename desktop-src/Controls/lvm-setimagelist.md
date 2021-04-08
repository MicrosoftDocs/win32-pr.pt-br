---
title: Mensagem de LVM_SETIMAGELIST (commctrl. h)
description: Atribui uma lista de imagens a um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro Defaultimagelist de ListView.
ms.assetid: 5241065b-85e4-412e-9868-fd5b15ff7c17
keywords:
- Controles de LVM_SETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 779d31fd781a72dbdfbc4738e091482ca4a08528
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917991"
---
# <a name="lvm_setimagelist-message"></a><span data-ttu-id="2384c-105">Mensagem do LVM \_ SETimagelist</span><span class="sxs-lookup"><span data-stu-id="2384c-105">LVM\_SETIMAGELIST message</span></span>

<span data-ttu-id="2384c-106">Atribui uma lista de imagens a um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="2384c-106">Assigns an image list to a list-view control.</span></span> <span data-ttu-id="2384c-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ defaultimagelist de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) .</span><span class="sxs-lookup"><span data-stu-id="2384c-107">You can send this message explicitly or by using the [**ListView\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2384c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2384c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2384c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2384c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2384c-110">Tipo de lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="2384c-110">Type of image list.</span></span> <span data-ttu-id="2384c-111">Esse parâmetro pode ser um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="2384c-111">This parameter can be one of the following values:</span></span>



| <span data-ttu-id="2384c-112">Valor</span><span class="sxs-lookup"><span data-stu-id="2384c-112">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="2384c-113">Significado</span><span class="sxs-lookup"><span data-stu-id="2384c-113">Meaning</span></span>                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span id="LVSIL_NORMAL"></span><span id="lvsil_normal"></span><dl> <span data-ttu-id="2384c-114"><dt>**LVSIL \_ normal**</dt></span><span class="sxs-lookup"><span data-stu-id="2384c-114"><dt>**LVSIL\_NORMAL**</dt></span></span> </dl>                | <span data-ttu-id="2384c-115">Lista de imagens com ícones grandes.</span><span class="sxs-lookup"><span data-stu-id="2384c-115">Image list with large icons.</span></span><br/>  |
| <span id="LVSIL_SMALL"></span><span id="lvsil_small"></span><dl> <span data-ttu-id="2384c-116"><dt>**LVSIL \_ pequeno**</dt></span><span class="sxs-lookup"><span data-stu-id="2384c-116"><dt>**LVSIL\_SMALL**</dt></span></span> </dl>                   | <span data-ttu-id="2384c-117">Lista de imagens com ícones pequenos.</span><span class="sxs-lookup"><span data-stu-id="2384c-117">Image list with small icons.</span></span><br/>  |
| <span id="LVSIL_STATE"></span><span id="lvsil_state"></span><dl> <span data-ttu-id="2384c-118"><dt>**\_estado LVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="2384c-118"><dt>**LVSIL\_STATE**</dt></span></span> </dl>                   | <span data-ttu-id="2384c-119">Lista de imagem com imagens de estado.</span><span class="sxs-lookup"><span data-stu-id="2384c-119">Image list with state images.</span></span><br/> |
| <span id="LVSIL_GROUPHEADER"></span><span id="lvsil_groupheader"></span><dl> <span data-ttu-id="2384c-120"><dt>**\_GROUPHEADER LVSIL**</dt></span><span class="sxs-lookup"><span data-stu-id="2384c-120"><dt>**LVSIL\_GROUPHEADER**</dt></span></span> </dl> | <span data-ttu-id="2384c-121">Lista de imagens para cabeçalho de grupo.</span><span class="sxs-lookup"><span data-stu-id="2384c-121">Image list for group header.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="2384c-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2384c-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2384c-123">Identificador para a lista de imagens a ser atribuída.</span><span class="sxs-lookup"><span data-stu-id="2384c-123">Handle to the image list to assign.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2384c-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2384c-124">Return value</span></span>

<span data-ttu-id="2384c-125">Retorna o identificador para a lista de imagens associada anteriormente ao controle, se for bem-sucedido, ou **NULL** de outra forma.</span><span class="sxs-lookup"><span data-stu-id="2384c-125">Returns the handle to the image list previously associated with the control if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2384c-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="2384c-126">Remarks</span></span>

<span data-ttu-id="2384c-127">A lista de imagens atual será destruída quando o controle de exibição de lista for destruído, a menos que o estilo [**LVS \_ SHAREIMAGELISTS**](list-view-window-styles.md) seja definido.</span><span class="sxs-lookup"><span data-stu-id="2384c-127">The current image list will be destroyed when the list-view control is destroyed unless the [**LVS\_SHAREIMAGELISTS**](list-view-window-styles.md) style is set.</span></span> <span data-ttu-id="2384c-128">Se você usar essa mensagem para substituir uma lista de imagens por outra, seu aplicativo deverá destruir explicitamente todas as listas de imagens diferentes da atual.</span><span class="sxs-lookup"><span data-stu-id="2384c-128">If you use this message to replace one image list with another, your application must explicitly destroy all image lists other than the current one.</span></span>

## <a name="requirements"></a><span data-ttu-id="2384c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2384c-129">Requirements</span></span>



| <span data-ttu-id="2384c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2384c-130">Requirement</span></span> | <span data-ttu-id="2384c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="2384c-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2384c-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2384c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2384c-133">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2384c-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2384c-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2384c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2384c-135">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2384c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2384c-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2384c-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="2384c-137"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="2384c-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





