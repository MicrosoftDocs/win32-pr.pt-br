---
description: Coloca uma palavra e sua posição no objeto IWordSink.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: 'IWordSink: método utWord de:P (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 5f622e09c2b82bc8de986dafcc83247617caec75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813574"
---
# <a name="iwordsinkputword-method"></a><span data-ttu-id="e8464-103">IWordSink: método utWord de:P</span><span class="sxs-lookup"><span data-stu-id="e8464-103">IWordSink::PutWord method</span></span>

<span data-ttu-id="e8464-104">Coloca uma palavra e sua posição no objeto [**IWordSink**](iwordsink.md) .</span><span class="sxs-lookup"><span data-stu-id="e8464-104">Puts a word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8464-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8464-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="e8464-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8464-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8464-107">*CWC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8464-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8464-108">O número de caracteres em *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="e8464-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="e8464-109">*pwcInBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8464-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8464-110">Um ponteiro para um buffer que contém uma forma alternativa de uma palavra do texto de origem.</span><span class="sxs-lookup"><span data-stu-id="e8464-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="e8464-111">Esse parâmetro não é modificado por **PutWord**.</span><span class="sxs-lookup"><span data-stu-id="e8464-111">This parameter is not modified by **PutWord**.</span></span> <span data-ttu-id="e8464-112">Você pode passar o parâmetro *pTextSource* de [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="e8464-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="e8464-113">*cwcSrcLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8464-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8464-114">O número de caracteres no buffer de texto de origem (indicado pelo parâmetro *pTextSource* para [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) que correspondem à palavra contida em *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="e8464-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="e8464-115">*cwcSrcPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e8464-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8464-116">A posição inicial da palavra em *pwcInBuf* no buffer de texto de origem (indicado pelo parâmetro *pTextSource* como [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="e8464-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8464-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e8464-117">Return value</span></span>

<span data-ttu-id="e8464-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="e8464-118">This method can return one of these values.</span></span>



| <span data-ttu-id="e8464-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="e8464-119">Return code</span></span>                                                                                              | <span data-ttu-id="e8464-120">Description</span><span class="sxs-lookup"><span data-stu-id="e8464-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8464-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8464-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="e8464-122">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="e8464-122">The operation was completed successfully.</span></span> <span data-ttu-id="e8464-123">Também indica que não há mais texto disponível para reabastecer o buffer.</span><span class="sxs-lookup"><span data-stu-id="e8464-123">Also indicates that no more text is available to refill the buffer.</span></span><br/>                                  |
| <dl> <span data-ttu-id="e8464-124"><dt>**Idioma \_ do \_ \_ palavra grande**</dt></span><span class="sxs-lookup"><span data-stu-id="e8464-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="e8464-125">O valor de *CWC* é maior que o valor de *UlMaxTokenSize* especificado em [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span><span class="sxs-lookup"><span data-stu-id="e8464-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="e8464-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8464-126">Remarks</span></span>

<span data-ttu-id="e8464-127">Recomendamos que o método **IWordSink::P utword** sempre contenha a palavra original como encontrada em *pTextSource*.</span><span class="sxs-lookup"><span data-stu-id="e8464-127">We recommend that the **IWordSink::PutWord** method always contain the original word as found in *pTextSource*.</span></span> <span data-ttu-id="e8464-128">Formas alternativas da palavra são passadas para WordSink usando [**IWordSink::P utaltword**](iwordsink-putaltword.md).</span><span class="sxs-lookup"><span data-stu-id="e8464-128">Alternative forms of the word are passed to WordSink by using [**IWordSink::PutAltWord**](iwordsink-putaltword.md).</span></span> <span data-ttu-id="e8464-129">Também recomendamos que as palavras em *pwcInBuf* correspondam ao texto de origem o mais próximo possível.</span><span class="sxs-lookup"><span data-stu-id="e8464-129">We also recommend that the words in *pwcInBuf* match the source text as closely as possible.</span></span> <span data-ttu-id="e8464-130">Por exemplo, mantenha a capitalização e os acentos sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="e8464-130">For example, retain capitalization and accents where possible.</span></span>

<span data-ttu-id="e8464-131">Essa chamada deve ser feita para cada palavra recuperada de *pTextSource* , exceto aquelas para as quais a chamada [**IWordSink::P utaltword**](iwordsink-putaltword.md) foi feita.</span><span class="sxs-lookup"><span data-stu-id="e8464-131">This call must be made for every word retrieved from *pTextSource* except those for which the [**IWordSink::PutAltWord**](iwordsink-putaltword.md) call was made.</span></span> <span data-ttu-id="e8464-132">A palavra é terminada com um caractere EOW quando é salva no WordSink.</span><span class="sxs-lookup"><span data-stu-id="e8464-132">The word is terminated with an EOW character when it is saved to the WordSink.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8464-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8464-133">Requirements</span></span>



| <span data-ttu-id="e8464-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8464-134">Requirement</span></span> | <span data-ttu-id="e8464-135">Valor</span><span class="sxs-lookup"><span data-stu-id="e8464-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e8464-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8464-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e8464-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e8464-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e8464-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8464-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e8464-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e8464-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e8464-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e8464-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8464-141"><dt>Pesquisar. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8464-141"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8464-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8464-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8464-143">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="e8464-143">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
