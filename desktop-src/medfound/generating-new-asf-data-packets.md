---
description: Gerando novos pacotes de dados ASF
ms.assetid: 7afa9694-c965-40e2-8549-e32ff48def2a
title: Gerando novos pacotes de dados ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f3432ecf34c58247a1533adb202b75f59d770c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457212"
---
# <a name="generating-new-asf-data-packets"></a>Gerando novos pacotes de dados ASF

O *multiplexador* de ASF é um componente de camada WMContainer que funciona com o [objeto de dados ASF](asf-file-structure.md) e dá a um aplicativo a capacidade de gerar pacotes de dados ASF para um fluxo que corresponde aos requisitos definidos no objeto ContentInfo.

O multiplexador tem uma entrada e uma saída. Ele recebe um exemplo de fluxo que contém dados de mídia digital e produz um ou mais pacotes de dados que podem ser gravados em um contêiner ASF.

A lista a seguir resume o processo de geração de pacotes de dados ASF:

1.  Passe os dados de entrada para o multiplexador em [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).
2.  Colete os pacotes de dados chamando [**IMFASFMultiplexer:: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) em um loop até que todos os pacotes completos tenham sido recuperados.
3.  Depois que os dados de entrada são convertidos em pacotes completos, pode haver alguns dados pendentes no Multiplexador, que não foi recuperado pelo [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket). Chame [**IMFASFMultiplexer:: flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) para reunir os exemplos pendentes e coletá-los do Multiplexador chamando **GetNextPacket** novamente.
4.  Atualize os objetos de cabeçalho ASF associados chamando [**IMFASFMultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) para refletir as alterações feitas pelo multiplexador durante a geração de pacotes de dados.

O diagrama a seguir ilustra a geração de pacotes de dados para um arquivo ASF por meio do Multiplexador.

![diagrama mostrando a geração de pacotes de dados para um arquivo ASF](images/packet.gif)

## <a name="asf-data-packet-creation"></a>Criação de pacote de dados ASF

Depois de criar e inicializar o multiplexador conforme descrito em [criando o objeto multiplexador](creating-the-multiplexer-object.md), chame [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) para passar dados de entrada para o multiplexador para processamento em pacotes de dados. A entrada especificada deve estar em um exemplo de mídia (interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ) que pode ter um ou mais buffers de mídia (interface [**IMFMediaBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) ) que contém os dados de um fluxo. No caso de transcodificação de ASF para ASF, o exemplo de mídia de entrada pode ser gerado a partir do divisor que cria amostras de fluxo em pacotes. Para obter mais informações, consulte [divisor de ASF](asf-splitter.md).

Antes de chamar [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), certifique-se de que o carimbo de data/hora do exemplo de mídia de entrada seja um horário de apresentação válido; caso contrário, **ProcessSample** falhará e retornará o \_ código de carimbo de \_ \_ data/hora MF e no Sample \_ .

O multiplexador pode aceitar entrada como amostras de mídia compactadas ou descompactadas por meio do [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample). O multiplexador atribui horas de envio a esses exemplos, dependendo do uso de largura de banda do fluxo. Durante esse processo, o multiplexador verifica os parâmetros de Bucket vazado (taxa de bits e utilização da janela de buffer) e pode rejeitar amostras que não aderem a esses valores. O exemplo de mídia de entrada pode falhar a verificação de largura de banda por qualquer um dos seguintes motivos:

-   Se o exemplo de mídia de entrada chegou atrasado porque a hora de envio da última atribuição é maior do que o carimbo de data/hora neste exemplo de mídia. [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) falhará e retornará o código de erro de **\_ \_ \_ exemplo MF e tardia** .
-   Se o carimbo de data/hora no exemplo de mídia de entrada for anterior à hora de envio atribuída (isso indica estouro de buffer). O multiplexador pode ignorar essa situação se ela estiver configurada para ajustar a taxa de bits definindo o sinalizador do **MFASF \_ multiplexador \_ AutoAjuste de \_ taxa** de bit durante a inicialização do Multiplexador. Para obter mais informações, consulte "inicialização do Multiplexador e configurações de Bucket de vazamentos" em [criando o objeto multiplexador](creating-the-multiplexer-object.md). Se esse sinalizador não estiver definido e o multiplexador encontrar saturação de largura de banda, [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) falhará e retornará o código de erro de **saturação da largura de \_ \_ banda \_ e MF** .

Depois que o multiplexador atribui a hora de envio, o exemplo de mídia de entrada é adicionado à *janela de envio*— uma lista de amostras de mídia de entrada ordenada por horas de envio e pronta para ser processada em pacotes de dados. Durante a construção do pacote de dados, o exemplo de mídia de entrada é analisado e os dados relevantes são gravados em um pacote de dados como carga. Um pacote de dados completo pode conter dados de um ou mais exemplos de mídia de entrada.

Quando novas amostras de mídia de entrada chegam na janela enviar, elas são adicionadas a uma fila até que haja amostras de mídia suficientes para formar um pacote completo. Os dados nos buffers de mídia contidos no exemplo de mídia de entrada não são copiados para o pacote de dados gerado. O pacote de dados armazena referências aos buffers de mídia de entrada até que o exemplo de mídia de entrada tenha sido totalmente em pacote e o pacote completo tenha sido coletado do Multiplexador.

