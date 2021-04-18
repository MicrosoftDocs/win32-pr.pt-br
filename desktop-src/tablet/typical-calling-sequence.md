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
# <a name="typical-calling-sequence"></a>Sequência de chamada típica

Os métodos que você deve implementar para criar um reconhecedor de tinta são chamados pelas APIs da plataforma do Tablet PC e não diretamente por um aplicativo habilitado para tinta.

As etapas a seguir representam uma sequência de chamada típica para a implementação desses métodos:

1.  A DLL está carregada.
2.  Um identificador [HRECOGNIZER](hrecognizer-handle.md) é criado.
3.  Um identificador [HRECOCONTEXT](hrecocontext-handle.md) é criado.
4.  As opções e os modos do reconhecedor são definidos para este contexto.
5.  Os traços são adicionados aos dados de tinta.
6.  A entrada foi encerrada.
7.  A tinta é reconhecida.
8.  Os resultados de reconhecimento são retornados.
9.  O identificador [HRECOCONTEXT](hrecocontext-handle.md) é destruído.
10. O identificador [HRECOGNIZER](hrecognizer-handle.md) é destruído.

A sequência de chamada também é ilustrada na seguinte estrutura de código:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[APIs do Recognizer](recognizer-apis.md)
</dt> <dt>

[Arquitetura da API de reconhecimento](recognition-api-architecture.md)
</dt> </dl>

 

 



