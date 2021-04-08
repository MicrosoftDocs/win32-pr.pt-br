---
title: Mensagem de LB_SETLOCALE (WinUser. h)
description: Define a localidade atual da caixa de listagem. Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o \_ estilo de classificação lbs) e o texto adicionado pela mensagem do lb \_ AddString.
ms.assetid: e9503124-de9f-4b92-a59e-ec9320864ae7
keywords:
- Controles de LB_SETLOCALE de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_SETLOCALE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8ea7bb7b6d19144a84ab166f56cd2c0ad49e05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009652"
---
# <a name="lb_setlocale-message"></a><span data-ttu-id="70acf-105">\_Mensagem SETlocal do lb</span><span class="sxs-lookup"><span data-stu-id="70acf-105">LB\_SETLOCALE message</span></span>

<span data-ttu-id="70acf-106">Define a localidade atual da caixa de listagem.</span><span class="sxs-lookup"><span data-stu-id="70acf-106">Sets the current locale of the list box.</span></span> <span data-ttu-id="70acf-107">Você pode usar a localidade para determinar a ordem de classificação correta do texto exibido (para caixas de listagem com o estilo de [**\_ classificação lbs**](list-box-styles.md) ) e o texto adicionado pela mensagem do [**lb \_ AddString**](lb-addstring.md) .</span><span class="sxs-lookup"><span data-stu-id="70acf-107">You can use the locale to determine the correct sorting order of displayed text (for list boxes with the [**LBS\_SORT**](list-box-styles.md) style) and of text added by the [**LB\_ADDSTRING**](lb-addstring.md) message.</span></span>

## <a name="parameters"></a><span data-ttu-id="70acf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="70acf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70acf-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="70acf-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70acf-110">Especifica o identificador de localidade que a caixa de listagem usará para classificar ao adicionar texto.</span><span class="sxs-lookup"><span data-stu-id="70acf-110">Specifies the locale identifier that the list box will use for sorting when adding text.</span></span>

</dd> <dt>

<span data-ttu-id="70acf-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="70acf-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="70acf-112">Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="70acf-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70acf-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="70acf-113">Return value</span></span>

<span data-ttu-id="70acf-114">O valor de retorno é o identificador de localidade anterior.</span><span class="sxs-lookup"><span data-stu-id="70acf-114">The return value is the previous locale identifier.</span></span> <span data-ttu-id="70acf-115">Se o parâmetro *wParam* especificar uma localidade que não esteja instalada no sistema, o valor de retorno será lb \_ Err e a localidade da caixa de listagem atual não será alterada.</span><span class="sxs-lookup"><span data-stu-id="70acf-115">If the *wParam* parameter specifies a locale that is not installed on the system, the return value is LB\_ERR and the current list box locale is not changed.</span></span>

## <a name="remarks"></a><span data-ttu-id="70acf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="70acf-116">Remarks</span></span>

<span data-ttu-id="70acf-117">Use a macro [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) para construir um identificador de localidade.</span><span class="sxs-lookup"><span data-stu-id="70acf-117">Use the [**MAKELCID**](/windows/desktop/api/winnt/nf-winnt-makelcid) macro to construct a locale identifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="70acf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70acf-118">Requirements</span></span>



| <span data-ttu-id="70acf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="70acf-119">Requirement</span></span> | <span data-ttu-id="70acf-120">Valor</span><span class="sxs-lookup"><span data-stu-id="70acf-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70acf-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70acf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="70acf-122">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70acf-122">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="70acf-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="70acf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="70acf-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="70acf-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="70acf-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="70acf-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="70acf-126"><dt>WinUser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="70acf-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70acf-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="70acf-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="70acf-128">**Referência**</span><span class="sxs-lookup"><span data-stu-id="70acf-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="70acf-129">**seqüência de caracteres de LB \_**</span><span class="sxs-lookup"><span data-stu-id="70acf-129">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> <dt>

[<span data-ttu-id="70acf-130">**\_local lb**</span><span class="sxs-lookup"><span data-stu-id="70acf-130">**LB\_GETLOCALE**</span></span>](lb-getlocale.md)
</dt> </dl>

 

