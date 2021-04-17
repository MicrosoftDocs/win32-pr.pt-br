---
description: Este exemplo demonstra os recursos avançados da API (interface de programação de aplicativo) do MicrosoftTablet PC Automation usada para o reconhecimento de manuscrito.
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: Exemplo de vários reconhecedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a21d24001e3544be16dde4d288a8adc7ea0081f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748345"
---
# <a name="multiple-recognizers-sample"></a><span data-ttu-id="563ba-103">Exemplo de vários reconhecedores</span><span class="sxs-lookup"><span data-stu-id="563ba-103">Multiple Recognizers Sample</span></span>

<span data-ttu-id="563ba-104">Este exemplo demonstra os recursos avançados da API (interface de programação de aplicativo) do MicrosoftTablet PC Automation usada para o reconhecimento de *manuscrito* .</span><span class="sxs-lookup"><span data-stu-id="563ba-104">This sample demonstrates advanced features of the MicrosoftTablet PC Automation application programming interface (API) used for *handwriting* recognition.</span></span>

<span data-ttu-id="563ba-105">Ele inclui o seguinte:</span><span class="sxs-lookup"><span data-stu-id="563ba-105">It includes the following:</span></span>

-   <span data-ttu-id="563ba-106">Enumerando os reconhecedores instalados</span><span class="sxs-lookup"><span data-stu-id="563ba-106">Enumerating the installed recognizers</span></span>
-   <span data-ttu-id="563ba-107">Criando um *contexto de reconhecedor* com um reconhecedor de idioma específico</span><span class="sxs-lookup"><span data-stu-id="563ba-107">Creating a *recognizer context* with a specific language recognizer</span></span>
-   <span data-ttu-id="563ba-108">Serializando resultados de reconhecimento com uma coleção de traços</span><span class="sxs-lookup"><span data-stu-id="563ba-108">Serializing recognition results with a stroke collection</span></span>
-   <span data-ttu-id="563ba-109">Organizando coleções de traços em uma coleção personalizada dentro do objeto [**InkDisp**](inkdisp-class.md)</span><span class="sxs-lookup"><span data-stu-id="563ba-109">Organizing stroke collections into a custom collection within the [**InkDisp**](inkdisp-class.md) object</span></span>
-   <span data-ttu-id="563ba-110">Serializando objetos de *tinta* para e recuperando-os de um arquivo de *formato serializado da tinta (ISF)*</span><span class="sxs-lookup"><span data-stu-id="563ba-110">Serializing *ink* objects to and retrieving them from an *ink serialized format (ISF)* file</span></span>
-   <span data-ttu-id="563ba-111">Definindo guias de entrada do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="563ba-111">Setting recognizer input guides</span></span>
-   <span data-ttu-id="563ba-112">Usando o reconhecimento síncrono e assíncrono</span><span class="sxs-lookup"><span data-stu-id="563ba-112">Using synchronous and asynchronous recognition</span></span>

## <a name="ink-headers"></a><span data-ttu-id="563ba-113">Cabeçalhos de tinta</span><span class="sxs-lookup"><span data-stu-id="563ba-113">Ink Headers</span></span>

<span data-ttu-id="563ba-114">Primeiro, inclua os cabeçalhos para interfaces de automação do Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="563ba-114">First, include the headers for Tablet PC Automation interfaces.</span></span> <span data-ttu-id="563ba-115">Eles são instalados com o SDK (Software Development Kit) do Microsoft Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="563ba-115">These are installed with the Microsoft Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="563ba-116">O arquivo EventSinks. h define as interfaces IInkEventsImpl e IInkRecognitionEventsImpl.</span><span class="sxs-lookup"><span data-stu-id="563ba-116">The EventSinks.h file defines the IInkEventsImpl and IInkRecognitionEventsImpl interfaces.</span></span>


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a><span data-ttu-id="563ba-117">Enumerando os reconhecedores instalados</span><span class="sxs-lookup"><span data-stu-id="563ba-117">Enumerating the Installed Recognizers</span></span>

