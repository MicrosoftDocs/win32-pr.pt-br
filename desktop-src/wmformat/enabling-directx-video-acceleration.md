---
title: Habilitando a aceleração de vídeo do DirectX
description: Habilitando a aceleração de vídeo do DirectX
ms.assetid: 5cb2f564-88e3-4b60-bde3-6ccf69c97c48
keywords:
- SDK do Windows Media Format, habilitando o DXVA
- SDK do Windows Media Format, DXVA (aceleração de vídeo do DirectX)
- SDK do Windows Media Format, aceleração de vídeo
- ASF (Advanced Systems Format), habilitando o DXVA
- ASF (formato de sistemas avançados), habilitando o DXVA
- ASF (Advanced Systems Format), DXVA (aceleração de vídeo do DirectX)
- ASF (formato de sistemas avançados), DXVA (aceleração de vídeo do DirectX)
- ASF (Advanced Systems Format), aceleração de vídeo
- ASF (formato de sistemas avançados), aceleração de vídeo
- DXVA (aceleração de vídeo do DirectX), habilitando
- DXVA (aceleração de vídeo DirectX), habilitando
- DXVA (aceleração de vídeo do DirectX), ordem de operações
- DXVA (aceleração de vídeo DirectX), ordem de operações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896147fe11b4b7f5fb91d8dc288e616b643bd5ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365539"
---
# <a name="enabling-directx-video-acceleration"></a>Habilitando a aceleração de vídeo do DirectX

Esta seção descreve como habilitar a aceleração de vídeo do Microsoft® DirectX® ao reproduzir conteúdo em fluxo em um player personalizado.

## <a name="background"></a>Tela de fundo

DirectX Video Acceleration (DirectX VA) é uma especificação de API para aceleração de hardware de operações de decodificação 2D. Ele permite que os decodificadores de software descarreguem determinadas operações com uso intensivo de CPU para a placa gráfica para processamento. Para os usuários finais, isso torna possível vídeo de alta taxa de bits, como reprodução de DVD de tela inteira em computadores mais antigos equipados com placas gráficas compatíveis com DirectX VA.

A partir do SDK do Windows Media Format 9 Series, o filtro de invólucro do DMO dá suporte ao DirectX VA. Isso significa que, para reprodução local, os aplicativos podem usar o filtro de leitor ASF do WM para reproduzir conteúdo baseado no Windows Media e a aceleração de hardware DirectX VA será invocada automaticamente se a placa gráfica oferecer suporte a ela. No entanto, o filtro de leitor ASF do WM não oferece suporte à reprodução de conteúdo transmitido. Portanto, se você quiser dar suporte ao DirectX VA ao reproduzir conteúdo transmitido em um player personalizado, deverá usar um mecanismo alternativo, que é aquele usado pelo Windows Media Player, começando com o Windows Media 9 Series.

Como o Windows Media Player foi projetado antes de os filtros QASF terem sido desenvolvidos, o Windows Media Player tem seu próprio filtro de origem, com base no Windows Media Format SDK, para reproduzir conteúdo baseado no Windows Media. O filtro de origem do Windows Media do WMP entrega dados descompactados downstream diretamente para os renderizadores de áudio e vídeo. Por outro lado, o leitor de ASF do WM fornece conteúdo compactado downstream para os DMOs (objetos de mídia do DirectX) do Windows Media Decoder, que são hospedados dentro do invólucro do DMO. Os diagramas a seguir ilustram as diferenças entre o leitor ASF do WM e o filtro de origem do Windows Media do WMP.

![exemplos de saídas não compactadas de filtro de origem personalizado](images/wmp-dxva-graph.png)

![o filtro de origem qasf gera amostras compactadas](images/qasf-dxva-graph.png)

Para habilitar o DirectX VA para conteúdo transmitido, você deve criar um filtro de origem personalizado como aquele no diagrama superior. Basicamente, esse filtro usará o Windows Media Format SDK para criar uma instância de um objeto do WM Reader, descompactar os exemplos e enviá-los downstream em seus PINs de saída. Esta discussão pressupõe que você já criou o filtro de origem e agora está pronto para implementar o suporte do DirectX VA.

