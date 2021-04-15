---
description: Por padrão, o reconhecedor usa um dicionário do sistema que contém todas as palavras normalmente escritas em uma linguagem.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Usando dicionários de aplicativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfda443a688af9dfcec44a81f0e5ed2d50846c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461076"
---
# <a name="using-application-dictionaries"></a><span data-ttu-id="1fe55-103">Usando dicionários de aplicativos</span><span class="sxs-lookup"><span data-stu-id="1fe55-103">Using Application Dictionaries</span></span>

<span data-ttu-id="1fe55-104">Por padrão, o reconhecedor usa um dicionário do sistema que contém todas as palavras normalmente escritas em uma linguagem.</span><span class="sxs-lookup"><span data-stu-id="1fe55-104">By default, the recognizer uses a system dictionary that contains all of the commonly written words in a language.</span></span> <span data-ttu-id="1fe55-105">Além disso, o reconhecedor tem um dicionário do usuário que contém palavras que o usuário adicionou ao dicionário.</span><span class="sxs-lookup"><span data-stu-id="1fe55-105">In addition, the recognizer has a user dictionary that contains words that the user has added to the dictionary.</span></span> <span data-ttu-id="1fe55-106">Os usuários adicionam uma palavra ao dicionário do usuário por meio do painel de entrada do Tablet PC por meio de seleções em:</span><span class="sxs-lookup"><span data-stu-id="1fe55-106">Users add a word to the user dictionary through Tablet PC Input Panel through selections in:</span></span>

-   <span data-ttu-id="1fe55-107">A lista alternativa (ao escrever).</span><span class="sxs-lookup"><span data-stu-id="1fe55-107">The alternate list (when writing).</span></span>
-   <span data-ttu-id="1fe55-108">O menu ferramentas de fala (quando estiver falando).</span><span class="sxs-lookup"><span data-stu-id="1fe55-108">The Speech Tools menu (when speaking).</span></span>

<span data-ttu-id="1fe55-109">Se você estiver criando um aplicativo no qual você prevê que o usuário irá gravar palavras que não são encontradas no dicionário do sistema ou no dicionário do usuário, crie um dicionário de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1fe55-109">If you are designing an application into which you anticipate the user will write words that are not found in either the system dictionary or the user dictionary, create an application dictionary.</span></span> <span data-ttu-id="1fe55-110">Um dicionário de aplicativos melhora ainda mais a precisão do reconhecimento ao fornecer ao reconhecedor uma lista personalizada adicional de palavras que provavelmente serão inseridas como manuscritos em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1fe55-110">An application dictionary further improves recognition accuracy by providing the recognizer with an additional customized list of words likely to be entered as handwriting into an application.</span></span>

<span data-ttu-id="1fe55-111">Você cria um dicionário de aplicativos usando o objeto de [**listas de palavras**](inkwordlist-class.md) .</span><span class="sxs-lookup"><span data-stu-id="1fe55-111">You create an application dictionary by using the [**WordList**](inkwordlist-class.md) object.</span></span> <span data-ttu-id="1fe55-112">O dicionário de aplicativos incorretos aumenta a precisão do reconhecimento fornecendo ao reconhecedor uma lista de palavras esperadas.</span><span class="sxs-lookup"><span data-stu-id="1fe55-112">The ensuing application dictionary increases recognition accuracy by providing the recognizer with a list of expected words.</span></span> <span data-ttu-id="1fe55-113">Por exemplo, um dicionário de aplicativo que contém a terminologia médica aumenta a precisão do reconhecimento dentro de um aplicativo desenvolvido para o setor médico no qual os termos provavelmente serão escritos.</span><span class="sxs-lookup"><span data-stu-id="1fe55-113">For example, an application dictionary that contains medical terminology increases recognition accuracy within an application developed for the medical industry into which the terms are likely to be written.</span></span>

<span data-ttu-id="1fe55-114">Como outro exemplo, ao criar um formulário para alguém solicitar instrumentos musicais, crie um objeto de [**listas de palavras**](inkwordlist-class.md) que contenha os nomes dos fabricantes de instrumentos mais comuns.</span><span class="sxs-lookup"><span data-stu-id="1fe55-114">As another example, when designing a form for someone to order musical instruments, create a [**WordList**](inkwordlist-class.md) object that contains the names of the most common instrument manufacturers.</span></span> <span data-ttu-id="1fe55-115">Defina a propriedade de [**listas de palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) para o objeto de faixa de **palavras** que você criou.</span><span class="sxs-lookup"><span data-stu-id="1fe55-115">Set the [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) property of the [**RecognizerContext**](inkrecognizercontext-class.md) object to the **WordList** object you created.</span></span> <span data-ttu-id="1fe55-116">Em seguida, essa lista de palavras é passada para o reconhecedor pelo objeto **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="1fe55-116">This list of words is then passed to the recognizer by the **RecognizerContext** object.</span></span> <span data-ttu-id="1fe55-117">O dicionário do aplicativo aumenta a precisão do reconhecimento quando esses nomes são gravados em um campo no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1fe55-117">The application dictionary increases recognition accuracy when those names are written in a field in the application.</span></span>

<span data-ttu-id="1fe55-118">Os tópicos a seguir descrevem como usar dicionários de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1fe55-118">The following topics describe how to use application dictionaries.</span></span>

-   [<span data-ttu-id="1fe55-119">Compreendendo as listas de palavras, o contexto do reconhecedor e as chaves</span><span class="sxs-lookup"><span data-stu-id="1fe55-119">Understanding Word Lists, Recognizer Context, and Factoids</span></span>](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [<span data-ttu-id="1fe55-120">Usando dicionários de aplicativos com as APIs de plataforma do Tablet PC</span><span class="sxs-lookup"><span data-stu-id="1fe55-120">Using Application Dictionaries with the Tablet PC Platform APIs</span></span>](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [<span data-ttu-id="1fe55-121">Criando dicionários personalizados para reconhecimento de manuscrito</span><span class="sxs-lookup"><span data-stu-id="1fe55-121">Creating Custom Dictionaries for Handwriting Recognition</span></span>](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