<span data-ttu-id="563ba-118">O método LoadMenu do aplicativo popula o menu criar novos traços com os reconhecedores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="563ba-118">The application's LoadMenu method populates the Create New Strokes menu with the available recognizers.</span></span> <span data-ttu-id="563ba-119">Um [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) é criado.</span><span class="sxs-lookup"><span data-stu-id="563ba-119">An [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) is created.</span></span> <span data-ttu-id="563ba-120">Se a propriedade [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) de um objeto **InkRecognizers** não estiver vazia, o reconhecedor será um *reconhecedor de texto* e o valor de sua propriedade [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) será adicionado ao menu.</span><span class="sxs-lookup"><span data-stu-id="563ba-120">If the [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) property of an **InkRecognizers** object is not empty, then the recognizer is a *text recognizer*, and the value of its [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) property is added to the menu.</span></span>


```C++
// Create the enumerator for the installed recognizers
hr = m_spIInkRecognizers.CoCreateInstance(CLSID_InkRecognizers);
...
    // Filter out non-language recognizers by checking for
    // the languages supported by the recognizer - there is not
    // any if it is a gesture or object recognizer.
    CComVariant vLanguages;
    if (SUCCEEDED(spIInkRecognizer->get_Languages(&vLanguages)))
    {
        if ((VT_ARRAY == (VT_ARRAY & vLanguages.vt))           // it should be an array
            && (NULL != vLanguages.parray)
            && (0 < vLanguages.parray->rgsabound[0].cElements)) // with at least one element
        {
            // This is a language recognizer. Add its name to the menu.
            CComBSTR bstrName;
            if (SUCCEEDED(spIInkRecognizer->get_Name(&bstrName)))
                ...
        }
    }
```



## <a name="creating-an-ink-collector"></a><span data-ttu-id="563ba-121">Criando um coletor de tinta</span><span class="sxs-lookup"><span data-stu-id="563ba-121">Creating an Ink Collector</span></span>

<span data-ttu-id="563ba-122">O método OnCreate do aplicativo cria um objeto [**InkCollector**](inkcollector-class.md) , conecta-o à sua origem de evento e habilita a coleta de tinta.</span><span class="sxs-lookup"><span data-stu-id="563ba-122">The application's OnCreate method creates an [**InkCollector**](inkcollector-class.md) object, connects it to its event source, and enables ink collection.</span></span>


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a><span data-ttu-id="563ba-123">Criando um contexto de reconhecedor</span><span class="sxs-lookup"><span data-stu-id="563ba-123">Creating a Recognizer Context</span></span>

<span data-ttu-id="563ba-124">O método CreateRecoContext do aplicativo cria e inicializa um novo contexto de reconhecedor e configura os guias com suporte no idioma associado.</span><span class="sxs-lookup"><span data-stu-id="563ba-124">The application's CreateRecoContext method creates and initializes a new recognizer context, and sets up the guides supported by the associated language.</span></span> <span data-ttu-id="563ba-125">O método [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) do objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) cria um objeto [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) para o idioma.</span><span class="sxs-lookup"><span data-stu-id="563ba-125">The [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object's [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) method creates a [**IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) object for the language.</span></span> <span data-ttu-id="563ba-126">Se necessário, o contexto do reconhecedor antigo é substituído.</span><span class="sxs-lookup"><span data-stu-id="563ba-126">If necessary, the old recognizer context is replaced.</span></span> <span data-ttu-id="563ba-127">O contexto está conectado à origem do evento.</span><span class="sxs-lookup"><span data-stu-id="563ba-127">The context is connected to its event source.</span></span> <span data-ttu-id="563ba-128">Por fim, a propriedade [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) do contexto do reconhecedor é verificada para quais guias o contexto do reconhecedor dá suporte.</span><span class="sxs-lookup"><span data-stu-id="563ba-128">Finally, the [**Capabilities**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) property of the recognizer context is checked for which guides the recognizer context supports.</span></span>


```C++
// Create a recognizer context
CComPtr<IInkRecognizerContext2> spNewContext;
if (FAILED(pIInkRecognizer2->CreateRecognizerContext(&spNewContext)))
    return false;

// Replace the current context with the new one
if (m_spIInkRecoContext != NULL)
{
    // Close the connection to the recognition events source
    IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventUnadvise(m_spIInkRecoContext);
}
m_spIInkRecoContext.Attach(spNewContext.Detach());

// Establish a connection with the recognizer context's event source
if (FAILED(IInkRecognitionEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkRecoContext)))
    ...

// Set the guide if it's supported by the recognizer and has been created 
int cRows = 0, cColumns = 0;
InkRecognizerCapabilities dwCapabilities = IRC_DontCare;
if (SUCCEEDED(pIInkRecognizer->get_Capabilities(&dwCapabilities)))
    ...
```



