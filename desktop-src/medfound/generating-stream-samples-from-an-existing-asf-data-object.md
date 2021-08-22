---
description: Gerando amostras de fluxo de um objeto de dados ASF existente
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Gerando amostras de fluxo de um objeto de dados ASF existente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97fb99440c3fc4721851f183b3bfc7aefafd3f652d0436b29e9cea1209ba59b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974445"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a>Gerando amostras de fluxo de um objeto de dados ASF existente

O objeto *divisor* de ASF é um componente de camada WMContainer que analisa o objeto de dados ASF de um arquivo ASF (Advanced Systems Format).

Antes de passar pacotes de dados para o separador, o aplicativo deve inicializar, configurar e selecionar fluxos no divisor para prepará-lo para o processo de análise. Para obter informações, consulte [criando o objeto divisor de ASF](creating-the-asf-splitter-object.md) e [Configurando o objeto divisor de ASF](configuring-the-asf-splitter-object.md).

Os métodos necessários para analisar o objeto de dados ASF são:

-   [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) que inicia o processo de análise enviando por push o buffer que contém os pacotes de dados para o divisor.
-   [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) que coleta amostras de fluxo que foram geradas do buffer passado para o divisor.

## <a name="finding-the-data-offset"></a>Localizando o deslocamento de dados

Antes de iniciar o processo de análise, o aplicativo deve localizar o objeto de dados no arquivo ASF. Há duas maneiras de obter o deslocamento do objeto de dados a partir do início do arquivo:

-   Antes de inicializar o objeto ContentInfo, você pode chamar o método [**IMFASFContentInfo:: Getheaders**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) . Esse método requer um buffer que contém os primeiros 30 bytes do cabeçalho ASF. Ele retorna o tamanho do cabeçalho inteiro que indica o deslocamento para o primeiro pacote de dados. Esse valor também inclui o tamanho do cabeçalho do objeto de dados de 50 bytes.
-   Depois de inicializar o objeto ContentInfo, você pode obter o descritor de apresentação chamando [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)e consultando o descritor de apresentação para o atributo de [**deslocamento de início de \_ dados MF PD \_ ASF \_ \_ \_**](mf-pd-asf-data-start-offset-attribute.md) . O valor desse atributo é o tamanho do cabeçalho.
    > [!Note]  
    > O atributo de [**\_ comprimento de dados MF PD \_ ASF \_ \_**](mf-pd-asf-data-length-attribute.md) no descritor de apresentação especifica o comprimento do objeto de dados ASF.

     

Em ambos os casos, o valor retornado é o tamanho do objeto de cabeçalho mais o tamanho da seção de cabeçalho do objeto de dados. Portanto, o valor resultante é o deslocamento para o início dos pacotes de dados no objeto de dados ASF. Quando você começa a enviar dados para o separador, os dados devem começar com esse deslocamento desde o início do arquivo ASF.

O valor de deslocamento é passado como um parâmetro para **ParseData** que inicia o processo de análise.

O objeto de dados é dividido em pacotes de dados. Cada pacote de dados contém um cabeçalho de pacote de dados que fornece informações de análise de pacotes e os dados de carga — os dados de mídia digital reais. Em um cenário de busca, o aplicativo pode querer que o divisor inicie a análise em um pacote de dados específico. Para fazer isso, você pode usar o indexador ASF é usado para recuperar o deslocamento. O indexador retorna um valor de deslocamento que começa no limite do pacote. Se você não estiver usando o indexador, verifique se o deslocamento começa no início do cabeçalho do pacote de dados. Se um deslocamento inválido for passado para o separador, como o valor não aponta para o limite do pacote, as chamadas **ParseHeader** e **GetNextSample** são bem sucedidos, mas **GetNextSample** não recupera quaisquer amostras e **NULL** é recebido no parâmetro *pSample* .

Se o divisor estiver configurado para analisar na direção inversa, o divisor sempre iniciará a análise no final do buffer de mídia que é passado para **ParseData**. Portanto, para a análise reversa na chamada para **ParseData**, passe o deslocamento no parâmetro *cbLength* , que especifica o comprimento dos dados e defina *cbBufferOffset* como zero.

