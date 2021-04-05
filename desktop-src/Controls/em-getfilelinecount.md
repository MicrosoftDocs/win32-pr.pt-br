---
title: Mensagem de EM_GETFILELINECOUNT (CommCtrl. h)
description: Obtém o número de linhas em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- Controles de EM_GETFILELINECOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085940"
---
# <a name="em_getfilelinecount-message-commctrlh"></a><span data-ttu-id="40705-104">Mensagem de EM_GETFILELINECOUNT (CommCtrl. h)</span><span class="sxs-lookup"><span data-stu-id="40705-104">EM_GETFILELINECOUNT message (CommCtrl.h)</span></span>

<span data-ttu-id="40705-105">Obtém o número de linhas em um controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.</span><span class="sxs-lookup"><span data-stu-id="40705-105">Gets the number of lines in a multiline edit control, independently of how lines are displayed on the screen.</span></span>

## <a name="parameters"></a><span data-ttu-id="40705-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40705-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40705-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="40705-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40705-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="40705-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="40705-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40705-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40705-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="40705-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40705-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="40705-111">Return value</span></span>

<span data-ttu-id="40705-112">O valor de retorno é um inteiro que especifica o número total de linhas de texto no controle de edição de várias linhas, independentemente de como as linhas são exibidas na tela.</span><span class="sxs-lookup"><span data-stu-id="40705-112">The return value is an integer specifying the total number of text lines in the multiline edit control, independently of how lines are displayed on the screen.</span></span> <span data-ttu-id="40705-113">Se o controle não tiver texto, o valor de retorno será 1.</span><span class="sxs-lookup"><span data-stu-id="40705-113">If the control has no text, the return value is 1.</span></span> <span data-ttu-id="40705-114">O valor de retorno nunca será menor que 1.</span><span class="sxs-lookup"><span data-stu-id="40705-114">The return value will never be less than 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="40705-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="40705-115">Remarks</span></span>

<span data-ttu-id="40705-116">A mensagem em **\_ GETFILELINECOUNT** recupera o número total de linhas de texto, independentemente de como as linhas são exibidas na tela, e não apenas o número de linhas que estão visíveis no momento.</span><span class="sxs-lookup"><span data-stu-id="40705-116">The **EM\_GETFILELINECOUNT** message retrieves the total number of text lines, independently of how lines are displayed on the screen, not just the number of lines that are currently visible.</span></span>

<span data-ttu-id="40705-117">A quebra automática de linha não altera o número de linhas que essa mensagem retorna, pois essa mensagem funciona independentemente de como as linhas são exibidas na tela.</span><span class="sxs-lookup"><span data-stu-id="40705-117">Word-wrap does not change the number of lines this message returns, as this message works independently of how lines are displayed on the screen.</span></span>

## <a name="requirements"></a><span data-ttu-id="40705-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40705-118">Requirements</span></span>



| <span data-ttu-id="40705-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="40705-119">Requirement</span></span> | <span data-ttu-id="40705-120">Valor</span><span class="sxs-lookup"><span data-stu-id="40705-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40705-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40705-121">Minimum supported client</span></span><br/> | <span data-ttu-id="40705-122">\[Somente aplicativos de área de trabalho do Windows 10, 1809\]</span><span class="sxs-lookup"><span data-stu-id="40705-122">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="40705-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="40705-123">Minimum supported server</span></span><br/> | <span data-ttu-id="40705-124">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="40705-124">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="40705-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="40705-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="40705-126"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="40705-126"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40705-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="40705-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="40705-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="40705-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="40705-129">**em \_ GETfilee**</span><span class="sxs-lookup"><span data-stu-id="40705-129">**EM\_GETFILELINE**</span></span>](em-getfileline.md)
</dt> <dt>

[<span data-ttu-id="40705-130">**em \_ FILELINELENGTH**</span><span class="sxs-lookup"><span data-stu-id="40705-130">**EM\_FILELINELENGTH**</span></span>](em-filelinelength.md)
</dt> <dt>

[<span data-ttu-id="40705-131">**Editar \_ GetFileLineCount**</span><span class="sxs-lookup"><span data-stu-id="40705-131">**Edit\_GetFileLineCount**</span></span>](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





