---
title: Mensagem de SB_GETTIPTEXT (commctrl. h)
description: Recupera o texto da dica de ferramenta de uma parte em uma barra de status. A barra de status deve ser criada com o \_ estilo de dicas de ferramenta SBT para habilitar dicas de ferramenta.
ms.assetid: a3936830-a855-4ef6-b179-3aa3730cd0b8
keywords:
- Controles de SB_GETTIPTEXT de mensagens do Windows
topic_type:
- apiref
api_name:
- SB_GETTIPTEXT
- SB_GETTIPTEXTA
- SB_GETTIPTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d492bc19f82300f460666b3213c545fe95b8db85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824622"
---
# <a name="sb_gettiptext-message"></a><span data-ttu-id="a721e-105">\_Mensagem de GETTIPTEXT SB</span><span class="sxs-lookup"><span data-stu-id="a721e-105">SB\_GETTIPTEXT message</span></span>

<span data-ttu-id="a721e-106">Recupera o texto da dica de ferramenta de uma parte em uma barra de status.</span><span class="sxs-lookup"><span data-stu-id="a721e-106">Retrieves the tooltip text for a part in a status bar.</span></span> <span data-ttu-id="a721e-107">A barra de status deve ser criada com o estilo de [**\_ dicas de ferramenta SBT**](status-bar-styles.md) para habilitar dicas de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="a721e-107">The status bar must be created with the [**SBT\_TOOLTIPS**](status-bar-styles.md) style to enable tooltips.</span></span>

## <a name="parameters"></a><span data-ttu-id="a721e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a721e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a721e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a721e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a721e-110">O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica o índice de base zero da parte que recebe o texto da dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="a721e-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the part that receives the tooltip text.</span></span> <span data-ttu-id="a721e-111">O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o tamanho do buffer em *lParam*, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="a721e-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the size of the buffer at *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="a721e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a721e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a721e-113">Ponteiro para um buffer de caracteres que recebe o texto da dica de ferramenta.</span><span class="sxs-lookup"><span data-stu-id="a721e-113">Pointer to a character buffer that receives the tooltip text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a721e-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a721e-114">Return value</span></span>

<span data-ttu-id="a721e-115">O valor de retorno não é usado.</span><span class="sxs-lookup"><span data-stu-id="a721e-115">The return value is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="a721e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="a721e-116">Remarks</span></span>

<span data-ttu-id="a721e-117">**Aviso de segurança:** Usar essa mensagem incorretamente pode causar problemas para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a721e-117">**Security Warning:** Using this message incorrectly can cause problems for your application.</span></span> <span data-ttu-id="a721e-118">Por exemplo, se o texto for muito grande para o buffer *lParam* , ele poderá causar um estouro de buffer.</span><span class="sxs-lookup"><span data-stu-id="a721e-118">For example, if the text is too large for the *lParam* buffer, it could cause a buffer overflow.</span></span> <span data-ttu-id="a721e-119">Você deve examinar as [considerações de segurança: controles do Microsoft Windows](sec-comctls.md) antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="a721e-119">You should review the [Security Considerations: Microsoft Windows Controls](sec-comctls.md) before continuing.</span></span>

## <a name="requirements"></a><span data-ttu-id="a721e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a721e-120">Requirements</span></span>



| <span data-ttu-id="a721e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a721e-121">Requirement</span></span> | <span data-ttu-id="a721e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a721e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a721e-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a721e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a721e-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a721e-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a721e-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a721e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a721e-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a721e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a721e-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a721e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a721e-128"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a721e-128"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="a721e-129">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="a721e-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a721e-130">**SB \_ GETTIPTEXTW** (Unicode) e **SB \_ GETTIPTEXTA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a721e-130">**SB\_GETTIPTEXTW** (Unicode) and **SB\_GETTIPTEXTA** (ANSI)</span></span><br/>               |



 

