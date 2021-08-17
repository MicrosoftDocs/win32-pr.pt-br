---
title: Copiar Fluxos sem descompactar os dados
description: Copiar Fluxos sem descompactar os dados
ms.assetid: c268ce44-a09d-4304-bc39-8b6657da2bdb
keywords:
- Windows SDK de Formato de Mídia, copiando fluxos
- ASF (Advanced Systems Format), copiando fluxos
- ASF (Formato de Sistemas Avançados), copiando fluxos
- fluxos, copiando sem descompactar dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2387861c25ad565298fb2731300f6da8ccc00c26c5f7c82c36fede1bb7f62f9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931556"
---
# <a name="copying-streams-without-decompressing-the-data"></a>Copiar Fluxos sem descompactar os dados

A maneira mais simples e mais comum de copiar um fluxo de um arquivo para outro é recuperar os exemplos em seu estado compactado e, em seguida, grave-os no novo arquivo sem descompactá-los e recompactá-los. Exemplos obtidos de um arquivo em seu estado compactado são chamados de exemplos de fluxo, porque eles são inalterados de sua representação no fluxo. É recomendável que você sempre use exemplos de fluxo para copiar fluxos, pois descompactar e recompactar dados de mídia digital degrada a qualidade. Se você precisa copiar um fluxo de dados descompactados, consulte Copiando Fluxos [usando exemplos descompactados.](copying-streams-using-decompressed-samples.md)

É possível concatenar dois ou mais fluxos em um único fluxo usando amostras compactadas, mas somente se as taxas de bits são idênticas. O processo é essencialmente o mesmo que as etapas descritas abaixo, exceto que você deve ler vários arquivos originais para obter todo o conteúdo necessário. No entanto, você só poderá gravar amostras compactadas de vários arquivos em um único fluxo se as estruturas **WM \_ MEDIA \_ TYPE** (incluindo todos os membros da estrutura **pbFormat)** de todos os fluxos compactados são idênticas. Para combinar dados de vários fluxos que não são do mesmo formato, você deve descompactar o conteúdo e recompactá-lo no fluxo de destino. Além disso, ao combinar dados de dois ou mais fluxos em um único fluxo, você deve adicionar os valores da janela de buffer para todos os fluxos juntos para obter a janela de buffer para o novo fluxo. Isso é porque é impossível determinar quanto do buffer é retirado no final de um fluxo e no início de outro.

Você pode recuperar exemplos de fluxo com o leitor assíncrono usando [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples). Os exemplos de fluxo são entregues a [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample), não a [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample). Se você estiver lendo um arquivo e recuperando alguns fluxos compactados e alguns descompactados, deverá implementar os dois métodos de retorno de chamada.

O leitor síncrono fornece mais flexibilidade para recuperar exemplos. Você pode alternar entre amostras compactadas e descompactados livremente durante a reprodução usando [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples).

Para copiar um fluxo inteiro de um arquivo ASF para um novo arquivo ASF, execute as etapas a seguir. Essas etapas usam o leitor síncrono porque é muito mais simples de usar para esse tipo de operação.

1.  Crie um objeto de leitor síncrono chamando a [**função WMCreateSyncReader.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader)
2.  Abra um arquivo no leitor com uma chamada para [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).
3.  Obter um ponteiro para a interface [**IWMProfile**](iwmprofile.md) do objeto de leitor síncrono chamando **IWMSyncReader::QueryInterface**.
4.  Recupere as propriedades do fluxo desejado chamando [**IWMProfile::GetStreamByNumber.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstreambynumber) Isso recuperará um ponteiro para a interface [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) do objeto de configuração de fluxo para o fluxo que você deseja.
5.  Obter uma cópia da estrutura [**WM \_ MEDIA \_ TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o fluxo. Faça duas chamadas para [**IWMMediaProps::GetMediaType:**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)a primeira para obter o tamanho da estrutura, a segunda para obter a própria estrutura.
6.  Crie um objeto do gerenciador de perfil chamando [**a função WMCreateProfileManager.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager)
7.  Chame [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile) para criar um novo perfil (ou abra um perfil existente ao qual você deseja adicionar o fluxo). Chame [**IWMProfile::AddStream no**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream) novo perfil para adicionar o fluxo do arquivo existente. Ao adicionar o fluxo, use o ponteiro **IWMStreamConfig** obtido na etapa 4.
8.  Crie um objeto writer com uma chamada para a [**função WMCreateWriter.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) De definir o perfil recém-criado como o perfil ativo no autor chamando [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). Crie um arquivo para saída chamando [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).
9.  Para cada entrada associada ao fluxo ou aos fluxos que você está copiando, chame [**IWMWriter::SetInputProps,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops)passando **NULL** para a interface [**IWMInputMediaProps.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) Isso informa ao objeto de autor que ele não precisa validar os dados que você está passando. Você deve fazer essa chamada antes de chamar **BeginWriting** (etapa 14), caso contrário, um objeto de leitura pode não conseguir decodificar o conteúdo.
10. De configurar o leitor síncrono para fornecer amostras de fluxo compactado para o fluxo selecionado chamando [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) com o parâmetro *fCompressed* definido como True.
11. Obtenha informações de codec para cada fluxo que está sendo copiado e adicione as informações de codec ao header antes de escrever. Para obter as informações de codec, chame [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar os codecs associados ao arquivo no leitor. Selecione as informações de codec que corresponde à configuração do fluxo. Em seguida, de definir as informações de codec no autor chamando [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando as informações obtidas do leitor.
12. Obtenha um ponteiro para a interface [**IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced) chamando **IWMWriter::QueryInterface**.
13. Descrição do autor para o modo de escrita chamando [**IWMWriter::BeginWriting.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)
14. Faça chamadas repetidas [**para IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample), especificando o número de fluxo desejado. Quando exemplos são recebidos, passe-os para o autor com chamadas para [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample). Para fluxos de vídeo, você deve verificar os sinalizadores (se algum) definidos pelo autor em cada chamada para **GetNextSample**. Se WM SF CLEANPOINT estiver definido, você também deverá \_ \_ defini-lo em sua chamada para **WriteStreamSample.**
15. Quando a leitura for concluída, chame [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting). O fluxo deve ser transferido.

> [!Note]  
> Os fluxos de imagem não podem ser copiados de um arquivo para outro usando exemplos de fluxo. Para copiar dados de fluxo de imagem, recupere os exemplos descompactados e processe-os por meio do writer como faria normalmente.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Copiando dados de um arquivo para outro**](copying-data-from-one-file-to-another.md)
</dt> <dt>

[**Copiando Fluxos usando exemplos descompactados**](copying-streams-using-decompressed-samples.md)
</dt> </dl>

 

 




