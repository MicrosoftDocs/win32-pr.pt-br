---
title: Tipos de extensão de exemplo
description: Tipos de extensão de exemplo
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- SDK do Windows Media Format, extensões de exemplo
- ASF (Advanced Systems Format), extensões de exemplo
- ASF (formato de sistemas avançados), extensões de exemplo
- SDK do Windows Media Format, extensões de unidade de dados
- ASF (Advanced Systems Format), extensões de unidade de dados
- ASF (formato de sistemas avançados), extensões de unidade de dados
- SDK do Windows Media Format, propriedades do buffer
- Formato de sistema avançado (ASF), propriedades de buffer
- ASF (formato de sistemas avançados), propriedades de buffer
- extensões de exemplo, tipos
- extensões de unidade de dados, tipos
- Propriedades do buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972e3da1ecaad277158bb270cc358436f53db9e2
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "105808235"
---
# <a name="sample-extension-types"></a>Tipos de extensão de exemplo

As extensões de exemplo, também chamadas de extensões de unidade de dados (dívidas) ou propriedades de buffer, são itens de dados anexados aos exemplos de mídia na seção de dados do arquivo ASF. Vários tipos de extensões de exemplo são definidos no SDK do Windows Media Format. Você também pode criar seus próprios tipos de extensão.

Para usar extensões de exemplo, você deve identificar o tipo de extensão nos dados de configuração de fluxo do perfil. Chame o método [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) para configurar um fluxo para aceitar amostras com dados estendidos.

Extensões de exemplo individuais devem ser adicionadas aos exemplos de entrada chamando o método [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) . Ao ler exemplos, você pode chamar o método [**INSSBuffer3:: GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) para recuperar os dados de extensão. Você também pode usar os métodos da interface [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) para enumerar as extensões de unidade de dados anexadas a um exemplo.