Para habilitar o DirectX VA, a tarefa básica do filtro de origem é fornecer o processador de vídeo e o decodificador de WMV DMO com as interfaces de que eles precisarão para negociar a conexão do DirectX VA. O filtro de origem não participa dessas negociações. Após o streaming começar, a única tarefa relacionada ao DirectX VA que o filtro de origem pode executar é modificar os carimbos de data/hora nos exemplos de vídeo antes que o decodificador WMV os entregue ao processador de vídeo. O principal motivo para fazer isso é fornecer controle de linha do tempo personalizado além do que as interfaces padrão do DirectShow® habilitam.

Três interfaces são definidas para habilitar as comunicações necessárias entre o Windows Media Format SDK, o filtro de origem do Player, o Windows Media Video Decoder DMO e o mixer de sobreposição ou o processador de mixagem de vídeo. Essas interfaces são descritas na tabela a seguir.



| Interface                                                        | Descrição                                                                                                                                                                                        |
|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecAMVideoAccelerator**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmcodecamvideoaccelerator) | Exposto pelo decodificador do Windows Media DMO e chamado pelo filtro de origem do player de mídia para configurar as várias conexões necessárias para habilitar o DirectX VA para a decodificação do conteúdo de vídeo do Windows Media. |
| [**IWMPlayerTimestampHook**](/previous-versions/windows/desktop/api/wmdxva/nn-wmdxva-iwmplayertimestamphook)         | Implementado no filtro de origem do Player. Ele permite que o filtro modifique os carimbos de data/hora nos exemplos de vídeo antes de entregá-los.                                                 |
| [**IWMReaderAccelerator**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderaccelerator)             | Implementado no objeto leitor do WM. Ele é chamado por um filtro de origem do Player para obter interfaces do decodificador DMO.                                                                             |



 

## <a name="order-of-operations-in-directx-vaenabled-playback"></a>Ordem de operações no DirectX VA – reprodução habilitada

Esta seção descreve a ordem geral de operações em tempo de execução para um player habilitado para DirectX VA e seu filtro de origem. Os componentes mencionados nesta seção são:

-   Um player de mídia de terceiros, chamado de jogador.
-   Um filtro de origem personalizado, instanciado pelo Player, que usa o Windows Media Format SDK para descompactar o conteúdo baseado no Windows Media.
-   O pino de saída do vídeo do filtro de origem do Player, conhecido como o pino de saída.
-   O grafo de filtro de reprodução de vídeo do DirectShow, conhecido como grafo.
-   O processador de mixagem de vídeo, chamado de VMR.
-   O objeto leitor assíncrono do Windows Media Format SDK, conhecido como leitor.
-   O objeto de mídia DirectX do Windows Media decodificador de vídeo, conhecido como o decodificador DMO.

A ordem das operações é a seguinte:

1.  O Player instancia seu filtro de origem e um objeto leitor. O leitor cria um decodificador de vídeo DMO e define o tipo de entrada (compactado) nele. Isso deve ocorrer antes que o Player tente configurar seu grafo de reprodução de vídeo porque o SDK e o decodificador DMO devem estar envolvidos no processo de negociação com o grafo, e o DMO deve saber o formato de entrada durante a etapa 9.
2.  O Player chama **IGraphBuilder:: render**, fornecendo a ele o pino de saída do filtro de fonte de vídeo. Neste ponto, o Gerenciador de gráficos de filtro do DirectShow tenta conectar o VMR ao filtro de origem de vídeo do jogador.
3.  O Gerenciador do grafo de filtro chama **IPin:: Connect** no pino de saída do filtro de origem de vídeo do jogador.

As etapas 4 a 10 ocorrem dentro de **IPin:: Connect**.

