---
description: Representa uma lista de palavras que podem ser usadas para melhorar o resultado do reconhecimento.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Classe InkWordList (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813628"
---
# <a name="inkwordlist-class"></a><span data-ttu-id="d7097-103">Classe InkWordList</span><span class="sxs-lookup"><span data-stu-id="d7097-103">InkWordList class</span></span>

<span data-ttu-id="d7097-104">Representa uma lista de palavras que podem ser usadas para melhorar o resultado do reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="d7097-104">Represents a list of words that can be used to improve the recognition result.</span></span>

<span data-ttu-id="d7097-105">**InkWordList** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d7097-105">**InkWordList** has these types of members:</span></span>

-   [<span data-ttu-id="d7097-106">Interfaces</span><span class="sxs-lookup"><span data-stu-id="d7097-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="d7097-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7097-107">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="d7097-108">Interfaces</span><span class="sxs-lookup"><span data-stu-id="d7097-108">Interfaces</span></span>

<span data-ttu-id="d7097-109">A classe **InkWordList** define essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="d7097-109">The **InkWordList** class defines these interfaces.</span></span>



| <span data-ttu-id="d7097-110">Interface</span><span class="sxs-lookup"><span data-stu-id="d7097-110">Interface</span></span>        | <span data-ttu-id="d7097-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7097-111">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="d7097-112">**IInkWordList**</span><span class="sxs-lookup"><span data-stu-id="d7097-112">**IInkWordList**</span></span> | <span data-ttu-id="d7097-113">Esse objeto implementa a interface com do **IInkWordList** .</span><span class="sxs-lookup"><span data-stu-id="d7097-113">This object implements the **IInkWordList** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="d7097-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7097-114">Methods</span></span>

<span data-ttu-id="d7097-115">A classe **InkWordList** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="d7097-115">The **InkWordList** class has these methods.</span></span>



| <span data-ttu-id="d7097-116">Método</span><span class="sxs-lookup"><span data-stu-id="d7097-116">Method</span></span>                                       | <span data-ttu-id="d7097-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7097-117">Description</span></span>                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="d7097-118">**AddWord**</span><span class="sxs-lookup"><span data-stu-id="d7097-118">**AddWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | <span data-ttu-id="d7097-119">Adiciona uma única palavra ao **InkWordList**.</span><span class="sxs-lookup"><span data-stu-id="d7097-119">Adds a single word to the **InkWordList**.</span></span><br/>                   |
| [<span data-ttu-id="d7097-120">**Mescle**</span><span class="sxs-lookup"><span data-stu-id="d7097-120">**Merge**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | <span data-ttu-id="d7097-121">Mescla outro **InkWordList** com este **InkWordList**.</span><span class="sxs-lookup"><span data-stu-id="d7097-121">Merges another **InkWordList** to into this **InkWordList**.</span></span><br/> |
| [<span data-ttu-id="d7097-122">**RemoveWord**</span><span class="sxs-lookup"><span data-stu-id="d7097-122">**RemoveWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | <span data-ttu-id="d7097-123">Remove uma única palavra de um **InkWordList**.</span><span class="sxs-lookup"><span data-stu-id="d7097-123">Removes a single word from a **InkWordList**.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="d7097-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7097-124">Remarks</span></span>

<span data-ttu-id="d7097-125">Esse objeto pode ser instanciado chamando o método [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) em C++.</span><span class="sxs-lookup"><span data-stu-id="d7097-125">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7097-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7097-126">Requirements</span></span>



| <span data-ttu-id="d7097-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7097-127">Requirement</span></span> | <span data-ttu-id="d7097-128">Valor</span><span class="sxs-lookup"><span data-stu-id="d7097-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7097-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7097-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d7097-130">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="d7097-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d7097-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d7097-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d7097-132">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d7097-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d7097-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7097-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7097-134"><dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d7097-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d7097-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7097-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7097-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7097-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d7097-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7097-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7097-138">**Propriedade de listas de palavras**</span><span class="sxs-lookup"><span data-stu-id="d7097-138">**WordList Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[<span data-ttu-id="d7097-139">Constantes do factor</span><span class="sxs-lookup"><span data-stu-id="d7097-139">Factoid Constants</span></span>](factoid-constants.md)
</dt> <dt>

[<span data-ttu-id="d7097-140">**Classe InkRecognizerContext**</span><span class="sxs-lookup"><span data-stu-id="d7097-140">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