A tabela a seguir lista os identificadores de extensão de unidade de dados predefinidos e descreve os dados anexados a exemplos para cada um.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID de extensão de exemplo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WM_SampleExtensionGUID_OutputCleanPoint</td>
<td>Os dados indicam se o exemplo é um <a href="wmformat-glossary.md"><em>cleanpoint</em></a>. Um valor de zero indica que o exemplo não é um cleanpoint. Um valor diferente de zero indica que se trata de um cleanpoint. Esse tipo de extensão de unidade de dados (devido) de exemplo é usado para controlar o cleanpoints ao gravar fluxos de mídia compactados que foram codificados com codecs de terceiros.</td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_Timecode</td>
<td>Os dados são uma estrutura de <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> que contém dados de código de tempo SMPTE associados ao exemplo. O tamanho para isso devido é sempre WM_SampleExtension_Timecode_Size, que é de 14 bytes.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_FileName</td>
<td>Esse tipo de extensão de exemplo é usado para fluxos de arquivo. Os dados em um exemplo de fluxo de arquivo são uma parte de um arquivo de dados. Os dados na extensão de exemplo especificam o nome do arquivo do qual o conteúdo no exemplo foi tirado. O nome do arquivo é uma cadeia de caracteres largos que contém o nome do arquivo no formato name. Extension sem nenhuma informação de caminho.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ContentType</td>
<td>Os dados identificam o tipo de conteúdo que o exemplo contém. Esse tipo de extensão de exemplo é usado com fluxos de vídeo entrelaçados. Todo o conteúdo entrelaçado usa o sinalizador de WM_CT_INTERLACED combinado por um OR-bit <strong>ou</strong> com WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST ou WM_CT_REPEAT_FIRST_FIELD.<br/> A ordem de campo não é usada no processo de codificação, mas é mantida com os exemplos compactados para que ele possa ser passado para o hardware de renderização. A reprodução de conteúdo entrelaçado com a ordem de campo incorreta apresenta artefatos como a tremulação de movimento no vídeo.<br/> O tamanho para isso devido é sempre WM_SampleExtension_ContentType_Size.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_PixelAspectRatio</td>
<td>Os dados indicam a taxa de proporção de pixel do conteúdo no exemplo. Isso se aplica somente a vídeo. Esse tipo de extensão é usado para identificar a taxa de proporção de pixels não quadrados. Para obter mais informações, consulte <a href="to-read-and-write-video-streams-with-non-square-pixels.md">para ler e gravar fluxos de vídeo com pixels não quadrados</a>.<br/> Os valores de taxa de proporção são armazenados como uma palavra cujo byte baixo é o aspecto X e cujo byte alto é o aspecto Y. Por exemplo, 16:9 é armazenado como 0x0910.<br/> O tamanho para isso devido é sempre WM_SampleExtension_PixelAspectRatio_Size, que é de 2 bytes.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleDuration</td>
<td>Os dados indicam a duração, em milissegundos, do exemplo contido no objeto de buffer. Na reprodução, se isso devido for definido, o objeto de leitor o usará para substituir o valor de duração de exemplo existente. Isso devido é definido automaticamente pelos componentes de tempo de execução do SDK em fluxos de vídeo com taxas de bits de 100 kbps ou mais, em que a sobrecarga das informações de conclusão não é significativa. Ele não está definido para fluxos com taxas de bits em 100 kbps. Os aplicativos não devem definir isso de forma manual porque o gravador (em fluxos de alta taxa de bits) substituirá o valor por seus próprios dados.<br/> O tamanho para isso devido é sempre WM_SampleExtension_SampleDuration_Size, que é de 2 bytes.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_ChromaLocation</td>
<td>Os dados indicam o tipo de subamostragem croma usado no formato de vídeo I420. O valor dessa extensão é definido como um dos seguintes valores:<br/>
<ul>
<li>WM_CL_INTERLACED420</li>
<li>WM_CL_PROGRESSIVE420</li>
</ul>
Esta extensão de unidade de dados não está configurada no perfil. Ele é incluído na saída de exemplos do decodificador.<br/> O tamanho desta conclusão é sempre WM_SampleExtension_ChromaLocation_Size, que é de 1 byte.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_ColorSpaceInfo</td>
<td>Os dados fornecem informações sobre o espaço de cores usado para o quadro de vídeo atual. O valor dessa extensão é uma estrutura de <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> .<br/> Esta extensão de unidade de dados não está configurada no perfil. Ele é incluído na saída de exemplos do decodificador.<br/> O tamanho desta conclusão é sempre WM_SampleExtension_ColorSpaceInfo_Size, que é de 3 bytes.<br/></td>
</tr>
<tr class="odd">
<td>WM_SampleExtensionGUID_UserDataInfo</td>
<td>Os dados são dados de usuário personalizados. Os quatro primeiros bytes dos dados contêm o tamanho dos dados personalizados.<br/> O próximo byte contém os tipos de dados de usuário fornecidos na extensão de exemplo. Os seguintes tipos têm suporte:<br/>
<ul>
<li>0x1F-dados de usuário de nível de sequência</li>
<li>0x1E-dados de usuário do nível de ponto de entrada</li>
<li>0x1D-dados de usuário de nível de quadro</li>
<li>0x1C-dados de usuário de nível de campo</li>
<li>0x1B-dados de usuário de nível de fatia</li>
</ul>
O sexto e os bytes subsequentes contêm os dados do usuário. Há quantos bytes de dados de usuário são especificados pelo número nos primeiros quatro bytes.<br/> Esta extensão de unidade de dados não está configurada no perfil. Ele é incluído em exemplos que são gerados do decodificador.<br/></td>
</tr>
<tr class="even">
<td>WM_SampleExtensionGUID_SampleProtectionSalt</td>
<td>Os dados são criptografados por exemplo. Esse tipo de extensão de exemplo é usado para o conteúdo que é importado de um formato de arquivo não ASF e um esquema de proteção de direitos que não seja o DRM do Windows Media. Ao importar conteúdo protegido, cada amostra deve incluir um Salt exclusivo. Normalmente, esse valor é um contador que aumenta de forma monotônico.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 





