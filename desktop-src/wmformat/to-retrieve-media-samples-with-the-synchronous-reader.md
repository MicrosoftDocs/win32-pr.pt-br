---
title: Para recuperar amostras de mídia com o leitor síncrono
description: Para recuperar amostras de mídia com o leitor síncrono
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- ASF (Advanced Systems Format), recuperando amostras de mídia
- ASF (formato de sistemas avançados), recuperando amostras de mídia
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- leitores síncronos, recuperando amostras de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365568"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a>Para recuperar amostras de mídia com o leitor síncrono

Você deve solicitar cada exemplo um de cada vez do leitor síncrono. Isso lhe dá mais controle sobre os exemplos recebidos e quando você os recebe.

Use o método [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) para recuperar um exemplo. Você precisa passar principalmente ponteiros para variáveis que serão preenchidas com informações sobre o exemplo recuperado como parâmetros. O único parâmetro de entrada é *wStreamNum*. Se você passar um número de fluxo, o **GetNextSample** recuperará o próximo exemplo com o número de fluxo especificado. Se você passar zero para *wStreamNum*, o próximo exemplo que ocorre cronologicamente no arquivo será recuperado.

Por padrão, o leitor síncrono recupera todas as amostras das saídas em um arquivo em ordem cronológica. Se você chamar **GetNextSample** e não houver mais amostras para obter, ele retornará \_ o NS e \_ não \_ mais \_ amostras, que é um código de erro com falha. Ao codificar, portanto, você pode simplesmente executar um loop por meio de amostras até que o método falhe.

> [!Note]  
> Para garantir que o leitor síncrono forneça as durações de exemplo corretas para fluxos de vídeo, você deve primeiro configurar a saída do fluxo. Chame o método [**IWMSyncReader:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) para definir a configuração de g \_ wszVideoSampleDurations como **true**.

 

Código de exemplo

O código de exemplo a seguir mostra como usar **GetNextSample** para recuperar todas as amostras em um arquivo.


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lendo arquivos com o leitor síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




