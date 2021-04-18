---
title: Configurando perfis e outras propriedades de arquivo (QASF)
description: Configurando perfis e outras propriedades de arquivo (QASF)
ms.assetid: a462fc8b-5a2e-4c93-828d-177d1965b734
keywords:
- SDK do Windows Media Format, Configurando perfis (QASF)
- SDK do Windows Media Format, Configurando propriedades do arquivo (QASF)
- SDK do Windows Media Format, metadados (QASF)
- ASF (Advanced Systems Format), Configurando perfis (QASF)
- ASF (formato de sistemas avançados), Configurando perfis (QASF)
- ASF (Advanced Systems Format), Configurando propriedades de arquivo (QASF)
- ASF (formato de sistemas avançados), Configurando propriedades de arquivo (QASF)
- Formato de sistema avançado (ASF), metadados (QASF)
- ASF (formato de sistemas avançados), metadados (QASF)
- SDK do Windows Media Format, QASF
- ASF (Advanced Systems Format), QASF
- ASF (formato de sistemas avançados), QASF
- metadados, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ebb6afedfa00813e7447e5bcaefe1f251c02575
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454220"
---
# <a name="configuring-profiles-and-other-file-properties-qasf"></a>Configurando perfis e outras propriedades de arquivo (QASF)

Os itens a seguir descrevem como executar várias tarefas relacionadas à criação de arquivos ASF.

## <a name="creating-a-profile-qasf"></a>Criando um perfil (QASF)

Para criar um perfil personalizado, use o SDK do Windows Media Format diretamente para criar um objeto do Gerenciador de perfis usando a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) . Em seguida, crie o perfil e passe-o para o [gravador ASF do WM](wm-asf-writer-filter.md) usando o método [**IConfigASFWriter:: ConfigureFilterUsingProfile**](iconfigasfwriter-configurefilterusingprofile.md) . Essa é a única maneira de configurar o filtro com um perfil que usa os codecs de áudio do Windows Media e vídeo 9 Series. Os perfis de sistema para versões anteriores desses codecs podem ser adicionados usando o método [**IConfigASFWriter:: ConfigureFilterUsingProfileGuid**](iconfigasfwriter-configurefilterusingprofileguid.md) .

## <a name="adding-metadata-qasf"></a>Adicionando metadados (QASF)

Para adicionar metadados a um arquivo, chame **QueryInterface** da interface **IBASEFILTER** no [gravador ASF do WM](wm-asf-writer-filter.md) para recuperar a interface [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) . Depois que o filtro receber um perfil, use os métodos de interface **IWMHeaderInfo** para gravar os metadados.

## <a name="indexing-a-file-qasf"></a>Indexando um arquivo (QASF)

O gravador ASF do WM cria arquivos indexados de temporal por padrão. Para criar um arquivo indexado por quadro, use o método [**IConfigAsfWriter:: Setindexmode**](iconfigasfwriter-setindexmode.md) para desabilitar toda a indexação e, em seguida, crie o arquivo. Quando estiver concluído, use o SDK do Windows Media Format diretamente para criar um índice baseado em quadro para o arquivo.

## <a name="performing-two-pass-encoding-qasf"></a>Executando codificação de Two-Pass (QASF)

Há suporte para codificação de duas passagens apenas em codecs de mídia do Windows da versão 8 e posterior. Coloque o gravador ASF do WM no modo de pré-processamento chamando [**IConfigAsfWriter2:: SetParam**](iconfigasfwriter2-setparam.md) e especificando am \_ CONFIGASFWRITER \_ param \_ MultiPASS no parâmetro *dwParam* e **true** no parâmetro *dwParam1* .

Em seguida, execute o gráfico de filtro. Quando todas as passagens de pré-processamento são concluídas (normalmente, apenas uma passagem de pré-processamento será executada), o aplicativo receberá um evento **de \_ pré- \_ processamento de EC** no filtro. Quando esse evento for recebido, use **IMediaSeeking:: Setpositiones** para redefinir o ponteiro de fluxo de volta ao início e execute o gráfico de filtro novamente. Após a última passagem (normalmente a segunda passagem), o aplicativo receberá um evento de **\_ conclusão do EC** para significar que o processo de codificação foi concluído. Se uma passagem de pré-processamento for cancelada antes de o evento de **\_ \_ conclusão de pré-processamento do EC** ser recebido, chame [**IConfigAsfWriter2:: ResetMultiPassState**](iconfigasfwriter2-resetmultipassstate.md) para redefinir o filtro antes de tentar executar outra execução de pré-processamento.

Só é necessário chamar **IConfigAsfWriter:: SetParam**(am \_ CONFIGASFWRITER param All \_ \_ Pass, **false**) se você quiser colocar o filtro fora do modo de pré-processamento completamente.