## <a name="collecting-strokes-and-displaying-recognition-results"></a><span data-ttu-id="563ba-129">Coletando traços e exibindo resultados de reconhecimento</span><span class="sxs-lookup"><span data-stu-id="563ba-129">Collecting Strokes and Displaying Recognition Results</span></span>

<span data-ttu-id="563ba-130">O método onstroke do aplicativo atualiza o [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) do coletor de tinta, cancela as solicitações de reconhecimento assíncrono existentes e cria uma solicitação de reconhecimento no contexto do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="563ba-130">The application's OnStroke method updates the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) of the ink collector, cancels existing asynchronous recognition requests, and creates a recognition request on the recognizer context.</span></span>


```C++
// Add the new stroke to the current collection
hr = m_spIInkStrokes->Add(pIInkStroke);

if (SUCCEEDED(hr))
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();

    // Ask the context to update the recognition results with newly added strokes
    // When the results are ready, the recognizer context returns them
    // through the corresponding event RecognitionWithAlternates
    CComVariant vCustomData;
    m_spIInkRecoContext->BackgroundRecognize(vCustomData);
}
```



<span data-ttu-id="563ba-131">O método do aplicativo `OnRecognition` envia os resultados da solicitação de reconhecimento para o método da janela de saída `UpdateString` .</span><span class="sxs-lookup"><span data-stu-id="563ba-131">The application's `OnRecognition` method sends the results of the recognition request to the output window's `UpdateString` method.</span></span>


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a><span data-ttu-id="563ba-132">Excluindo os traços e os resultados de reconhecimento</span><span class="sxs-lookup"><span data-stu-id="563ba-132">Deleting Strokes and Recognition Results</span></span>

