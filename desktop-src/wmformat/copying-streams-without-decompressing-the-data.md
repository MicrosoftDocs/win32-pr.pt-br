---
title: Copiando fluxos sem descompactar os dados
description: Copiando fluxos sem descompactar os dados
ms.assetid: c268ce44-a09d-4304-bc39-8b6657da2bdb
keywords:
- SDK do Windows Media Format, copiando fluxos
- ASF (Advanced Systems Format), copiando fluxos
- ASF (formato de sistemas avançados), copiando fluxos
- fluxos, copiando sem descompactar dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831b85ad431a6c4d3f4255c281d22ca17004674f
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104365736"
---
# <a name="copying-streams-without-decompressing-the-data"></a>Copiando fluxos sem descompactar os dados

A maneira mais simples e mais comum de copiar um fluxo de um arquivo para outro é recuperar os exemplos em seu estado compactado e, em seguida, gravá-los no novo arquivo sem descompactá-los e recompactá-los. Amostras obtidas de um arquivo em seu estado compactado são chamadas de amostras de fluxo, porque elas não são alteradas de sua representação no fluxo. É recomendável que você sempre use amostras de fluxo para copiar fluxos, pois descompactar e recompactar dados de mídia digital degrada a qualidade. Se você precisar copiar um fluxo de dados descompactados, consulte [copiando fluxos usando amostras descompactadas](copying-streams-using-decompressed-samples.md).

É possível concatenar dois ou mais fluxos em um único fluxo usando amostras compactadas, mas somente se as taxas de bits forem idênticas. O processo é essencialmente o mesmo que as etapas descritas abaixo, exceto pelo fato de que você deve ler vários arquivos originais para obter todo o conteúdo de que precisa. No entanto, você só poderá gravar amostras compactadas de vários arquivos em um único fluxo se as estruturas de **\_ \_ tipo de mídia do WM** (incluindo todos os membros da estrutura **pbFormat** ) de todos os fluxos compactados forem idênticas. Para combinar dados de vários fluxos que não são do mesmo formato, você deve descompactar o conteúdo e recompactá-lo no fluxo de destino. Além disso, ao combinar dados de dois ou mais fluxos em um único fluxo, você deve adicionar os valores da janela de buffer para todos os fluxos juntos para obter a janela de buffer para o novo fluxo. Isso ocorre porque é impossível determinar quanto do buffer é retirado no final de um fluxo e no início de outro.

Você pode recuperar amostras de fluxo com o leitor assíncrono usando [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples). Exemplos de fluxo são entregues a [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample), não a [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Se você estiver lendo um arquivo e recuperando alguns fluxos compactados e alguns descompactados, você deve implementar ambos os métodos de retorno de chamada.

O leitor síncrono fornece mais flexibilidade para recuperar amostras. Você pode alternar entre exemplos compactados e descompactados livremente durante a reprodução usando [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples).

Para copiar um fluxo inteiro de um arquivo ASF para um novo arquivo ASF, execute as etapas a seguir. Essas etapas usam o leitor síncrono porque é muito mais simples de usar para esse tipo de operação.

1.  Crie um objeto leitor síncrono chamando a função [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) .
2.  Abra um arquivo no leitor com uma chamada para [**IWMSyncReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).
3.  Obtenha um ponteiro para a interface [**IWMProfile**](iwmprofile.md) do objeto leitor síncrono chamando **IWMSyncReader:: QueryInterface**.
4.  Recupere as propriedades do fluxo desejado chamando [**IWMProfile:: GetStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber). Isso recuperará um ponteiro para a interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) do objeto de configuração de fluxo para o fluxo desejado.
5.  Obtenha uma cópia da estrutura [**do \_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o fluxo. Faça duas chamadas para [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype): a primeira para obter o tamanho da estrutura, a segunda para obter a estrutura em si.
6.  Crie um objeto do Gerenciador de perfis chamando a função [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) .
7.  Chame [**IWMProfileManager:: CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) para criar um novo perfil (ou abra um perfil existente ao qual você deseja adicionar o fluxo). Chame [**IWMProfile:: AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) no novo perfil para adicionar o fluxo do arquivo existente. Ao adicionar o fluxo, use o ponteiro **IWMStreamConfig** obtido na etapa 4.
8.  Crie um objeto gravador com uma chamada para a função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) . Defina o perfil recém-criado como o perfil ativo no gravador chamando [**IWMWriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). Crie um arquivo para saída chamando [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).
9.  Para cada entrada associada ao fluxo ou aos fluxos que você está copiando, chame [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops), passando **NULL** para a interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) . Isso informa ao objeto Writer que não é necessário validar os dados que você está passando. Você deve fazer essa chamada antes de chamar **BeginWriting** (etapa 14), caso contrário, um objeto de leitura pode não ser capaz de decodificar o conteúdo.
10. Defina o leitor síncrono para fornecer amostras de fluxo compactadas para o fluxo selecionado chamando [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) com o parâmetro *FCompressed* definido como true.
11. Obtenha informações de codec para cada fluxo que está sendo copiado e adicione as informações do codec ao cabeçalho antes de gravar. Para obter as informações do codec, chame [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar os codecs associados ao arquivo no leitor. Selecione as informações de codec que correspondem à configuração de fluxo. Em seguida, defina as informações do codec no gravador chamando [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando as informações obtidas do leitor.
12. Obtenha um ponteiro para a interface [**IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced) chamando **IWMWriter:: QueryInterface**.
13. Defina o gravador para o modo de gravação chamando [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).
14. Faça chamadas repetidas para [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample), especificando o número de fluxo desejado. Quando os exemplos são recebidos, passe-os para o gravador com chamadas para [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample). Para fluxos de vídeo, você deve verificar os sinalizadores (se houver) definidos pelo gravador em cada chamada para **GetNextSample**. Se o WM \_ it \_ CLEANPOINT estiver definido, você também deverá defini-lo em sua chamada para **WriteStreamSample**.
15. Quando a leitura estiver concluída, chame [**IWMWriter:: redação**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting). O fluxo deve ser transferido.

> [!Note]  
> Os fluxos de imagem não podem ser copiados de um arquivo para outro usando amostras de fluxo. Para copiar dados de fluxo de imagem, recupere os exemplos descompactados e, em seguida, processe-os por meio do gravador como faria normalmente.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Copiando dados de um arquivo para outro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copiando fluxos usando amostras descompactadas**](copying-streams-using-decompressed-samples.md)
</dt> </dl>

 

 




