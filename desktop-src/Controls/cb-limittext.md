---
title: Mensagem de CB_LIMITTEXT (WinUser. h)
description: Limita o comprimento do texto que o usuário pode digitar no controle de edição de uma caixa de combinação.
ms.assetid: 95b7d07a-594b-4096-afbb-4dab77bdc41d
keywords:
- Controles de CB_LIMITTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_LIMITTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34ea9ccd63bb1503e73aebdd584a53bc32bcb8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009355"
---
# <a name="cb_limittext-message"></a><span data-ttu-id="62462-104">\_Mensagem de LIMITTEXT CB</span><span class="sxs-lookup"><span data-stu-id="62462-104">CB\_LIMITTEXT message</span></span>

<span data-ttu-id="62462-105">Limita o comprimento do texto que o usuário pode digitar no controle de edição de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="62462-105">Limits the length of the text the user may type into the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="62462-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62462-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62462-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="62462-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62462-108">O número máximo de **TCHARs** que o usuário pode inserir, não incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="62462-108">The maximum number of **TCHARs** the user can enter, not including the terminating null character.</span></span> <span data-ttu-id="62462-109">Se esse parâmetro for zero, o tamanho do texto será limitado a 0x7FFFFFFE caracteres.</span><span class="sxs-lookup"><span data-stu-id="62462-109">If this parameter is zero, the text length is limited to 0x7FFFFFFE characters.</span></span>

</dd> <dt>

<span data-ttu-id="62462-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="62462-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="62462-111">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="62462-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62462-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62462-112">Return value</span></span>

<span data-ttu-id="62462-113">O valor de retorno é sempre **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="62462-113">The return value is always **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="62462-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="62462-114">Remarks</span></span>

<span data-ttu-id="62462-115">Se a caixa de combinação não tiver o estilo [**CBS \_ AUTOHSCROLL**](combo-box-styles.md) , definir o limite de texto como maior que o tamanho do controle de edição não terá nenhum efeito.</span><span class="sxs-lookup"><span data-stu-id="62462-115">If the combo box does not have the [**CBS\_AUTOHSCROLL**](combo-box-styles.md) style, setting the text limit to be larger than the size of the edit control has no effect.</span></span>

<span data-ttu-id="62462-116">A mensagem **CB \_ LIMITTEXT** limita apenas o texto que o usuário pode inserir.</span><span class="sxs-lookup"><span data-stu-id="62462-116">The **CB\_LIMITTEXT** message limits only the text the user can enter.</span></span> <span data-ttu-id="62462-117">Ele não tem nenhum efeito em nenhum texto que já esteja no controle de edição quando a mensagem é enviada, nem afeta o comprimento do texto copiado para o controle de edição quando uma cadeia de caracteres na caixa de listagem é selecionada.</span><span class="sxs-lookup"><span data-stu-id="62462-117">It has no effect on any text already in the edit control when the message is sent, nor does it affect the length of the text copied to the edit control when a string in the list box is selected.</span></span>

<span data-ttu-id="62462-118">O limite padrão para o texto que um usuário pode inserir no controle de edição é 30.000 **TCHARs**.</span><span class="sxs-lookup"><span data-stu-id="62462-118">The default limit to the text a user can enter in the edit control is 30,000 **TCHARs**.</span></span>

## <a name="requirements"></a><span data-ttu-id="62462-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62462-119">Requirements</span></span>



| <span data-ttu-id="62462-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="62462-120">Requirement</span></span> | <span data-ttu-id="62462-121">Valor</span><span class="sxs-lookup"><span data-stu-id="62462-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62462-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62462-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62462-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="62462-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="62462-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62462-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62462-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="62462-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="62462-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="62462-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="62462-127"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62462-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



 

 





