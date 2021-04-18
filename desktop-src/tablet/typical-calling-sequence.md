---
description: 'Os métodos que você deve implementar para criar um reconhecedor de tinta são chamados pelas APIs da plataforma do Tablet PC e não diretamente por um aplicativo habilitado para tinta. As etapas a seguir representam uma sequência de chamada típica para a implementação desses métodos: a DLL é carregada. Um&\# 160; O identificador HRECOGNIZER é criado. Um&\# 160; O identificador HRECOCONTEXT é criado. As opções e os modos do reconhecedor são definidos para este contexto. Os traços são adicionados aos dados de tinta. A entrada foi encerrada. A tinta é reconhecida. Os resultados de reconhecimento são retornados. O identificador HRECOCONTEXT é destruído. O identificador HRECOGNIZER é destruído. A sequência de chamada também é ilustrada na seguinte estrutura de código: C + + Recognizer (CLSID, &HREC); tempo (mais informações de tinta para reconhecer...) {//Criar um contexto, uma vez por parte da tinta a ser reconhecida HRC = CreateContext (HREC, &HRC);//Functions para configurar opções e modos para esse contexto setguide (HRC, pGuide, 0); Setfactoid (HRC, 5, telefone); somente se estiver no aplicativo com o Forms SetFlags (HRC, RECOFLAG \_ WordMode);//raro, somente se você quiser o modo de palavra, nenhum dicionário fora de Dictionary ou uma Unwordlist de segmentação única (HRC, HWL);//adicionar todos os traços nessa folha de tinta enquanto (mais traços...) {Addstroke (HRC, NULL, 800, pPacket, pXForm);//uma chamada por traço} EndInkInput(hrc); Isso Obtém o processo reconhecido pela tinta (HRC); Se esse for um aplicativo simples, ele o chamará para uma resposta simples GetBestResultString (HRC, Length, buffer); Se esse for um aplicativo complexo, ele o chamará para uma resposta completa GetLatticePtr (HRC, &pLattice); Destruir o contexto DestroyContext (HRC); }//Chamado pouco antes de o aplicativo desligar DestroyRecognizer (HREC);'
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: Sequência de chamada típica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832ea396c1d73748c4636d2cad5e17529b8d54df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105773037"
---
# <a name="typical-calling-sequence"></a><span data-ttu-id="99f6c-103">Sequência de chamada típica</span><span class="sxs-lookup"><span data-stu-id="99f6c-103">Typical Calling Sequence</span></span>

<span data-ttu-id="99f6c-104">Os métodos que você deve implementar para criar um reconhecedor de tinta são chamados pelas APIs da plataforma do Tablet PC e não diretamente por um aplicativo habilitado para tinta.</span><span class="sxs-lookup"><span data-stu-id="99f6c-104">The methods you must implement to create an ink recognizer are called by the Tablet PC Platform APIs and not directly by an ink-enabled application.</span></span>

<span data-ttu-id="99f6c-105">As etapas a seguir representam uma sequência de chamada típica para a implementação desses métodos:</span><span class="sxs-lookup"><span data-stu-id="99f6c-105">The following steps represent a typical calling sequence for the implementation of these methods:</span></span>

1.  <span data-ttu-id="99f6c-106">A DLL está carregada.</span><span class="sxs-lookup"><span data-stu-id="99f6c-106">The DLL is loaded.</span></span>
2.  <span data-ttu-id="99f6c-107">Um identificador [HRECOGNIZER](hrecognizer-handle.md) é criado.</span><span class="sxs-lookup"><span data-stu-id="99f6c-107">An [HRECOGNIZER](hrecognizer-handle.md) handle is created.</span></span>
3.  <span data-ttu-id="99f6c-108">Um identificador [HRECOCONTEXT](hrecocontext-handle.md) é criado.</span><span class="sxs-lookup"><span data-stu-id="99f6c-108">An [HRECOCONTEXT](hrecocontext-handle.md) handle is created.</span></span>
4.  <span data-ttu-id="99f6c-109">As opções e os modos do reconhecedor são definidos para este contexto.</span><span class="sxs-lookup"><span data-stu-id="99f6c-109">Recognizer options and modes are set for this context.</span></span>
5.  <span data-ttu-id="99f6c-110">Os traços são adicionados aos dados de tinta.</span><span class="sxs-lookup"><span data-stu-id="99f6c-110">Strokes are added to the ink data.</span></span>
6.  <span data-ttu-id="99f6c-111">A entrada foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="99f6c-111">Input is ended.</span></span>
7.  <span data-ttu-id="99f6c-112">A tinta é reconhecida.</span><span class="sxs-lookup"><span data-stu-id="99f6c-112">The ink is recognized.</span></span>
8.  <span data-ttu-id="99f6c-113">Os resultados de reconhecimento são retornados.</span><span class="sxs-lookup"><span data-stu-id="99f6c-113">The recognition results are returned.</span></span>
9.  <span data-ttu-id="99f6c-114">O identificador [HRECOCONTEXT](hrecocontext-handle.md) é destruído.</span><span class="sxs-lookup"><span data-stu-id="99f6c-114">The [HRECOCONTEXT](hrecocontext-handle.md) handle is destroyed.</span></span>
10. <span data-ttu-id="99f6c-115">O identificador [HRECOGNIZER](hrecognizer-handle.md) é destruído.</span><span class="sxs-lookup"><span data-stu-id="99f6c-115">The [HRECOGNIZER](hrecognizer-handle.md) handle is destroyed.</span></span>

<span data-ttu-id="99f6c-116">A sequência de chamada também é ilustrada na seguinte estrutura de código:</span><span class="sxs-lookup"><span data-stu-id="99f6c-116">The calling sequence is also illustrated in the following code outline:</span></span>


```C++
CreateRecognizer(CLSID, &hrec);
while (more pieces of ink to recognize ... )
{
  // Create a context, once per piece of ink to be recognized
  hrc = CreateContext(hrec, &hrc);

  // Functions to set up options and modes for this context
  SetGuide(hrc, pGuide, 0);
  SetFactoid(hrc, 5, PHONE); // only if in application with forms
  SetFlags(hrc, RECOFLAG_WORDMODE); // rare, only if wanting word mode, no out-of-dictionary, or single segmentation
  SetWordList(hrc, hwl);

  // Adding all the strokes in this piece of ink
  while (more strokes ... )
  {
    AddStroke(hrc, NULL, 800, pPacket, pXForm);  // one call per stroke
  }
  EndInkInput(hrc);

  // This gets the ink recognized
  Process(hrc);

  // If this is a simple application, it calls this for a simple answer
  GetBestResultString(hrc, length, buffer);

  // If this is a complex application, it calls this for a complete answer
  GetLatticePtr(hrc, &pLattice);

  // Destroy the context
  DestroyContext(hrc);
}
// Called just before the application shuts down
DestroyRecognizer(hrec);
```



## <a name="related-topics"></a><span data-ttu-id="99f6c-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="99f6c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99f6c-118">APIs do Recognizer</span><span class="sxs-lookup"><span data-stu-id="99f6c-118">Recognizer APIs</span></span>](recognizer-apis.md)
</dt> <dt>

[<span data-ttu-id="99f6c-119">Arquitetura da API de reconhecimento</span><span class="sxs-lookup"><span data-stu-id="99f6c-119">Recognition API Architecture</span></span>](recognition-api-architecture.md)
</dt> </dl>

 

 



