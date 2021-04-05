---
title: Mensagem de LVM_GETVIEW (commctrl. h)
description: Recupera a exibição atual de um controle de exibição de lista.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- Controles de LVM_GETVIEW de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2da295fa5a5b335de60169ce06b777d9e355121
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086157"
---
# <a name="lvm_getview-message"></a><span data-ttu-id="6529b-104">\_Mensagem GETVIEW LVM</span><span class="sxs-lookup"><span data-stu-id="6529b-104">LVM\_GETVIEW message</span></span>

<span data-ttu-id="6529b-105">Recupera a exibição atual de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="6529b-105">Retrieves the current view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6529b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6529b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6529b-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6529b-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6529b-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6529b-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6529b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6529b-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6529b-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6529b-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6529b-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6529b-111">Return value</span></span>

<span data-ttu-id="6529b-112">Retorna um **DWORD** que especifica a exibição atual.</span><span class="sxs-lookup"><span data-stu-id="6529b-112">Returns a **DWORD** that specifies the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="6529b-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="6529b-113">Remarks</span></span>

<span data-ttu-id="6529b-114">A seguir estão os valores para exibições.</span><span class="sxs-lookup"><span data-stu-id="6529b-114">Following are the values for views.</span></span>

-   <span data-ttu-id="6529b-115">\_detalhes da exibição de LV \_</span><span class="sxs-lookup"><span data-stu-id="6529b-115">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="6529b-116">\_ícone de exibição LV \_</span><span class="sxs-lookup"><span data-stu-id="6529b-116">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="6529b-117">\_lista de exibição de LV \_</span><span class="sxs-lookup"><span data-stu-id="6529b-117">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="6529b-118">\_SMALLICON de exibição LV \_</span><span class="sxs-lookup"><span data-stu-id="6529b-118">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="6529b-119">\_bloco de exibição LV \_</span><span class="sxs-lookup"><span data-stu-id="6529b-119">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="6529b-120">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="6529b-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6529b-121">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6529b-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6529b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6529b-122">Requirements</span></span>



| <span data-ttu-id="6529b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="6529b-123">Requirement</span></span> | <span data-ttu-id="6529b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="6529b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6529b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6529b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6529b-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6529b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6529b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6529b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6529b-128">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6529b-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6529b-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6529b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6529b-130"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6529b-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





