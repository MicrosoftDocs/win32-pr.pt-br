---
title: Mensagem de EM_SELECTIONTYPE (RichEdit. h)
description: Determina o tipo de seleção para um controle de edição rico.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- Controles de EM_SELECTIONTYPE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499676"
---
# <a name="em_selectiontype-message"></a><span data-ttu-id="7e027-104">\_Mensagem de SelectionType em</span><span class="sxs-lookup"><span data-stu-id="7e027-104">EM\_SELECTIONTYPE message</span></span>

<span data-ttu-id="7e027-105">Determina o tipo de seleção para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="7e027-105">Determines the selection type for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e027-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e027-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e027-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e027-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e027-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7e027-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7e027-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e027-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e027-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="7e027-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e027-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7e027-111">Return value</span></span>

<span data-ttu-id="7e027-112">Se a seleção estiver vazia, o valor de retorno será \_ vazio.</span><span class="sxs-lookup"><span data-stu-id="7e027-112">If the selection is empty, the return value is SEL\_EMPTY.</span></span>

<span data-ttu-id="7e027-113">Se a seleção não estiver vazia, o valor de retorno será um conjunto de sinalizadores contendo um ou mais dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7e027-113">If the selection is not empty, the return value is a set of flags containing one or more of the following values.</span></span>



| <span data-ttu-id="7e027-114">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7e027-114">Return code</span></span>                                                                                     | <span data-ttu-id="7e027-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e027-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="7e027-116"><dt>**texto do SEL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7e027-116"><dt>**SEL\_TEXT**</dt></span></span> </dl>        | <span data-ttu-id="7e027-117">Text.</span><span class="sxs-lookup"><span data-stu-id="7e027-117">Text.</span></span><br/>                            |
| <dl> <span data-ttu-id="7e027-118"><dt>**\_objeto SEL**</dt></span><span class="sxs-lookup"><span data-stu-id="7e027-118"><dt>**SEL\_OBJECT**</dt></span></span> </dl>      | <span data-ttu-id="7e027-119">Pelo menos um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="7e027-119">At least one COM object.</span></span><br/>         |
| <dl> <span data-ttu-id="7e027-120"><dt>**multichar de SEL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7e027-120"><dt>**SEL\_MULTICHAR**</dt></span></span> </dl>   | <span data-ttu-id="7e027-121">Mais de um caractere de texto.</span><span class="sxs-lookup"><span data-stu-id="7e027-121">More than one character of text.</span></span><br/> |
| <dl> <span data-ttu-id="7e027-122"><dt>**multiobjeto SEL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7e027-122"><dt>**SEL\_MULTIOBJECT**</dt></span></span> </dl> | <span data-ttu-id="7e027-123">Mais de um objeto COM.</span><span class="sxs-lookup"><span data-stu-id="7e027-123">More than one COM object.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="7e027-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e027-124">Remarks</span></span>

<span data-ttu-id="7e027-125">Essa mensagem é útil durante o processamento de [**\_ tamanho do WM**](/windows/desktop/winmsg/wm-size) para o pai de um controle de edição com formatação inferior.</span><span class="sxs-lookup"><span data-stu-id="7e027-125">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e027-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e027-126">Requirements</span></span>



| <span data-ttu-id="7e027-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e027-127">Requirement</span></span> | <span data-ttu-id="7e027-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7e027-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e027-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e027-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7e027-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7e027-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7e027-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e027-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7e027-132">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7e027-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e027-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7e027-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e027-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e027-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e027-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e027-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e027-136">**tamanho do WM \_**</span><span class="sxs-lookup"><span data-stu-id="7e027-136">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

