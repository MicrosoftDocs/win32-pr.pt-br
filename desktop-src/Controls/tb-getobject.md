---
title: Mensagem de TB_GETOBJECT (commctrl. h)
description: Recupera o IDropTarget para um controle ToolBar.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- Controles de TB_GETOBJECT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086014"
---
# <a name="tb_getobject-message"></a><span data-ttu-id="be7f7-104">\_Mensagem de objeto GETobject de TB</span><span class="sxs-lookup"><span data-stu-id="be7f7-104">TB\_GETOBJECT message</span></span>

<span data-ttu-id="be7f7-105">Recupera o [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) para um controle ToolBar.</span><span class="sxs-lookup"><span data-stu-id="be7f7-105">Retrieves the [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) for a toolbar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="be7f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be7f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be7f7-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="be7f7-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be7f7-108">Identificador da interface que está sendo solicitada.</span><span class="sxs-lookup"><span data-stu-id="be7f7-108">Identifier of the interface being requested.</span></span> <span data-ttu-id="be7f7-109">Esse valor deve apontar para **\_ IDropTarget IID**.</span><span class="sxs-lookup"><span data-stu-id="be7f7-109">This value must point to **IID\_IDropTarget**.</span></span>

</dd> <dt>

<span data-ttu-id="be7f7-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="be7f7-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="be7f7-111">Endereço que recebe o ponteiro de interface.</span><span class="sxs-lookup"><span data-stu-id="be7f7-111">Address that receives the interface pointer.</span></span> <span data-ttu-id="be7f7-112">Se ocorrer um erro, um ponteiro **NULL** será colocado nesse endereço.</span><span class="sxs-lookup"><span data-stu-id="be7f7-112">If an error occurs, a **NULL** pointer is placed in this address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be7f7-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="be7f7-113">Return value</span></span>

<span data-ttu-id="be7f7-114">Retorna um valor **HRESULT** que indica êxito ou falha da operação.</span><span class="sxs-lookup"><span data-stu-id="be7f7-114">Returns an **HRESULT** value indicating success or failure of the operation.</span></span>

## <a name="remarks"></a><span data-ttu-id="be7f7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="be7f7-115">Remarks</span></span>

<span data-ttu-id="be7f7-116">A [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) da barra de ferramentas é usada pela barra de ferramentas quando os objetos são arrastados ou soltos nela.</span><span class="sxs-lookup"><span data-stu-id="be7f7-116">The toolbar's [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) is used by the toolbar when objects are dragged over or dropped onto it.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7f7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be7f7-117">Requirements</span></span>



| <span data-ttu-id="be7f7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="be7f7-118">Requirement</span></span> | <span data-ttu-id="be7f7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="be7f7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be7f7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be7f7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="be7f7-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="be7f7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be7f7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="be7f7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="be7f7-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="be7f7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be7f7-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="be7f7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="be7f7-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="be7f7-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

