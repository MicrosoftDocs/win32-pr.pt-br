---
description: Um mecanismo de reconhecimento de manuscrito, ou reconhecedor, é um software que processa a tinta e converte essa tinta em texto.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Usando o contexto para melhorar a precisão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769143"
---
# <a name="using-context-to-improve-accuracy"></a><span data-ttu-id="e3940-103">Usando o contexto para melhorar a precisão</span><span class="sxs-lookup"><span data-stu-id="e3940-103">Using Context to Improve Accuracy</span></span>

<span data-ttu-id="e3940-104">Um mecanismo de reconhecimento de manuscrito, ou reconhecedor, é um software que processa a tinta e converte essa tinta em texto.</span><span class="sxs-lookup"><span data-stu-id="e3940-104">A handwriting recognition engine, or recognizer, is software that processes ink and converts that ink into text.</span></span> <span data-ttu-id="e3940-105">Um contexto é relevante, informações específicas do aplicativo que você fornece a um reconhecedor para melhorar a precisão do reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="e3940-105">A context is relevant, application-specific information that you provide to a recognizer to improve recognition accuracy.</span></span> <span data-ttu-id="e3940-106">Em outras palavras, o contexto é qualquer informação sobre entrada que ajude o reconhecedor a processar com precisão a tinta em um campo.</span><span class="sxs-lookup"><span data-stu-id="e3940-106">In other words, context is any piece of information about input that aids the recognizer in accurately processing the ink in a field.</span></span>

<span data-ttu-id="e3940-107">Esta seção descreve as diferentes maneiras pelas quais você pode aproveitar o contexto em seu aplicativo do Tablet PC, dando ênfase à técnica de programação preferida para aplicativos que não estão habilitados para tinta.</span><span class="sxs-lookup"><span data-stu-id="e3940-107">This section describes the different ways you can take advantage of context in your Tablet PC application, placing emphasis on the preferred programmatic technique for applications that are not ink enabled.</span></span>

> [!Note]  
> <span data-ttu-id="e3940-108">Há locais nas seções de tecnologia do Tablet PC do SDK (Software Development Kit) do Windows Vista, em que o termo "contexto" é usado em relação ao objeto [**RecognizerContext**](inkrecognizercontext-class.md) e suas propriedades [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) e [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) .</span><span class="sxs-lookup"><span data-stu-id="e3940-108">There are places in the Tablet PC Technology sections of the Windows Vista Software Development Kit (SDK) where the term "context" is used in regard to the [**RecognizerContext**](inkrecognizercontext-class.md) object and its [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) and [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) properties.</span></span> <span data-ttu-id="e3940-109">Não confunda esses outros usos de "contexto" com a definição nesta seção.</span><span class="sxs-lookup"><span data-stu-id="e3940-109">Do not confuse these other usages of "context" with the definition in this section.</span></span>

 

 

 



