---
title: Mensagem de PSM_GETTABCONTROL (Prsht. h)
description: Recupera o identificador para o controle guia de uma folha de propriedades. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetTabControl PropSheet.
ms.assetid: 5ddea541-c8e0-4357-b08e-3b5e64be377f
keywords:
- Controles de PSM_GETTABCONTROL de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_GETTABCONTROL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab296159cac4dbfb4ef894d90d31bcd74d6ca2e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499624"
---
# <a name="psm_gettabcontrol-message"></a><span data-ttu-id="8ede4-105">Mensagem do PSM \_ GETtabcontrol</span><span class="sxs-lookup"><span data-stu-id="8ede4-105">PSM\_GETTABCONTROL message</span></span>

<span data-ttu-id="8ede4-106">Recupera o identificador para o controle guia de uma folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8ede4-106">Retrieves the handle to the tab control of a property sheet.</span></span> <span data-ttu-id="8ede4-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetTabControl PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) .</span><span class="sxs-lookup"><span data-stu-id="8ede4-107">You can send this message explicitly or by using the [**PropSheet\_GetTabControl**](/windows/desktop/api/Prsht/nf-prsht-propsheet_gettabcontrol) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8ede4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ede4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ede4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8ede4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ede4-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8ede4-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8ede4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8ede4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8ede4-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="8ede4-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ede4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ede4-113">Return value</span></span>

<span data-ttu-id="8ede4-114">Retorna o identificador para o controle de guia.</span><span class="sxs-lookup"><span data-stu-id="8ede4-114">Returns the handle to the tab control.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ede4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ede4-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8ede4-116">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="8ede4-116">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8ede4-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ede4-117">Requirements</span></span>



| <span data-ttu-id="8ede4-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ede4-118">Requirement</span></span> | <span data-ttu-id="8ede4-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8ede4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8ede4-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ede4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8ede4-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8ede4-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8ede4-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ede4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8ede4-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ede4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8ede4-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ede4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ede4-125"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ede4-125"><dt>Prsht.h</dt></span></span> </dl> |



 

 





