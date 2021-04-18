---
description: Manipula palavras identificadas por quebras de palavras durante tanto o tempo de índice quanto o tempo de consulta.
ms.assetid: 220FCAE5-D22D-45ED-9689-E78C0D8E0BB3
title: Interface IWordSink (Search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 2eab8eee4f7b07b0f712e68d7ad05b970506b00b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807279"
---
# <a name="iwordsink-interface"></a><span data-ttu-id="2c477-103">Interface IWordSink</span><span class="sxs-lookup"><span data-stu-id="2c477-103">IWordSink interface</span></span>

<span data-ttu-id="2c477-104">Manipula palavras identificadas por quebras de palavras durante tanto o tempo de índice quanto o tempo de consulta.</span><span class="sxs-lookup"><span data-stu-id="2c477-104">Handles words identified by word breaks during both index time and query time.</span></span>

## <a name="members"></a><span data-ttu-id="2c477-105">Membros</span><span class="sxs-lookup"><span data-stu-id="2c477-105">Members</span></span>

<span data-ttu-id="2c477-106">A interface **IWordSink** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2c477-106">The **IWordSink** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2c477-107">**IWordSink** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2c477-107">**IWordSink** also has these types of members:</span></span>

-   [<span data-ttu-id="2c477-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="2c477-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2c477-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="2c477-109">Methods</span></span>

<span data-ttu-id="2c477-110">A interface **IWordSink** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2c477-110">The **IWordSink** interface has these methods.</span></span>



| <span data-ttu-id="2c477-111">Método</span><span class="sxs-lookup"><span data-stu-id="2c477-111">Method</span></span>                                             | <span data-ttu-id="2c477-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="2c477-112">Description</span></span>                                                                                                                             |
|:---------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2c477-113">**EndAltPhrase**</span><span class="sxs-lookup"><span data-stu-id="2c477-113">**EndAltPhrase**</span></span>](iwordsink-endaltphrase.md)     | <span data-ttu-id="2c477-114">Indica o fim da frase final em uma sequência de frases alternativas que um separador de palavras gera durante o tempo do índice.</span><span class="sxs-lookup"><span data-stu-id="2c477-114">Indicates the end of the final phrase in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/>  |
| [<span data-ttu-id="2c477-115">**PutAltWord**</span><span class="sxs-lookup"><span data-stu-id="2c477-115">**PutAltWord**</span></span>](iwordsink-putaltword.md)         | <span data-ttu-id="2c477-116">Coloca uma palavra alternativa e sua posição no objeto **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="2c477-116">Puts an alternative word and its position in the **IWordSink** object.</span></span><br/>                                                       |
| [<span data-ttu-id="2c477-117">**PutBreak**</span><span class="sxs-lookup"><span data-stu-id="2c477-117">**PutBreak**</span></span>](iwordsink-putbreak.md)             | <span data-ttu-id="2c477-118">Coloca uma quebra após a palavra anterior.</span><span class="sxs-lookup"><span data-stu-id="2c477-118">Puts a break after the preceding word.</span></span><br/>                                                                                       |
| [<span data-ttu-id="2c477-119">**PutWord**</span><span class="sxs-lookup"><span data-stu-id="2c477-119">**PutWord**</span></span>](iwordsink-putword.md)               | <span data-ttu-id="2c477-120">Coloca uma palavra e sua posição no objeto **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="2c477-120">Puts a word and its position in the **IWordSink** object.</span></span><br/>                                                                    |
| [<span data-ttu-id="2c477-121">**StartAltPhrase**</span><span class="sxs-lookup"><span data-stu-id="2c477-121">**StartAltPhrase**</span></span>](iwordsink-startaltphrase.md) | <span data-ttu-id="2c477-122">Indica o limite entre as frases em uma sequência de frases alternativas que um separador de palavras gera durante o tempo de indexação.</span><span class="sxs-lookup"><span data-stu-id="2c477-122">Indicates the boundary between phrases in a sequence of alternative phrases that a word breaker generates during index time.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2c477-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="2c477-123">Remarks</span></span>

<span data-ttu-id="2c477-124">O Windows Search cria e inicializa instâncias do objeto **IWordSink** .</span><span class="sxs-lookup"><span data-stu-id="2c477-124">Windows Search creates and initializes instances of the **IWordSink** object.</span></span> <span data-ttu-id="2c477-125">O objeto **IWordSink** recebe o parâmetro *fQuery* durante a inicialização e usa esse parâmetro para determinar o contexto de quebra de palavras no qual o objeto é usado.</span><span class="sxs-lookup"><span data-stu-id="2c477-125">The **IWordSink** object receives the *fQuery* parameter during initialization and uses this parameter to determine the word-breaking context in which the object is used.</span></span>

<span data-ttu-id="2c477-126">Implementações [**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) recebem um ponteiro para o objeto **IWordSink** no método [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) .</span><span class="sxs-lookup"><span data-stu-id="2c477-126">[**IWordBreaker**](/windows/win32/api/indexsrv/nn-indexsrv-iwordbreaker) implementations receive a pointer to the **IWordSink** object in the [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c477-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c477-127">Requirements</span></span>



| <span data-ttu-id="2c477-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c477-128">Requirement</span></span> | <span data-ttu-id="2c477-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2c477-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2c477-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c477-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2c477-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2c477-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2c477-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2c477-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2c477-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2c477-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2c477-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2c477-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c477-135"><dt>Pesquisar. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c477-135"><dt>Search.h</dt></span></span> </dl> |



 

 
