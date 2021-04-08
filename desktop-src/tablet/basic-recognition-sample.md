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
# <a name="basic-recognition-sample"></a><span data-ttu-id="57bad-103">Exemplo de reconhecimento básico</span><span class="sxs-lookup"><span data-stu-id="57bad-103">Basic Recognition Sample</span></span>

<span data-ttu-id="57bad-104">Este aplicativo demonstra como você pode criar um aplicativo simples de reconhecimento de *manuscrito* .</span><span class="sxs-lookup"><span data-stu-id="57bad-104">This application demonstrates how you can build a simple *handwriting* recognition application.</span></span>

<span data-ttu-id="57bad-105">Este programa cria um objeto [**InkCollector**](inkcollector-class.md) para habilitar a *tinta* na janela e um objeto de *contexto do reconhecedor* padrão.</span><span class="sxs-lookup"><span data-stu-id="57bad-105">This program creates an [**InkCollector**](inkcollector-class.md) object to *ink*-enable the window and a default *recognizer context* object.</span></span> <span data-ttu-id="57bad-106">Após receber o "Recognize!"</span><span class="sxs-lookup"><span data-stu-id="57bad-106">Upon receiving the "Recognize!"</span></span> <span data-ttu-id="57bad-107">, acionado do menu do aplicativo, os traços de tinta coletados são passados para o contexto do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="57bad-107">command, fired from the application's menu, the collected ink strokes are passed to the recognizer context.</span></span> <span data-ttu-id="57bad-108">A melhor cadeia de caracteres de resultado é apresentada em uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="57bad-108">The best result string is presented in a message box.</span></span>

## <a name="creating-the-recognizercontext-object"></a><span data-ttu-id="57bad-109">Criando o objeto RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="57bad-109">Creating the RecognizerContext Object</span></span>

<span data-ttu-id="57bad-110">No procedimento WndProc para o aplicativo, quando a mensagem de \_ criação do WM é recebida na inicialização, um novo contexto de reconhecedor que usa o reconhecedor padrão é criado.</span><span class="sxs-lookup"><span data-stu-id="57bad-110">In the WndProc procedure for the application, when the WM\_CREATE message is received on startup, a new recognizer context that uses the default recognizer is created.</span></span> <span data-ttu-id="57bad-111">Esse contexto é usado para todo o reconhecimento no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="57bad-111">This context is used for all recognition in the application.</span></span>


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



## <a name="recognizing-the-strokes"></a><span data-ttu-id="57bad-112">Reconhecendo os traços</span><span class="sxs-lookup"><span data-stu-id="57bad-112">Recognizing the Strokes</span></span>

<span data-ttu-id="57bad-113">O comando Recognize é recebido quando o usuário clica no Recognize!</span><span class="sxs-lookup"><span data-stu-id="57bad-113">The recognize command is received when the user clicks the Recognize!</span></span> <span data-ttu-id="57bad-114">.</span><span class="sxs-lookup"><span data-stu-id="57bad-114">menu item.</span></span> <span data-ttu-id="57bad-115">O código obtém um ponteiro para a [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) de tinta (pIInkStrokes) do objeto [**InkDisp**](inkdisp-class.md) e, em seguida, passa o **InkStrokes** para o contexto do reconhecedor usando uma chamada para os traços de PUTREF \_ .</span><span class="sxs-lookup"><span data-stu-id="57bad-115">The code gets a pointer to the ink [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) (pIInkStrokes) off of the [**InkDisp**](inkdisp-class.md) object, and then passes the **InkStrokes** to the recognizer context using a call to putref\_Strokes.</span></span>


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



<span data-ttu-id="57bad-116">Em seguida, o código chama o método [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) do objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) , passando um ponteiro para um objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) para manter os resultados.</span><span class="sxs-lookup"><span data-stu-id="57bad-116">The code then calls the [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method of the [**InkRecognizerContext**](inkrecognizercontext-class.md) object, passing in a pointer to an [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object to hold the results.</span></span>


```C++
              // Recognize
              IInkRecognitionResult* pIInkRecoResult = NULL;
              hr = g_pIInkRecoContext->Recognize(&pIInkRecoResult);
              if (SUCCEEDED(hr)) 
              {
```



<span data-ttu-id="57bad-117">Por fim, o código usa a propriedade [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) do objeto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) para recuperar o resultado do reconhecimento superior em uma variável de cadeia de caracteres, libera o objeto **IInkRecognitionResult** e exibe a cadeia de caracteres em uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="57bad-117">Finally, the code uses the [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object's [**TopString**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionresult-get_topstring) property retrieve the top recognition result into a string variable, releases the **IInkRecognitionResult** object, and displays the string in a message box.</span></span>


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



<span data-ttu-id="57bad-118">Certifique-se de redefinir o contexto do reconhecedor entre os usos.</span><span class="sxs-lookup"><span data-stu-id="57bad-118">Be sure to reset the recognizer context between usages.</span></span>


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



 

 
