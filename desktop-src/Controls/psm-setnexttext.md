---
title: Mensagem de PSM_SETNEXTTEXT (Prsht. h)
description: Define o texto do botão Avançar em um assistente. Você pode enviar essa mensagem explicitamente ou usando a macro PropSheet \_ SetNextText.
ms.assetid: 4608425e-1724-4d0b-b0f6-9fec147a85f6
keywords:
- Controles de PSM_SETNEXTTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- PSM_SETNEXTTEXT
- PSM_SETNEXTTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d781a8d76fca5c1e74bcda452b6ab7e03a32aacc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644298"
---
# <a name="psm_setnexttext-message"></a><span data-ttu-id="83c1b-105">Mensagem de PSM \_ SETNEXTTEXT</span><span class="sxs-lookup"><span data-stu-id="83c1b-105">PSM\_SETNEXTTEXT message</span></span>

<span data-ttu-id="83c1b-106">Define o texto do botão **Avançar** em um assistente.</span><span class="sxs-lookup"><span data-stu-id="83c1b-106">Sets the text of the **Next** button in a wizard.</span></span> <span data-ttu-id="83c1b-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**PropSheet \_ SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) .</span><span class="sxs-lookup"><span data-stu-id="83c1b-107">You can send this message explicitly or by using the [**PropSheet\_SetNextText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setnexttext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="83c1b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="83c1b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83c1b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83c1b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83c1b-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="83c1b-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="83c1b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83c1b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83c1b-112">Ponteiro para um buffer que contém o texto.</span><span class="sxs-lookup"><span data-stu-id="83c1b-112">Pointer to a buffer that contains the text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83c1b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="83c1b-113">Return value</span></span>

<span data-ttu-id="83c1b-114">Nenhum valor de retorno significativo.</span><span class="sxs-lookup"><span data-stu-id="83c1b-114">No meaningful return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="83c1b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="83c1b-115">Requirements</span></span>



| <span data-ttu-id="83c1b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="83c1b-116">Requirement</span></span> | <span data-ttu-id="83c1b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="83c1b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="83c1b-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83c1b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="83c1b-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83c1b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="83c1b-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="83c1b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="83c1b-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="83c1b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="83c1b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="83c1b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="83c1b-123"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="83c1b-123"><dt>Prsht.h</dt></span></span> </dl> |
| <span data-ttu-id="83c1b-124">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="83c1b-124">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="83c1b-125">**PSM \_ SETNEXTTEXTW** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="83c1b-125">**PSM\_SETNEXTTEXTW** (Unicode)</span></span><br/>                                         |



 

 





