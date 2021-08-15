---
title: Transmissão de dados ASF
description: Transmissão de dados ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows SDK de Formato de Mídia, transmitindo dados ASF
- ASF (Advanced Systems Format), transmitindo dados
- ASF (Formato de Sistemas Avançados), transmitindo dados
- Windows SDK de Formato de Mídia, enviando dados ASF
- ASF (Advanced Systems Format), enviando dados
- ASF (Formato de Sistemas Avançados), enviando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44fc9ea0515822c765b0cb3af457254341a64f08e64d566aa9e226a48758e7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434460"
---
# <a name="broadcasting-asf-data"></a>Transmissão de dados ASF

Este tópico descreve como enviar dados ASF em uma rede usando o protocolo HTTP. O envio de arquivos por uma rede requer o uso do objeto writer, portanto, você deve ter uma compreensão geral desse objeto antes de ler este tópico. Para obter mais informações, consulte [Escrevendo arquivos ASF](writing-asf-files.md).

Se você estiver começando com dados descompactados, faça o seguinte:

1.  Crie o objeto writer chamando a [**função WMCreateWriter.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) Essa função retorna um **ponteiro IWMWriter.**
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  Crie o objeto de sink de rede chamando a [**função WMCreateWriterNetworkSink,**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) que retorna um ponteiro **IWMWriterNetworkSink.**
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  Chame [**IWMWriterNetworkSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) no sink de rede e especifique o número da porta a ser aberta; por exemplo, 8080. Opcionalmente, chame [**IWMWriterNetworkSink::GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) para obter a URL do host. Os clientes acessarão o conteúdo dessa URL. Você também pode chamar [**IWMWriterNetworkSink::SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) para restringir o número de clientes.
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  Anexe o sink de rede ao autor chamando [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) no autor, com um ponteiro para a interface **IWMWriterNetworkSink** do sink de rede.
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  De definir o perfil ASF chamando o método [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) no objeto writer, com um [**ponteiro IWMProfile.**](iwmprofile.md) Para obter informações sobre como criar um perfil, consulte [Trabalhando com perfis](working-with-profiles.md).
6.  Opcionalmente, especifique os metadados usando a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) no autor.
7.  Chame [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) no autor.
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  Para cada exemplo, chame o [**método IWMWriter::WriteSample.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) Especifique o número do fluxo, o tempo de apresentação, a duração do exemplo e um ponteiro para o buffer de exemplo. O **método WriteSample** compacta os exemplos.
9.  Quando terminar, chame [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) no autor.
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. Chame [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) no autor para desconectar o objeto do sink de rede.
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. Chame [**IWMWriterNetworkSink::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) no sink de rede para liberar a porta.
    ```C++
    hr = pNetSink->Close();
    ```

    

Outra maneira de transmitir conteúdo ASF em uma rede é lê-lo de um arquivo ASF existente. O exemplo WMVNetWrite fornecido no SDK demonstra essa abordagem. Além das etapas listadas anteriormente, faça o seguinte:

1.  Crie um objeto de leitor e chame **o método Open** com o nome do arquivo.
2.  Chame [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) no objeto de leitor, com o **valor TRUE.** Isso permite que o aplicativo leia todos os fluxos no arquivo, incluindo fluxos com exclusão mútua.
3.  Consulte o leitor para a interface [**IWMProfile.**](iwmprofile.md) Use esse ponteiro ao chamar [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) no objeto writer (etapa 5 no procedimento anterior).
4.  Para cada fluxo definido no perfil, chame [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) para obter o número do fluxo. Passe esse número de fluxo para o método [**IWMReaderAdvanced::SetReceiveStreamSamples do**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) leitor. Esse método informa ao leitor para fornecer amostras compactadas, em vez de decodificá-las. Os exemplos serão entregues ao aplicativo por meio do método de retorno de chamada [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) do aplicativo.

    Você deve obter informações de codec para cada fluxo que lê descompactado e adicioná-los ao header antes da difusão. Para obter as informações de codec, chame [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar os codecs associados ao arquivo no leitor. Selecione as informações de codec que corresponde à configuração do fluxo. Em seguida, de definir as informações de codec no autor chamando [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando as informações obtidas do leitor.

5.  Depois de definir o perfil no autor, chame [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) no autor para obter o número de entradas. Para cada entrada, chame [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) com o valor **NULL**. Isso indica ao objeto de autor que o aplicativo fornecerá amostras compactadas, portanto, o autor não precisa usar nenhum codecs para compactar os dados. Certifique-se de chamar **SetInputProps antes** de **chamar BeginWriting**.
6.  Opcionalmente, copie os atributos de metadados do leitor para o autor
7.  Como os exemplos do leitor já estão compactados, use o método [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) para gravar os exemplos, em vez do **método WriteSample.** O **método WriteStreamSample** ignora os procedimentos de compactação comuns do objeto de gravação.
8.  Quando o leitor atinge o final do arquivo, ele envia uma notificação \_ EOF wmt para o aplicativo.

Além disso, o aplicativo deve conduzir o relógio no objeto de leitor, para que o leitor esvaia dados do arquivo o mais rápido possível. Para fazer isso, chame o método [**IWMReaderAdvanced::SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) no leitor, com o **valor TRUE**. Depois que o leitor enviar a notificação WMT STARTED, chame \_ [**IWMReaderAdvanced::D eliverTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) e especifique o intervalo de tempo que o leitor deve fornecer. Depois que o leitor terminar de ler esse intervalo de tempo, ele chamará o método de retorno de chamada [**IWMReaderCallbackAdvanced::OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) do aplicativo. O aplicativo deve chamar **DeliverTime novamente** para ler o próximo intervalo de tempo. Por exemplo, para ler do arquivo em intervalos de um segundo:


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Enviando dados ASF por uma rede**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Trabalhando com os sinks do Writer**](working-with-writer-sinks.md)
</dt> </dl>

 

 




