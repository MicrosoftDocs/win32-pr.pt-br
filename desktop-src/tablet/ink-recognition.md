---
description: Nem todos os aplicativos exigem o uso de reconhecimento, mas como a maioria dos aplicativos foi projetada com texto como seu tipo de dados primário, a capacidade de converter tinta em texto é muito valiosa.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Reconhecimento de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c3f1431aca97f41b4de9aef64108f3e619ef7b6f9239f46fdde9f7bf4ff3da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718282"
---
# <a name="ink-recognition"></a>Reconhecimento de tinta

Nem todos os aplicativos exigem o uso de reconhecimento, mas como a maioria dos aplicativos foi projetada com texto como seu tipo de dados primário, a capacidade de converter tinta em texto é muito valiosa. Você pode usar os recursos de reconhecimento da API da plataforma tablet pc para consultar informações sobre os mecanismos de reconhecimento disponíveis, como quais idiomas eles reconhecem. Em seguida, você pode enviar uma coleção [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) de um [**objeto Ink**](inkdisp-class.md) para um mecanismo de reconhecimento e fazer com que ela retorne um [**objeto RecognitionResult.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult)

## <a name="recognizercontext-object"></a>Objeto RecognizerContext

Um [**objeto RecognizerContext**](inkrecognizercontext-class.md) é a insta instaência de um determinado reconhecedor. O **objeto RecognizerContext** permite que você reconheça uma determinada coleção de traços de forma síncrona ou assíncrona. Ao reconhecer de forma assíncrona, o objeto **RecognizerContext** retorna o objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) em um retorno de chamada de evento para o aplicativo.

## <a name="recognizers-and-recognizer-objects"></a>Reconhecedores e objetos reconhecedores

Um único tablet pc pode ter um ou mais reconhecedores disponíveis. Você pode consultar a coleção do reconhecedor para determinar qual reconhecedor usar. Um reconhecedor fornece informações específicas sobre seus recursos, como o idioma que ele pode reconhecer e o fabricante.

Para determinar se pelo menos um reconhecedor está instalado, insinue um objeto [**InkRecognizerContext,**](inkrecognizercontext-class.md) conforme mostrado nos exemplos de código C++ e C a \# seguir. Se um reconhecedor não estiver presente, essa chamada para [**CoCreateInstance falhará.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)


```C++
CComPtr<IInkRecognizerContext> g_pIInkRecoContext;
hr = CoCreateInstance(CLSID_InkRecognizerContext, 
      NULL, CLSCTX_INPROC_SERVER,
      IID_IInkRecognizerContext, 
(void **) &g_pIInkRecoContext);
if (FAILED(hr)) 
{
      ::MessageBox(NULL, TEXT("No recognizers installed.\nExiting."), 
      gc_szAppName, MB_ICONERROR);
      return -1;
}
```




```CSharp
try
{
  Recognizers recos = new Recognizers();//Check for recognizer.
  Recognizer defReco = recos.GetDefaultRecognizer();
  recoContext = defReco.CreateRecognizerContext();
}
catch
{
  MessageBox.Show("No recognizers installed.");
}
```



## <a name="recognitionresult-and-recognitionalternate-objects"></a>Objetos RecognitionResult e RecognitionAlternate

Os resultados do reconhecimento são retornados em um [**objeto RecognitionResult.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) Os resultados contêm uma melhor cadeia de caracteres de resultado na propriedade [TopString,](/previous-versions/ms829602(v=msdn.10)) bem como uma coleção de resultados alternativos em uma [**coleção RecognitionAlternates.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) O **objeto RecognitionResult** pode ser persistido com a coleção [**original strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) da qual ele foi gerado.

## <a name="recognizerguide-structure"></a>Estrutura RecognizerGuide

O guia do reconhecedor pode consistir em linhas e colunas e fornece ao reconhecedor um contexto melhor no qual executar o reconhecimento. Por exemplo, você pode desenhar linhas horizontais na tela de um usuário, quase como um trecho de papel, que mostra onde a manuscrito deve ocorrer (esse tipo de guia consistiria apenas em linhas e nenhuma coluna). Se um usuário grava nas linhas, em vez de algum espaço arbitrário, a precisão do reconhecimento melhora.

A ilustração a seguir mostra [**uma estrutura RecognizerGuide**](inkrecognizerguide-class.md) com duas linhas para entrada.

![ilustração mostrando o guia do reconhecedor de duas linhas](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

A ilustração a seguir mostra [**uma estrutura RecognizerGuide**](inkrecognizerguide-class.md) com quatro colunas e três linhas.

![ilustração mostrando o guia do reconhecedor de três por quatro](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

Para obter mais informações sobre como usar a [**estrutura RecognizerGuide,**](inkrecognizerguide-class.md) consulte o tópico de referência **RecognizerGuide.**

 

 
