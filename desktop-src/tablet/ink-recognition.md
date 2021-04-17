---
description: Nem todos os aplicativos exigem o uso de reconhecimento, mas como a maioria dos aplicativos foi projetada com texto como seu tipo de dados primário, a capacidade de converter tinta em texto é muito valiosa.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Reconhecimento de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca4ec6f897c797d86df96c5d9c2cfd5d80f16c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556909"
---
# <a name="ink-recognition"></a><span data-ttu-id="fd032-103">Reconhecimento de tinta</span><span class="sxs-lookup"><span data-stu-id="fd032-103">Ink Recognition</span></span>

<span data-ttu-id="fd032-104">Nem todos os aplicativos exigem o uso de reconhecimento, mas como a maioria dos aplicativos foi projetada com texto como seu tipo de dados primário, a capacidade de converter tinta em texto é muito valiosa.</span><span class="sxs-lookup"><span data-stu-id="fd032-104">Not all applications require the use of recognition, but because most applications were designed with text as their primary data type, the ability to convert ink into text is very valuable.</span></span> <span data-ttu-id="fd032-105">Você pode usar os recursos de reconhecimento da API da plataforma Tablet PC para consultar informações sobre os mecanismos de reconhecimento disponíveis, como quais idiomas eles reconhecem.</span><span class="sxs-lookup"><span data-stu-id="fd032-105">You can use the recognition features of the Tablet PC platform API to query for information about the recognition engines that are available, such as what languages they recognize.</span></span> <span data-ttu-id="fd032-106">Em seguida, você pode enviar uma coleção de [**traços**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) de um objeto de [**tinta**](inkdisp-class.md) para um mecanismo de reconhecimento e fazer com que ele retorne um objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .</span><span class="sxs-lookup"><span data-stu-id="fd032-106">You can then send a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from an [**Ink**](inkdisp-class.md) object to a recognition engine and have it return a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span>

## <a name="recognizercontext-object"></a><span data-ttu-id="fd032-107">Objeto RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="fd032-107">RecognizerContext Object</span></span>

<span data-ttu-id="fd032-108">Um objeto [**RecognizerContext**](inkrecognizercontext-class.md) é a instanciação de um determinado reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="fd032-108">A [**RecognizerContext**](inkrecognizercontext-class.md) object is the instantiation of a given recognizer.</span></span> <span data-ttu-id="fd032-109">O objeto **RecognizerContext** permite que você reconheça uma determinada coleção de traços de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="fd032-109">The **RecognizerContext** object enables you to recognize a given collection of strokes synchronously or asynchronously.</span></span> <span data-ttu-id="fd032-110">Ao reconhecer de forma assíncrona, o objeto **RecognizerContext** retorna o objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) em um retorno de chamada de evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fd032-110">When recognizing asynchronously, the **RecognizerContext** object returns the [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object in an event callback to the application.</span></span>

## <a name="recognizers-and-recognizer-objects"></a><span data-ttu-id="fd032-111">Reconhecedores e objetos reconhecedor</span><span class="sxs-lookup"><span data-stu-id="fd032-111">Recognizers and Recognizer Objects</span></span>

<span data-ttu-id="fd032-112">Um único Tablet PC pode ter um ou mais reconhecedores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="fd032-112">A single Tablet PC may have one or more recognizers available.</span></span> <span data-ttu-id="fd032-113">Você pode consultar a coleção do reconhecedor para determinar qual reconhecedor usar.</span><span class="sxs-lookup"><span data-stu-id="fd032-113">You can query the recognizer's collection to determine which recognizer to use.</span></span> <span data-ttu-id="fd032-114">Um reconhecedor fornece informações específicas sobre seus recursos, como o idioma que ele pode reconhecer e o fabricante.</span><span class="sxs-lookup"><span data-stu-id="fd032-114">A recognizer provides specific information about its capabilities such as the language it can recognize and the manufacturer.</span></span>

