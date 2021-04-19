---
description: O léxico ou a lista de palavras possíveis usadas pelo modelo de linguagem de um reconhecedor específico está contido em um ou mais dicionários.
ms.assetid: e975a75f-ab88-4164-afc8-3b817988504d
title: Listas de dicionários e de frases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f88dc2f6b05eea322b6e88dda1f986b3c54b7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781613"
---
# <a name="dictionaries-and-phrase-lists"></a><span data-ttu-id="bd11f-103">Listas de dicionários e de frases</span><span class="sxs-lookup"><span data-stu-id="bd11f-103">Dictionaries and Phrase lists</span></span>

<span data-ttu-id="bd11f-104">O léxico ou a lista de palavras possíveis usadas pelo modelo de linguagem de um reconhecedor específico está contido em um ou mais dicionários.</span><span class="sxs-lookup"><span data-stu-id="bd11f-104">The lexicon, or list of possible words used by a particular recognizer's language model, is contained in one or more dictionaries.</span></span> <span data-ttu-id="bd11f-105">O reconhecedor pesquisa todos os dicionários disponíveis no sistema durante a compilação de correspondências de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="bd11f-105">The recognizer searches all dictionaries available on the system when compiling recognition matches.</span></span> <span data-ttu-id="bd11f-106">Você pode usar o SAPI (Microsoft Speech APIs) para modificar alguns desses dicionários.</span><span class="sxs-lookup"><span data-stu-id="bd11f-106">You can use the Microsoft Speech APIs (SAPI) to modify some of these dictionaries.</span></span>

<span data-ttu-id="bd11f-107">Uma lista de frases fornece outro meio de modificar o vocabulário do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="bd11f-107">A phrase list provides another means of modifying the recognizer's vocabulary.</span></span> <span data-ttu-id="bd11f-108">A adição de palavras a uma lista de frases estende o vocabulário; adicionar palavras e, em seguida, restringir o reconhecedor para usar apenas a lista de frases (ao contrário da lista de frases e dos dicionários) restringe o vocabulário.</span><span class="sxs-lookup"><span data-stu-id="bd11f-108">Adding words to a phrase list extends the vocabulary; adding words and then constraining the recognizer to use only the phrase list (as opposed to the phrase list and the dictionaries) restricts the vocabulary.</span></span>

<span data-ttu-id="bd11f-109">Versões anteriores das APIs de tecnologia do Tablet PC contavam com o conceito de listas de palavras.</span><span class="sxs-lookup"><span data-stu-id="bd11f-109">Previous releases of the Tablet PC Technology APIs relied on the concept of word lists.</span></span> <span data-ttu-id="bd11f-110">As listas de palavras são quase idênticas às listas de frases e são usadas para a mesma finalidade ao trabalhar diretamente com um objeto [**RecognizerContext**](inkrecognizercontext-class.md) em um aplicativo habilitado para tinta.</span><span class="sxs-lookup"><span data-stu-id="bd11f-110">Word lists are almost identical to phrase lists and are used for the same purpose when working directly with a [**RecognizerContext**](inkrecognizercontext-class.md) object in an application that is ink enabled.</span></span> <span data-ttu-id="bd11f-111">Para obter mais detalhes sobre onde e quando usar listas de palavras, consulte [Configurando contexto para controles de Ink-Enabled](setting-context-for-ink-enabled-controls.md).</span><span class="sxs-lookup"><span data-stu-id="bd11f-111">For more details about where and when to use word lists, see [Setting Context for Ink-Enabled Controls](setting-context-for-ink-enabled-controls.md).</span></span>

<span data-ttu-id="bd11f-112">Quando o tamanho da lista com o qual você deseja estender o léxico excede 100.000 palavras, recomendamos que você use um dicionário em vez de uma lista de palavras ou de expressões.</span><span class="sxs-lookup"><span data-stu-id="bd11f-112">When the size of the list with which you want to extend the lexicon exceeds 100,000 words, we recommend that you use a dictionary instead of a word list or phrase list.</span></span>

 

 