Quando um pacote de dados completo está disponível, ele pode ser recuperado chamando [**IMFASFMultiplexer:: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket). Se você chamar [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) enquanto houver pacotes completos prontos para recuperação, ele falhará e retornará o código de erro **MF \_ e não \_ aceitar** . Isso indica que o multiplexador não pode aceitar mais entrada e você deve chamar **GetNextPacket** para recuperar os pacotes em espera. Idealmente, cada chamada **ProcessSample** deve ser seguida por uma ou mais chamadas **GetNextPacket** para obter os pacotes de dados completos. Pode levar mais de um exemplo de mídia de entrada para criar um pacote de dados completo. Por outro lado, os dados em um exemplo de mídia de entrada podem abranger vários pacotes. Portanto, nem todas as chamadas para **ProcessSample** produzirão exemplos de mídia de saída.

Se o exemplo de mídia de entrada contiver um quadro-chave indicado pelo atributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) , o multiplexador copiará o atributo para o pacote.

## <a name="getting-asf-data-packets"></a>Obtendo pacotes de dados ASF

Para coletar exemplos de mídia de saída para um pacote de dados completo gerado pelo Multiplexador, chame [**IMFASFMultiplexer:: GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) em um loop até que não haja mais exemplos de mídia de saída restantes para o pacote. O seguinte lista os casos de êxito:

-   Se houver um pacote de dados completo disponível, o [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) receberá o sinalizador **\_ \_ \_ incompleto de sinalizadores de status do ASF** no parâmetro *pdwStatusFlags* ; o parâmetro *ppIPacket* receberá um ponteiro para o primeiro pacote de dados. Você deve chamar esse método desde que ele receba esse sinalizador. Com cada iteração, *ppIPacket* aponta para o próximo pacote na fila.
-   Se houver apenas um pacote de dados, *ppIPacket* apontará para ele e o sinalizador **status do ASF \_ \_ sinalizadores \_ incompletos** não será recebido em *pdwStatusFlags*.
-   O [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) pode ser bem sucedido sem gerar nenhum pacote de dados se o multiplexador ainda estiver no processo de pacotes e adição de pacotes de dados. Nesse caso, *ppIPacket* aponta para **NULL**. Para continuar, você deve fornecer o multiplexador com mais amostras de mídia de entrada chamando [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).

O código de exemplo a seguir mostra uma função que gera pacotes de dados usando o multiplexador. O conteúdo do pacote de dados gerado será gravado no fluxo de bytes de dados alocado pelo chamador.


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



A `WriteBufferToByteStream` função é mostrada no tópico [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).

Para ver um aplicativo completo que usa este exemplo de código, consulte [tutorial: copiando fluxos ASF de um arquivo para outro](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="post-packet-generation-calls"></a>Postar chamadas de Packet-Generation

Para certificar-se de que não há nenhum pacote de dados completo aguardando no Multiplexador, chame [**IMFASFMultiplexer:: flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush). Isso força o multiplexador a fazer o pacote de todos os exemplos de mídia em andamento. O aplicativo pode coletar esses pacotes na forma de amostras de mídia por meio de **GetNextPacket** em um loop até que não haja mais nenhum pacote restante a ser recuperado.

Depois que todas as amostras de mídia forem geradas, chame [**IMFASFMultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) para atualizar o objeto de cabeçalho ASF que está associado a esses pacotes de dados. O objeto de cabeçalho é especificado passando o objeto ContentInfo que foi usado para inicializar o multiplexador. Essa chamada atualiza vários objetos de cabeçalho para refletir as alterações feitas pelo multiplexador durante a geração de pacotes de dados. Essas informações incluem contagem de pacotes, duração de envio, duração da reprodução e números de fluxo de todos os fluxos. O tamanho geral do cabeçalho também é atualizado.

Você deve garantir que [**end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) seja chamado depois que todos os pacotes de dados forem recuperados. Se houver algum pacote aguardando no Multiplexador, o **fim** falhará e retornará o código de erro **MF \_ E \_ flush \_ necessário** . Nesse caso, obtenha o pacote em espera chamando [**flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) e [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) em um loop.

> [!Note]  
> Para a codificação de VBR, depois de chamar **end**, você deve definir as estatísticas de codificação nas propriedades de codificação do objeto ContentInfo. Para obter informações sobre esse processo, consulte "Configurando o objeto ContentInfo com as configurações do codificador" em [definindo propriedades no objeto ContentInfo](setting-properties-in-the-contentinfo-object.md). A lista a seguir mostra as propriedades específicas a serem definidas:
>
> -   [**MFPKEY \_ RAVG**](mfpkey-ravgproperty.md) é a taxa de bits média do conteúdo da VBR.
> -   [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md) é a janela de buffer para a taxa média de bits.
> -   [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md) é a taxa de bits de pico do conteúdo da VBR.
> -   [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) é a janela de buffer de pico.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Multiplexador ASF](asf-multiplexer.md)
</dt> <dt>

[Tutorial: copiando fluxos ASF de um arquivo para outro](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Tutorial: gravando um arquivo WMA usando a codificação de CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



