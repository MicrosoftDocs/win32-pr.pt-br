---
description: A interface IWordInfo é um componente de recurso de linguagem específico do japonês. O objeto analisa o texto e identifica palavras individuais, retornando as palavras na cadeia de caracteres ou retorna os formulários de dicionário (raiz) das palavras no texto da cadeia de caracteres.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: Interface IWordInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 9d685f2aa1b4ba4d31f221812c12729e4e689360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500781"
---
# <a name="iwordinfo-interface"></a><span data-ttu-id="731ca-104">Interface IWordInfo</span><span class="sxs-lookup"><span data-stu-id="731ca-104">IWordInfo interface</span></span>

<span data-ttu-id="731ca-105">\[Essa interface é obsoleta e não tem suporte no Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="731ca-105">\[This interface is obsolete and is not supported on Windows Vista.\]</span></span>

<span data-ttu-id="731ca-106">A interface **IWordInfo** é um componente de recurso de linguagem específico do japonês.</span><span class="sxs-lookup"><span data-stu-id="731ca-106">The **IWordInfo** interface is a Japanese-specific language resource component.</span></span> <span data-ttu-id="731ca-107">O objeto analisa o texto e identifica palavras individuais, retornando as palavras na cadeia de caracteres ou retorna os formulários de dicionário (raiz) das palavras no texto da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="731ca-107">The object parses text and identifies individual words, returning either the words in the string or returns the dictionary (root) forms of the words in the text of the string.</span></span>

## <a name="members"></a><span data-ttu-id="731ca-108">Membros</span><span class="sxs-lookup"><span data-stu-id="731ca-108">Members</span></span>

<span data-ttu-id="731ca-109">A interface **IWordInfo** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="731ca-109">The **IWordInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="731ca-110">**IWordInfo** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="731ca-110">**IWordInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="731ca-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="731ca-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="731ca-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="731ca-112">Methods</span></span>

<span data-ttu-id="731ca-113">A interface **IWordInfo** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="731ca-113">The **IWordInfo** interface has these methods.</span></span>



| <span data-ttu-id="731ca-114">Método</span><span class="sxs-lookup"><span data-stu-id="731ca-114">Method</span></span>        | <span data-ttu-id="731ca-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="731ca-115">Description</span></span>                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="731ca-116">**BreakText**</span><span class="sxs-lookup"><span data-stu-id="731ca-116">**BreakText**</span></span> | <span data-ttu-id="731ca-117">Analisa o texto para identificar palavras e fornece os resultados para o objeto [WordSink](/previous-versions//ms691570(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="731ca-117">Parses text to identify words and provides the results to the [WordSink](/previous-versions//ms691570(v=vs.85)) object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="731ca-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="731ca-118">Remarks</span></span>

<span data-ttu-id="731ca-119">Essa interface é usada para recuperar as quebras de palavra japonesas ou os formulários de dicionário para o texto a ser analisado.</span><span class="sxs-lookup"><span data-stu-id="731ca-119">This interface is used to retrieve Japanese word breaks or dictionary forms for the text to be analyzed.</span></span> <span data-ttu-id="731ca-120">A forma de dicionário de uma palavra é a forma uninflected da palavra.</span><span class="sxs-lookup"><span data-stu-id="731ca-120">The dictionary form of a word is the uninflected form of the word.</span></span>

## <a name="requirements"></a><span data-ttu-id="731ca-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="731ca-121">Requirements</span></span>



| <span data-ttu-id="731ca-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="731ca-122">Requirement</span></span> | <span data-ttu-id="731ca-123">Valor</span><span class="sxs-lookup"><span data-stu-id="731ca-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="731ca-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="731ca-124">Minimum supported client</span></span><br/> | <span data-ttu-id="731ca-125">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="731ca-125">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="731ca-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="731ca-126">Minimum supported server</span></span><br/> | <span data-ttu-id="731ca-127">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="731ca-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="731ca-128">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="731ca-128">End of client support</span></span><br/>    | <span data-ttu-id="731ca-129">Windows XP</span><span class="sxs-lookup"><span data-stu-id="731ca-129">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="731ca-130">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="731ca-130">End of server support</span></span><br/>    | <span data-ttu-id="731ca-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="731ca-131">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="731ca-132">DLL</span><span class="sxs-lookup"><span data-stu-id="731ca-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="731ca-133"><dt>Msir3jp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="731ca-133"><dt>Msir3jp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="731ca-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="731ca-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="731ca-135">**WordInfo**</span><span class="sxs-lookup"><span data-stu-id="731ca-135">**WordInfo**</span></span>](wordinfo-coclass.md)
</dt> <dt>

<span data-ttu-id="731ca-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="731ca-136">[WordSink](/previous-versions//ms691570(v=vs.85))</span></span>
</dt> </dl>

 

 
