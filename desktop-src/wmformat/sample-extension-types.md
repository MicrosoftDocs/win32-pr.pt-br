---
title: Tipos de extensão de exemplo
description: Tipos de extensão de exemplo
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows SDK de Formato de Mídia, extensões de exemplo
- ASF (Advanced Systems Format), extensões de exemplo
- ASF (Formato de Sistemas Avançados), extensões de exemplo
- Windows SDK de Formato de Mídia, extensões de unidade de dados
- ASF (Advanced Systems Format), extensões de unidade de dados
- ASF (Formato de Sistemas Avançados), extensões de unidade de dados
- Windows SDK de Formato de Mídia, propriedades do buffer
- FORMATO DE SISTEMAS Avançados (ASF), propriedades do buffer
- ASF (Formato de Sistemas Avançados), propriedades do buffer
- extensões de exemplo, tipos
- extensões de unidade de dados, tipos
- propriedades do buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1404dfee60c3de179df2bee0f7f123112002108
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479772"
---
# <a name="sample-extension-types"></a>Tipos de extensão de exemplo

Extensões de exemplo, também chamadas de DUEs (extensões de unidade de dados) ou propriedades de buffer, são itens de dados anexados aos exemplos de mídia na seção de dados do arquivo ASF. Vários tipos de extensões de exemplo são definidos no SDK Windows Formato de Mídia. Você também pode criar seus próprios tipos de extensão.

Para usar extensões de exemplo, você deve identificar o tipo de extensão nos dados de configuração de fluxo do perfil. Chame o [**método IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) para configurar um fluxo para aceitar exemplos com dados estendidos.

Extensões de exemplo individuais devem ser adicionadas aos exemplos de entrada chamando o [**método INSSBuffer3::SetProperty.**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) Ao ler exemplos, você pode chamar o [**método INSSBuffer3::GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) para recuperar os dados da extensão. Você também pode usar os métodos da interface [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) para enumerar as extensões de unidade de dados anexadas a um exemplo.

A tabela a seguir lista os identificadores de extensão de unidade de dados predefinidos e descreve os dados anexados a exemplos para cada um.




