---
title: Mensagem de EM_GETTEXTRANGE (RichEdit. h)
description: Recupera um intervalo de caracteres especificado de um controle de edição rico.
ms.assetid: 18398963-eb2c-4f64-99f5-9614a5d34b52
keywords:
- Controles de EM_GETTEXTRANGE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTRANGE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d68c4089bbe2cc09daa39d69e9094a4abaead787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918882"
---
# <a name="em_gettextrange-message"></a><span data-ttu-id="77abd-104">\_Mensagem em GETtextrange</span><span class="sxs-lookup"><span data-stu-id="77abd-104">EM\_GETTEXTRANGE message</span></span>

<span data-ttu-id="77abd-105">Recupera um intervalo de caracteres especificado de um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="77abd-105">Retrieves a specified range of characters from a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="77abd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77abd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77abd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77abd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77abd-108">Esse parâmetro não é usado; Ele deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="77abd-108">This parameter is not used; it must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="77abd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77abd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77abd-110">Ponteiro para uma estrutura [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) que especifica o intervalo de caracteres a serem recuperados e um buffer no qual os caracteres são copiados.</span><span class="sxs-lookup"><span data-stu-id="77abd-110">Pointer to a [**TEXTRANGE**](/windows/win32/api/richedit/ns-richedit-textrangea) structure that specifies the range of characters to retrieve and a buffer to copy the characters to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77abd-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77abd-111">Return value</span></span>

<span data-ttu-id="77abd-112">A mensagem retorna o número de caracteres copiados, não incluindo o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="77abd-112">The message returns the number of characters copied, not including the terminating null character.</span></span>

## <a name="requirements"></a><span data-ttu-id="77abd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77abd-113">Requirements</span></span>



| <span data-ttu-id="77abd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="77abd-114">Requirement</span></span> | <span data-ttu-id="77abd-115">Valor</span><span class="sxs-lookup"><span data-stu-id="77abd-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77abd-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77abd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="77abd-117">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77abd-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77abd-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77abd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="77abd-119">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77abd-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77abd-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77abd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="77abd-121"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="77abd-121"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77abd-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="77abd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77abd-123">**TEXTRANGE**</span><span class="sxs-lookup"><span data-stu-id="77abd-123">**TEXTRANGE**</span></span>](/windows/win32/api/richedit/ns-richedit-textrangea)
</dt> </dl>

 

 





