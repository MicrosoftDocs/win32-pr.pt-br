---
title: Mensagem de LM_SETITEM (commctrl. h)
description: Define os Estados e atributos de um item.
ms.assetid: 02a68a31-2541-480e-b768-449d40e5e9e0
keywords:
- Controles de LM_SETITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LM_SETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11888a76b11ccec7e8e659ca3a33bb23a71667ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085181"
---
# <a name="lm_setitem-message"></a><span data-ttu-id="905e9-104">\_Mensagem SETITEM de LM</span><span class="sxs-lookup"><span data-stu-id="905e9-104">LM\_SETITEM message</span></span>

<span data-ttu-id="905e9-105">Define os Estados e atributos de um item.</span><span class="sxs-lookup"><span data-stu-id="905e9-105">Sets the states and attributes of an item.</span></span>

## <a name="parameters"></a><span data-ttu-id="905e9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="905e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="905e9-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="905e9-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="905e9-108">Deve ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="905e9-108">Must be **NULL**.</span></span> </dd> <dt>

<span data-ttu-id="905e9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="905e9-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="905e9-110">Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litem</a> que contém os novos Estados e atributos desejados para o link.</span><span class="sxs-lookup"><span data-stu-id="905e9-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-litem">LITEM</a> structure containing the new states and attributes desired for the link.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="905e9-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="905e9-111">Return value</span></span>

<span data-ttu-id="905e9-112">Retornará **true** se a mensagem tiver sucesso na definição dos valores e atributos especificados.</span><span class="sxs-lookup"><span data-stu-id="905e9-112">Returns **TRUE** if the message succeeds in setting the values and attributes specified.</span></span>

## <a name="remarks"></a><span data-ttu-id="905e9-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="905e9-113">Remarks</span></span>

<span data-ttu-id="905e9-114">Com a [**mensagem \_ GETITEM do LM**](lm-getitem.md) , os links só podem ser acessados por meio do índice numérico retornado no membro **iLink** de [**litem**](/windows/win32/api/commctrl/ns-commctrl-litem).</span><span class="sxs-lookup"><span data-stu-id="905e9-114">With the [**LM\_GETITEM**](lm-getitem.md) message, links can only be accessed through the numeric index returned in the **iLink** member of [**LITEM**](/windows/win32/api/commctrl/ns-commctrl-litem).</span></span> <span data-ttu-id="905e9-115">Não há suporte para o acesso ao link por meio do nome de ID retornado em **szID** .</span><span class="sxs-lookup"><span data-stu-id="905e9-115">Accessing the link through the ID name returned in **szID** is not supported.</span></span>

> [!Note]  
> <span data-ttu-id="905e9-116">Para usar essa mensagem, você deve fornecer um manifesto especificando Comctl32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="905e9-116">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="905e9-117">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="905e9-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="905e9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="905e9-118">Requirements</span></span>



| <span data-ttu-id="905e9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="905e9-119">Requirement</span></span> | <span data-ttu-id="905e9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="905e9-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="905e9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="905e9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="905e9-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="905e9-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="905e9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="905e9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="905e9-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="905e9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="905e9-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="905e9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="905e9-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="905e9-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





