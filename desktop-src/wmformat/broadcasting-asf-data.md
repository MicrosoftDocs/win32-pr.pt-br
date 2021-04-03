---
title: Transmissão de dados ASF
description: Transmissão de dados ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- SDK do Windows Media Format, transmitindo dados ASF
- ASF (Advanced Systems Format), dados de difusão
- ASF (formato de sistemas avançados), dados de difusão
- SDK do Windows Media Format, enviando dados do ASF
- ASF (Advanced Systems Format), enviando dados
- ASF (formato de sistemas avançados), enviando dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42339b4a3e60666c1ea0cb69a07dfdc836b19409
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104007223"
---
# <a name="broadcasting-asf-data"></a>Transmissão de dados ASF

Este tópico descreve como enviar dados ASF em uma rede usando o protocolo HTTP. O envio de arquivos por uma rede requer o uso do objeto Writer, portanto, você deve ter uma compreensão geral desse objeto antes de ler este tópico. Para obter mais informações, consulte [Writing ASF files](writing-asf-files.md).

Se você estiver iniciando com dados descompactados, faça o seguinte:

1.  Crie o objeto gravador chamando a função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . Essa função retorna um ponteiro **IWMWriter** .
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  Crie o objeto de coletor de rede chamando a função [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) , que retorna um ponteiro **IWMWriterNetworkSink** .
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  Chame [**IWMWriterNetworkSink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) no coletor de rede e especifique o número da porta a ser aberta; por exemplo, 8080. Opcionalmente, chame [**IWMWriterNetworkSink:: GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) para obter a URL do host. Os clientes acessarão o conteúdo dessa URL. Você também pode chamar [**IWMWriterNetworkSink:: SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) para restringir o número de clientes.
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  Anexe o coletor de rede ao gravador chamando [**IWMWriterAdvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) no gravador, com um ponteiro para a interface **IWMWriterNetworkSink** do coletor de rede.
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  Defina o perfil do ASF chamando o método [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) no objeto do gravador, com um ponteiro [**IWMProfile**](iwmprofile.md) . Para obter informações sobre como criar um perfil, consulte [trabalhando com perfis](working-with-profiles.md).
6.  Opcionalmente, especifique os metadados usando a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) no gravador.
7.  Chame [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) no gravador.
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  Para cada exemplo, chame o método [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) . Especifique o número do fluxo, a hora da apresentação, a duração do exemplo e um ponteiro para o buffer de exemplo. O método **WriteSample** compacta os exemplos.
9.  Quando terminar, chame [**IWMWriter:: redação**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) no gravador.
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. Chame [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) no gravador para desanexar o objeto de coletor de rede.
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. Chame [**IWMWriterNetworkSink:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) no coletor de rede para liberar a porta.
    ```C++
    hr = pNetSink->Close();
    ```

    

Outra maneira de transmitir conteúdo ASF por meio de uma rede é lê-lo de um arquivo ASF existente. O exemplo de WMVNetWrite fornecido no SDK demonstra essa abordagem. Além das etapas listadas anteriormente, faça o seguinte:

1.  Crie um objeto leitor e chame o método **Open** com o nome do arquivo.
2.  Chame [**IWMReaderAdvanced:: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) no objeto Reader, com o valor **true**. Isso permite que o aplicativo Leia cada fluxo no arquivo, incluindo fluxos com exclusão mútua.
3.  Consulte o leitor para a interface [**IWMProfile**](iwmprofile.md) . Use esse ponteiro quando você chamar [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) no objeto do gravador (etapa 5 no procedimento anterior).
4.  Para cada fluxo definido no perfil, chame [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) para obter o número do fluxo. Passe este número de fluxo para o método [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) do leitor. Esse método informa o leitor para fornecer amostras compactadas, em vez de decodificá-las. Os exemplos serão entregues ao aplicativo por meio do método de retorno de chamada [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) do aplicativo.

    Você deve obter informações de codec para cada fluxo que ler não compactado e adicioná-lo ao cabeçalho antes da transmissão. Para obter as informações do codec, chame [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar os codecs associados ao arquivo no leitor. Selecione as informações de codec que correspondem à configuração de fluxo. Em seguida, defina as informações do codec no gravador chamando [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando as informações obtidas do leitor.

5.  Depois de definir o perfil no gravador, chame [**IWMWriter:: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) no gravador para obter o número de entradas. Para cada entrada, chame [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) com o valor **NULL**. Isso indica para o objeto do gravador que o aplicativo fornecerá amostras compactadas, de modo que o gravador não precisa usar nenhum codec para compactar os dados. Certifique-se de chamar **SetInputProps** antes de chamar **BeginWriting**.
6.  Opcionalmente, copie os atributos de metadados do leitor para o gravador
7.  Como os exemplos do leitor já estão compactados, use o método [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) para gravar os exemplos, em vez do método **WriteSample** . O método **WriteStreamSample** ignora os procedimentos de compactação usuais do objeto gravador.
8.  Quando o leitor atinge o final do arquivo, ele envia uma notificação de \_ EOF WMT para o aplicativo.

Além disso, o aplicativo deve orientar o relógio no objeto leitor, para que o leitor receba os dados do arquivo o mais rápido possível. Para fazer isso, chame o método [**IWMReaderAdvanced:: SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) no leitor, com o valor **true**. Depois que o leitor envia a \_ notificação de WMT iniciado, chame [**IWMReaderAdvanced::D elivertime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) e especifique o intervalo de tempo que o leitor deve entregar. Depois que o leitor terminar de ler esse intervalo de tempo, ele chamará o método de retorno de chamada [**IWMReaderCallbackAdvanced:: ontime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) do aplicativo. O aplicativo deve chamar o atendimento de **entrega** novamente para ler o próximo intervalo de tempo. Por exemplo, para ler o arquivo em intervalos de um segundo:


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

[**Enviando dados ASF por meio de uma rede**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Trabalhando com coletores de gravador**](working-with-writer-sinks.md)
</dt> </dl>

 

 




