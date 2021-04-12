---
title: Mensagem de CCM_SETUNICODEFORMAT (commctrl. h)
description: Define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.
ms.assetid: 8028b7d7-30d2-4154-81c7-ba1ed095ef02
keywords:
- Controles de CCM_SETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- CCM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffbe9f5032c193cb612f68ca8ed6ec6b04ce8094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455450"
---
# <a name="ccm_setunicodeformat-message"></a><span data-ttu-id="b0fc7-105">CCM \_ SETUNICODEFORMAT mensagem</span><span class="sxs-lookup"><span data-stu-id="b0fc7-105">CCM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="b0fc7-106">Define o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="b0fc7-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="b0fc7-107">Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.</span><span class="sxs-lookup"><span data-stu-id="b0fc7-107">This message enables you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0fc7-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0fc7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0fc7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0fc7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0fc7-110">Um valor que determina o conjunto de caracteres que é usado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="b0fc7-110">A value that determines the character set that is used by the control.</span></span> <span data-ttu-id="b0fc7-111">Se esse valor for **true**, o controle usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="b0fc7-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="b0fc7-112">Se esse valor for **false**, o controle usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="b0fc7-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="b0fc7-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0fc7-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b0fc7-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b0fc7-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0fc7-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b0fc7-115">Return value</span></span>

<span data-ttu-id="b0fc7-116">Retorna o sinalizador de formato Unicode anterior para o controle.</span><span class="sxs-lookup"><span data-stu-id="b0fc7-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0fc7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0fc7-117">Requirements</span></span>



| <span data-ttu-id="b0fc7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0fc7-118">Requirement</span></span> | <span data-ttu-id="b0fc7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b0fc7-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0fc7-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0fc7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b0fc7-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b0fc7-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0fc7-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0fc7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b0fc7-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b0fc7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0fc7-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b0fc7-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0fc7-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0fc7-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0fc7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0fc7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0fc7-127">**CCM \_ GETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="b0fc7-127">**CCM\_GETUNICODEFORMAT**</span></span>](ccm-getunicodeformat.md)
</dt> </dl>

 

 





