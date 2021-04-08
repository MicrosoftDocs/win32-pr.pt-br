---
description: Este aplicativo demonstra como você pode criar um aplicativo simples de reconhecimento de manuscrito. Este programa cria um objeto InkCollector para habilitar a tinta na janela e um objeto de contexto do reconhecedor padrão.
ms.assetid: 6dc94293-cdf7-4b90-a5e8-559f376add26
title: Exemplo de reconhecimento básico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19679a6d1642a94ed813ba0428654b6e03009ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829699"
---
# <a name="basic-recognition-sample"></a>Exemplo de reconhecimento básico

Este aplicativo demonstra como você pode criar um aplicativo simples de reconhecimento de *manuscrito* .

Este programa cria um objeto [**InkCollector**](inkcollector-class.md) para habilitar a *tinta* na janela e um objeto de *contexto do reconhecedor* padrão. Após receber o "Recognize!" , acionado do menu do aplicativo, os traços de tinta coletados são passados para o contexto do reconhecedor. A melhor cadeia de caracteres de resultado é apresentada em uma caixa de mensagem.

## <a name="creating-the-recognizercontext-object"></a>Criando o objeto RecognizerContext

No procedimento WndProc para o aplicativo, quando a mensagem de \_ criação do WM é recebida na inicialização, um novo contexto de reconhecedor que usa o reconhecedor padrão é criado. Esse contexto é usado para todo o reconhecimento no aplicativo.


```C++
case WM_CREATE:
{
    HRESULT hr;
    hr = CoCreateInstance(CLSID_InkRecognizerContext,
             NULL, CLSCTX_INPROC_SERVER, IID_IInkRecognizerContext,
             (void **) &g_pIInkRecoContext);
    if (FAILED(hr))
    {
        ::MessageBox(NULL, TEXT("There are no handwriting recognizers installed.\n"
            "You need to have at least one in order to run this sample.\nExiting."),
            gc_szAppName, MB_ICONERROR);
        return -1;
    }
  //...
```



## <a name="recognizing-the-strokes"></a>Reconhecendo os traços

O comando Recognize é recebido quando o usuário clica no Recognize! . O código obtém um ponteiro para a [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) de tinta (pIInkStrokes) do objeto [**InkDisp**](inkdisp-class.md) e, em seguida, passa o **InkStrokes** para o contexto do reconhecedor usando uma chamada para os traços de PUTREF \_ .


```C++
 case WM_COMMAND:
  //...
  else if (wParam == ID_RECOGNIZE)
  {
      // change cursor to the system's Hourglass
      HCURSOR hCursor = ::SetCursor(::LoadCursor(NULL, IDC_WAIT));
      // Get a pointer to the ink stroke collection
      // This collection is a snapshot of the entire ink object
      IInkStrokes* pIInkStrokes = NULL;
      HRESULT hr = g_pIInkDisp->get_Strokes(&pIInkStrokes);
      if (SUCCEEDED(hr)) 
      {
          // Pass the stroke collection to the recognizer context
          hr = g_pIInkRecoContext->putref_Strokes(pIInkStrokes);
          if (SUCCEEDED(hr)) 
          {
```



Em seguida, o código chama o método [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) do objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) , passando um ponteiro para um objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) para manter os resultados.


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



Por fim, o código usa a propriedade [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) do objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) para recuperar o resultado do reconhecimento superior em uma variável de cadeia de caracteres, libera o objeto **IInkRecognitionResult** e exibe a cadeia de caracteres em uma caixa de mensagem.


```C++
                  // Get the best result of the recognition 
                  BSTR bstrBestResult = NULL;
                  hr = pIInkRecoResult->get_TopString(&bstrBestResult);
                  pIInkRecoResult->Release();
                  pIInkRecoResult = NULL;

                  // Show the result string
                  if (SUCCEEDED(hr) && bstrBestResult)
                  {
                      MessageBoxW(hwnd, bstrBestResult, 
                                  L"Recognition Results", MB_OK);
                      SysFreeString(bstrBestResult);
                  }  }
        
```



Certifique-se de redefinir o contexto do reconhecedor entre os usos.


```
              // Reset the recognizer context
              g_pIInkRecoContext->putref_Strokes(NULL);
          }
          pIInkStrokes->Release();
      }
      // restore the cursor
      ::SetCursor(hCursor);
  }
```



 

 
