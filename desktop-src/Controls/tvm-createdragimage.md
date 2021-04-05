---
title: Mensagem de TVM_CREATEDRAGIMAGE (commctrl. h)
description: Cria um bitmap de arrastar para o item especificado em um controle de exibição de árvore.
ms.assetid: fbe97921-c9d3-473c-933c-d6bc0599e24d
keywords:
- Controles de TVM_CREATEDRAGIMAGE de mensagens do Windows
topic_type:
- apiref
api_name:
- TVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 189b37affc6a4382541faea13199cacfcb9b7df5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085630"
---
# <a name="tvm_createdragimage-message"></a><span data-ttu-id="9ba8e-104">\_Mensagem TVM CREATEDRAGIMAGE</span><span class="sxs-lookup"><span data-stu-id="9ba8e-104">TVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="9ba8e-105">Cria um bitmap de arrastar para o item especificado em um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-105">Creates a dragging bitmap for the specified item in a tree-view control.</span></span> <span data-ttu-id="9ba8e-106">A mensagem também cria uma lista de imagens para o bitmap e adiciona o bitmap à lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-106">The message also creates an image list for the bitmap and adds the bitmap to the image list.</span></span> <span data-ttu-id="9ba8e-107">Um aplicativo pode exibir a imagem ao arrastar o item usando as funções de lista de imagens.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-107">An application can display the image when dragging the item by using the image list functions.</span></span> <span data-ttu-id="9ba8e-108">Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) .</span><span class="sxs-lookup"><span data-stu-id="9ba8e-108">You can send this message explicitly or by using the [**TreeView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9ba8e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9ba8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ba8e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9ba8e-110">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9ba8e-111">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-111">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9ba8e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9ba8e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9ba8e-113">Identificador para o item que recebe o novo bitmap de arrastar.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-113">Handle to the item that receives the new dragging bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ba8e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9ba8e-114">Return value</span></span>

<span data-ttu-id="9ba8e-115">Retorna o identificador para a lista de imagens para a qual o bitmap de arrastar foi adicionado, se for bem-sucedido, ou **NULL** de outra forma.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-115">Returns the handle to the image list to which the dragging bitmap was added if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ba8e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="9ba8e-116">Remarks</span></span>

<span data-ttu-id="9ba8e-117">Se você criar um controle de exibição de árvore sem uma lista de imagens associada, não poderá usar a mensagem **TVM \_ CREATEDRAGIMAGE** para criar a imagem a ser exibida durante uma operação de arrastar.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-117">If you create a tree-view control without an associated image list, you cannot use the **TVM\_CREATEDRAGIMAGE** message to create the image to display during a drag operation.</span></span> <span data-ttu-id="9ba8e-118">Você deve implementar seu próprio método de criação de um cursor de arrastar.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-118">You must implement your own method of creating a drag cursor.</span></span>

<span data-ttu-id="9ba8e-119">Seu aplicativo é responsável por destruir a lista de imagens quando ela não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="9ba8e-119">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ba8e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ba8e-120">Requirements</span></span>



| <span data-ttu-id="9ba8e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ba8e-121">Requirement</span></span> | <span data-ttu-id="9ba8e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9ba8e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9ba8e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ba8e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9ba8e-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9ba8e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9ba8e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9ba8e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9ba8e-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9ba8e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9ba8e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9ba8e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ba8e-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ba8e-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





