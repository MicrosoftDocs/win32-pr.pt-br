---
title: Mensagem de EM_GETAUTOURLDETECT (RichEdit. h)
description: Indica se a detecção automática de URL está ativada no controle rich edit.
ms.assetid: f723f15c-bf8f-41ab-aef0-bd8f2c0b9e5d
keywords:
- Controles de EM_GETAUTOURLDETECT de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_GETAUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e68e4f2991c5f8780cb587594289674e07ec992
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009453"
---
# <a name="em_getautourldetect-message"></a><span data-ttu-id="f4d70-104">\_Mensagem em GETAUTOURLDETECT</span><span class="sxs-lookup"><span data-stu-id="f4d70-104">EM\_GETAUTOURLDETECT message</span></span>

<span data-ttu-id="f4d70-105">Indica se a detecção automática de URL está ativada no controle rich edit.</span><span class="sxs-lookup"><span data-stu-id="f4d70-105">Indicates whether the auto URL detection is turned on in the rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f4d70-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4d70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4d70-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f4d70-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4d70-108">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f4d70-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="f4d70-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f4d70-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f4d70-110">Não usado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="f4d70-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4d70-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f4d70-111">Return value</span></span>

<span data-ttu-id="f4d70-112">Se a detecção de URL automática estiver ativa, o valor de retorno será 1.</span><span class="sxs-lookup"><span data-stu-id="f4d70-112">If auto-URL detection is active, the return value is 1.</span></span>

<span data-ttu-id="f4d70-113">Se a detecção de URL automática estiver inativa, o valor de retorno será 0.</span><span class="sxs-lookup"><span data-stu-id="f4d70-113">If auto-URL detection is inactive, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4d70-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4d70-114">Remarks</span></span>

<span data-ttu-id="f4d70-115">Quando a detecção automática de URL está ativada, a edição rica da Microsoft está verificando constantemente o texto digitado em busca de uma URL válida.</span><span class="sxs-lookup"><span data-stu-id="f4d70-115">When auto URL detection is on, Microsoft Rich Edit is constantly checking typed text for a valid URL.</span></span> <span data-ttu-id="f4d70-116">O Rich Edit reconhece URLs que começam com estes prefixos:</span><span class="sxs-lookup"><span data-stu-id="f4d70-116">Rich Edit recognizes URLs that start with these prefixes:</span></span>

-   <span data-ttu-id="f4d70-117">http:</span><span class="sxs-lookup"><span data-stu-id="f4d70-117">http:</span></span>
-   <span data-ttu-id="f4d70-118">file:</span><span class="sxs-lookup"><span data-stu-id="f4d70-118">file:</span></span>
-   <span data-ttu-id="f4d70-119">mailto:</span><span class="sxs-lookup"><span data-stu-id="f4d70-119">mailto:</span></span>
-   <span data-ttu-id="f4d70-120">FTP</span><span class="sxs-lookup"><span data-stu-id="f4d70-120">ftp:</span></span>
-   <span data-ttu-id="f4d70-121">https</span><span class="sxs-lookup"><span data-stu-id="f4d70-121">https:</span></span>
-   <span data-ttu-id="f4d70-122">Gopher</span><span class="sxs-lookup"><span data-stu-id="f4d70-122">gopher:</span></span>
-   <span data-ttu-id="f4d70-123">NNTP</span><span class="sxs-lookup"><span data-stu-id="f4d70-123">nntp:</span></span>
-   <span data-ttu-id="f4d70-124">prospero:</span><span class="sxs-lookup"><span data-stu-id="f4d70-124">prospero:</span></span>
-   <span data-ttu-id="f4d70-125">estabelecer</span><span class="sxs-lookup"><span data-stu-id="f4d70-125">telnet:</span></span>
-   <span data-ttu-id="f4d70-126">Notícias</span><span class="sxs-lookup"><span data-stu-id="f4d70-126">news:</span></span>
-   <span data-ttu-id="f4d70-127">WAIS</span><span class="sxs-lookup"><span data-stu-id="f4d70-127">wais:</span></span>
-   <span data-ttu-id="f4d70-128">Outlook</span><span class="sxs-lookup"><span data-stu-id="f4d70-128">outlook:</span></span>

<span data-ttu-id="f4d70-129">A edição avançada também reconhece nomes de caminho padrão que começam com \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="f4d70-129">Rich Edit also recognizes standard path names that start with \\\\.</span></span> <span data-ttu-id="f4d70-130">Quando a edição avançada localiza uma URL, ela altera a cor do texto da URL, sublinha o texto e notifica o cliente usando o [ \_ link en](en-link.md).</span><span class="sxs-lookup"><span data-stu-id="f4d70-130">When Rich Edit locates a URL, it changes the URL text color, underlines the text, and notifies the client using [EN\_LINK](en-link.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4d70-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4d70-131">Requirements</span></span>



| <span data-ttu-id="f4d70-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4d70-132">Requirement</span></span> | <span data-ttu-id="f4d70-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f4d70-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4d70-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4d70-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f4d70-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4d70-135">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f4d70-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f4d70-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f4d70-137">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f4d70-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f4d70-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4d70-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4d70-139"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4d70-139"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4d70-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4d70-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4d70-141">\_link para</span><span class="sxs-lookup"><span data-stu-id="f4d70-141">EN\_LINK</span></span>](en-link.md)
</dt> </dl>

 

 





