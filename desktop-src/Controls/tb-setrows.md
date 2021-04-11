---
title: Mensagem de TB_SETROWS (commctrl. h)
description: Define o número de linhas de botões em uma barra de ferramentas.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- Controles de TB_SETROWS de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0065a3f5f6a277713e368177886ebd064ea132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009772"
---
# <a name="tb_setrows-message"></a><span data-ttu-id="a6c01-104">Mensagem de TB \_ SETrows</span><span class="sxs-lookup"><span data-stu-id="a6c01-104">TB\_SETROWS message</span></span>

<span data-ttu-id="a6c01-105">Define o número de linhas de botões em uma barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a6c01-105">Sets the number of rows of buttons in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="a6c01-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6c01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6c01-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6c01-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6c01-108">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o número de linhas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="a6c01-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the number of rows requested.</span></span> <span data-ttu-id="a6c01-109">O número mínimo de linhas é um, e o número máximo de linhas é igual ao número de botões na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="a6c01-109">The minimum number of rows is one, and the maximum number of rows is equal to the number of buttons in the toolbar.</span></span>

<span data-ttu-id="a6c01-110">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) é um **bool** que indica se é necessário criar mais linhas do que o solicitado quando o sistema não pode criar o número de linhas especificado por *wParam*.</span><span class="sxs-lookup"><span data-stu-id="a6c01-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **BOOL** that indicates whether to create more rows than requested when the system cannot create the number of rows specified by *wParam*.</span></span> <span data-ttu-id="a6c01-111">Se **for true**, o sistema criará mais linhas.</span><span class="sxs-lookup"><span data-stu-id="a6c01-111">If **TRUE**, the system creates more rows.</span></span> <span data-ttu-id="a6c01-112">Se **for false**, o sistema criará menos linhas.</span><span class="sxs-lookup"><span data-stu-id="a6c01-112">If **FALSE**, the system creates fewer rows.</span></span>

</dd> <dt>

<span data-ttu-id="a6c01-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6c01-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6c01-114">Ponteiro para uma estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe o retângulo delimitador da barra de ferramentas depois que as linhas são definidas.</span><span class="sxs-lookup"><span data-stu-id="a6c01-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the toolbar after the rows are set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6c01-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6c01-115">Return value</span></span>

<span data-ttu-id="a6c01-116">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="a6c01-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6c01-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6c01-117">Remarks</span></span>

<span data-ttu-id="a6c01-118">Como o sistema não divide os grupos de botões ao definir o número de linhas, o número resultante de linhas pode ser diferente do número solicitado.</span><span class="sxs-lookup"><span data-stu-id="a6c01-118">Because the system does not break up button groups when setting the number of rows, the resulting number of rows might differ from the number requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6c01-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6c01-119">Requirements</span></span>



| <span data-ttu-id="a6c01-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6c01-120">Requirement</span></span> | <span data-ttu-id="a6c01-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a6c01-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6c01-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6c01-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a6c01-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a6c01-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6c01-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a6c01-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a6c01-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6c01-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6c01-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6c01-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6c01-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6c01-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

