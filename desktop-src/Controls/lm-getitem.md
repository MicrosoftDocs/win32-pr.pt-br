---
title: Mensagem de LM_GETITEM (commctrl. h)
description: Recupera os Estados e atributos de um item.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- Controles de LM_GETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085183"
---
# <a name="lm_getitem-message"></a><span data-ttu-id="a3a17-104">\_Mensagem GETITEM de LM</span><span class="sxs-lookup"><span data-stu-id="a3a17-104">LM\_GETITEM message</span></span>

<span data-ttu-id="a3a17-105">Recupera os Estados e atributos de um item.</span><span class="sxs-lookup"><span data-stu-id="a3a17-105">Retrieves the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="a3a17-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3a17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a3a17-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a3a17-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a3a17-108">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a3a17-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="a3a17-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a3a17-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="a3a17-110">Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litem</a> a ser preenchida com informações sobre o item.</span><span class="sxs-lookup"><span data-stu-id="a3a17-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure to be filled with information about the item.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a3a17-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a3a17-111">Return value</span></span>

<span data-ttu-id="a3a17-112">Retornará **true** se a mensagem tiver sucesso ao obter os valores e os atributos especificados.</span><span class="sxs-lookup"><span data-stu-id="a3a17-112">Returns **TRUE** if the message succeeds in getting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3a17-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3a17-113">Remarks</span></span>

<span data-ttu-id="a3a17-114">Com a **mensagem \_ GETITEM do LM** , os links só podem ser acessados por meio do índice numérico retornado no membro **iLink** de [**litem**](/windows/win32/api/commctrl/ns-commctrl-litem).</span><span class="sxs-lookup"><span data-stu-id="a3a17-114">With the **LM\_GETITEM** message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="a3a17-115">Não há suporte para o acesso ao link por meio do nome de ID retornado em **szID** .</span><span class="sxs-lookup"><span data-stu-id="a3a17-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="a3a17-116">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="a3a17-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="a3a17-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a3a17-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a3a17-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3a17-118">Requirements</span></span>



| <span data-ttu-id="a3a17-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3a17-119">Requirement</span></span> | <span data-ttu-id="a3a17-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a3a17-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a3a17-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3a17-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a3a17-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a3a17-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a3a17-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a3a17-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a3a17-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a3a17-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a3a17-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a3a17-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a3a17-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3a17-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





