---
title: Mensagem de CCM_GETUNICODEFORMAT (commctrl. h)
description: Obtém o sinalizador de formato de caractere Unicode para o controle.
ms.assetid: 8a23cd1c-549e-4d48-891a-b37dbf5c524b
keywords:
- Controles de CCM_GETUNICODEFORMAT de mensagens do Windows
topic_type:
- apiref
api_name:
- CCM_GETUNICODEFORMAT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095d49ccc57faa05e86d12df130b12ce3d542bf6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085834"
---
# <a name="ccm_getunicodeformat-message"></a><span data-ttu-id="1e82c-104">CCM \_ GETUNICODEFORMAT mensagem</span><span class="sxs-lookup"><span data-stu-id="1e82c-104">CCM\_GETUNICODEFORMAT message</span></span>

<span data-ttu-id="1e82c-105">Obtém o sinalizador de formato de caractere Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="1e82c-105">Gets the Unicode character format flag for the control.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e82c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e82c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e82c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e82c-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="1e82c-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1e82c-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="1e82c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e82c-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="1e82c-110">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="1e82c-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e82c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e82c-111">Return value</span></span>

<span data-ttu-id="1e82c-112">Retorna o sinalizador de formato Unicode para o controle.</span><span class="sxs-lookup"><span data-stu-id="1e82c-112">Returns the Unicode format flag for the control.</span></span> <span data-ttu-id="1e82c-113">Se esse valor for diferente de zero, o controle estará usando caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="1e82c-113">If this value is nonzero, the control is using Unicode characters.</span></span> <span data-ttu-id="1e82c-114">Se esse valor for zero, o controle estará usando caracteres ANSI.</span><span class="sxs-lookup"><span data-stu-id="1e82c-114">If this value is zero, the control is using ANSI characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e82c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e82c-115">Requirements</span></span>



| <span data-ttu-id="1e82c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e82c-116">Requirement</span></span> | <span data-ttu-id="1e82c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="1e82c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e82c-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e82c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1e82c-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e82c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e82c-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e82c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1e82c-121">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1e82c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e82c-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e82c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e82c-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e82c-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e82c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e82c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e82c-125">**CCM \_ SETUNICODEFORMAT**</span><span class="sxs-lookup"><span data-stu-id="1e82c-125">**CCM\_SETUNICODEFORMAT**</span></span>](ccm-setunicodeformat.md)
</dt> </dl>

 

 





