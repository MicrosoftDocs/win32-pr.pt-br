---
description: Configurar perfis e outras propriedades de arquivo ASF
ms.assetid: c43df556-9d8a-4010-9ed6-f84d8ac6d9bc
title: Configurar perfis e outras propriedades de arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e26dcbb49cb5ff8309dccafc3f1d8d66397871
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370255"
---
# <a name="configuring-profiles-and-other-asf-file-properties"></a>Configurar perfis e outras propriedades de arquivo ASF

Os itens a seguir descrevem como executar várias tarefas relacionadas à criação de arquivos ASF. Algumas das interfaces mencionadas neste tópico estão documentadas na documentação do SDK do Windows Media Format.

Criando um perfil

Os perfis ASF são discutidos em detalhes no SDK do Windows Media Format; essencialmente, eles descrevem atributos de um arquivo de formato de mídia do Windows, como taxa de bits, número e tipo de fluxos e qualidade de compactação. O filtro usa o perfil para determinar que tipo de arquivo de formato de mídia do Windows gravar, quantos Pins de entrada devem ser configurados e quais tipos de mídia eles podem aceitar.

Para criar um perfil personalizado, use o SDK do Windows Media Format diretamente para criar um objeto do Gerenciador de perfis usando a função **WMCreateProfileManager** . Em seguida, crie o perfil e passe-o para o [gravador ASF do WM](wm-asf-writer-filter.md) usando o método [**IConfigASFWriter:: ConfigureFilterUsingProfile**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofile) . Essa é a única maneira de configurar o filtro com um perfil que usa os codecs de áudio do Windows Media e vídeo 9 Series. Os perfis de sistema para versões anteriores desses codecs podem ser adicionados usando o método [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-configurefilterusingprofileguid) .

Você pode redefinir o perfil enquanto os Pins de entrada do filtro estiverem conectados, desde que o novo perfil não exija nenhum pino de entrada adicional. Por exemplo, se você alterar o perfil de um perfil somente de áudio de uma entrada para um perfil de áudio e vídeo de duas entradas, apenas o PIN de áudio será reconectado e nenhum novo PIN será criado para o fluxo de vídeo.

Adicionando metadados

Para adicionar metadados a um arquivo, consulte o filtro do [gravador ASF do WM](wm-asf-writer-filter.md) para a interface **IWMHeaderInfo** . Depois que o filtro receber um perfil, use os métodos de interface **IWMHeaderInfo** para gravar os metadados.

Indexando um arquivo

O gravador ASF do WM cria arquivos indexados de temporal por padrão. Para criar um arquivo indexado por quadro, use o método [**IConfigAsfWriter:: Setindexmode**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter-setindexmode) para desabilitar toda a indexação e, em seguida, crie o arquivo. Quando estiver concluído, use o SDK do Windows Media Format diretamente para criar um índice baseado em quadro para o arquivo.

Codificação de Two-Pass

Há suporte para codificação de duas passagens apenas em codecs de mídia do Windows da versão 8 e posterior. Coloque o gravador ASF do WM no modo de pré-processamento chamando [**IConfigAsfWriter2:: SetParam**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-setparam) e especificando am \_ CONFIGASFWRITER \_ param \_ MultiPASS no parâmetro *dwParam* e **true** no parâmetro *dwParam1* .

Em seguida, execute o gráfico de filtro. Quando todas as passagens de pré-processamento são concluídas (normalmente, apenas uma passagem de pré-processamento será executada), o aplicativo receberá um evento [**de \_ pré- \_ processamento de EC**](ec-preprocess-complete.md) no filtro. Quando esse evento for recebido, use [**IMediaSeeking:: Setpositiones**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) para redefinir o ponteiro de fluxo de volta ao início e execute o gráfico de filtro novamente. Após a última passagem (normalmente a segunda passagem), o aplicativo receberá um evento de [**\_ conclusão do EC**](ec-complete.md) para significar que o processo de codificação foi concluído. Se uma passagem de pré-processamento for cancelada antes de o evento de **\_ \_ conclusão de pré-processamento do EC** ser recebido, chame [**IConfigAsfWriter2:: ResetMultiPassState**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iconfigasfwriter2-resetmultipassstate) para redefinir o filtro antes de tentar executar outra execução de pré-processamento.

Só é necessário definir o \_ \_ parâmetro CONFIGASFWRITER param \_ MultiPASS como **false** se você quiser colocar o filtro fora do modo de pré-processamento completamente.

> [!IMPORTANT]
> É responsabilidade do aplicativo habilitar o modo de pré-processamento com base no perfil que será usado para codificação. Alguns perfis exigem codificação de duas passagens; Se você tentar codificar um arquivo com um perfil como esse, e não definir \_ CONFIGASFWRITER \_ param \_ multipasse para **true**, ocorrerá um erro do [**EC \_ userabort**](ec-userabort.md) . Para obter mais informações, consulte a documentação do Windows Media Format SDK.

 

