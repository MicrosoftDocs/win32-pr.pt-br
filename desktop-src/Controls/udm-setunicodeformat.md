---
title: Mensagem de UDM_SETUNICODEFORMAT (commctrl. h)
description: Define o sinalizador de formato de caractere Unicode para o controle. Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.
ms.assetid: abe882db-bf32-40b0-a1c0-3e89cdc93fe7
keywords:
- Controles de UDM_SETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- UDM_SETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3f9dbc1e19fdb43aa0b7d5e6de6fdddd308eb6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009422"
---
# <a name="udm_setunicodeformat-message"></a><span data-ttu-id="6440a-105">\_Mensagem de SETUNICODEFORMAT UDM</span><span class="sxs-lookup"><span data-stu-id="6440a-105">UDM\_SETUNICODEFORMAT message</span></span>

<span data-ttu-id="6440a-106">Define o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="6440a-106">Sets the Unicode character format flag for the control.</span></span> <span data-ttu-id="6440a-107">Essa mensagem permite que você altere o conjunto de caracteres usado pelo controle em tempo de execução em vez de ter que recriar o controle.</span><span class="sxs-lookup"><span data-stu-id="6440a-107">This message allows you to change the character set used by the control at run time rather than having to re-create the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="6440a-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6440a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6440a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6440a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6440a-110">Determina o conjunto de caracteres que é usado pelo controle.</span><span class="sxs-lookup"><span data-stu-id="6440a-110">Determines the character set that is used by the control.</span></span> <span data-ttu-id="6440a-111">Se esse valor for **true**, o controle usará caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="6440a-111">If this value is **TRUE**, the control will use Unicode characters.</span></span> <span data-ttu-id="6440a-112">Se esse valor for **false**, o controle usará caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="6440a-112">If this value is **FALSE**, the control will use ANSI characters.</span></span>

</dd> <dt>

<span data-ttu-id="6440a-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6440a-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6440a-114">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6440a-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6440a-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6440a-115">Return value</span></span>

<span data-ttu-id="6440a-116">Retorna o sinalizador de formato Unicode anterior para o controle.</span><span class="sxs-lookup"><span data-stu-id="6440a-116">Returns the previous Unicode format flag for the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="6440a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6440a-117">Remarks</span></span>

<span data-ttu-id="6440a-118">Consulte os comentários para [**CCM \_ SETUNICODEFORMAT**](ccm-setunicodeformat.md) para uma discussão sobre esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="6440a-118">See the remarks for [**CCM\_SETUNICODEFORMAT**](ccm-setunicodeformat.md) for a discussion of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="6440a-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6440a-119">Requirements</span></span>



| <span data-ttu-id="6440a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="6440a-120">Requirement</span></span> | <span data-ttu-id="6440a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6440a-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6440a-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6440a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="6440a-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6440a-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6440a-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6440a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="6440a-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6440a-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6440a-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6440a-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="6440a-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6440a-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6440a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="6440a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6440a-129">**\_GETUNICODEFORMAT UDM**</span><span class="sxs-lookup"><span data-stu-id="6440a-129">**UDM\_GETUNICODEFORMAT**</span></span>](udm-getunicodeformat.md)
</dt> </dl>

 

 





