---
title: Mensagem de BCM_GETNOTE (commctrl. h)
description: Obtém o texto da nota associada a um botão de link de comando. Você pode enviar essa mensagem explicitamente ou usar a macro do botão \_ getnote.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- Controles de BCM_GETNOTE de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752950"
---
# <a name="bcm_getnote-message"></a><span data-ttu-id="77149-105">\_Mensagem de GETnote do BCM</span><span class="sxs-lookup"><span data-stu-id="77149-105">BCM\_GETNOTE message</span></span>

<span data-ttu-id="77149-106">Obtém o texto da nota associada a um botão de link de comando.</span><span class="sxs-lookup"><span data-stu-id="77149-106">Gets the text of the note associated with a command link button.</span></span> <span data-ttu-id="77149-107">Você pode enviar essa mensagem explicitamente ou usar a macro do [**botão \_ getnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .</span><span class="sxs-lookup"><span data-stu-id="77149-107">You can send this message explicitly or use the [**Button\_GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="77149-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="77149-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77149-109">*wParam* \[ entrada, saída\]</span><span class="sxs-lookup"><span data-stu-id="77149-109">*wParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="77149-110">Um **DWORD** que especifica o tamanho do buffer apontado por *lParam*, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="77149-110">A **DWORD** that specifies the size of the buffer pointed to by *lParam*, in characters.</span></span>

</dd> <dt>

<span data-ttu-id="77149-111">*lParam* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="77149-111">*lParam* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77149-112">O buffer de cadeia de caracteres para receber o texto.</span><span class="sxs-lookup"><span data-stu-id="77149-112">The string buffer to receive the text.</span></span> <span data-ttu-id="77149-113">O buffer deve ser grande o suficiente para acomodar o caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="77149-113">The buffer must be large enough to accommodate the terminating NULL character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77149-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="77149-114">Return value</span></span>

<span data-ttu-id="77149-115">Se a mensagem tiver sucesso, retornará **true**.</span><span class="sxs-lookup"><span data-stu-id="77149-115">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="77149-116">Caso contrário, retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="77149-116">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="77149-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="77149-117">Remarks</span></span>

<span data-ttu-id="77149-118">A mensagem do **BCM \_ getnote** funciona apenas com botões que têm o estilo de botão [**BS \_ COMMANDLINK**](button-styles.md) ou [**BS \_ DEFCOMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="77149-118">The **BCM\_GETNOTE** message works only with buttons that have the [**BS\_COMMANDLINK**](button-styles.md) or [**BS\_DEFCOMMANDLINK**](button-styles.md) button style.</span></span>

<span data-ttu-id="77149-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) conterá:</span><span class="sxs-lookup"><span data-stu-id="77149-119">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will contain:</span></span>

-   <span data-ttu-id="77149-120">\_Não \_ há suporte para o erro, se o botão não tiver o estilo [**BS \_ DEFCOMMANDLINK**](button-styles.md) ou [**BS \_ COMMANDLINK**](button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="77149-120">ERROR\_NOT\_SUPPORTED, if the button does not have the [**BS\_DEFCOMMANDLINK**](button-styles.md) or [**BS\_COMMANDLINK**](button-styles.md) style.</span></span>
-   <span data-ttu-id="77149-121">ERRO \_ \_ de buffer insuficiente se o buffer de *lParam* for muito pequeno.</span><span class="sxs-lookup"><span data-stu-id="77149-121">ERROR\_INSUFFICIENT\_BUFFER, if the *lParam* buffer is too small.</span></span> <span data-ttu-id="77149-122">O parâmetro *wParam* conterá o tamanho de buffer necessário, em caracteres.</span><span class="sxs-lookup"><span data-stu-id="77149-122">The *wParam* parameter will contain the required buffer size, in characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="77149-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77149-123">Requirements</span></span>



| <span data-ttu-id="77149-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="77149-124">Requirement</span></span> | <span data-ttu-id="77149-125">Valor</span><span class="sxs-lookup"><span data-stu-id="77149-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77149-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77149-126">Minimum supported client</span></span><br/> | <span data-ttu-id="77149-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77149-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77149-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="77149-128">Minimum supported server</span></span><br/> | <span data-ttu-id="77149-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77149-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77149-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77149-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="77149-131"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="77149-131"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77149-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="77149-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="77149-133">**Referência**</span><span class="sxs-lookup"><span data-stu-id="77149-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="77149-134">Estilos de botão</span><span class="sxs-lookup"><span data-stu-id="77149-134">Button Styles</span></span>](button-styles.md)
</dt> <dt>

<span data-ttu-id="77149-135">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="77149-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="77149-136">Tipos de botão</span><span class="sxs-lookup"><span data-stu-id="77149-136">Button Types</span></span>](button-types-and-styles.md)
</dt> </dl>

 

