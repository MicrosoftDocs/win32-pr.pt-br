---
description: Um identificador HRECOWORDLIST é usado para gerenciar uma lista de palavras anexada a um contexto de reconhecedor. Você usa uma lista de palavras para melhorar os resultados de reconhecimento.
ms.assetid: 7333307b-1857-48a7-bb9f-bdbd8530f093
title: Identificador HRECOWORDLIST (recapitular. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5e5d33862cacb7040a26edc23d7db04c57206c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501829"
---
# <a name="hrecowordlist-handle"></a><span data-ttu-id="485bd-104">Identificador de HRECOWORDLIST</span><span class="sxs-lookup"><span data-stu-id="485bd-104">HRECOWORDLIST Handle</span></span>

<span data-ttu-id="485bd-105">Um identificador **HRECOWORDLIST** é usado para gerenciar uma lista de palavras anexada a um contexto de reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="485bd-105">An **HRECOWORDLIST** handle is used to manage a word list you attach to a recognizer context.</span></span> <span data-ttu-id="485bd-106">Você usa uma lista de palavras para melhorar os resultados de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="485bd-106">You use a word list to improve recognition results.</span></span>


```C++
typedef HANDLE HRECOWORDLIST;
```



## <a name="remarks"></a><span data-ttu-id="485bd-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="485bd-107">Remarks</span></span>

<span data-ttu-id="485bd-108">A função a seguir usa um **HRECOWORDLIST**.</span><span class="sxs-lookup"><span data-stu-id="485bd-108">The following function use an **HRECOWORDLIST**.</span></span>



| <span data-ttu-id="485bd-109">Função</span><span class="sxs-lookup"><span data-stu-id="485bd-109">Function</span></span>                                         | <span data-ttu-id="485bd-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="485bd-110">Description</span></span>                                         |
|--------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="485bd-111">**AddWordsToWordList**</span><span class="sxs-lookup"><span data-stu-id="485bd-111">**AddWordsToWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-addwordstowordlist) | <span data-ttu-id="485bd-112">Adiciona uma ou mais palavras à lista de palavras.</span><span class="sxs-lookup"><span data-stu-id="485bd-112">Adds one or more words to the word list.</span></span><br/> |
| [<span data-ttu-id="485bd-113">**DestroyWordList**</span><span class="sxs-lookup"><span data-stu-id="485bd-113">**DestroyWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-destroywordlist)       | <span data-ttu-id="485bd-114">Destrói a lista atual de palavras.</span><span class="sxs-lookup"><span data-stu-id="485bd-114">Destroys the current word list.</span></span><br/>          |
| [<span data-ttu-id="485bd-115">**MakeWordList**</span><span class="sxs-lookup"><span data-stu-id="485bd-115">**MakeWordList**</span></span>](/windows/desktop/api/recapis/nf-recapis-makewordlist)             | <span data-ttu-id="485bd-116">Cria uma lista de palavras.</span><span class="sxs-lookup"><span data-stu-id="485bd-116">Creates a word list.</span></span><br/>                     |



 

## <a name="requirements"></a><span data-ttu-id="485bd-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="485bd-117">Requirements</span></span>



| <span data-ttu-id="485bd-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="485bd-118">Requirement</span></span> | <span data-ttu-id="485bd-119">Valor</span><span class="sxs-lookup"><span data-stu-id="485bd-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="485bd-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="485bd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="485bd-121">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="485bd-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="485bd-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="485bd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="485bd-123">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="485bd-123">None supported</span></span><br/>                                                            |
| <span data-ttu-id="485bd-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="485bd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="485bd-125"><dt>Recapitular. h</dt></span><span class="sxs-lookup"><span data-stu-id="485bd-125"><dt>Recapis.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="485bd-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="485bd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="485bd-127">**Função setwordlist**</span><span class="sxs-lookup"><span data-stu-id="485bd-127">**SetWordList Function**</span></span>](/windows/desktop/api/recapis/nf-recapis-setwordlist)
</dt> </dl>

 

 




