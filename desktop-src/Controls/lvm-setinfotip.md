---
title: Mensagem de LVM_SETINFOTIP (commctrl. h)
description: Define o texto da dica de ferramenta em resposta atrasada à notificação de GETINFOTIP de LVN \_ .
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- Controles de LVM_SETINFOTIP de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771696"
---
# <a name="lvm_setinfotip-message"></a><span data-ttu-id="bcb18-104">\_Mensagem SETINFOTIP LVM</span><span class="sxs-lookup"><span data-stu-id="bcb18-104">LVM\_SETINFOTIP message</span></span>

<span data-ttu-id="bcb18-105">Define o texto da dica de ferramenta em resposta atrasada à notificação de [ \_ GETINFOTIP de LVN](lvn-getinfotip.md) .</span><span class="sxs-lookup"><span data-stu-id="bcb18-105">Sets tooltip text in delayed response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification.</span></span>

## <a name="parameters"></a><span data-ttu-id="bcb18-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bcb18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcb18-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bcb18-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bcb18-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="bcb18-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bcb18-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bcb18-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bcb18-110">Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> que contém as informações a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="bcb18-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcb18-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bcb18-111">Return value</span></span>

<span data-ttu-id="bcb18-112">Retornará **true** se o texto da dica de ferramenta for definido com êxito ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="bcb18-112">Returns **TRUE** if the tooltip text is set successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcb18-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bcb18-113">Remarks</span></span>

<span data-ttu-id="bcb18-114">A mensagem **LVM \_ SETINFOTIP** permite que um aplicativo Calcule Infotips em segundo plano executando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="bcb18-114">The **LVM\_SETINFOTIP** message lets an application calculate infotips in the background by performing the following steps:</span></span>

1.  <span data-ttu-id="bcb18-115">Em resposta à notificação [LVN \_ GETINFOTIP](lvn-getinfotip.md) , defina o membro **pszText** da estrutura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) como uma cadeia de caracteres vazia e retorne 0.</span><span class="sxs-lookup"><span data-stu-id="bcb18-115">In response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification, set the **pszText** member of the [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure to an empty string and return 0.</span></span>
2.  <span data-ttu-id="bcb18-116">Em segundo plano, COMPUTE o InfoTip.</span><span class="sxs-lookup"><span data-stu-id="bcb18-116">In the background, compute the infotip.</span></span>
3.  <span data-ttu-id="bcb18-117">Depois de computar o InfoTip, envie a mensagem **LVM \_ SETINFOTIP** , definindo o membro **pszText** da estrutura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) para o InfoTip e os membros **iItem** e **iSubItem** para o item e o subitem ao qual a InfoTip se aplica.</span><span class="sxs-lookup"><span data-stu-id="bcb18-117">After computing the infotip, send the **LVM\_SETINFOTIP** message, setting the **pszText** member of the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure to the infotip and the **iItem** and **iSubItem** members to the item and sub-item to which the infotip applies.</span></span>

<span data-ttu-id="bcb18-118">O texto passado para a **mensagem \_ SETINFOTIP do LVM** aparece apenas se o item e o subitem descritos pela estrutura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) ainda estiverem em um estado que exija um InfoTip</span><span class="sxs-lookup"><span data-stu-id="bcb18-118">The text passed to the **LVM\_SETINFOTIP** message appears only if the item and sub-item described by the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure are still in a state that requires an infotip</span></span>

> [!Note]  
> <span data-ttu-id="bcb18-119">Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="bcb18-119">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="bcb18-120">Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="bcb18-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bcb18-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bcb18-121">Requirements</span></span>



| <span data-ttu-id="bcb18-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="bcb18-122">Requirement</span></span> | <span data-ttu-id="bcb18-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bcb18-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb18-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcb18-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bcb18-125">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bcb18-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bcb18-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bcb18-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bcb18-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bcb18-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bcb18-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bcb18-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bcb18-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="bcb18-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





