---
description: Indica o limite entre as frases em uma sequência de frases alternativas que um separador de palavras gera durante o tempo de indexação.
ms.assetid: 3F3B6761-887B-426E-A44F-E636397180C7
title: 'Método IWordSink:: StartAltPhrase (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.StartAltPhrase
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: e4e35c5ed75016292dd420e7a832c6cfb780284a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164324"
---
# <a name="iwordsinkstartaltphrase-method"></a><span data-ttu-id="9e34e-103">Método IWordSink:: StartAltPhrase</span><span class="sxs-lookup"><span data-stu-id="9e34e-103">IWordSink::StartAltPhrase method</span></span>

<span data-ttu-id="9e34e-104">Indica o limite entre as frases em uma sequência de frases alternativas que um separador de palavras gera durante o tempo de indexação.</span><span class="sxs-lookup"><span data-stu-id="9e34e-104">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e34e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e34e-105">Syntax</span></span>


```C++
HRESULT StartAltPhrase();
```



## <a name="parameters"></a><span data-ttu-id="9e34e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e34e-106">Parameters</span></span>

<span data-ttu-id="9e34e-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9e34e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9e34e-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e34e-108">Return value</span></span>

<span data-ttu-id="9e34e-109">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="9e34e-109">This method can return one of these values.</span></span>



| <span data-ttu-id="9e34e-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9e34e-110">Return code</span></span>                                                                                           | <span data-ttu-id="9e34e-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="9e34e-111">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9e34e-112"><dt>**\_ \_ somente consulta WBREAK \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="9e34e-112"><dt>**WBREAK\_E\_QUERY\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="9e34e-113">[**StartAltPhrase**](iwordsink-startaltphrase.md) é chamado durante o tempo de consulta.</span><span class="sxs-lookup"><span data-stu-id="9e34e-113">[**StartAltPhrase**](iwordsink-startaltphrase.md) is called during query time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9e34e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e34e-114">Remarks</span></span>

<span data-ttu-id="9e34e-115">Cada frase alternativa começa com uma chamada **StartAltPhrase** .</span><span class="sxs-lookup"><span data-stu-id="9e34e-115">Each alternative phrase starts with a **StartAltPhrase** call.</span></span> <span data-ttu-id="9e34e-116">A frase é colocada no objeto [**IWordSink**](iwordsink.md) por meio de chamadas subsequentes para o método [**IWordSink::P utword**](iwordsink-putword.md) ou [**IWordSink::P utaltword**](iwordsink-putaltword.md) .</span><span class="sxs-lookup"><span data-stu-id="9e34e-116">The phrase is put in the [**IWordSink**](iwordsink.md) object through subsequent calls to the [**IWordSink::PutWord**](iwordsink-putword.md) or [**IWordSink::PutAltWord**](iwordsink-putaltword.md) method.</span></span> <span data-ttu-id="9e34e-117">A frase alternativa final em uma sequência de frases é encerrada com uma chamada para o método [**IWordSink:: EndAltPhrase**](iwordsink-endaltphrase.md) .</span><span class="sxs-lookup"><span data-stu-id="9e34e-117">The final alternative phrase in a sequence of phrases is terminated with a call to the [**IWordSink::EndAltPhrase**](iwordsink-endaltphrase.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e34e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e34e-118">Requirements</span></span>



| <span data-ttu-id="9e34e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e34e-119">Requirement</span></span> | <span data-ttu-id="9e34e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9e34e-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9e34e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e34e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9e34e-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e34e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9e34e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9e34e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9e34e-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9e34e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9e34e-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="9e34e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e34e-126"><dt>Pesquisar. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e34e-126"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e34e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e34e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e34e-128">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="9e34e-128">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 




