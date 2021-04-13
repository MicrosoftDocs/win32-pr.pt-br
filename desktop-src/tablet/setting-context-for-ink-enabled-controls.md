---
description: Todo o reconhecimento de controles habilitados para tinta ocorre por meio de um objeto RecognizerContext. As APIs de tecnologia do Tablet PC permitem definir a propriedade factoid em um objeto RecognizerContext.
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: Configurando contexto para controles de Ink-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6776978834f030353a84c04f03e5ecf05ba060cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297374"
---
# <a name="setting-context-for-ink-enabled-controls"></a><span data-ttu-id="e587c-104">Configurando contexto para controles de Ink-Enabled</span><span class="sxs-lookup"><span data-stu-id="e587c-104">Setting Context for Ink-Enabled Controls</span></span>

<span data-ttu-id="e587c-105">Todo o reconhecimento de controles habilitados para tinta ocorre por meio de um objeto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e587c-105">All recognition for ink-enabled controls occurs through a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="e587c-106">As APIs de tecnologia do Tablet PC permitem definir a propriedade [**factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) em um objeto **RecognizerContext** .</span><span class="sxs-lookup"><span data-stu-id="e587c-106">The Tablet PC Technology APIs enable you to set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on a **RecognizerContext** object.</span></span>

<span data-ttu-id="e587c-107">Se você estiver criando um aplicativo habilitado para tinta, use as propriedades de [**facto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) e lista de [**palavras**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) para definir contextos.</span><span class="sxs-lookup"><span data-stu-id="e587c-107">If you are creating an ink-enabled application, use the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) and [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) properties to set contexts.</span></span>

