---
description: Você pode definir escopos de entrada personalizados usando modelos de linguagem compostos por expressões regulares para manuscrito e atribuindo-os a campos. Por exemplo, se você estiver criando um aplicativo de banco de dados para partes de depósito e quiser que os usuários possam inserir números de peça usando o painel de escrita do Tablet PC. Se a sintaxe do número da peça consistir em três letras seguidas por quatro números seguidos por outra letra (por exemplo, ABC1234D), o reconhecedor de manuscrito teria um tempo difícil de reconhecer essa entrada porque não está definido no modelo de linguagem. Não há nenhum factor predefinido que corresponda a tal sintaxe, nem a Microsoft pode incluir a sintaxe de todos os campos possíveis que um aplicativo possa precisar. As expressões regulares de manuscrito fornecem uma maneira fácil para que os aplicativos definam seu próprio modelo de linguagem para um campo de uso especial específico. Observação ao trabalhar em um aplicativo habilitado para tinta que usa a propriedade facto do objeto RecognizerContext, você não pode usar as da versão 1 em uma expressão regular.
ms.assetid: 71f80196-0a36-4a14-a115-712bc909f6d7
title: Escopos de entrada personalizados com expressões regulares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bdd7807221aca7b05ed4dc1facf7ddb01470c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010298"
---
# <a name="custom-input-scopes-with-regular-expressions"></a><span data-ttu-id="cbd23-106">Escopos de entrada personalizados com expressões regulares</span><span class="sxs-lookup"><span data-stu-id="cbd23-106">Custom Input Scopes with Regular Expressions</span></span>

<span data-ttu-id="cbd23-107">Você pode definir escopos de entrada personalizados usando modelos de linguagem compostos por expressões regulares para manuscrito e atribuindo-os a campos.</span><span class="sxs-lookup"><span data-stu-id="cbd23-107">You can define custom input scopes by using language models composed of regular expressions for handwriting and assigning them to fields.</span></span>

<span data-ttu-id="cbd23-108">Por exemplo, se você estiver criando um aplicativo de banco de dados para partes de depósito e quiser que os usuários possam inserir números de peça usando o painel de escrita do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="cbd23-108">For example, if you are creating a database application for warehouse parts and want users to be able to enter part numbers using the Tablet PC Input Panel's writing pad.</span></span> <span data-ttu-id="cbd23-109">Se a sintaxe do número da peça consistir em três letras seguidas por quatro números seguidos por outra letra (por exemplo, ABC1234D), o reconhecedor de manuscrito teria um tempo difícil de reconhecer essa entrada porque não está definido no modelo de linguagem.</span><span class="sxs-lookup"><span data-stu-id="cbd23-109">If the part number syntax consists of three letters followed by four numbers followed by another letter (for example, ABC1234D), the handwriting recognizer would have a difficult time recognizing such input because it is not defined in the language model.</span></span> <span data-ttu-id="cbd23-110">Não há nenhum factor predefinido que corresponda a tal sintaxe, nem a Microsoft pode incluir a sintaxe de todos os campos possíveis que um aplicativo possa precisar.</span><span class="sxs-lookup"><span data-stu-id="cbd23-110">There is no predefined factoid that corresponds to such syntax, nor can Microsoft include the syntax for every possible field an application might need.</span></span> <span data-ttu-id="cbd23-111">As expressões regulares de manuscrito fornecem uma maneira fácil para que os aplicativos definam seu próprio modelo de linguagem para um campo de uso especial específico.</span><span class="sxs-lookup"><span data-stu-id="cbd23-111">Handwriting regular expressions provide an easy way for applications to define their own language model for a particular special-use field.</span></span>

> [!Note]  
> <span data-ttu-id="cbd23-112">Ao trabalhar em um aplicativo habilitado para tinta que usa a propriedade [**facto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) , você não pode usar o factos de versão 1 em uma expressão regular.</span><span class="sxs-lookup"><span data-stu-id="cbd23-112">When working in an ink-enabled application that uses the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object, you cannot use version 1 factoids in a regular expression.</span></span>

 

 

 