> [!IMPORTANT]
> É responsabilidade do aplicativo habilitar o modo de pré-processamento com base no perfil que será usado para codificação. Alguns perfis exigem codificação de duas passagens; Se você tentar codificar um arquivo com um perfil como esse, e não definir \_ CONFIGASFWRITER \_ param \_ multipasse para **true**, \_ ocorrerá um erro do EC userabort. Para obter mais informações sobre como determinar se um determinado perfil requer codificação de duas passagens, consulte [usando Two-Pass codificação](using-two-pass-encoding.md) ou [gravando fluxos de taxa de bits variáveis](writing-variable-bit-rate-streams.md).

 

## <a name="getting-and-setting-buffer-properties-at-run-time-qasf"></a>Obter e definir propriedades de buffer em tempo de execução (QASF)

Em alguns cenários, por exemplo, se você quiser forçar a inserção de quadro-chave ao gravar um arquivo, um aplicativo pode precisar obter ou definir informações sobre um buffer de mídia do Windows em tempo de execução. O [leitor ASF do WM](wm-asf-reader-filter.md) e o [gravador ASF do WM](wm-asf-writer-filter.md) dão suporte a um mecanismo de retorno de chamada que permite que um aplicativo acesse a interface [**INSSBuffer3**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3) em cada buffer de mídia individual durante a leitura do arquivo ou a gravação de arquivos. Os aplicativos podem usar essa interface para designar amostras específicas como quadros-chave, ou [*cleanpoints*](wmformat-glossary.md), para definir códigos de tempo SMPTE, especificar configurações de entrelaçamento ou adicionar qualquer tipo de dados privados a um fluxo.

Use a interface [**IAMWMBufferPass**](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass) para se registrar para retornos de chamada do PIN que está manipulando o fluxo de vídeo. Quando o PIN chama o método [**IAMWMBufferPassCallback:: Notify**](iamwmbufferpasscallback-notify.md) , examine os carimbos de data/hora no buffer e, se apropriado, chame [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) para definir a propriedade **OutputCleanPoint do WM \_ SampleExtensionGUID \_** no buffer como **true**.

## <a name="non-square-pixel-support-qasf"></a>Suporte a pixel não quadrado (QASF)

O gravador ASF do WM se conecta a um filtro upstream, como o codificador DV, que gera informações de taxa de proporção de pixel. O gravador ASF do WM gravará essas informações como extensões de unidade de dados para cada exemplo no arquivo.

Quando o leitor ASF do WM encontrar informações de taxa de proporção de pixel no cabeçalho do arquivo ou em extensões de unidade de dados para os exemplos, ele oferecerá um tipo de mídia **VIDEOINFOHEADER2** como uma primeira opção em seu pino de saída. Os membros **dwPictAspectRatioX** e **dwPictAspectRatioY** da estrutura, que descrevem a taxa de proporção do retângulo de vídeo, serão ajustados corretamente para considerar a taxa de proporção de pixel.

## <a name="maintaining-interlaced-format"></a>Mantendo o formato entrelaçado

Se você capturar vídeo entrelaçado de uma televisão ou de uma câmera de vídeo digital, talvez queira preservar o vídeo original como campos independentes se esperar que o arquivo codificado seja reproduzido em uma televisão ou em outro dispositivo de vídeo entrelaçado. (Monitores de computador são dispositivos de verificação progressiva.) Se você desentrelaçar um vídeo e, em seguida, reentrelaçar-o para reprodução em uma televisão, uma perda de dados será incorrida. Em um arquivo ASF, as informações de entrelaçamento são armazenadas como extensões de unidade de dados que o aplicativo aplica a cada exemplo usando o método **IAMWMBufferPassCallback** descrito anteriormente. Para codificar um arquivo que preserva as configurações de entrelaçamento originais, siga estas etapas:

-   Implemente uma classe que dê suporte a **IAMWMBufferPassCallback** e grave uma função Notify que defina os sinalizadores entrelaçados para cada amostra. Essa função será chamada pelo gravador ASF do WM antes de processar cada exemplo.


```C++
// Set to WM_CT_TOP_FIELD_FIRST if that is your format.
BYTE flag = WM_CT_INTERLACED | WM_CT_BOTTOM_FIELD_FIRST;
            HRESULT hr = pNSSBuffer3->SetProperty(WM_SampleExtensionGUID_ContentType, (void*) &flag, WM_SampleExtension_ContentType_Size);
           
```



-   Defina as extensões de unidade de dados no perfil antes de passar o perfil para o filtro.


```C++
hr = pWMStreamConfig2->AddDataUnitExtension( WM_SampleExtensionGUID_ContentType, WM_SampleExtension_ContentType_Size, NULL, 0 );
```



-   Depois de configurar o filtro com o perfil, obtenha a interface **IWMWriterAdvanced2** do gravador ASF do WM e chame o método **SetInputSettings** .

`// Must do this first.`

`hr = pConfigAsfWriter2->ConfigureFilterUsingProfile(pProfile);`


```C++
  
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



 

 