<span data-ttu-id="e587c-108">Você pode passar os valores de cadeia de caracteres dos nomes nos escopos de entrada definidos na enumeração [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) para a propriedade [**factor**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) , delimitada com uma abertura (!</span><span class="sxs-lookup"><span data-stu-id="e587c-108">You may pass in the string values of the names in the input scopes defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property, delimited with an opening (!</span></span> <span data-ttu-id="e587c-109">e um fechamento).</span><span class="sxs-lookup"><span data-stu-id="e587c-109">and a closing ).</span></span> <span data-ttu-id="e587c-110">Por exemplo, para definir o contexto de um objeto [**RecognizerContext**](inkrecognizercontext-class.md) com tendência de caracteres usados em uma URL, use a sintaxe mostrada nos exemplos C a seguir \# :</span><span class="sxs-lookup"><span data-stu-id="e587c-110">For example, to set the context for a [**RecognizerContext**](inkrecognizercontext-class.md) object to bias toward characters used in a URL, use the syntax shown in the following C\# examples:</span></span>


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> <span data-ttu-id="e587c-111">Os escopos de entrada, conforme definido na enumeração [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , substituem as entradas que estavam disponíveis nas versões anteriores do SDK do Windows XP Tablet PC Edition, embora essas paraestas continuem a funcionar para fornecer compatibilidade com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="e587c-111">The input scopes as defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration supersede the factoids that were available in previous versions of the Windows XP Tablet PC Edition SDK, although these factoids will continue to work in order to provide backward compatibility.</span></span>

 

<span data-ttu-id="e587c-112">O exemplo C a seguir \# define a propriedade [**factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) para CEPs:</span><span class="sxs-lookup"><span data-stu-id="e587c-112">The following C\# example sets the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property for postal codes:</span></span>


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



<span data-ttu-id="e587c-113">Você pode combinar escopos de entrada usando a sintaxe de expressão regular de manuscrito.</span><span class="sxs-lookup"><span data-stu-id="e587c-113">You can combine input scopes by using the handwriting regular expression syntax.</span></span> <span data-ttu-id="e587c-114">Para obter mais detalhes sobre como usar a sintaxe de expressão regular, consulte [escopos de entrada personalizados com expressões regulares](custom-input-scopes-with-regular-expressions.md).</span><span class="sxs-lookup"><span data-stu-id="e587c-114">For more details about using regular expression syntax, see [Custom Input Scopes with Regular Expressions](custom-input-scopes-with-regular-expressions.md).</span></span>

<span data-ttu-id="e587c-115">Você pode definir sinalizadores de reconhecimento no objeto [**RecognizerContext**](inkrecognizercontext-class.md) para afetar o comportamento do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="e587c-115">You can set recognition flags on the [**RecognizerContext**](inkrecognizercontext-class.md) object to affect the behavior of the recognizer.</span></span> <span data-ttu-id="e587c-116">Um desses sinalizadores é o sinalizador de **coerção** na enumeração [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) de **RecognizerContext**.</span><span class="sxs-lookup"><span data-stu-id="e587c-116">One such flag is the **Coerce** flag in the [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) enumeration of the **RecognizerContext**.</span></span> <span data-ttu-id="e587c-117">O sinalizador de **coerção** força o reconhecedor a retornar um resultado que corresponda à definição do factor definido.</span><span class="sxs-lookup"><span data-stu-id="e587c-117">The **Coerce** flag forces the recognizer to return a result that matches the definition of the factoid that is set.</span></span> <span data-ttu-id="e587c-118">Por exemplo, se você tiver um formulário que exige que o usuário insira uma quantidade numérica, pode ser útil definir o factor de **\_ número is** e também definir a propriedade [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) para **coerção**.</span><span class="sxs-lookup"><span data-stu-id="e587c-118">For example, if you have a form that requires the user to enter a numerical quantity, it may be useful to set the **IS\_NUMBER** factoid and also set the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**.</span></span> <span data-ttu-id="e587c-119">Nessa instância, o sinalizador de **coerção** garante que o reconhecedor retorne apenas números.</span><span class="sxs-lookup"><span data-stu-id="e587c-119">In that instance, the **Coerce** flag guarantees that the recognizer returns only numbers.</span></span>

<span data-ttu-id="e587c-120">O exemplo C a seguir \# define a propriedade [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) para **coerção**:</span><span class="sxs-lookup"><span data-stu-id="e587c-120">The following C\# example sets the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**:</span></span>


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



<span data-ttu-id="e587c-121">No entanto, tome cuidado ao decidir definir o sinalizador de **coerção** .</span><span class="sxs-lookup"><span data-stu-id="e587c-121">However, use caution when deciding to set the **Coerce** flag.</span></span> <span data-ttu-id="e587c-122">O sinalizador força o reconhecedor a corresponder apenas à definição do factor.</span><span class="sxs-lookup"><span data-stu-id="e587c-122">The flag forces the recognizer to match only the definition of the factoid.</span></span> <span data-ttu-id="e587c-123">Por exemplo, se você definir o \_ escopo de \_ entrada FULLTELEPHONENUMBER de telefone e o sinalizador de **coerção** , o reconhecedor retornará resultados que correspondam exatamente à definição de somente o escopo de \_ entrada de telefone \_ FULLTELEPHONENUMBER.</span><span class="sxs-lookup"><span data-stu-id="e587c-123">For example, if you set the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag, the recognizer returns results that exactly match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope only.</span></span> <span data-ttu-id="e587c-124">Se um usuário gravar "911" com o \_ escopo de \_ entrada FULLTELEPHONENUMBER de telefone e o sinalizador de **coerção** definido, o reconhecedor poderá retornar uma cadeia de caracteres vazia ou uma cadeia de caracteres aleatória no formato (xxx) xxx-xxxx (em que X é um dígito).</span><span class="sxs-lookup"><span data-stu-id="e587c-124">If a user writes "911" with the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag set, the recognizer may return either an empty string or a random string in the format of (XXX) XXX-XXXX (where X is a digit).</span></span> <span data-ttu-id="e587c-125">O formato XXX não corresponde à definição do FULLTELEPHONENUMBER de telefone IS \_ \_ , embora seja um número de telefone válido.</span><span class="sxs-lookup"><span data-stu-id="e587c-125">The format of XXX does not match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER factoid, even though it is a valid phone number.</span></span>

<span data-ttu-id="e587c-126">Para obter listas dos formatos com suporte para cada escopo de entrada, consulte a referência de [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) .</span><span class="sxs-lookup"><span data-stu-id="e587c-126">For lists of the supported formats for each input scope, see the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) reference.</span></span>

<span data-ttu-id="e587c-127">Para retornar um campo para a configuração padrão para o reconhecedor, defina o facto como \_ padrão, como no exemplo C a seguir \# :</span><span class="sxs-lookup"><span data-stu-id="e587c-127">To return a field to the default setting for the recognizer, set the factoid to IS\_DEFAULT , as in the following C\# example:</span></span>


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



<span data-ttu-id="e587c-128">Para aplicativos que usam o controle [InkEdit](inkedit-control-reference.md) , defina o tipo de facto para o controle especificando:</span><span class="sxs-lookup"><span data-stu-id="e587c-128">For applications that use the [InkEdit](inkedit-control-reference.md) control, set the factoid type for the control by specifying:</span></span>


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



<span data-ttu-id="e587c-129">Em que `IS_INPUTSCOPE` é o nome do escopo de entrada que você deseja aplicar.</span><span class="sxs-lookup"><span data-stu-id="e587c-129">Where `IS_INPUTSCOPE` is the name of the input scope you want to apply.</span></span>

<span data-ttu-id="e587c-130">O controle [InkEdit](inkedit-control-reference.md) não expõe um objeto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e587c-130">The [InkEdit](inkedit-control-reference.md) control does not expose a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="e587c-131">Você ainda pode atribuir contexto usando a propriedade [**factoname**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) do controle InkEdit, mas não pode definir o sinalizador **WordMode** .</span><span class="sxs-lookup"><span data-stu-id="e587c-131">You can still assign context by using the [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) property of the InkEdit control, but you cannot set the **WORDMODE** flag.</span></span>

 

 
