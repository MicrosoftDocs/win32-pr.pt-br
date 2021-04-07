---
title: Mensagem de EM_SETEDITSTYLEEX (RichEdit. h)
description: Define os sinalizadores de estilo de edição estendida atuais.
ms.assetid: C5CECC7C-6418-4A72-9F0B-6F55BE89E302
keywords:
- Controles de EM_SETEDITSTYLEEX de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fe7a1ff420048f620d69196360678e9718a510
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918984"
---
# <a name="em_seteditstyleex-message"></a><span data-ttu-id="a48b1-104">\_Mensagem em SETEDITSTYLEEX</span><span class="sxs-lookup"><span data-stu-id="a48b1-104">EM\_SETEDITSTYLEEX message</span></span>

<span data-ttu-id="a48b1-105">Define os sinalizadores de estilo de edição estendida atuais.</span><span class="sxs-lookup"><span data-stu-id="a48b1-105">Sets the current extended edit style flags.</span></span>


```C++
#define EM_SETEDITSTYLEEX       (WM_USER + 275)
```



## <a name="parameters"></a><span data-ttu-id="a48b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a48b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a48b1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a48b1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a48b1-108">Especifica um ou mais sinalizadores de estilo de edição estendida.</span><span class="sxs-lookup"><span data-stu-id="a48b1-108">Specifies one or more extended edit style flags.</span></span> <span data-ttu-id="a48b1-109">Para obter uma lista de valores possíveis, consulte em [**\_ GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).</span><span class="sxs-lookup"><span data-stu-id="a48b1-109">For a list of possible values, see [**EM\_GETEDITSTYLEEX**](/windows/desktop/Controls/em-geteditstyleex).</span></span>

</dd> <dt>

<span data-ttu-id="a48b1-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a48b1-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a48b1-111">Uma máscara que consiste em um ou mais dos valores *wParam* .</span><span class="sxs-lookup"><span data-stu-id="a48b1-111">A mask consisting of one or more of the *wParam* values.</span></span> <span data-ttu-id="a48b1-112">Somente os valores especificados nesta máscara serão definidos ou apagados.</span><span class="sxs-lookup"><span data-stu-id="a48b1-112">Only the values specified in this mask will be set or cleared.</span></span> <span data-ttu-id="a48b1-113">Isso permite que um único sinalizador seja definido ou limpo sem a leitura dos Estados de sinalizador atuais.</span><span class="sxs-lookup"><span data-stu-id="a48b1-113">This allows a single flag to be set or cleared without reading the current flag states.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a48b1-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a48b1-114">Return value</span></span>

<span data-ttu-id="a48b1-115">O valor de retorno é o estado dos sinalizadores de estilo de edição estendida depois que a edição avançada tentou implementar as alterações de estilo de edição.</span><span class="sxs-lookup"><span data-stu-id="a48b1-115">The return value is the state of the extended edit style flags after rich edit has attempted to implement your edit style changes.</span></span> <span data-ttu-id="a48b1-116">Os sinalizadores de estilo de edição são um conjunto de sinalizadores que indicam o estilo de edição atual.</span><span class="sxs-lookup"><span data-stu-id="a48b1-116">The edit style flags are a set of flags that indicate the current edit style.</span></span>

## <a name="requirements"></a><span data-ttu-id="a48b1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a48b1-117">Requirements</span></span>



| <span data-ttu-id="a48b1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a48b1-118">Requirement</span></span> | <span data-ttu-id="a48b1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a48b1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a48b1-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a48b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a48b1-121">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a48b1-121">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a48b1-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a48b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a48b1-123">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a48b1-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a48b1-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a48b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a48b1-125"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="a48b1-125"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a48b1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a48b1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a48b1-127">**em \_ GETEDITSTYLEEX**</span><span class="sxs-lookup"><span data-stu-id="a48b1-127">**EM\_GETEDITSTYLEEX**</span></span>](em-geteditstyleex.md)
</dt> </dl>

 

