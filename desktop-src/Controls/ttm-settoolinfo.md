---
title: Mensagem de TTM_SETTOOLINFO (commctrl. h)
description: Define as informações que um controle ToolTip mantém para uma ferramenta.
ms.assetid: ba18f651-2e52-46e2-871b-c1760e94ab59
keywords:
- Controles de TTM_SETTOOLINFO de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_SETTOOLINFO
- TTM_SETTOOLINFOA
- TTM_SETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 327dd853e3304f8233b95c947a890c4f49298cc7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455891"
---
# <a name="ttm_settoolinfo-message"></a><span data-ttu-id="0d824-104">\_Mensagem TTM SETTOOLINFO</span><span class="sxs-lookup"><span data-stu-id="0d824-104">TTM\_SETTOOLINFO message</span></span>

<span data-ttu-id="0d824-105">Define as informações que um controle ToolTip mantém para uma ferramenta.</span><span class="sxs-lookup"><span data-stu-id="0d824-105">Sets the information that a tooltip control maintains for a tool.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d824-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d824-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d824-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d824-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="0d824-108">Deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0d824-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="0d824-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d824-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d824-110">Ponteiro para uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que especifica as informações a serem definidas.</span><span class="sxs-lookup"><span data-stu-id="0d824-110">Pointer to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that specifies the information to set.</span></span> <span data-ttu-id="0d824-111">O membro **cbSize** desta estrutura deve ser definido antes de enviar esta mensagem.</span><span class="sxs-lookup"><span data-stu-id="0d824-111">The **cbSize** member of this structure must be set before sending this message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d824-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d824-112">Return value</span></span>

<span data-ttu-id="0d824-113">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="0d824-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d824-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d824-114">Remarks</span></span>

<span data-ttu-id="0d824-115">Algumas propriedades internas de uma ferramenta são estabelecidas quando a ferramenta é criada e não são recomputadas quando uma mensagem **TTM \_ SETTOOLINFO** é enviada.</span><span class="sxs-lookup"><span data-stu-id="0d824-115">Some internal properties of a tool are established when the tool is created, and are not recomputed when a **TTM\_SETTOOLINFO** message is sent.</span></span> <span data-ttu-id="0d824-116">Se você simplesmente atribuir valores a uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) e passá-lo para o controle ToolTip com uma mensagem **TTM \_ SETTOOLINFO** , essas propriedades poderão ser perdidas.</span><span class="sxs-lookup"><span data-stu-id="0d824-116">If you simply assign values to a [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure and pass it to the tooltip control with a **TTM\_SETTOOLINFO** message, these properties may be lost.</span></span> <span data-ttu-id="0d824-117">Em vez disso, seu aplicativo deve primeiro solicitar a estrutura **TOOLINFO** atual da ferramenta enviando o controle ToolTip a uma mensagem [**TTM \_ GETTOOLINFO**](ttm-gettoolinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="0d824-117">Instead, your application should first request the tool's current **TOOLINFO** structure by sending the tooltip control a [**TTM\_GETTOOLINFO**](ttm-gettoolinfo.md) message.</span></span> <span data-ttu-id="0d824-118">Em seguida, modifique os membros dessa estrutura conforme necessário e passe-os de volta para o controle ToolTip com **TTM \_ SETTOOLINFO**.</span><span class="sxs-lookup"><span data-stu-id="0d824-118">Then, modify the members of this structure as needed and pass it back to the tooltip control with **TTM\_SETTOOLINFO**.</span></span>

<span data-ttu-id="0d824-119">Ao chamar **TTM \_ SETTOOLINFO**, a cadeia de caracteres apontada pelo membro **lpszText** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) não deve exceder 80 **TCHARs** de comprimento, incluindo o **nulo** de terminação.</span><span class="sxs-lookup"><span data-stu-id="0d824-119">When calling **TTM\_SETTOOLINFO**, the string pointed to by the **lpszText** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure must not exceed 80 **TCHARs** in length, including the terminating **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d824-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d824-120">Requirements</span></span>



| <span data-ttu-id="0d824-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d824-121">Requirement</span></span> | <span data-ttu-id="0d824-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0d824-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d824-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d824-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0d824-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d824-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d824-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d824-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0d824-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d824-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d824-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d824-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d824-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d824-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="0d824-129">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="0d824-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="0d824-130">**TTM \_ SETTOOLINFOW** (Unicode) e **TTM \_ SETTOOLINFOA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="0d824-130">**TTM\_SETTOOLINFOW** (Unicode) and **TTM\_SETTOOLINFOA** (ANSI)</span></span><br/>           |



 

 





