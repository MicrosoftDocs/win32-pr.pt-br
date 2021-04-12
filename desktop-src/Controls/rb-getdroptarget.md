---
title: Mensagem de RB_GETDROPTARGET (commctrl. h)
description: Recupera o ponteiro de interface IDropTarget de um controle rebar.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- Controles de RB_GETDROPTARGET de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455531"
---
# <a name="rb_getdroptarget-message"></a><span data-ttu-id="68142-104">\_Mensagem GETDROPTARGET RB</span><span class="sxs-lookup"><span data-stu-id="68142-104">RB\_GETDROPTARGET message</span></span>

<span data-ttu-id="68142-105">Recupera o ponteiro de interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de um controle rebar.</span><span class="sxs-lookup"><span data-stu-id="68142-105">Retrieves a rebar control's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) interface pointer.</span></span>

## <a name="parameters"></a><span data-ttu-id="68142-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="68142-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68142-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="68142-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68142-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="68142-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="68142-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="68142-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="68142-110">Ponteiro para um ponteiro [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) que recebe o ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="68142-110">Pointer to an [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pointer that receives the interface pointer.</span></span> <span data-ttu-id="68142-111">É responsabilidade do chamador chamar [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) neste ponteiro quando ele não for mais necessário.</span><span class="sxs-lookup"><span data-stu-id="68142-111">It is the caller's responsibility to call [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on this pointer when it is no longer needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68142-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="68142-112">Return value</span></span>

<span data-ttu-id="68142-113">O valor retornado para esta mensagem não é usado.</span><span class="sxs-lookup"><span data-stu-id="68142-113">The return value for this message is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="68142-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68142-114">Requirements</span></span>



| <span data-ttu-id="68142-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="68142-115">Requirement</span></span> | <span data-ttu-id="68142-116">Valor</span><span class="sxs-lookup"><span data-stu-id="68142-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68142-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68142-117">Minimum supported client</span></span><br/> | <span data-ttu-id="68142-118">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68142-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="68142-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68142-119">Minimum supported server</span></span><br/> | <span data-ttu-id="68142-120">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="68142-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68142-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68142-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="68142-122"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="68142-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

