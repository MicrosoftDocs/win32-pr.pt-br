---
title: Mensagem de TB_SETUNICODEFORMAT (commctrl. h)
description: Define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.
ms.assetid: d4eec78d-c25b-4b86-9449-64f091cd8501
keywords:
- Controles de TB_SETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cf53a6c252690de8f9e001d34c1001d24aac57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824842"
---
# <a name="tb_setunicodeformat-message"></a><span data-ttu-id="77a25-105">TB de \_ mensagem SETUNICODEFORMAT</span><span class="sxs-lookup"><span data-stu-id="77a25-105">TB\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="77a25-106">Define o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="77a25-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="77a25-107">Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.</span><span class="sxs-lookup"><span data-stu-id="77a25-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="77a25-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77a25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77a25-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77a25-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77a25-110">Determina o conjunto de caracteres que é usado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="77a25-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="77a25-111">Se esse valor for diferente de zero, o controle usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="77a25-111">If this value is nonzero, the control will use Unicode characters.</span></span> <span data-ttu-id="77a25-112">Se esse valor for zero, o controle usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="77a25-112">If this value is zero, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="77a25-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77a25-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="77a25-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="77a25-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77a25-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77a25-115">Return value</span></span>

<span data-ttu-id="77a25-116">Retorna o sinalizador de formato Unicode anterior para o controle.</span><span class="sxs-lookup"><span data-stu-id="77a25-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="77a25-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="77a25-117">Remarks</span></span>

<span data-ttu-id="77a25-118">Consulte os comentários para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="77a25-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="77a25-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77a25-119">Requirements</span></span>



| <span data-ttu-id="77a25-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="77a25-120">Requirement</span></span> | <span data-ttu-id="77a25-121">Valor</span><span class="sxs-lookup"><span data-stu-id="77a25-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77a25-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77a25-122">Minimum supported client</span></span><br/> | <span data-ttu-id="77a25-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77a25-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77a25-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77a25-124">Minimum supported server</span></span><br/> | <span data-ttu-id="77a25-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77a25-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77a25-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77a25-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="77a25-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77a25-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77a25-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="77a25-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77a25-129">**TB de \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="77a25-129">**TB\_GETUNICODEFORMAT**</span></span>](tb-getunicodeformat.md)
</dt> </dl>

 

 





