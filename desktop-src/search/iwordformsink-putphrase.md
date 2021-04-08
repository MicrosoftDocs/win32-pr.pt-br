---
description: Coloca uma forma alternativa de uma palavra no objeto IWordFormSink.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: 'IWordFormSink: método utAltWord de:P (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 43539bbf67e23bc37ca92f6a961b945ae581e746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646864"
---
# <a name="iwordformsinkputaltword-method"></a><span data-ttu-id="0f6c8-103">IWordFormSink: método utAltWord de:P</span><span class="sxs-lookup"><span data-stu-id="0f6c8-103">IWordFormSink::PutAltWord method</span></span>

<span data-ttu-id="0f6c8-104">Coloca uma forma alternativa de uma palavra no objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .</span><span class="sxs-lookup"><span data-stu-id="0f6c8-104">Puts an alternative form of a word in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f6c8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f6c8-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="0f6c8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f6c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f6c8-107">*pwcInBuf* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f6c8-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6c8-108">Um ponteiro para um buffer que contém uma forma alternativa de uma palavra.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-108">A pointer to a buffer that contains an alternative form of a word.</span></span>

</dd> <dt>

<span data-ttu-id="0f6c8-109">*CWC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0f6c8-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6c8-110">O número de caracteres em *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f6c8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0f6c8-111">Return value</span></span>

<span data-ttu-id="0f6c8-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="0f6c8-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0f6c8-113">Return code</span></span>                                                                                              | <span data-ttu-id="0f6c8-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f6c8-114">Description</span></span>                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f6c8-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f6c8-115"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="0f6c8-116">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-116">The operation was completed successfully.</span></span> <br/>                                                                                             |
| <dl> <span data-ttu-id="0f6c8-117"><dt>**Idioma \_ do \_ \_ palavra grande**</dt></span><span class="sxs-lookup"><span data-stu-id="0f6c8-117"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="0f6c8-118">O valor de *CWC* é maior que o valor de *UlMaxTokenSize* especificado em [**IStemmer:: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span><span class="sxs-lookup"><span data-stu-id="0f6c8-118">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IStemmer::Init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f6c8-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f6c8-119">Remarks</span></span>

<span data-ttu-id="0f6c8-120">Esse método é chamado a partir do método [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) da implementação [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) .</span><span class="sxs-lookup"><span data-stu-id="0f6c8-120">This method is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="0f6c8-121">Todas as formas alternativas para uma palavra, exceto a última, são colocadas no objeto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) chamando **IWordFormSink::P utaltword**.</span><span class="sxs-lookup"><span data-stu-id="0f6c8-121">All alternative forms for a word, except the last, are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling **IWordFormSink::PutAltWord**.</span></span> <span data-ttu-id="0f6c8-122">A forma alternativa final de uma palavra, que é sempre a forma original da palavra, é tratada chamando [**IWordFormSink::P utword**](iwordformsink-putword.md).</span><span class="sxs-lookup"><span data-stu-id="0f6c8-122">The final alternative form of a word, which is always the original form of the word, is handled by calling [**IWordFormSink::PutWord**](iwordformsink-putword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f6c8-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f6c8-123">Requirements</span></span>



| <span data-ttu-id="0f6c8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f6c8-124">Requirement</span></span> | <span data-ttu-id="0f6c8-125">Valor</span><span class="sxs-lookup"><span data-stu-id="0f6c8-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6c8-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f6c8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0f6c8-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0f6c8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0f6c8-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f6c8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0f6c8-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0f6c8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0f6c8-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0f6c8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f6c8-131"><dt>Pesquisar. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f6c8-131"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f6c8-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f6c8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6c8-133">**IWordFormSink**</span><span class="sxs-lookup"><span data-stu-id="0f6c8-133">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