1.  O filtro de origem Obtém a interface **IWMCodecAMVideoAccelerator** do método **IWMReaderAccelerator:: GetCodecInterface** do leitor. Se o codec não der suporte ao DirectX VA, a chamada para **GetCodecInterface** poderá falhar. Nesse caso, a negociação prossegue como de costume, sem o suporte do DirectX VA.
2.  O filtro de origem passa o ponteiro **IAMVideoAccelerator** do PIN passado para **conectar-se** ao decodificador DMO por meio de **IWMCodecAMVideoAccelerator:: SetAcceleratorInterface**.
3.  Em seguida, o filtro de origem delega o restante da operação **IPin:: Connect** para o método **CBaseOutputPin:: Connect** . A enumeração de formato com o SDK continua como faz hoje. Se o codec der suporte ao DirectX VA para o conteúdo que está sendo conectado, o codec DMO apresentará esses subtipos do DirectX VA primeiro, antes dos tipos YUV e RGB com suporte. Se o suporte do DirectX VA estiver disponível, serão tentadas as etapas 7 a 11 no contexto de um subtipo DirectX VA. O trecho de código a seguir mostra como identificar um subtipo de mídia DirectX VA.
    ```C++
    bool IsDXVASubtype( AM_MEDIA_TYPE * pmt )
    {
        // All DXVA types have the same last 3 DWORDs.
        // guidDXVA is the base GUID for all DXVA subtypes.

        GUID guidDXVA = { 0x00000000, 0xa0c7, 0x11d3, { 0xb9,0x84,0x00,0xc0,0x4f,0x2e,0x73,0xc5 } };

        unsigned long const * plguid;
        unsigned long const * plguidDXVA;
        plguid = (unsigned long const *)&pmt->subtype;
        plguidDXVA = (unsigned long *)&guidDXVA;

        if( ( plguid[1] == plguidDXVA[1] ) &&
            ( plguid[2] == plguidDXVA[2] ) &&
            ( plguid[3] == plguidDXVA[3] ) )
        {
            return true;
        }

        return false;
    }
    
    ```

    

4.  A implementação **CBaseOutputPin:: Connect** chama **IPin:: CompleteConnect** durante a etapa 3. Se um subtipo DirectX VA estiver sendo considerado, a negociação do DirectX VA será tentada. O pino de saída chama **IWMCodecAMVideoAccelerator:: NegotiateConnection**, passando-o para o tipo de mídia de saída atual.
5.  O decodificador DMO executa a negociação necessária com o VMR por meio da interface **IAMVideoAccelerator** e retorna o GUID de subtipo de vídeo que os dois concordaram. O pino de saída delega todas as chamadas de **IAMVideoAcceleratorNotify** recebidas durante esse processo para a interface **IAMVideoAcceleratorNotify** do decodificador de DMO, que também pode ser obtida por meio do método **IWMReaderAccelerator:: GetCodecInterface** .
6.  Se **NegotiateConnection** tiver sucesso, o pino de saída chamará **IWMCodecAMVideoAccelerator:: SetPlayerNotify** com uma interface **IWMPlayerTimestampHook** . Esse gancho permite que o filtro de origem atualize os carimbos de data/hora nos exemplos antes que eles sejam entregues ao renderizador.
7.  O filtro de origem chama **IWMReaderAccelerator:: Notify** com o tipo de mídia negociado. Isso permite que o leitor atualize suas variáveis internas e confirme o DirectX VA. Esse é o último lugar em que o codec ou leitor pode falhar. Se qualquer uma das etapas acima falhar, o filtro de origem deverá retornar à etapa 3 e tentar o próximo tipo enumerado pelo leitor.
8.  A reprodução é iniciada. O leitor ignora os buffers de saída do decodificador DMO se o tipo de saída de conexão for DirectX VA.
9.  Quando **IPin::D isconnect** ocorre, o filtro de origem chama **IWMCodecAMVideoAccelerator:: SetAcceleratorInterface** com um **NULL**. Isso interrompe a conexão do DirectX VA entre o codec e o processador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Lendo arquivos ASF**](reading-asf-files.md)
</dt> </dl>

 

 




