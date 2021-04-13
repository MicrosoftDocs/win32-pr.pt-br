---
title: Mensagem de PSM_QUERYSIBLINGS (Prsht. h)
description: Enviado a uma folha de propriedades, que, em seguida, encaminha a mensagem para cada uma de suas páginas. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ QuerySiblings.
ms.assetid: 96f48847-b7b8-4d6f-8bde-ada915b7c962
keywords:
- Controles de PSM_QUERYSIBLINGS de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_QUERYSIBLINGS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5943fefa906475e34d1cc7acc7f8a86cd99252
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499437"
---
# <a name="psm_querysiblings-message"></a><span data-ttu-id="0daef-105">Mensagem de PSM \_ QUERYSIBLINGS</span><span class="sxs-lookup"><span data-stu-id="0daef-105">PSM\_QUERYSIBLINGS message</span></span>

<span data-ttu-id="0daef-106">Enviado a uma folha de propriedades, que, em seguida, encaminha a mensagem para cada uma de suas páginas.</span><span class="sxs-lookup"><span data-stu-id="0daef-106">Sent to a property sheet, which then forwards the message to each of its pages.</span></span> <span data-ttu-id="0daef-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) .</span><span class="sxs-lookup"><span data-stu-id="0daef-107">You can send this message explicitly or by using the [**PropSheet\_QuerySiblings**](/windows/desktop/api/Prsht/nf-prsht-propsheet_querysiblings) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="0daef-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0daef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0daef-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0daef-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0daef-110">Primeiro parâmetro definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0daef-110">First application-defined parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0daef-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0daef-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0daef-112">Segundo parâmetro definido pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0daef-112">Second application-defined parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0daef-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0daef-113">Return value</span></span>

<span data-ttu-id="0daef-114">Retorna o valor diferente de zero de uma página na folha de propriedades ou zero se nenhuma página retornar um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="0daef-114">Returns the nonzero value from a page in the property sheet, or zero if no page returns a nonzero value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0daef-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0daef-115">Remarks</span></span>

<span data-ttu-id="0daef-116">Se uma página retornar um valor diferente de zero, a folha de propriedades não enviará a mensagem para as páginas subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0daef-116">If a page returns a nonzero value, the property sheet does not send the message to subsequent pages.</span></span>

## <a name="requirements"></a><span data-ttu-id="0daef-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0daef-117">Requirements</span></span>



| <span data-ttu-id="0daef-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0daef-118">Requirement</span></span> | <span data-ttu-id="0daef-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0daef-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0daef-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0daef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0daef-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0daef-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0daef-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0daef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0daef-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0daef-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0daef-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0daef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0daef-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="0daef-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