Obter e definir propriedades de buffer em tempo de execução

Em alguns cenários, por exemplo, se você quiser forçar a inserção de quadro-chave ao gravar um arquivo, um aplicativo pode precisar obter ou definir informações sobre um buffer de mídia do Windows em tempo de execução. O [leitor ASF do WM](wm-asf-reader-filter.md) e o [gravador ASF do WM](wm-asf-writer-filter.md) dão suporte a um mecanismo de retorno de chamada que permite que um aplicativo acesse a interface **INSSBuffer3** em cada buffer de mídia individual durante a leitura do arquivo ou a gravação de arquivos. Os aplicativos podem usar essa interface para designar exemplos específicos como quadros-chave, definir códigos de tempo SMPTE, especificar configurações de entrelaçamento ou adicionar qualquer tipo de dados privados a um fluxo.

Use a interface [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpass) para se registrar para retornos de chamada do PIN que está manipulando o fluxo de vídeo. O PIN chamará o método [**IAMWMBufferPassCallback:: Notify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpasscallback-notify) para cada buffer.

Pixels não quadrados

O gravador ASF do WM se conecta a um filtro upstream, como o codificador DV, que gera informações de taxa de proporção de pixel. O gravador ASF do WM gravará essas informações como extensões de unidade de dados para cada exemplo no arquivo.

Quando o leitor ASF do WM encontrar informações de taxa de proporção de pixel no cabeçalho do arquivo ou nas extensões de unidade de dados para os exemplos, ele oferecerá um formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) como uma primeira opção em seu pino de saída. Os membros **dwPictAspectRatioX** e **dwPictAspectRatioY** da estrutura, que descrevem a taxa de proporção do retângulo de vídeo, serão ajustados corretamente para considerar a taxa de proporção de pixel.

Mantendo o formato entrelaçado

Se você capturar vídeo entrelaçado de uma televisão ou de uma câmera de vídeo digital, talvez queira preservar o vídeo original como campos independentes se esperar que o arquivo codificado seja reproduzido em uma televisão ou em outro dispositivo de vídeo entrelaçado. (Monitores de computador são dispositivos de verificação progressiva.) Se você desentrelaçar um vídeo e, em seguida, reentrelaçar-o para reprodução em uma televisão, uma perda de dados será incorrida. Em um arquivo ASF, as informações de entrelaçamento são armazenadas como extensões de unidade de dados que o aplicativo aplica a cada exemplo usando o método [**IAMWMBufferPassCallback**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iamwmbufferpasscallback) descrito anteriormente. Para codificar um arquivo que preserva as configurações de entrelaçamento originais, siga estas etapas:

1.  Implemente uma classe que dê suporte a **IAMWMBufferPassCallback** e grave uma função Notify que defina os sinalizadores entrelaçados para cada amostra. Essa função será chamada pelo gravador ASF do WM antes de processar cada exemplo.
    ```C++
    // Set to WM_CT_TOP_FIELD_FIRST if that is your format.
    BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
    HRESULT hr = S_OK;

    hr = pNSSBuffer3->SetProperty(
        WM_SampleExtensionGUID_ContentType, 
        (void*) &flag, 
        WM_SampleExtension_ContentType_Size
        );         
    ```

    

2.  Defina as extensões de unidade de dados no perfil antes de passar o perfil para o filtro.
    ```C++
    hr = pWMStreamConfig2->AddDataUnitExtension(
        WM_SampleExtensionGUID_ContentType, 
        WM_SampleExtension_ContentType_Size, 
        NULL, 
        0 
        );
    ```

    

3.  Depois de configurar o filtro com o perfil, obtenha a interface **IWMWriterAdvanced2** do gravador ASF do WM e chame o método **SetInputSettings** .

    ``

    ``

    ```C++
    // Must do this first.
    hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);
      
    CComPtr<IServiceProvider> pProvider;
    CComPtr<IWMWriterAdvanced2> pWMWA2;

    hr = pConfigAsfWriter2->QueryInterface( __uuidof(IServiceProvider),
                                             (void**)&pProvider);
    if (SUCCEEDED(hr))
    {
        hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
            IID_IWMWriterAdvanced2,
            (void**)&pWMWA2);
    }

    BOOL pValue = TRUE;

    // Set the first parameter to your actual input number.
    hr = pWMWA2->SetInputSetting(0, g_wszInterlacedCoding,
        WMT_TYPE_BOOL, (BYTE*) &pValue, sizeof(WMT_TYPE_BOOL));
                
    ```

    

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 