| GUID de extensão de exemplo | Descrição | 
|-----------------------|-------------|
| WM_SampleExtensionGUID_OutputCleanPoint | Os dados indicam se o exemplo é um <a href="wmformat-glossary.md"><em>ponto de limpeza</em></a>. Um valor de zero indica que o exemplo não é um ponto de limpeza. Um valor não zero indica que ele é um ponto de limpeza. Esse tipo due (extensão de unidade de dados) de exemplo é usado para controlar os pontos de limpeza ao escrever fluxos de mídia pré-compactados que foram codificados com codecs de terceiros. | 
| WM_SampleExtensionGUID_Timecode | Os dados são uma <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> que contém dados de código de tempo SMPTE associados ao exemplo. O tamanho desse DUE é sempre WM_SampleExtension_Timecode_Size, que é de 14 bytes.<br /> | 
| WM_SampleExtensionGUID_FileName | Esse tipo de extensão de exemplo é usado para fluxos de arquivos. Os dados em um exemplo de fluxo de arquivos são uma parte de um arquivo de dados. Os dados na extensão de exemplo especificam o nome do arquivo do qual o conteúdo na amostra foi tirado. O nome do arquivo é uma cadeia de caracteres largos que contém o nome do arquivo no formato name.extension sem nenhuma informação de caminho.<br /> | 
| WM_SampleExtensionGUID_ContentType | Os dados identificam o tipo de conteúdo que o exemplo contém. Esse tipo de extensão de exemplo é usado com fluxos de vídeo entrelaçados. Todo o conteúdo entrelaçado usa o sinalizador WM_CT_INTERLACED de WM_CT_INTERLACED combinado por um <strong>OR</strong> bit a bit com WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST ou WM_CT_REPEAT_FIRST_FIELD.<br /> A ordem de campo não é usada no processo de codificação, mas é mantida com as amostras compactadas para que ela possa ser passada para o hardware de renderização. A reprodução de conteúdo entrelaçado com a ordem de campo incorreta introduz artefatos, como tremedação de movimento no vídeo.<br /> O tamanho desse DUE é sempre WM_SampleExtension_ContentType_Size.<br /> | 
| WM_SampleExtensionGUID_PixelAspectRatio | Os dados indicam a taxa de proporção de pixel do conteúdo no exemplo. Isso se aplica somente ao vídeo. Esse tipo de extensão é usado para identificar a taxa de proporção de pixels não quadrados. Para obter mais informações, <a href="to-read-and-write-video-streams-with-non-square-pixels.md">consulte To Read and Write Video Fluxos with Non-Square Pixels</a>.<br /> Os valores de taxa de proporção são armazenados como uma palavra cujo byte baixo é o aspecto X e cujo byte alto é o aspecto Y. Por exemplo, 16:9 é armazenado como 0x0910.<br /> O tamanho desse DUE é sempre WM_SampleExtension_PixelAspectRatio_Size, que é de 2 bytes.<br /> | 
| WM_SampleExtensionGUID_SampleDuration | Os dados indicam a duração, em milissegundos, do exemplo contido no objeto de buffer. Na reprodução, se due estiver definido, o objeto de leitor o usará para substituir o valor de duração de exemplo existente. Esse DUE é definido automaticamente pelos componentes de tempo de run time do SDK em fluxos de vídeo com taxas de bits de 100 kbps ou superior, em que a sobrecarga das informações due não é significativa. Ele não está definido para fluxos com taxas de bits abaixo de 100 kbps. Os aplicativos não devem definir esse DUE manualmente porque o autor (em fluxos de alta taxa de bits) substituirá o valor por seus próprios dados.<br /> O tamanho desse DUE é sempre WM_SampleExtension_SampleDuration_Size, que é de 2 bytes.<br /> | 
| WM_SampleExtensionGUID_ChromaLocation | Os dados indicam o tipo de subampling chroma usado no formato de vídeo I420. O valor dessa extensão é definido como um dos valores a seguir:<br /><ul><li>WM_CL_INTERLACED420</li><li>WM_CL_PROGRESSIVE420</li></ul>Essa extensão de unidade de dados não está configurada no perfil. Ele está incluído na saída de exemplos do decodificador.<br /> O tamanho desse DUE é sempre WM_SampleExtension_ChromaLocation_Size, que é de 1 byte.<br /> | 
| WM_SampleExtensionGUID_ColorSpaceInfo | Os dados fornece informações sobre o espaço de cores usado para o quadro de vídeo atual. O valor dessa extensão é uma <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>estrutura WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> dados.<br /> Essa extensão de unidade de dados não está configurada no perfil. Ele está incluído na saída de exemplos do decodificador.<br /> O tamanho desse DUE é sempre WM_SampleExtension_ColorSpaceInfo_Size, que é de 3 bytes.<br /> | 
| WM_SampleExtensionGUID_UserDataInfo | Os dados são dados de usuário personalizados. Os primeiros quatro bytes dos dados contêm o tamanho dos dados personalizados.<br /> O próximo byte contém o tipo de dados de usuário fornecidos na extensão de exemplo. Os seguintes tipos têm suporte:<br /><ul><li>0x1F - Dados de usuário no nível da sequência</li><li>0x1E - Dados de usuário no nível do ponto de entrada</li><li>0x1D - Dados de usuário no nível do quadro</li><li>0x1C - Dados de usuário no nível do campo</li><li>0x1B - Dados de usuário no nível da fatia</li></ul>O sexto e os bytes subsequentes contêm os dados do usuário. Há quantos bytes de dados do usuário são especificados pelo número nos primeiros quatro bytes.<br /> Essa extensão de unidade de dados não está configurada no perfil. Ele está incluído em amostras que são saídas do decodificador.<br /> | 
| WM_SampleExtensionGUID_SampleProtectionSalt | Os dados são criptografados por exemplo. Esse tipo de extensão de exemplo é usado para conteúdo importado de um formato de arquivo não ASF e um esquema de proteção de direitos diferente Windows DRM de Mídia. Ao importar conteúdo protegido, cada amostra deve incluir um sal exclusivo. Normalmente, esse valor é um contador que aumenta de forma monotônica.<br /> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 





