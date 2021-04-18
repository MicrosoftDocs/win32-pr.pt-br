---
description: Coloca uma palavra alternativa e sua posição no objeto IWordSink.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: 'IWordSink: método utAltWord de:P (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761251"
---
# <a name="iwordsinkputaltword-method"></a><span data-ttu-id="5f540-103">IWordSink: método utAltWord de:P</span><span class="sxs-lookup"><span data-stu-id="5f540-103">IWordSink::PutAltWord method</span></span>

<span data-ttu-id="5f540-104">Coloca uma palavra alternativa e sua posição no objeto [**IWordSink**](iwordsink.md) .</span><span class="sxs-lookup"><span data-stu-id="5f540-104">Puts an alternative word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f540-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f540-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="5f540-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f540-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f540-107">*CWC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f540-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f540-108">O número de caracteres em *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="5f540-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="5f540-109">*pwcInBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f540-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f540-110">Um ponteiro para um buffer que contém uma forma alternativa de uma palavra do texto de origem.</span><span class="sxs-lookup"><span data-stu-id="5f540-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="5f540-111">Esse parâmetro não é modificado por **PutAltWord**.</span><span class="sxs-lookup"><span data-stu-id="5f540-111">This parameter is not modified by **PutAltWord**.</span></span> <span data-ttu-id="5f540-112">Você pode passar o parâmetro *pTextSource* de [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="5f540-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="5f540-113">*cwcSrcLen* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f540-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f540-114">O número de caracteres no buffer de texto de origem (indicado pelo parâmetro *pTextSource* para [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) que correspondem à palavra contida em *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="5f540-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="5f540-115">*cwcSrcPos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="5f540-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f540-116">A posição inicial da palavra em *pwcInBuf* no buffer de texto de origem (indicado pelo parâmetro *pTextSource* como [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="5f540-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f540-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f540-117">Return value</span></span>

<span data-ttu-id="5f540-118">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="5f540-118">This method can return one of these values.</span></span>



| <span data-ttu-id="5f540-119">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5f540-119">Return code</span></span>                                                                                              | <span data-ttu-id="5f540-120">Description</span><span class="sxs-lookup"><span data-stu-id="5f540-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5f540-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5f540-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="5f540-122">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="5f540-122">The operation was completed successfully.</span></span> <span data-ttu-id="5f540-123">Também indica que não há mais texto a ser processado.</span><span class="sxs-lookup"><span data-stu-id="5f540-123">Also indicates that no more text remains to be processed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="5f540-124"><dt>**Idioma \_ do \_ \_ palavra grande**</dt></span><span class="sxs-lookup"><span data-stu-id="5f540-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="5f540-125">O valor de *CWC* é maior que o valor de *UlMaxTokenSize* especificado em [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span><span class="sxs-lookup"><span data-stu-id="5f540-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="5f540-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f540-126">Remarks</span></span>

<span data-ttu-id="5f540-127">**PutAltWord** coloca uma forma alternativa de uma palavra no [**IWordSink**](iwordsink.md).</span><span class="sxs-lookup"><span data-stu-id="5f540-127">**PutAltWord** puts an alternative form of a word in the [**IWordSink**](iwordsink.md).</span></span> <span data-ttu-id="5f540-128">A palavra é colocada na mesma posição que a palavra original na fonte de texto (*pTextSource* em [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="5f540-128">The word is put in the same position as the original word in the text source (*pTextSource* in [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span> <span data-ttu-id="5f540-129">Por padrão, o **PutAltWord** encerra palavras com um tipo de quebra de WORDREP de interrupção de **\_ \_ EOW** do tipo enumerado de [**\_ quebra \_ de WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5f540-129">By default, **PutAltWord** terminates words with a **WORDREP\_BREAK\_EOW** break type from the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f540-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f540-130">Requirements</span></span>



| <span data-ttu-id="5f540-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f540-131">Requirement</span></span> | <span data-ttu-id="5f540-132">Valor</span><span class="sxs-lookup"><span data-stu-id="5f540-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5f540-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f540-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5f540-134">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5f540-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5f540-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5f540-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5f540-136">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="5f540-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5f540-137">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="5f540-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f540-138"><dt>Pesquisar. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f540-138"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f540-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f540-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f540-140">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="5f540-140">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
