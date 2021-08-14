---
title: Para criar arquivos ASF usando codecs de terceiros
description: Para criar arquivos ASF usando codecs de terceiros
ms.assetid: 5cd348ca-1f86-429d-92ee-4eab4ced8571
keywords:
- Windows SDK do formato de mídia, criando arquivos ASF
- Windows SDK do formato de mídia, codecs de terceiros
- ASF (Advanced Systems Format), criando arquivos
- ASF (formato de sistemas avançados), criando arquivos
- Formato de sistema avançado (ASF), codecs de terceiros
- ASF (formato de sistemas avançados), codecs de terceiros
- codecs de terceiros
- codecs, terceiros
- codecs, criando arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1eeeb891037581a550d8c15c2f2b4cefa14f81f20d0d55623d382d0e933e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197071"
---
# <a name="to-create-asf-files-using-third-party-codecs"></a>Para criar arquivos ASF usando codecs de terceiros

você pode usar o SDK do formato de mídia Windows para criar arquivos ASF que contêm mídia digital codificada com qualquer codec escolhido. Ao usar um codec diferente de um incluído neste SDK, você deve executar as etapas a seguir.

1.  Codifique o conteúdo com o codec desejado.
2.  Localize ou crie um valor de GUID para identificar o conteúdo codificado com o codec usado na etapa 1.
3.  Crie um novo perfil ou modifique um perfil existente para uso com o conteúdo codificado.
    -   Crie um fluxo para o conteúdo codificado com o tipo principal apropriado. Para obter mais informações sobre os principais tipos de mídia, consulte [tipos de mídia](media-types.md). Use o GUID identificado na etapa 2 como o subtipo de mídia.
    -   Defina a taxa de bits e a janela de buffer para o fluxo para valores que não resultarão no estouro de buffer. Você deve ser capaz de obter esses valores do codec no momento da codificação. Os componentes de tempo de execução do SDK verificam os valores da janela de taxa de bits/buffer e removem amostras, se necessário, para que os dados específicos caibam com esses valores. Se você definir os valores incorretamente, o arquivo não será transmitido corretamente, resultando em uma reprodução ruim.
    -   Para fluxos de vídeo, você deve definir o membro de **bicompressão** da estrutura **BITMAPINFOHEADER** contida na estrutura [**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader) para o valor FOURCC apropriado para o conteúdo. Esse valor deve ser igual aos quatro primeiros bytes do GUID do subtipo. Por exemplo, se **biCompression** for MAKEFOURCC (' T', ' E ', ' s', ' T') = 0x54455354, o GUID do subtipo começará da seguinte maneira: 54455354-XXXX-XXXX-XXXX-XXXXXXXXXXXX.
4.  Crie um objeto do gravador e carregue o perfil criado na etapa anterior. Para obter mais informações sobre como gravar arquivos, consulte [Writing ASF files](writing-asf-files.md).
5.  Faça um loop pelas entradas do arquivo e atribua Propriedades de entrada para cada um como faria normalmente. Para obter mais informações sobre entradas, consulte [trabalhando com entradas](working-with-inputs.md). Para o fluxo codificado com um codec de terceiros, defina o ponteiro de interface [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) como **nulo** antes de chamar [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).
6.  Use o novo perfil criado na etapa anterior para gravar o arquivo. Passe os exemplos compactados usando [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) em vez de [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample). Para vídeo, você deve especificar quais exemplos são quadros-chave passando \_ o WM it \_ CLEANPOINT como o parâmetro *dwFlags* .

Para processar e descompactar o fluxo codificado com um codec de terceiros, você deve ler exemplos de fluxo compactados. Seu aplicativo de leitura também deve tratar a descompactação de exemplo para o fluxo.

## <a name="putting-mpeg-2-streams-into-asf"></a>Colocando fluxos MPEG-2 no ASF

> [!Note]  
> este tópico se aplica a aplicativos que usam o SDK do formato de mídia Windows para colocar MPEG-2 (ou outros formatos de compactação que usam quadros B) no contêiner do arquivo ASF.

 

O objeto do gravador requer que todos os exemplos de entrada tenham carimbos de data/hora e supõe que cada amostra de entrada tem um tempo de apresentação posterior ao que o precede. Embora praticamente todos os vídeos descompactados e até mesmo alguns fluxos de vídeo compactados atendam a essas condições, os fluxos MPEG-2 não fazem isso. Em MPEG-2, nem todas as amostras são de data e hora e quando os quadros B estão presentes, a ordem de decodificação de exemplo não é a mesma que a ordem de renderização. Quando o objeto do gravador encontra amostras fora de ordem, ele os organiza na ordem "correta". Portanto, para armazenar fluxos MPEG-2 nativamente (não decodificados) em um contêiner ASF, você deve executar as seguintes etapas:

Ao gravar o arquivo:

1.  Adicione uma extensão de unidade de dados de tamanho fixo (devido) a cada amostra de entrada que conterá uma estrutura que contém os valores reais de hora de início e tempo de parada de carimbo de hora MPEG para o exemplo. Use-1 para esses valores se o exemplo não tiver carimbo de data/hora.
2.  Forneça os carimbos de data/hora de entrada "fictícios" do objeto gravador que estão sempre aumentando para que eles gravem os exemplos no arquivo exatamente na mesma ordem em que são recebidos. Os carimbos de data/hora fictícios devem corresponder aproximadamente aos tempos de apresentação reais, conforme a média ao longo do tempo. Os carimbos de data/hora fictícios formarão a linha do tempo de busca, portanto, se eles divergirem em relação aos carimbos em tempo real, as operações de busca no arquivo produzirão resultados inesperados. No entanto, uma quantidade limitada de tremulação entre os tempos de amostra não afetará seriamente as operações de busca.

Ao ler o arquivo:

-   Para cada exemplo de leitura do arquivo, examine a conclusão. Se ele contiver uma hora de início maior ou igual a zero, copie esse valor para o carimbo de data/hora do exemplo de saída antes que ele seja entregue ao decodificador. Defina todos os outros carimbos de data/hora na saída exemplos como **NULL**. em DirectShow, isso é feito chamando **IMediaSample:: settime**(**null**,**null**).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Armazenando conteúdo em buffer**](buffering-content.md)
</dt> <dt>

[**Interface IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Interface IWMWriterAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Para fornecer amostras compactadas com o leitor assíncrono**](to-deliver-compressed-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**Para recuperar exemplos de fluxo com o leitor síncrono**](to-retrieve-stream-samples-with-the-synchronous-reader.md)
</dt> <dt>

[**WMVIDEOINFOHEADER**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader)
</dt> <dt>

[**Trabalhando com perfis**](working-with-profiles.md)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




