---
description: Este exemplo demonstra os recursos avançados da API (interface de programação) de aplicativo (API) de Automação de PC MicrosoftTablet usada para reconhecimento de manuscrito.
ms.assetid: c9e6613c-5797-44c3-8ce1-92d4d1459ecf
title: Exemplo de vários reconhecedores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d687f1bddd1f3c57cc482070b8e5826126b6e5b0f716fa3649df01ad6eab30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856545"
---
# <a name="multiple-recognizers-sample"></a>Exemplo de vários reconhecedores

Este exemplo demonstra os recursos avançados da API (interface de programação) de aplicativo (API) de Automação de PC MicrosoftTablet usada para reconhecimento *de* manuscrito.

Isso inclui o seguinte:

-   Enumerando os reconhecedores instalados
-   Criando um *contexto de reconhecedor* com um reconhecedor de idioma específico
-   Serializando resultados de reconhecimento com uma coleção de traços
-   Organizando coleções de traços em uma coleção personalizada dentro do [**objeto InkDisp**](inkdisp-class.md)
-   Serializando *objetos* de tinta para e recuperando-os de um arquivo *ISF (formato serializado de tinta)*
-   Configurar guias de entrada do reconhecedor
-   Usando o reconhecimento síncrono e assíncrono

## <a name="ink-headers"></a>Headers de tinta

Primeiro, inclua os títulos para interfaces de Automação de Tablet PC. Eles são instalados com o SDK (Software Development Kit) do Microsoft Windows Tablet XP Edition.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



O arquivo EventSinks.h define as interfaces IInkEventsImpl e IInkRecognitionEventsImpl.


```C++
#include "EventSinks.h"
```



## <a name="enumerating-the-installed-recognizers"></a>Enumerando os reconhecedores instalados

O método LoadMenu do aplicativo preenche o menu Criar Novos Traços com os reconhecedores disponíveis. Um [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) é criado. Se *a* propriedade [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) de um objeto **InkRecognizers** não estiver vazia, o reconhecedor será um reconhecedor de texto e o valor de sua propriedade [**Name**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_name) será adicionado ao menu.


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



## <a name="creating-an-ink-collector"></a>Criando um coletor de tinta

O método OnCreate do aplicativo cria um objeto [**InkCollector,**](inkcollector-class.md) conecta-o à origem do evento e habilita a coleta de tinta.


```C++
// Create an ink collector object.
hr = m_spIInkCollector.CoCreateInstance(CLSID_InkCollector);

// Establish a connection to the collector's event source.
hr = IInkCollectorEventsImpl<CMultiRecoApp>::DispEventAdvise(m_spIInkCollector);

// Enable ink input in the m_wndInput window
hr = m_spIInkCollector->put_hWnd((long)m_wndInput.m_hWnd);
hr = m_spIInkCollector->put_Enabled(VARIANT_TRUE);
```



## <a name="creating-a-recognizer-context"></a>Criando um contexto de reconhecedor

O método CreateRecoContext do aplicativo cria e inicializa um novo contexto de reconhecedor e configura os guias com suporte no idioma associado. O método [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) do objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) cria um [**objeto IInkRecognizerContext2**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizercontext2) para o idioma. Se necessário, o contexto antigo do reconhecedor será substituído. O contexto está conectado à origem do evento. Por fim, [**a propriedade Funcionalidades**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_capabilities) do contexto do reconhecedor é verificada para a qual guia o contexto do reconhecedor dá suporte.


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



## <a name="collecting-strokes-and-displaying-recognition-results"></a>Coletando traços e exibindo resultados de reconhecimento

O método OnTumke do aplicativo atualiza os [**InkStrkes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) do coletor de tinta, cancela as solicitações de reconhecimento assíncronas existentes e cria uma solicitação de reconhecimento no contexto do reconhecedor.


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



O método do `OnRecognition` aplicativo envia os resultados da solicitação de reconhecimento para o método da janela de `UpdateString` saída.


```C++
// Update the output window with the new results
m_wndResults.UpdateString(bstrRecognizedString);
```



## <a name="deleting-strokes-and-recognition-results"></a>Excluindo traços e resultados de reconhecimento

O método OnClear do aplicativo exclui todos os traços e resultados de reconhecimento do objeto [**InkDisp**](inkdisp-class.md) e limpa as janelas. A associação do contexto do reconhecedor com sua [**coleção InkStrkes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) é removida.


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



## <a name="changing-recognizer-contexts"></a>Alterando contextos do reconhecedor

O método OnNewStrkes do aplicativo é chamado quando o usuário seleciona um reconhecedor no menu Criar Novos Traços. O [**InkStrkes atual**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) é salvo. Se um reconhecedor de idioma diferente tiver sido selecionado, um novo contexto de reconhecedor será criado. Em seguida, um **novo InkStrkes** é anexado ao novo contexto de reconhecedor.


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



Em seguida, ele chama StartNewRogkeCollection, que cria um [**InkStrkes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) vazio e o anexa ao contexto do reconhecedor.

## <a name="saving-the-strokes-collection-for-a-recognizer-context"></a>Salvando a coleção de traços para um contexto de reconhecedor

O método do aplicativo verifica um contexto de reconhecedor existente e finaliza o `SaveStrokeCollection` reconhecimento da coleção de traços atual. Em [**seguida, a coleção InkStrkes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) é adicionada [**ao CustomStrkes**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-get_customstrokes) do objeto de tinta.


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



 

 
