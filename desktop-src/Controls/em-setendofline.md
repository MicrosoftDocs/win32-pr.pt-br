---
title: Mensagem de EM_SETENDOFLINE (CommCtrl. h)
description: Define o caractere de fim de linha usado quando um LineBreak é inserido.
ms.assetid: a10b3f57-0e67-4a0f-89f3-9c8ebd1514f8
keywords:
- Controles de EM_SETENDOFLINE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETENDOFLINE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 5ee7c500ba3818cad0f5ee74e9994ed8af049ea0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455764"
---
# <a name="em_setendofline-message"></a><span data-ttu-id="1947d-104">\_Mensagem em SETENDOFLINE</span><span class="sxs-lookup"><span data-stu-id="1947d-104">EM\_SETENDOFLINE message</span></span>

<span data-ttu-id="1947d-105">Define o caractere de fim de linha usado quando um LineBreak é inserido.</span><span class="sxs-lookup"><span data-stu-id="1947d-105">Sets the end-of-line character used when a linebreak is inserted.</span></span>

## <a name="parameters"></a><span data-ttu-id="1947d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1947d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1947d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1947d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1947d-108">Especifica o caractere de fim de linha usado quando um LineBreak é inserido.</span><span class="sxs-lookup"><span data-stu-id="1947d-108">Specifies the end-of-line character used when a linebreak is inserted.</span></span> <span data-ttu-id="1947d-109">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1947d-109">This can be one of the following values.</span></span>


| <span data-ttu-id="1947d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1947d-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="1947d-111">Significado</span><span class="sxs-lookup"><span data-stu-id="1947d-111">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="EC_ENDOFLINE_DETECTFROMCONTENT"></span><span id="ec_endofline_detectfromcontent"></span><dl> <span data-ttu-id="1947d-112"><dt>**EC \_ ENDOFLINE \_ DETECTFROMCONTENT**</dt></span><span class="sxs-lookup"><span data-stu-id="1947d-112"><dt>**EC\_ENDOFLINE\_DETECTFROMCONTENT**</dt></span></span> </dl> | <span data-ttu-id="1947d-113">Define o caractere de fim de linha usado para New quebras para o caractere usado pelo documento atual.</span><span class="sxs-lookup"><span data-stu-id="1947d-113">Sets the end-of-line character used for new linebreaks to the character used by the current document.</span></span><br/>  |
| <span id="EC_ENDOFLINE_CRLF"></span><span id="ec_endofline_crlf"></span><dl> <span data-ttu-id="1947d-114"><dt>**ENDOFLINE da EC \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1947d-114"><dt>**EC\_ENDOFLINE\_CRLF**</dt></span></span> </dl>                                        | <span data-ttu-id="1947d-115">Define o caractere de fim de linha usado para New quebras para retorno de carro seguido por linha de alimentação (CRLF).</span><span class="sxs-lookup"><span data-stu-id="1947d-115">Sets the end-of-line character used for new linebreaks to carriage return followed by linefeed (CRLF).</span></span><br/> |
| <span id="EC_ENDOFLINE_CR"></span><span id="ec_endofline_cr"></span><dl> <span data-ttu-id="1947d-116"><dt>**EC \_ ENDOFLINE \_ CR**</dt></span><span class="sxs-lookup"><span data-stu-id="1947d-116"><dt>**EC\_ENDOFLINE\_CR**</dt></span></span> </dl>                                              | <span data-ttu-id="1947d-117">Define o caractere de fim de linha usado para New quebras para retorno de carro (CR).</span><span class="sxs-lookup"><span data-stu-id="1947d-117">Sets the end-of-line character used for new linebreaks to carriage return (CR).</span></span><br/>                        |
| <span id="EC_ENDOFLINE_LF"></span><span id="ec_endofline_lf"></span><dl> <span data-ttu-id="1947d-118"><dt>**EC \_ ENDOFLINE \_ LF**</dt></span><span class="sxs-lookup"><span data-stu-id="1947d-118"><dt>**EC\_ENDOFLINE\_LF**</dt></span></span> </dl>                                              | <span data-ttu-id="1947d-119">Define o caractere de fim de linha usado para New quebras to avançoing (LF).</span><span class="sxs-lookup"><span data-stu-id="1947d-119">Sets the end-of-line character used for new linebreaks to linefeed (LF).</span></span><br/>                               |

</dd> <dt>

<span data-ttu-id="1947d-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1947d-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1947d-121">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="1947d-121">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1947d-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1947d-122">Return value</span></span>

<span data-ttu-id="1947d-123">Se a operação for concluída com sucesso, o valor de retorno será diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="1947d-123">If the operation succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="1947d-124">Se a operação falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="1947d-124">If the operation fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1947d-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="1947d-125">Remarks</span></span>

<span data-ttu-id="1947d-126">Quando o conjunto de caracteres de fim de linha é o **EC \_ ENDOFLINE \_ DETECTFROMCONTENT**, o controle de edição detecta apenas caracteres de fim de linha com suporte de acordo com seu estilo de janela estendido, consulte [Editar estilos estendidos de controle](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="1947d-126">When the end-of-line character set is **EC\_ENDOFLINE\_DETECTFROMCONTENT**, the edit control will only detect end-of-line characters supported according to its extended window style, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1947d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1947d-127">Requirements</span></span>



| <span data-ttu-id="1947d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1947d-128">Requirement</span></span> | <span data-ttu-id="1947d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1947d-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1947d-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1947d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1947d-131">\[Somente aplicativos de área de trabalho do Windows 10, 1809\]</span><span class="sxs-lookup"><span data-stu-id="1947d-131">Windows 10, 1809 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1947d-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1947d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1947d-133">\[Somente aplicativos da área de trabalho do Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="1947d-133">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1947d-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1947d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1947d-135"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1947d-135"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1947d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1947d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1947d-137">\**em \_ GETENDOFLINE*</span><span class="sxs-lookup"><span data-stu-id="1947d-137">\**EM\_GETENDOFLINE*</span></span>](em-getendofline.md)
</dt> </dl>

 

 





