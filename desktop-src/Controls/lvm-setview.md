---
title: Mensagem de LVM_SETVIEW (commctrl. h)
description: Define a exibição de um controle de exibição de lista.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- Controles de LVM_SETVIEW de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086150"
---
# <a name="lvm_setview-message"></a><span data-ttu-id="37cc9-104">Mensagem do LVM \_ SETview</span><span class="sxs-lookup"><span data-stu-id="37cc9-104">LVM\_SETVIEW message</span></span>

<span data-ttu-id="37cc9-105">Define a exibição de um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="37cc9-105">Sets the view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="37cc9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37cc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37cc9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37cc9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="37cc9-108">**DWORD** que especifica a exibição.</span><span class="sxs-lookup"><span data-stu-id="37cc9-108">**DWORD** that specifies the view.</span></span></dd> <dt>

<span data-ttu-id="37cc9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37cc9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="37cc9-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="37cc9-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37cc9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37cc9-111">Return value</span></span>

<span data-ttu-id="37cc9-112">Retornará 1 se for bem-sucedido ou-1 caso contrário.</span><span class="sxs-lookup"><span data-stu-id="37cc9-112">Returns 1 if successful, or -1 otherwise.</span></span> <span data-ttu-id="37cc9-113">Por exemplo,-1 será retornado se a exibição for inválida.</span><span class="sxs-lookup"><span data-stu-id="37cc9-113">For example, -1 is returned if the view is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="37cc9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="37cc9-114">Remarks</span></span>

<span data-ttu-id="37cc9-115">A seguir estão os valores para exibições.</span><span class="sxs-lookup"><span data-stu-id="37cc9-115">Following are the values for views.</span></span>

-   <span data-ttu-id="37cc9-116">\_detalhes da exibição de LV \_</span><span class="sxs-lookup"><span data-stu-id="37cc9-116">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="37cc9-117">\_ícone de exibição LV \_</span><span class="sxs-lookup"><span data-stu-id="37cc9-117">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="37cc9-118">\_lista de exibição de LV \_</span><span class="sxs-lookup"><span data-stu-id="37cc9-118">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="37cc9-119">\_SMALLICON de exibição LV \_</span><span class="sxs-lookup"><span data-stu-id="37cc9-119">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="37cc9-120">\_bloco de exibição LV \_</span><span class="sxs-lookup"><span data-stu-id="37cc9-120">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="37cc9-121">Para usar essa mensagem, você deve fornecer um manifesto especificando Comctl32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="37cc9-121">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="37cc9-122">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="37cc9-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="37cc9-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37cc9-123">Requirements</span></span>



| <span data-ttu-id="37cc9-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="37cc9-124">Requirement</span></span> | <span data-ttu-id="37cc9-125">Valor</span><span class="sxs-lookup"><span data-stu-id="37cc9-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37cc9-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37cc9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="37cc9-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="37cc9-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37cc9-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="37cc9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="37cc9-129">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="37cc9-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37cc9-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37cc9-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="37cc9-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="37cc9-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





