---
title: Para recuperar exemplos de mídia com o Leitor Síncrono
description: Para recuperar exemplos de mídia com o Leitor Síncrono
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- ASF (Advanced Systems Format), recuperando exemplos de mídia
- ASF (Formato de Sistemas Avançados), recuperando exemplos de mídia
- ASF (Advanced Systems Format), leitores síncronos
- ASF (Formato de Sistemas Avançados), leitores síncronos
- leitores síncronos, recuperando exemplos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e1ec4fc7e8a894de304ea828cef9d8e019f4cdedfd2fbd851a427382ba741a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807426"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a>Para recuperar exemplos de mídia com o Leitor Síncrono

Você deve solicitar cada exemplo um de cada vez do leitor síncrono. Isso lhe dá mais controle sobre os exemplos recebidos e quando você os recebe.

Use o [**método IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) para recuperar um exemplo. Você precisa passar principalmente ponteiros para variáveis que serão preenchidas com informações sobre o exemplo recuperado como parâmetros. O único parâmetro de entrada é *wStreamNum.* Se você passar um número de fluxo, **GetNextSample** recuperará o próximo exemplo com o número de fluxo especificado. Se você passar zero para *wStreamNum*, o próximo exemplo que ocorrer cronologicamente no arquivo será recuperado.

Por padrão, o leitor síncrono recupera todos os exemplos das saídas em um arquivo em ordem cronológica. Se você chamar **GetNextSample** e não houver mais exemplos para obter, ele retornará NS \_ E NO MORE \_ \_ SAMPLES, que é um código de erro \_ com falha. Portanto, ao codificar, você pode simplesmente fazer um loop em exemplos até que o método falhe.

> [!Note]  
> Para garantir que o leitor síncrono entregue durações de exemplo corretas para fluxos de vídeo, primeiro você deve configurar a saída do fluxo. Chame o [**método IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) para definir a configuração g \_ wszVideoSampleDurations **como TRUE.**

 

Código de exemplo

O código de exemplo a seguir mostra como usar **GetNextSample** para recuperar todos os exemplos em um arquivo.


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

[**IWMSyncReader Interface**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lendo arquivos com o Leitor Síncrono**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




