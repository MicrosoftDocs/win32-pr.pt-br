---
description: Coloca uma quebra após a palavra anterior.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: 'IWordSink: método utBreak de:P (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296235"
---
# <a name="iwordsinkputbreak-method"></a><span data-ttu-id="f7956-103">IWordSink: método utBreak de:P</span><span class="sxs-lookup"><span data-stu-id="f7956-103">IWordSink::PutBreak method</span></span>

<span data-ttu-id="f7956-104">Coloca uma quebra após a palavra anterior.</span><span class="sxs-lookup"><span data-stu-id="f7956-104">Puts a break after the preceding word.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7956-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7956-105">Syntax</span></span>


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a><span data-ttu-id="f7956-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7956-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7956-107">*breaktype* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7956-107">*breakType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7956-108">Um valor de [**\_ \_ tipo de quebra de WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) que indica o tipo de quebra que o WordSink insere após a palavra anterior.</span><span class="sxs-lookup"><span data-stu-id="f7956-108">A value from [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) that indicates the type of break that the WordSink inserts after the preceding word.</span></span> <span data-ttu-id="f7956-109">Cada quebra ocupa uma posição exclusiva no índice.</span><span class="sxs-lookup"><span data-stu-id="f7956-109">Each break occupies a unique position in the index.</span></span> <span data-ttu-id="f7956-110">Portanto, inserir quebras entre palavras altera a distância relativa entre palavras.</span><span class="sxs-lookup"><span data-stu-id="f7956-110">Therefore, inserting breaks between words changes the relative distance between words.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7956-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7956-111">Return value</span></span>

<span data-ttu-id="f7956-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="f7956-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f7956-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f7956-113">Return code</span></span>                                                                          | <span data-ttu-id="f7956-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f7956-114">Description</span></span>                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="f7956-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f7956-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f7956-116">A operação foi concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="f7956-116">The operation was completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7956-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7956-117">Remarks</span></span>

<span data-ttu-id="f7956-118">Os métodos [**IWordSinkPutWord**](iwordsink-putword.md) e [**IWordSink::P utaltword**](iwordsink-putaltword.md) inserem automaticamente uma quebra de fim de palavra (EOW, indicada pelo \_ elemento WORDREP Break EOW \_ do tipo enumerado [**de \_ \_ tipo de interrupção WORDREP**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) ) após cada palavra.</span><span class="sxs-lookup"><span data-stu-id="f7956-118">The [**IWordSinkPutWord**](iwordsink-putword.md) and [**IWordSink::PutAltWord**](iwordsink-putaltword.md) methods automatically insert an end-of-word break (EOW, indicated by the WORDREP\_BREAK\_EOW element of the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type) after each word.</span></span> <span data-ttu-id="f7956-119">Chame o método **PutBreak** para inserir um tipo de quebra diferente do fim da palavra.</span><span class="sxs-lookup"><span data-stu-id="f7956-119">Call the **PutBreak** method to insert a break type other than end of word.</span></span> <span data-ttu-id="f7956-120">Esse método não altera o buffer de texto de origem (*pSourceText*) ou incrementa a contagem de caracteres (*CWC*).</span><span class="sxs-lookup"><span data-stu-id="f7956-120">This method does not change the source text buffer (*pSourceText*) or increment the character count (*cwc*).</span></span> <span data-ttu-id="f7956-121">No entanto, ele incrementa a posição atual no índice e afeta os resultados da consulta.</span><span class="sxs-lookup"><span data-stu-id="f7956-121">However, it does increment the current position in the index and affects query results.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7956-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7956-122">Requirements</span></span>



| <span data-ttu-id="f7956-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7956-123">Requirement</span></span> | <span data-ttu-id="f7956-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f7956-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f7956-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7956-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f7956-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f7956-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f7956-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7956-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f7956-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f7956-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f7956-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f7956-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7956-130"><dt>Pesquisar. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7956-130"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7956-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7956-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7956-132">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="f7956-132">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
