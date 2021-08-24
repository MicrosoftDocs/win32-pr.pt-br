---
title: Adicionando coletores ao gravador
description: Adicionando coletores ao gravador
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- ASF (Advanced Systems Format), adicionando coletores ao gravador
- ASF (formato de sistemas avançados), adicionando coletores ao gravador
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- ASF (Advanced Systems Format), coletores de gravador
- ASF (formato de sistemas avançados), coletores de gravador
- coletores, adicionando ao gravador
- coletores de gravador, adicionando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca64b412dd83e9bbba1d8de66b2aef335573c9e50073c2afe898fed0c34761b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810016"
---
# <a name="adding-sinks-to-the-writer"></a>Adicionando coletores ao gravador

Os coletores de gravador são objetos separados do gravador e devem ser adicionados ao gravador a ser usado. Se estiver gravando em um arquivo, você pode simplesmente chamar [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), que configurará o coletor de arquivos automaticamente. Caso contrário, para adicionar um coletor ao gravador, chame o método [**IWMWriterAdvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) . **Addsink** requer um ponteiro para a interface [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) do coletor.

Quando você terminar de usar um coletor, deverá fechá-lo chamando o método apropriado, dependendo do tipo de coletor e, em seguida, remova-o do gravador chamando [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).

O código de exemplo a seguir mostra como criar um coletor de arquivos do gravador e adicioná-lo ao gravador. Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Obtendo mensagens de erro de um coletor**](getting-error-messages-from-a-sink.md)
</dt> <dt>

[**Interface IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Trabalhando com coletores de gravador**](working-with-writer-sinks.md)
</dt> </dl>

 

 




