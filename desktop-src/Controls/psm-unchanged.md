---
title: Mensagem de PSM_UNCHANGED (Prsht. h)
description: Informa uma folha de propriedades que as informações em uma página foram revertidas para o estado salvo anteriormente. Você pode enviar essa mensagem explicitamente ou usando a \_ macro inalterada PropSheet.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- Controles de PSM_UNCHANGED de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163617"
---
# <a name="psm_unchanged-message"></a><span data-ttu-id="71682-105">Mensagem de PSM \_ INalterada</span><span class="sxs-lookup"><span data-stu-id="71682-105">PSM\_UNCHANGED message</span></span>

<span data-ttu-id="71682-106">Informa uma folha de propriedades que as informações em uma página foram revertidas para o estado salvo anteriormente.</span><span class="sxs-lookup"><span data-stu-id="71682-106">Informs a property sheet that information in a page has reverted to the previously saved state.</span></span> <span data-ttu-id="71682-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ inalterada PropSheet**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) .</span><span class="sxs-lookup"><span data-stu-id="71682-107">You can send this message explicitly or by using the [**PropSheet\_UnChanged**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="71682-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71682-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71682-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="71682-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71682-110">Identificador para a página que foi revertida para o estado salvo anteriormente.</span><span class="sxs-lookup"><span data-stu-id="71682-110">Handle to the page that has reverted to the previously saved state.</span></span>

</dd> <dt>

<span data-ttu-id="71682-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="71682-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="71682-112">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="71682-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71682-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71682-113">Return value</span></span>

<span data-ttu-id="71682-114">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="71682-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71682-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="71682-115">Remarks</span></span>

<span data-ttu-id="71682-116">A folha de propriedades desabilita o botão **aplicar** se nenhuma outra página tiver registrado alterações com a folha de propriedades.</span><span class="sxs-lookup"><span data-stu-id="71682-116">The property sheet disables the **Apply** button if no other pages have registered changes with the property sheet.</span></span>

> [!Note]  
> <span data-ttu-id="71682-117">Não há suporte para esta mensagem ao usar o estilo de assistente Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span><span class="sxs-lookup"><span data-stu-id="71682-117">This message is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="71682-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71682-118">Requirements</span></span>



| <span data-ttu-id="71682-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="71682-119">Requirement</span></span> | <span data-ttu-id="71682-120">Valor</span><span class="sxs-lookup"><span data-stu-id="71682-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71682-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71682-121">Minimum supported client</span></span><br/> | <span data-ttu-id="71682-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="71682-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="71682-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="71682-123">Minimum supported server</span></span><br/> | <span data-ttu-id="71682-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="71682-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="71682-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="71682-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="71682-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="71682-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