<span data-ttu-id="563ba-133">O método OnClear do aplicativo exclui todos os traços e os resultados de reconhecimento do objeto [**InkDisp**](inkdisp-class.md) e limpa as janelas.</span><span class="sxs-lookup"><span data-stu-id="563ba-133">The application's OnClear method deletes all strokes and recognition results from the [**InkDisp**](inkdisp-class.md) object and clears the windows.</span></span> <span data-ttu-id="563ba-134">A associação do contexto do reconhecedor com sua coleção [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) é removida.</span><span class="sxs-lookup"><span data-stu-id="563ba-134">The recognizer context's association with its [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is removed.</span></span>


```C++
// Detach the current stroke collection from the recognizer context and release it
if (m_spIInkRecoContext != NULL)
    m_spIInkRecoContext->putref_Strokes(NULL);

m_spIInkStrokes.Release();

// Clear the custom strokes collection
if (m_spIInkCustomStrokes != NULL)
    m_spIInkCustomStrokes->Clear();

// Delete all strokes from the Ink object
// Passing NULL as a stroke collection pointer means asking to delete all strokes
m_spIInkDisp->DeleteStrokes(NULL);

// Get a new stroke collection from the ink object
...
// Ask for an empty collection by passing an empty variant 
if (SUCCEEDED(m_spIInkDisp->CreateStrokes(v, &m_spIInkStrokes)))
{
    // Attach it to the recognizer context
    if (FAILED(m_spIInkRecoContext->putref_Strokes(m_spIInkStrokes)))
        ...
}
```



## <a name="changing-recognizer-contexts"></a><span data-ttu-id="563ba-135">Alterando contextos do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="563ba-135">Changing Recognizer Contexts</span></span>

<span data-ttu-id="563ba-136">O método OnNewStrokes do aplicativo é chamado quando o usuário seleciona um reconhecedor no menu criar novos traços.</span><span class="sxs-lookup"><span data-stu-id="563ba-136">The application's OnNewStrokes method is called when the user selects a recognizer in the Create New Strokes menu.</span></span> <span data-ttu-id="563ba-137">O [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) atual é salvo.</span><span class="sxs-lookup"><span data-stu-id="563ba-137">The current [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) is saved.</span></span> <span data-ttu-id="563ba-138">Se um reconhecedor de idioma diferente tiver sido selecionado, um novo contexto de reconhecedor será criado.</span><span class="sxs-lookup"><span data-stu-id="563ba-138">If a different language recognizer was selected, a new recognizer context is created.</span></span> <span data-ttu-id="563ba-139">Em seguida, um novo **InkStrokes** é anexado ao novo contexto do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="563ba-139">Then, a new **InkStrokes** is attached to the new recognizer context.</span></span>


```C++
// Save the current stroke collection if there is any
if (m_spIInkRecoContext != NULL)
{
    // Cancel the previous background recognition requests
    // which have not been processed yet
    m_spIInkRecoContext->StopBackgroundRecognition();
    
    // Let the context know that there'll be no more input 
    // for the attached stroke collection
    m_spIInkRecoContext->EndInkInput();

    // Add the stroke collection to the Ink object's CustomStrokes collection
    SaveStrokeCollection();
}
...
// If a different recognizer was selected, create a new recognizer context
// Else, reuse the same recognizer context
if (wID != m_nCmdRecognizer)
{
    // Get a pointer to the recognizer object from the recognizer collection  
    CComPtr<IInkRecognizer> spIInkRecognizer;
    if ((m_spIInkRecognizers == NULL)
        || FAILED(m_spIInkRecognizers->Item(wID - ID_RECOGNIZER_FIRST,
                                             &spIInkRecognizer))
        || (false == CreateRecoContext(spIInkRecognizer)))
    {
        // restore the cursor
        ::SetCursor(hCursor);
        return 0;
    }

    // Update the status bar
    m_bstrCurRecoName.Empty();
    spIInkRecognizer->get_Name(&m_bstrCurRecoName);
    UpdateStatusBar();

    // Store the selected recognizer's command id
    m_nCmdRecognizer = wID;
}
```



<span data-ttu-id="563ba-140">Em seguida, ele chama StartNewStrokeCollection, que cria um [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) vazio e o anexa ao contexto do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="563ba-140">It then calls StartNewStrokeCollection, which creates an empty [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) and attaches it to the recognizer context.</span></span>

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a><span data-ttu-id="563ba-141">Salvando a coleção de traços para um contexto de reconhecedor</span><span class="sxs-lookup"><span data-stu-id="563ba-141">Saving the Strokes Collection for a Recognizer Context</span></span>

<span data-ttu-id="563ba-142">O método do aplicativo `SaveStrokeCollection` verifica um contexto de reconhecedor existente e finaliza o reconhecimento da coleção de traços atual.</span><span class="sxs-lookup"><span data-stu-id="563ba-142">The application's `SaveStrokeCollection` method checks for an existing recognizer context, and finalizes the recognition of the current strokes collection.</span></span> <span data-ttu-id="563ba-143">Em seguida, a coleção [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) é adicionada à [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) do objeto Ink.</span><span class="sxs-lookup"><span data-stu-id="563ba-143">Then the [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection is added to the [**CustomStrokes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) of the ink object.</span></span>


```C++
if (m_spIInkRecoContext != NULL)
{
    if (SUCCEEDED(m_spIInkStrokes->get_Count(&lCount)) && 0 != lCount)
    {
        CComPtr<IInkRecognitionResult> spIInkRecoResult;
        InkRecognitionStatus RecognitionStatus;
        if (SUCCEEDED(m_spIInkRecoContext->Recognize(&RecognitionStatus, &spIInkRecoResult)))
        {
            if (SUCCEEDED(spIInkRecoResult->SetResultOnStrokes()))
            {
                CComBSTR bstr;
                spIInkRecoResult->get_TopString(&bstr);
                m_wndResults.UpdateString(bstr);
            }
            ...
        }
    }
    // Detach the stroke collection from the old recognizer context
    m_spIInkRecoContext->putref_Strokes(NULL);
}

// Now add it to the ink's custom strokes collection
// Each item (stroke collection) of the custom strokes must be identified
// by a unique string. Here we generate a GUID for this.
if ((0 != lCount) && (m_spIInkCustomStrokes != NULL))
{
    GUID guid;
    WCHAR szGuid[40]; // format: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}"
    if (SUCCEEDED(::CoCreateGuid(&guid)) 
        && (::StringFromGUID2(guid, szGuid, countof(szGuid)) != 0))
    {
        CComBSTR bstrGuid(szGuid);
        if (FAILED(m_spIInkCustomStrokes->Add(bstrGuid, m_spIInkStrokes)))
            ...
```



 

 
