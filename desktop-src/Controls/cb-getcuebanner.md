---
title: Mensagem de CB_GETCUEBANNER (WinUser. h)
description: Obtém o texto da faixa de indicação exibido no controle de edição de uma caixa de combinação. Envie essa mensagem explicitamente ou usando a \_ macro GetCueBannerText da ComboBox.
ms.assetid: 38959228-9f07-4636-a1ea-681efe77b9ec
keywords:
- Controles de CB_GETCUEBANNER de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETCUEBANNER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866f51df0083c4cd72c3f34bb3ce045e0f577a24
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824533"
---
# <a name="cb_getcuebanner-message"></a><span data-ttu-id="8fc01-105">\_Mensagem de GETCUEBANNER CB</span><span class="sxs-lookup"><span data-stu-id="8fc01-105">CB\_GETCUEBANNER message</span></span>

<span data-ttu-id="8fc01-106">Obtém o texto da faixa de indicação exibido no controle de edição de uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="8fc01-106">Gets the cue banner text displayed in the edit control of a combo box.</span></span> <span data-ttu-id="8fc01-107">Envie essa mensagem explicitamente ou usando a macro [**\_ GetCueBannerText da ComboBox**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) .</span><span class="sxs-lookup"><span data-stu-id="8fc01-107">Send this message explicitly or by using the [**ComboBox\_GetCueBannerText**](/windows/desktop/api/Commctrl/nf-commctrl-combobox_getcuebannertext) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fc01-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8fc01-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc01-109">*wParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8fc01-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc01-110">Um ponteiro para um buffer de cadeia de caracteres Unicode que recebe o texto da faixa de indicação.</span><span class="sxs-lookup"><span data-stu-id="8fc01-110">A pointer to a Unicode string buffer that receives the cue banner text.</span></span> <span data-ttu-id="8fc01-111">O aplicativo de chamada é responsável por alocar a memória para o buffer.</span><span class="sxs-lookup"><span data-stu-id="8fc01-111">The calling application is responsible for allocating the memory for the buffer.</span></span> <span data-ttu-id="8fc01-112">O tamanho do buffer deve ser igual ao tamanho da cadeia de caracteres do banner de indicação em **WCHARs**, mais 1 para o encerramento **nulo** de **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="8fc01-112">The buffer size must be equal to the length of the cue banner string in **WCHARs**, plus 1 for the terminating **NULL** **WCHAR**.</span></span>

</dd> <dt>

<span data-ttu-id="8fc01-113">*lParam* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8fc01-113">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc01-114">O tamanho do buffer apontado por *lpcwText* em **WCHAR**.</span><span class="sxs-lookup"><span data-stu-id="8fc01-114">The size of the buffer pointed to by *lpcwText* in **WCHARs**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc01-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8fc01-115">Return value</span></span>

<span data-ttu-id="8fc01-116">Retornará 1 se for bem-sucedido ou um valor de erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="8fc01-116">Returns 1 if successful, or an error value otherwise.</span></span>

<span data-ttu-id="8fc01-117">Se não houver nenhum texto de faixa de indicação a ser obtido, o valor de retorno será 0.</span><span class="sxs-lookup"><span data-stu-id="8fc01-117">If there is no cue banner text to get, the return value is 0.</span></span> <span data-ttu-id="8fc01-118">Se o aplicativo de chamada falhar em alocar um buffer ou definir *lParam* antes de enviar essa mensagem, o comportamento indefinido poderá ser resultado e o valor de retorno poderá não ser confiável.</span><span class="sxs-lookup"><span data-stu-id="8fc01-118">If the calling application fails to allocate a buffer, or set *lParam* before sending this message, undefined behavior may result and the return value may not be reliable.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc01-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fc01-119">Requirements</span></span>



| <span data-ttu-id="8fc01-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fc01-120">Requirement</span></span> | <span data-ttu-id="8fc01-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8fc01-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc01-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fc01-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc01-123">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8fc01-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8fc01-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fc01-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc01-125">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8fc01-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8fc01-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8fc01-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fc01-127"><dt>CommCtrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fc01-127"><dt>CommCtrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fc01-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8fc01-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc01-129">Recursos da caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="8fc01-129">Combo Box Features</span></span>](combo-box-features.md)
</dt> </dl>

 

 





