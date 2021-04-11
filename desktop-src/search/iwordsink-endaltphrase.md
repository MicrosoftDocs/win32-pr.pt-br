---
description: Indica o fim da frase final em uma sequência de frases alternativas que um separador de palavras gera durante o tempo do índice.
ms.assetid: 50E4E208-A290-42B7-9152-9472C01B20D5
title: 'Método IWordSink:: EndAltPhrase (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.EndAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 4056357de5e3e479124e8f9a91d9b3d906300709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164325"
---
# <a name="iwordsinkendaltphrase-method"></a><span data-ttu-id="0d123-103">Método IWordSink:: EndAltPhrase</span><span class="sxs-lookup"><span data-stu-id="0d123-103">IWordSink::EndAltPhrase method</span></span>

<span data-ttu-id="0d123-104">Indica o fim da frase final em uma sequência de frases alternativas que um separador de palavras gera durante o tempo do índice.</span><span class="sxs-lookup"><span data-stu-id="0d123-104">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d123-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d123-105">Syntax</span></span>


```C++
HRESULT EndAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="0d123-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d123-106">Parameters</span></span>

<span data-ttu-id="0d123-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0d123-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0d123-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0d123-108">Return value</span></span>

<span data-ttu-id="0d123-109">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="0d123-109">This method can return one of these values.</span></span>



| <span data-ttu-id="0d123-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0d123-110">Return code</span></span>                                                                                           | <span data-ttu-id="0d123-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="0d123-111">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d123-112"><dt>**\_ \_ somente consulta WBREAK \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="0d123-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="0d123-113">[**EndAltPhrase**](iwordsink-endaltphrase.md) é chamado durante o tempo de consulta.</span><span class="sxs-lookup"><span data-stu-id="0d123-113">[**EndAltPhrase**](iwordsink-endaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0d123-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d123-114">Remarks</span></span>

<span data-ttu-id="0d123-115">Implementações de [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) chamam **IWordSink:: EndAltPhrase** do método [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) para encerrar uma sequência de frases alternativas.</span><span class="sxs-lookup"><span data-stu-id="0d123-115">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations call **IWordSink::EndAltPhrase** from the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method to terminate a sequence of alternative phrases.</span></span> <span data-ttu-id="0d123-116">O método [**IWordSink:: StartAltPhrase**](iwordsink-startaltphrase.md) é chamado para indicar o final de uma frase e o início de outra em uma sequência de frases.</span><span class="sxs-lookup"><span data-stu-id="0d123-116">The [**IWordSink::StartAltPhrase**](iwordsink-startaltphrase.md) method is called to indicate the end of one phrase and the beginning of another in a sequence of phrases.</span></span> <span data-ttu-id="0d123-117">Somente a última frase em uma sequência é encerrada com uma chamada para **EndAltPhrase**.</span><span class="sxs-lookup"><span data-stu-id="0d123-117">Only the last phrase in a sequence is terminated with a call to **EndAltPhrase**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d123-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d123-118">Requirements</span></span>



| <span data-ttu-id="0d123-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d123-119">Requirement</span></span> | <span data-ttu-id="0d123-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0d123-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0d123-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d123-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0d123-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0d123-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0d123-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d123-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0d123-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0d123-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0d123-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0d123-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d123-126"><dt>Pesquisar. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d123-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d123-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d123-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d123-128">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="0d123-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
