---
title: Mensagem de EM_SETEDITSTYLE (RichEdit. h)
description: Define os sinalizadores de estilo de edição atuais para um controle de edição rico.
ms.assetid: e48de6b3-0fd2-4791-9863-a6dcdafa3642
keywords:
- Controles de EM_SETEDITSTYLE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14c7b7e1d3990a00fb6931ed39bbd28aa6f8c2ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499672"
---
# <a name="em_seteditstyle-message"></a><span data-ttu-id="24783-104">\_Mensagem em SETeditstyle</span><span class="sxs-lookup"><span data-stu-id="24783-104">EM\_SETEDITSTYLE message</span></span>

<span data-ttu-id="24783-105">Define os sinalizadores de estilo de edição atuais para um controle de edição rico.</span><span class="sxs-lookup"><span data-stu-id="24783-105">Sets the current edit style flags for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="24783-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24783-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24783-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="24783-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24783-108">Especifica um ou mais sinalizadores de estilo de edição.</span><span class="sxs-lookup"><span data-stu-id="24783-108">Specifies one or more edit style flags.</span></span> <span data-ttu-id="24783-109">Para obter uma lista de valores possíveis, consulte em [**\_ GetEditStyle**](em-geteditstyle.md).</span><span class="sxs-lookup"><span data-stu-id="24783-109">For a list of possible values, see [**EM\_GETEDITSTYLE**](em-geteditstyle.md).</span></span>

</dd> <dt>

<span data-ttu-id="24783-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="24783-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="24783-111">Uma máscara que consiste em um ou mais dos valores *wParam* .</span><span class="sxs-lookup"><span data-stu-id="24783-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="24783-112">Somente os valores especificados nesta máscara serão definidos ou apagados.</span><span class="sxs-lookup"><span data-stu-id="24783-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="24783-113">Isso permite que um único sinalizador seja definido ou limpo sem a leitura dos Estados de sinalizador atuais.</span><span class="sxs-lookup"><span data-stu-id="24783-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24783-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24783-114">Return value</span></span>

<span data-ttu-id="24783-115">O valor de retorno é o estado dos sinalizadores de estilo de edição depois que o controle de edição rico tentou implementar as alterações de estilo de edição.</span><span class="sxs-lookup"><span data-stu-id="24783-115">The return value is the state of the edit style flags after the rich edit control has attempted to implement your edit style changes.</span></span> <span data-ttu-id="24783-116">Os sinalizadores de estilo de edição são um conjunto de sinalizadores que indicam o estilo de edição atual.</span><span class="sxs-lookup"><span data-stu-id="24783-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="24783-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24783-117">Requirements</span></span>



| <span data-ttu-id="24783-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="24783-118">Requirement</span></span> | <span data-ttu-id="24783-119">Valor</span><span class="sxs-lookup"><span data-stu-id="24783-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="24783-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24783-120">Minimum supported client</span></span><br/> | <span data-ttu-id="24783-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="24783-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="24783-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="24783-122">Minimum supported server</span></span><br/> | <span data-ttu-id="24783-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="24783-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="24783-124">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="24783-124">Redistributable</span></span><br/>          | <span data-ttu-id="24783-125">Edição avançada 3,0</span><span class="sxs-lookup"><span data-stu-id="24783-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="24783-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24783-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="24783-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="24783-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24783-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="24783-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24783-129">**em \_ GETeditstyle**</span><span class="sxs-lookup"><span data-stu-id="24783-129">**EM\_GETEDITSTYLE**</span></span>](em-geteditstyle.md)
</dt> </dl>

 

 