<span data-ttu-id="fd032-115">Para determinar se pelo menos um reconhecedor está instalado, crie uma instância de um objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) , conforme mostrado nos exemplos de código C++ e C a seguir \# .</span><span class="sxs-lookup"><span data-stu-id="fd032-115">To determine whether at least one recognizer is installed, instantiate an [**InkRecognizerContext**](inkrecognizercontext-class.md) object as shown in the following C++ and C\# code examples.</span></span> <span data-ttu-id="fd032-116">Se um reconhecedor não estiver presente, essa chamada para [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) falhará.</span><span class="sxs-lookup"><span data-stu-id="fd032-116">If a recognizer is not present, this call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails.</span></span>


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



## <a name="recognitionresult-and-recognitionalternate-objects"></a><span data-ttu-id="fd032-117">Objetos RecognitionResult e RecognitionAlternate</span><span class="sxs-lookup"><span data-stu-id="fd032-117">RecognitionResult and RecognitionAlternate Objects</span></span>

<span data-ttu-id="fd032-118">Os resultados do reconhecimento são retornados em um objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) .</span><span class="sxs-lookup"><span data-stu-id="fd032-118">The results of the recognition are returned in a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span> <span data-ttu-id="fd032-119">Os resultados contêm uma melhor cadeia de caracteres de resultado na propriedade [TopString](/previous-versions/ms829602(v=msdn.10)) , bem como uma coleção de resultados alternativos em uma coleção [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) .</span><span class="sxs-lookup"><span data-stu-id="fd032-119">The results contain a best result string in the [TopString](/previous-versions/ms829602(v=msdn.10)) property, as well as a collection of alternative results in a [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) collection.</span></span> <span data-ttu-id="fd032-120">O objeto **RecognitionResult** pode ser persistido com a coleção de [**traços**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) originais da qual foi gerado.</span><span class="sxs-lookup"><span data-stu-id="fd032-120">The **RecognitionResult** object can be persisted with the original [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from which it was generated.</span></span>

## <a name="recognizerguide-structure"></a><span data-ttu-id="fd032-121">Estrutura RecognizerGuide</span><span class="sxs-lookup"><span data-stu-id="fd032-121">RecognizerGuide Structure</span></span>

<span data-ttu-id="fd032-122">O guia do reconhecedor pode consistir em linhas e colunas e fornece ao reconhecedor um contexto melhor para executar o reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="fd032-122">The recognizer guide can consist of rows and columns, and gives the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="fd032-123">Por exemplo, você pode desenhar linhas horizontais na tela de um usuário, quase como um pedaço de papel, que mostra onde deve ocorrer o manuscrito (esse tipo de guia consistiria apenas em linhas e nenhuma coluna).</span><span class="sxs-lookup"><span data-stu-id="fd032-123">For example, you can draw horizontal lines on a user's screen, almost like a ruled piece of paper, that show where handwriting should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="fd032-124">Se um usuário gravar nas linhas, em vez de algum espaço arbitrário, a precisão de reconhecimento melhorará.</span><span class="sxs-lookup"><span data-stu-id="fd032-124">If a user writes on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="fd032-125">A ilustração a seguir mostra uma estrutura [**RecognizerGuide**](inkrecognizerguide-class.md) com duas linhas para entrada.</span><span class="sxs-lookup"><span data-stu-id="fd032-125">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with two lines for input.</span></span>

![ilustração mostrando o guia do reconhecedor de duas linhas](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

<span data-ttu-id="fd032-127">A ilustração a seguir mostra uma estrutura [**RecognizerGuide**](inkrecognizerguide-class.md) com quatro colunas e três linhas.</span><span class="sxs-lookup"><span data-stu-id="fd032-127">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with four columns and three rows.</span></span>

![ilustração mostrando o guia do reconhecedor de três por quatro](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

<span data-ttu-id="fd032-129">Para obter mais informações sobre como usar a estrutura [**RecognizerGuide**](inkrecognizerguide-class.md) , consulte o tópico referência do **RecognizerGuide** .</span><span class="sxs-lookup"><span data-stu-id="fd032-129">For more information about using the [**RecognizerGuide**](inkrecognizerguide-class.md) structure, see the **RecognizerGuide** reference topic.</span></span>

 

 