## <a name="generating-samples-for-asf-data-packets"></a>Gerando amostras para pacotes de dados ASF

Um aplicativo inicia o processo de análise passando os pacotes de dados para o divisor. A entrada para o separador é uma série de buffers de mídia que contêm todo ou fragmentos do objeto de dados. A saída do divisor é uma série de amostras de mídia que contêm os dados do pacote.

Para passar dados de entrada para o separador, crie um buffer de mídia e preencha-o com dados da seção objeto de dados do arquivo ASF. (Para obter mais informações sobre buffers de mídia, consulte [buffers de mídia](media-buffers.md).) Em seguida, passe o buffer de mídia para o método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . Você também pode especificar:

-   O deslocamento no buffer em que o divisor deve iniciar a análise. Se o deslocamento for zero, a análise começará no início do buffer. Para obter informações sobre como definir o deslocamento de dados, consulte a seção "Localizando o deslocamento de dados" neste tópico.
-   A quantidade de dados a ser analisada. Se esse valor for zero, o separador analisa até atingir o final do buffer, conforme especificado pelo método [**IMFMediaBuffer:: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) .

O divisor gera amostras de mídia referenciando os dados nos buffers de mídia. O cliente pode recuperar os exemplos de saída chamando [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) em um loop até que não haja mais dados a serem analisados. Se **GetNextSample** retornar o \_ sinalizador ASF STATUSFLAGS \_ incompleto no parâmetro *pdwStatusFlags* , significa que há mais exemplos a serem recuperados e o aplicativo pode chamar **GetNextSample** novamente. Caso contrário, chame **ParseData** para passar mais dados para o divisor. Para os exemplos gerados, o divisor define as seguintes informações:

-   O divisor define um carimbo de data/hora em todos os exemplos que ele gera. O tempo de amostra representa a hora da apresentação e não inclui o tempo de preversão. O aplicativo pode chamar [**IMFSample:: Getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) para obter o tempo de apresentação, em unidades de 100 a nanossegundos.
-   Se ocorrer uma interrupção durante a geração de amostra, o divisor definirá o atributo de [**\_ descontinuidade MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) no primeiro exemplo após a descontinuidade. Descontinuidades geralmente são causados por pacotes descartados em uma conexão de rede, dados de arquivo corrompidos ou o divisor alternando de um fluxo de origem para outro.
-   Para vídeo, o divisor verifica se o exemplo contém um quadro-chave. Se tiver, o divisor definirá o atributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) no exemplo.

Se o divisor estiver analisando pacotes de dados que são recebidos de um servidor de mídia, é possível que o tamanho do pacote seja variável. Nesse caso, o cliente deve chamar **ParseData** para cada pacote e definir o atributo [**de \_ \_ limite de pacote MFASFSPLITTER**](mfasfsplitter-packet-boundary-attribute.md) em cada buffer que é enviado ao divisor. Esse atributo indica ao divisor se o buffer de mídia contém o início de um pacote ASF. Defina o atributo como **true** se o buffer contiver o início de um novo pacote. Se o buffer contiver uma continuação do pacote anterior, defina o atributo como **false**. Os buffers não podem abranger vários pacotes.

Antes de passar novos buffers de mídia para o divisor, o aplicativo deve chamar [**IMFASFSplitter:: flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush). Esse método redefine o divisor e limpa qualquer quadro parcial que esteja aguardando para ser concluído. Isso é útil em um cenário de busca em que o deslocamento está em um local diferente.

### <a name="example"></a>Exemplo

O exemplo de código a seguir mostra como analisar pacotes de dados. Este exemplo analisa desde o início do objeto de dados até o final do fluxo e exibe informações sobre os exemplos que contêm quadros-chave. Para obter um exemplo completo que usa esse código, consulte [tutorial: lendo um arquivo ASF](tutorial--reading-an-asf-file.md).


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Divisor de ASF](asf-splitter.md)
</dt> </dl>

 

 



