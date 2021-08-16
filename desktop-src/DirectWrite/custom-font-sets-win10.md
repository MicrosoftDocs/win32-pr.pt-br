---
title: Conjuntos de fontes personalizados
description: Este tópico descreve várias maneiras em que você pode usar fontes personalizadas em seu aplicativo.
ms.assetid: 50842838-d150-df9a-f1b7-67ce5ea2bc80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b8b9c49895c2b137aaa33cf0788d9518a1d53834c74eb27feb6b44fa045d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650280"
---
# <a name="custom-font-sets"></a>Conjuntos de fontes personalizados

Este tópico descreve várias maneiras em que você pode usar fontes personalizadas em seu aplicativo.

-   [Apresentações ](#introduction)
-   [Resumo das APIs](#summary-of-apis)
-   [Principais conceitos](#key-concepts)
-   [Fontes e formatos de arquivo de fonte](#fonts-and-font-file-formats)
-   [Conjuntos de fontes e coleções de fontes](#font-sets-and-font-collections)
-   [Cenários comuns](#common-scenarios)
    -   [Criando um conjunto de fontes usando fontes arbitrárias no sistema de arquivos local](#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)
    -   [Criando um conjunto de fontes usando fontes conhecidas no sistema de arquivos local](#creating-a-font-set-using-known-fonts-in-the-local-file-system)
    -   [Criar um conjunto de fontes personalizado usando fontes remotas conhecidas na Web](#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)
    -   [Criando um conjunto de fontes personalizado usando dados de fonte carregados na memória](#creating-a-custom-font-set-using-font-data-loaded-into-memory)
-   [Cenários avançados](#advanced-scenarios)
    -   [Combinando conjuntos de fontes](#combining-font-sets)
    -   [Usando dados de fonte WOFF ou WOFF2 locais ](#using-local-woff-or-woff2-font-data)
    -   [usando DirectWrite mecanismos de fonte remota com implementação de rede de nível inferior personalizada](#using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation)
    -   [cenários de suporte em versões anteriores do Windows](#supporting-scenarios-on-earlier-windows-versions)

## <a name="introduction"></a>Introdução

Na maioria das vezes, os aplicativos usam as fontes que são instaladas localmente no sistema. DirectWrite fornece acesso a essas fontes usando os métodos [**IDWriteFactory3:: GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) ou [**IDWriteFactory:: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . em alguns casos, os aplicativos também podem querer usar fontes que são incluídas como parte do Windows 10, mas que não estão atualmente instaladas no sistema atual. essas fontes podem ser acessadas no serviço de fonte Windows usando o método **GetSystemFontSet** ou chamando [**IDWriteFactory3:: GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) com includeDownloadableFonts definido como TRUE. 

em alguns cenários de aplicativo, no entanto, os aplicativos precisam usar fontes que não estão instaladas no sistema e não são fornecidas pelo serviço de fonte Windows. Veja a seguir exemplos de tais cenários:

-   As fontes são inseridas como recursos dentro de um binário de aplicativo.
-   Os arquivos de fonte são agrupados em um pacote de aplicativo e armazenados em disco na pasta de instalação do aplicativo.
-   O aplicativo é uma ferramenta de desenvolvimento de fontes que precisa carregar arquivos de fonte especificados pelo usuário. 
-   As fontes são inseridas em arquivos de documento que podem ser exibidas ou editadas no aplicativo. 
-   O aplicativo usa fontes obtidas de um serviço de fontes da Web pública. 
-   O aplicativo usa dados de fonte transmitidos por meio de um protocolo de rede privada. 

DirectWrite fornece APIs para trabalhar com fontes personalizadas nesses e em outros cenários semelhantes. Os dados de fonte personalizados podem vir de arquivos no sistema de arquivos local; de fontes remotas baseadas em nuvem acessadas usando HTTP; ou de fontes arbitrárias depois de terem sido carregadas em um buffer de memória. 

> [!Note]  
> embora DirectWrite tenha fornecido apis para trabalhar com fontes personalizadas desde Windows 7, as apis mais recentes foram adicionadas Windows 10 e novamente no Atualização do Windows 10 para Criadores (versão prévia 15021 ou posterior) que facilita a implementação de vários dos cenários mencionados. Este tópico se concentra nas APIs disponíveis no Windows 10. para aplicativos que precisam trabalhar em versões anteriores do Windows, consulte [coleções de fontes personalizadas (Windows 7/8)](custom-font-collections.md). 

 

## <a name="summary-of-apis"></a>Resumo das APIs

Este tópico se concentra na funcionalidade fornecida pelas seguintes APIs: 

-   Interface [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   Interface [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   Interface [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 
-   Interface [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)
-   Interface [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)
-   Método [**IDWriteFactory:: CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 
-   Método [**IDWriteFactory:: CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) 
-   Métodos [**IDWriteFactory3:: CreateFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-createfontfacereference) 
-   [**DWRITE \_ Estrutura da \_ propriedade de fonte**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) 
-   [**DWRITE \_ Enumeração \_ de \_ ID de propriedade de fonte**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) 
-   Interface [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 
-   Método [**IDWriteFactory:: RegisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader) 
-   Método [**IDWriteFactory:: UnregisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader) 
-   Método [**IDWriteFactory5:: CreateInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader) 
-   Interface [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 
-   Método [**IDWriteFactory5:: CreateHttpFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader) 
-   Interface [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 
-   Interface [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 
-   Interface [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 
-   Interface [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 
-   Interface [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) 
-   Interface [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) 
-   Método [**IDWriteFactory5:: AnalyzeContainerType**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype) 
-   Método [**IDWriteFactory5:: UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile) 

 

## <a name="key-concepts"></a>Principais conceitos

para entender as apis de DirectWrite para trabalhar com fontes personalizadas, pode ser útil entender o modelo conceitual subjacente a essas apis. Os conceitos principais serão descritos aqui. 

quando DirectWrite faz o layout ou renderização real do texto, ele precisa acessar os dados reais da fonte. Um objeto de face de fonte contém dados de fonte reais, que devem existir no sistema local. Mas, para outras operações, como verificar a disponibilidade de uma fonte específica ou apresentar opções de fonte a um usuário, tudo o que é necessário é uma referência a uma fonte específica, e não os próprios dados da fonte propriamente dito. no DirectWrite, um objeto de referência de face de fonte contém apenas as informações necessárias para localizar e criar uma instância de uma fonte. como a referência de face de fonte não contém dados reais, DirectWrite pode lidar com referências de face de fonte para as quais os dados reais estão em um local de rede remota, bem como quando os dados reais são locais.

Um conjunto de fontes é um conjunto de referências de face de fonte, juntamente com determinadas propriedades básicas e informativas que podem ser usadas na referência à fonte ou na comparação com outras fontes, como o nome da família ou um valor de peso da fonte. Os dados reais para as várias fontes podem ser locais ou podem ser remotos ou ter alguma mistura.

Um conjunto de fontes pode ser usado para obter um objeto de coleção de fontes correspondente. Consulte conjuntos de fontes e coleções de fontes abaixo para obter mais detalhes. 

A interface IDWriteFontSet fornece métodos que permitem consultar valores de propriedade, como nome de família ou peso de fonte, ou para referências de face de fonte que correspondem a valores de propriedade específicos. Após a filtragem para uma seleção específica, uma instância da interface [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) pode ser obtida, com métodos para download (se os dados reais da fonte são remotos no momento), para obter o objeto [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) correspondente que pode ser usado para layout e renderização. 

A interface IDWriteFontFile baseia-se em cada face de fonte ou referência de face de fonte. Isso representa o local de um arquivo de fonte e tem dois componentes: um carregador de arquivo de fonte e uma chave de arquivo de fonte. O [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)(carregador de arquivo de fonte) é usado para abrir um arquivo, se necessário, e retorna um fluxo com os dados ([**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)). Dependendo do carregador, os dados podem estar localizados em um caminho de arquivo local, uma URL remota ou em um buffer de memória. A chave é um valor definido pelo carregador que identifica exclusivamente o arquivo dentro do contexto do carregador, permitindo que o carregador Localize os dados e crie um fluxo para ele. 

As fontes personalizadas podem ser facilmente adicionadas a um conjunto de fontes personalizado que, por sua vez, podem ser usadas para filtrar ou organizar informações de fonte para fins como a criação de uma interface de usuário de seletor de fonte. O conjunto de fontes também pode ser usado para criar uma coleção de fontes para uso em APIs de nível superior, como [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) e [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). A interface [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) pode ser usada para criar um conjunto de fontes personalizado que inclui várias fontes personalizadas. Ele também pode ser usado para criar um conjunto de fontes personalizado que combina fontes personalizadas e fontes fornecidas pelo sistema; ou que combina fontes com fontes diferentes para os dados reais — armazenamento local, URLs remotas e memória. 

Como mencionado, uma referência de face de fonte pode se referir a dados de fonte em uma fonte remota, mas os dados devem ser locais para obter um objeto de face de fonte que pode ser usado para layout e renderização. O download de dados remotos é manipulado por uma fila de download de fontes. Os aplicativos podem usar a interface [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) para enfileirar solicitações para baixar fontes remotas para iniciar o processo de download e registrar um objeto [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) para executar uma ação quando o processo de download for concluído. 

para a maioria das interfaces descritas aqui, DirectWrite fornece implementações do sistema. A única exceção é a interface [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) , que um aplicativo implementa para tomar as ações específicas do aplicativo quando as fontes remotas são baixadas localmente. Os aplicativos podem ter motivo para fornecer suas próprias implementações personalizadas para determinadas outras interfaces, embora isso seja necessário apenas em cenários específicos e mais avançados. Por exemplo, um aplicativo precisaria fornecer uma implementação personalizada da interface [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) para manipular arquivos de fonte no armazenamento local que usam o formato de contêiner WOFF2. Detalhes adicionais serão fornecidos abaixo. 

## <a name="fonts-and-font-file-formats"></a>Fontes e formatos de arquivo de fonte

Outro conceito importante que é útil entender é a relação entre as faces de fonte individuais e os arquivos de fonte que os contêm. A ideia de um arquivo de fonte OpenType (. ttf ou. otf) que contém uma única fonte é familiar. Mas o formato de fonte OpenType também permite uma coleção de fontes OpenType (. ttc ou. OTC), que é um único arquivo que contém várias fontes. Os arquivos de coleção OpenType são frequentemente usados para fontes grandes que estão fortemente relacionadas e têm valores idênticos para determinados dados de fonte: ao combinar as fontes em um único arquivo, os dados comuns podem ser eliminados de duplicação. Por esse motivo, um tipo de fonte ou referência de face de fonte precisa fazer referência não apenas a um arquivo de fonte (ou fonte de dados equivalente), mas também deve especificar um índice de fonte dentro desse arquivo, para o caso geral em que o arquivo pode ser um arquivo de coleção. 

Para fontes usadas na Web, os dados de fonte geralmente são incluídos em determinados formatos de contêiner, WOFF ou WOFF2, que fornecem alguma compactação dos dados da fonte e algum nível de proteção contra pirataria e violação de licenças de fontes. Funcionalmente, um arquivo WOFF ou WOFF2 é equivalente a uma fonte OpenType ou arquivo de coleção de fontes, mas os dados são codificados em um formato diferente que requer descompactação antes que possa ser usado. 

determinadas apis de DirectWrite podem lidar com rostos de fontes individuais, enquanto outras apis podem manipular arquivos que podem incluir arquivos de coleção OpenType que contêm várias faces. Da mesma forma, certas APIs lidam apenas com dados brutos de formato OpenType, enquanto outras APIs podem lidar com os formatos de contêiner embalado, WOFF e WOFF2. Esses detalhes são fornecidos na discussão abaixo. 

## <a name="font-sets-and-font-collections"></a>Conjuntos de fontes e coleções de fontes

Alguns aplicativos podem ser implementados para trabalhar com fontes usando a interface [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) . Há uma correspondência direta entre uma coleção de fontes e um conjunto de fontes. Cada uma pode conter as mesmas fontes, mas elas as apresentam com uma organização diferente. De qualquer coleção de fontes, um conjunto de fontes correspondente pode ser obtido, e vice-versa.

Ao trabalhar com várias fontes personalizadas, é mais fácil usar uma interface do construtor de conjunto de fontes para criar um conjunto de fontes personalizado e obter uma coleção de fontes após a criação do conjunto de fontes. O processo para criar um conjunto de fontes personalizado será descrito em detalhes abaixo. Para obter uma interface [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) de um conjunto de fontes, o método [**IDWriteFactory3:: CreateFontCollectionFromFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset) é usado.

Se o aplicativo tiver um objeto de coleção e precisar obter um conjunto de fontes correspondente, isso poderá ser feito usando o método [**IDWriteFontCollection1:: Getfontset**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) . 

## <a name="common-scenarios"></a>Cenários comuns

Esta seção descreve alguns dos cenários mais comuns que envolvem conjuntos de fontes personalizadas:

-   Criar um conjunto de fontes personalizado usando fontes arbitrárias em caminhos no sistema de arquivos local.
-   Criar um conjunto de fontes personalizado usando fontes conhecidas (talvez agrupadas com o aplicativo) armazenadas no sistema de arquivos local.
-   Criar um conjunto de fontes personalizado usando fontes remotas conhecidas na Web.
-   Criar um conjunto de fontes personalizado usando dados de fonte carregados na memória.

as implementações completas para esses cenários são fornecidas no [exemplo DirectWrite conjuntos de fontes personalizadas](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). Esse exemplo também ilustra um cenário mais avançado para manipulação de dados de fonte empacotados em formatos de contêiner WOFF ou WOFF2, que serão discutidos abaixo. 

### <a name="creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system"></a>Criando um conjunto de fontes usando fontes arbitrárias no sistema de arquivos local

Ao lidar com um conjunto arbitrário de arquivos de fonte no armazenamento local, o método [**IDWriteFontSetBuilder1:: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) é conveniente, já que, em uma única chamada, ele pode manipular todas as faces de fonte em um arquivo de coleção de fontes OpenType, bem como todas as instâncias para uma fonte de variável OpenType. isso está disponível no Atualização do Windows 10 para Criadores (versão prévia 15021 ou posterior) e é recomendado sempre que disponível. 

Para usar esse método, use o processo a seguir.

<dl> 1. Comece criando a interface <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a> : 


```C++
IDWriteFactory5* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
  DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



   
2. Use a fábrica para obter a <a href=""></a> interface [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) : 


```C++
IDWriteFontSetBuilder1* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
}  
                
```



  
3. Para cada arquivo de fonte no sistema de arquivos local, crie um [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) que se refira a ele: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



   
4. Adicione o objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) ao construtor de conjunto de fontes usando o método [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) : 


```C++
hr = pFontSetBuilder->AddFontFile(pFontFile); 
```

Se o caminho do arquivo especificado na chamada para [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) tiver sido referenciado como algo diferente de um arquivo OpenType com suporte, a chamada para [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) retornará um erro, DWRITE \_ E \_ FileFormat.

5. Depois que todos os arquivos tiverem sido adicionados ao construtor de conjunto de fontes, o conjunto de fontes personalizado poderá ser criado: 


```C++
IDWriteFontSet* pFontSet; 
hr = pFontSetBuilder->CreateFontSet(&pFontSet); 
```



   
</dl>

se o aplicativo precisar ser executado em versões Windows 10 anteriores à Atualização do Windows 10 para Criadores, o método addfontfile não estará disponível. A disponibilidade pode ser detectada criando-se uma interface [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) e, em seguida, usando QueryInterface para tentar obter uma interface [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) : se isso for bem sucedido, a interface [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) e o método [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) também estarão disponíveis.

Se o método AddFontFile não estiver disponível, o método [**IDWriteFontSetBuilder:: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) deverá ser usado para adicionar rostos de fonte individuais. Para permitir arquivos de coleção de fontes OpenType que contenham várias faces, o método [**IDWriteFontFile:: Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) pode ser usado para determinar o número de rostos contidas no arquivo. O processo é o seguinte.

<dl> 1. Comece criando a interface <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a> : 


```C++
IDWriteFactory3* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



  
2. Use a fábrica para obter a interface [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) : 


```C++
IDWriteFontSetBuilder* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
} 
```



  
3. Para cada arquivo de fonte, crie um [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), como acima: 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



Em vez de adicionar o arquivo diretamente ao construtor de conjunto de fontes, precisamos determinar o número de rostos e criar objetos [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) individuais.   
4. Use o método [**Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) para obter o número de faces no arquivo. 


```C++
BOOL isSupported; 
DWRITE_FONT_FILE_TYPE fileType; 
UINT32 numberOfFonts; 
hr = pFontFile->Analyze(&isSupported, &fileType, /* face type */ nullptr, &numberOfFonts); 
```



O método [**Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) também definirá valores para os parâmetros IsSupported e filetype. Se o arquivo não for um formato com suporte, IsSupported será FALSE e a ação apropriada, como ignorar o arquivo, poderá ser executada.   
5. Execute o loop sobre o número de fontes definidas no parâmetro numberOfFonts. Dentro do loop, crie um [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) para cada par de arquivo/índice e adicione-o ao construtor de conjunto de fontes. 


```C++
for (uint32_t fontIndex = 0; fontIndex < numberOfFonts; fontIndex++) 
{ 
  IDWriteFontFaceReference* pFontFaceReference;
  hr = pDWriteFactory->CreateFontFaceReference(pFontFile, fontIndex, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);

  if (SUCCEEDED(hr))
  {
    hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference);
  }
} 
```



  
6. Depois que todas as faces tiverem sido adicionadas ao construtor de conjunto de fontes, crie o conjunto de fontes personalizadas, conforme mostrado acima.  
</dl>

um aplicativo pode ser projetado para que use o método [**addfontfile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) preferencial ao ser executado na Atualização do Windows 10 para Criadores, mas volte a usar o método [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) ao ser executado em versões anteriores do Windows 10. Teste a disponibilidade da interface [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) , conforme descrito acima, e, em seguida, Branche de acordo. essa abordagem é ilustrada no [exemplo DirectWrite conjuntos de fontes personalizadas](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). 

### <a name="creating-a-font-set-using-known-fonts-in-the-local-file-system"></a>Criando um conjunto de fontes usando fontes conhecidas no sistema de arquivos local

Conforme mencionado acima, cada referência de face de fonte em um conjunto de fontes está associada a determinadas propriedades informativas, como o nome da família e a espessura da fonte. Quando fontes personalizadas são adicionadas a um construtor de conjunto de fontes usando as chamadas de API listadas acima, essas propriedades informativas são obtidas diretamente dos dados reais da fonte, que são lidas à medida que a fonte é adicionada. Em algumas situações, no entanto, se um aplicativo tiver outra fonte de informações sobre uma fonte, talvez queira fornecer seus próprios valores personalizados para essas propriedades. 

Como um exemplo de como isso pode ser útil, suponha que um aplicativo agrupe algumas fontes que são usadas para apresentar elementos específicos da interface do usuário dentro do aplicativo. Às vezes, como com uma nova versão do aplicativo, as fontes específicas que o aplicativo usa para esses elementos podem precisar ser alteradas. Se o aplicativo tiver referências codificadas para as fontes específicas, a substituição de uma fonte por outra exigirá a alteração de cada uma dessas referências. Em vez disso, se o aplicativo usar propriedades personalizadas para atribuir aliases funcionais com base no tipo de elemento ou texto que está sendo renderizado, o mapeará cada alias para uma fonte específica em um único lugar e, em seguida, usará os aliases em todos os contextos onde as fontes são criadas e manipuladas e, em seguida, a substituição de uma fonte por outra requer apenas a alteração 

Valores personalizados para propriedades informativas podem ser atribuídos quando o método [**IDWriteFontSetBuilder:: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) é chamado. O método para fazer isso é o seguinte: isso pode ser usado em qualquer versão de Windows 10. 

Como mostrado acima, comece obtendo as interfaces [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) e [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) . Para cada face de fonte personalizada a ser adicionada, crie um [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference), como mostrado acima. Antes que isso seja adicionado ao construtor de conjunto de fontes (dentro do loop na etapa 5, mostrado acima), no entanto, o aplicativo define os valores de propriedade personalizada a serem usados. 

Um conjunto de valores de propriedade personalizada é definido usando uma matriz de estruturas de [**\_ \_ propriedade de fonte DWRITE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) . Cada um deles identifica uma determinada propriedade da enumeração [**de \_ \_ \_ ID da propriedade de fonte DWRITE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) e o valor de propriedade correspondente a ser usado.  

Observe que todos os valores de propriedade são atribuídos como cadeias de caracteres. Se eles podem ser exibidos posteriormente para os usuários, os valores alternativos para uma determinada propriedade para diferentes idiomas podem ser definidos, mas isso não é necessário. Observe também que, se qualquer valor de propriedade personalizada for definido pelo aplicativo, somente os valores especificados serão usados dentro do conjunto de fontes; DirectWrite não derivará nenhum valor diretamente da fonte para as propriedades informativas usadas em um conjunto de fontes. 

O exemplo a seguir define valores personalizados para três propriedades informativas: nome da família, nome completo e espessura da fonte. 


```C++
DWRITE_FONT_PROPERTY props[] = 
{ 
  { DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_FULL_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_WEIGHT, L"400", nullptr } 
}; 
               
            
```



Depois de definir a matriz desejada de valores de propriedade para uma fonte, faça uma chamada para AddFontFaceRefence, passando a matriz de propriedade, bem como a referência de face de fonte. 


```C++
hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference, props, ARRAYSIZE(props)); 
```



 

Depois que todas as faces de fontes personalizadas tiverem sido adicionadas ao construtor de conjunto de fontes, junto com suas propriedades personalizadas, crie o conjunto de fontes personalizadas, conforme mostrado acima. 

### <a name="creating-a-custom-font-set-using-known-remote-fonts-on-the-web"></a>Criar um conjunto de fontes personalizado usando fontes remotas conhecidas na Web

As propriedades personalizadas são importantes para trabalhar com fontes remotas. Cada referência de face de fonte deve ter algumas propriedades informativas para caracterizar a fonte e distingui-la de outras fontes. como os dados de fonte para fontes remotas não são locais, DirectWrite não pode derivar propriedades diretamente dos dados da fonte. Portanto, as propriedades devem ser fornecidas explicitamente ao adicionar uma fonte remota ao construtor de conjunto de fontes.

A sequência de chamadas à API para adicionar fontes remotas a um conjunto de fontes é semelhante à sequência descrita para o cenário anterior. No entanto, como os dados da fonte são remotos, as operações envolvidas na leitura dos dados reais da fonte serão diferentes do que ao trabalhar com arquivos no armazenamento local. para essa situação, uma nova interface de nível inferior, [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader), foi adicionada na Atualização do Windows 10 para Criadores. 

para usar o carregador de arquivo de fonte remoto, ele deve primeiro ser registrado com uma fábrica de DirectWrite. O carregador precisará ser mantido pelo aplicativo enquanto as fontes associadas a ele estiverem sendo usadas. Depois que as fontes não estiverem mais em uso e em algum momento antes que a fábrica seja destruída, o carregador deverá ter o registro cancelado. Isso pode ser feito no destruidor para a classe que possui o objeto Loader. Essas etapas serão mostradas abaixo. 

O método para criar um conjunto de fontes personalizado usando fontes remotas é o seguinte: isso requer o Atualização do Windows 10 para Criadores.  

<dl> 1. Crie uma interface IDWriteFactory5, conforme mostrado acima.   
2. Crie uma interface <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a> , conforme mostrado acima.   
3. Use a fábrica para obter um <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>. 


```C++
IDWriteRemoteFontFileLoader* pRemoteFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateHttpFontFileLoader( 
        /* referrerURL */ nullptr, 
        /* extraHeaders */ nullptr, 
        &pRemoteFontFileLoader 
    ); 
} 
```



Isso retorna uma implementação fornecida pelo sistema da interface do carregador de arquivo de fonte remoto que é capaz de lidar com as interações de HTTP para baixar dados de fonte em nome do aplicativo. Uma URL de referencial ou cabeçalhos extras podem ser especificados se exigido pelo serviço de fonte ou serviços que são a origem das fontes.    

> [!IMPORTANT]
> Observação de segurança: quando é feita uma tentativa de buscar uma fonte remota, o potencial existe para um invasor falsificar o servidor desejado que será chamado. Nesse caso, as URLs de destino e referenciador e os detalhes do cabeçalho seriam divulgados para o invasor. Os desenvolvedores de aplicativos são responsáveis por mitigar esse risco. O uso do protocolo HTTPS, em vez de HTTP, é recomendado. 

 

Um único carregador de arquivo de fonte remoto pode ser usado para várias fontes, embora carregadores diferentes possam ser usados se as fontes forem obtidas de vários serviços que têm requisitos diferentes para URL referencial ou cabeçalhos adicionais.   
4. Registre o carregador de arquivo de fonte remoto com a fábrica. 


```C++
 if (SUCCEEDED(hr)) 
 { 
     hr = pDWriteFactory->RegisterFontFileLoader(pRemoteFontFileLoader); 
 } 
```



A partir desse ponto, as etapas para criar o conjunto de fontes personalizadas são semelhantes àquelas descritas para arquivos de fontes locais conhecidos, com duas exceções importantes. Primeiro, o objeto [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) é criado usando a interface do carregador do arquivo de fonte remoto em vez de usar a fábrica. Em segundo lugar, o método Analyze não pode ser usado porque os dados da fonte não são locais. Em vez disso, o aplicativo deve saber se o arquivo de fonte remoto é um arquivo de coleção de fontes OpenType e, nesse caso, ele deve saber qual das fontes dentro da coleção será usada e o índice de cada um. Portanto, as etapas restantes são as seguintes.   
5. Para cada arquivo de fonte remota, use a interface do carregador de arquivo de fonte remota para criar [**um IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), especificando a URL necessária para acessar o arquivo de fonte. 


```C++
 IDWriteFontFile* pFontFile; 
 hr = pRemoteFontFileLoader->CreateFontFileReferenceFromUrl( 
     pDWriteFactory, 
     /* baseUrl */ L"https://github.com/", 
     /* fontFileUrl */ L"winjs/winjs/blob/master/src/fonts/Symbols.ttf?raw=true", 
     &pFontFile 
 ); 
```



Observe que a URL completa pode ser especificada no parâmetro fontFileUrl ou pode ser dividida em partes base e relativas. Se uma URL base for especificada, a concatenação dos valores baseUrl e fontFileUrl deverá fornecer a URL completa – DirectWrite não fornecerá nenhumlimiter adicional.  

> [!IMPORTANT]
> Observação de segurança/desempenho: quando é feita uma tentativa de buscar uma fonte remota, não há nenhuma garantia de Windows receberá uma resposta do servidor. Em alguns casos, um servidor pode responder com um erro de arquivo não encontrado para uma URL relativa inválida, mas parar de responder se receber várias solicitações inválidas. Se o servidor não responder, Windows acabará com o tempo de vida, embora isso possa levar vários minutos se várias buscas são iniciadas. Você deve fazer o que puder para garantir que as URLs sejam válidas quando as chamadas são feitas. 

 

Observe também que a URL pode apontar para um arquivo de fonte OpenType bruto (.ttf, .otf, .ttc, .otc), mas também pode apontar para fontes em um arquivo de contêiner WOFF ou WOFF2. Se um arquivo WOFF ou WOFF2 for referenciado, DirectWrite implementação do carregador de arquivos de fonte remota desempacotará automaticamente os dados de fonte do arquivo de contêiner.   
6. Para cada índice facial de fonte dentro do arquivo de fonte remoto que deve ser usado, crie [**um IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference). 


```C++
 IDWriteFontFaceReference* pFontFaceReference; 
 hr = pDWriteFactory->CreateFontFaceReference(pFontFile, /* faceIndex */ 0, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);
```



  
7. Defina propriedades personalizadas para o rosto da fonte, conforme mostrado acima.   
8. Adicione a referência de face da fonte juntamente com propriedades personalizadas ao construtor do conjunto de fontes, conforme mostrado acima.   
9. Depois que todas as fontes foram adicionadas ao construtor do conjunto de fontes, crie o conjunto de fontes, conforme mostrado acima.   
10. Em algum momento em que as fontes remotas não serão mais usadas, o registro do carregador de arquivo de fonte remota será feito. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pRemoteFontFileLoader); 
```



  
</dl>

Depois que um conjunto de fontes personalizado com fontes remotas personalizadas é criado, o conjunto de fontes contém referências e propriedades informativas para as fontes remotas, mas os dados reais ainda são remotos. DirectWrite suporte para fontes remotas permite que uma referência facial de fonte seja mantida no conjunto de fontes e para que uma fonte seja selecionada para uso no layout e na renderização, mas que os dados reais não sejam baixados até que haja uma necessidade real de usá-lo, como quando o layout de texto será executado.  

Um aplicativo pode usar uma abordagem mais direta solicitando que DirectWrite os dados da fonte e, em seguida, aguardando a confirmação de um download bem-sucedido antes que qualquer processamento com a fonte seja iniciado. Mas um download de rede implica alguma latência de duração imprevisível e o sucesso também é incerto. Por esse motivo, geralmente será melhor usar uma abordagem diferente, permitindo que o layout e a renderização sejam feitos inicialmente usando fontes alternativas ou de fallback que já são locais, ao solicitar o download da fonte remota desejada em paralelo e, em seguida, atualizar os resultados depois que a fonte desejada tiver sido baixada. 

Para solicitar que toda a fonte seja baixada antes de ser usada, o método [**IDWriteFontFaceReference::EnqueueFontDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) pode ser usado. Se a fonte for muito grande, somente uma parte dos dados poderá ser necessária para processar cadeias de caracteres específicas. DirectWrite fornece métodos adicionais que podem ser usados para solicitar partes dos dados de fonte necessários para conteúdo específico, [**EnqueueCharacterDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) e [**EnqueueGlyphDownloadRequest.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest)  

Suponha que a abordagem a ser tomada no aplicativo seja permitir que o processamento seja feito inicialmente usando fontes locais, alternativas ou de fallback. O método IDWriteFontFallback::[**MapCharacters**](idwritefontfallback-mapcharacters.md) pode ser usado para identificar fontes de fallback locais e também enquete automaticamente uma solicitação para baixar a fonte preferencial. Além disso, se [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) for usado e algum ou todo o texto no layout for formatado usando uma referência de fonte remota, o DirectWrite usará automaticamente o método **MapCharacters** para obter fontes de fallback locais e enxertar uma solicitação para baixar os dados de fonte remota. 

DirectWrite mantém uma fila de download de fonte para cada fábrica e as solicitações feitas usando os métodos mencionados acima são adicionadas a essa fila. A fila de download de fonte pode ser obtida usando o [**método IDWriteFactory3::GetFontDownloadQueue.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) 

Se uma solicitação de download for feita, mas os dados da fonte já estão locais, isso resultará em uma não operação: nada será adicionado à fila de download. Um aplicativo pode verificar se a fila está vazia ou se há solicitações de download pendentes chamando o método [**IDWriteFontDownloadQueue::IsEmpty.**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) 

Depois que as solicitações de fonte remotas foram adicionadas à fila, o processo de download deve ser iniciado. Quando fontes remotas são usadas em [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout), o download será iniciado automaticamente quando o aplicativo chamar métodos **IDWriteTextLayout** que forçam operações de layout ou renderização, como os métodos GetLineMetrics ou Draw. Em outros cenários, o aplicativo deve iniciar o download diretamente chamando [**IDWriteFontDownloadQueue::BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload).  

Quando um download for concluído, será necessário que o aplicativo tome as medidas apropriadas – continuar com operações pendentes ou repetir operações que foram feitas inicialmente com fontes de fallback. (Se DirectWrite layout de texto do DirectWrite estiver sendo usado, [**IDWriteTextLayout3::InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) poderá ser usado para limpar os resultados temporários calculados usando fontes de fallback.) Para que o aplicativo seja notificado quando o processo de download for concluído e tomar as ações apropriadas, o aplicativo deve fornecer uma implementação da interface [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) e passá-la para a chamada BeginDownload. 

> [!IMPORTANT]
> Observação de segurança/desempenho: quando é feita uma tentativa de buscar uma fonte remota, não há nenhuma garantia de Windows receberá uma resposta do servidor. Se o servidor não responder, Windows eventualmente passará do tempo, embora isso possa levar vários minutos se várias fontes remotas estão sendo buscadas, mas falhando. A chamada BeginDownload retornará imediatamente. Os aplicativos não devem bloquear a interface do usuário enquanto aguardam que [**IDWriteFontDownloadListener::D ownloadCompleted**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) seja chamado. 

 

As implementações de exemplo dessas interações com a fila de download de fonte do DirectWrite e com [a](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/)interface [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) podem ser vistas no exemplo conjuntos de fontes personalizados do DirectWrite e também no exemplo fontes baixáveis do [DirectWrite](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont). 

### <a name="creating-a-custom-font-set-using-font-data-loaded-into-memory"></a>Criando um conjunto de fontes personalizado usando dados de fonte carregados na memória

Assim como as operações de baixo nível para leitura de dados de um arquivo de fonte são diferentes para arquivos em um disco local versus arquivos remotos na Web, o mesmo também é verdadeiro para dados de fonte carregados em um buffer de memória. Uma nova interface de baixo nível para lidar com dados de fonte na memória foi adicionada no Atualização do Windows 10 para Criadores, [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader). 

Assim como com um carregador de arquivo de fonte remota, um carregador de arquivos de fonte na memória deve primeiro ser registrado com um DirectWrite factory. O carregador precisará ser mantido pelo aplicativo enquanto as fontes associadas a ele estão sendo usadas. Depois que as fontes não estão mais em uso e, em algum momento, antes que a fábrica seja destruída, o carregador deve ter o registro não feito. Isso pode ser feito no destruidor da classe que possui o objeto do carregador. Essas etapas serão mostradas abaixo. 

Se o aplicativo tiver informações separadas sobre as faces de fonte representadas pelos dados, ele poderá adicionar referências de face de fonte individuais a um construtor de conjunto de fontes com propriedades personalizadas especificadas. Como os dados da fonte estão na memória local, no entanto, isso não é necessário; DirectWrite poderá ler os dados diretamente para derivar os valores de propriedade. 

DirectWrite supõe que os dados da fonte estão no formato raw, OpenType, equivalente a um arquivo OpenType (.ttf, .otf, .ttc, .otc), mas na memória em vez de no disco. Os dados não podem estar em um formato de contêiner WOFF ou WOFF2. Os dados podem representar uma Coleção de Fontes OpenType. Se as propriedades personalizadas não estão sendo usadas, o método [**IDWriteFontSetBuilder1::AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) pode ser usado para adicionar todos os rostos de fonte nos dados em uma única chamada. 

Uma consideração importante para o cenário na memória é o tempo de vida dos dados. Se um ponteiro para o buffer for fornecido para DirectWrite sem uma indicação clara de que há um proprietário, o DirectWrite fará uma cópia dos dados em um novo buffer de memória que ele terá. Para evitar a cópia de dados e alocação de memória adicional, o aplicativo pode passar um objeto de proprietário de dados que implementa IUnknown e que possui o buffer de memória que contém os dados da fonte. Ao implementar essa interface, DirectWrite pode adicionar à contagem ref do objeto, garantindo assim o tempo de vida dos dados de propriedade. 

O método para criar um conjunto de fontes personalizado usando dados de fonte na memória é o seguinte; isso requer a Atualização do Windows 10 para Criadores. Isso assumirá um objeto de proprietário de dados implementado pelo aplicativo, que implementa IUnknown e também tem métodos que retornam um ponteiro para o buffer de memória e o tamanho do buffer. 

<dl> 1. Crie uma interface IDWriteFactory5, conforme mostrado acima.  
2. Crie uma [**interface IDWriteFontSetBuilder1,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) conforme mostrado acima.  
3. Use a fábrica para obter um IDWriteInMemoryFontFileLoader. 


```C++
 IDWriteInMemoryFontFileLoader* pInMemoryFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateInMemoryFontFileLoader(&pInMemoryFontFileLoader); 
}
```



Isso retorna uma implementação fornecida pelo sistema da interface do carregador de arquivo de fonte na memória.   
4. Registre o carregador de arquivo de fonte na memória com a fábrica. 


```C++
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->RegisterFontFileLoader(pInMemoryFontFileLoader); 
}
```



   
5. Para cada arquivo de fonte na memória, use o carregador de arquivo de fonte na memória para criar [**um IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile). 


```C++
IDWriteFontFile* pFontFile; 
hr = pInMemoryFontFileLoader->CreateInMemoryFontFileReference( 
    pDWriteFactory, 
    pFontDataOwner->fontData /* returns void* */, 
    pFontDataOwner->fontDataSize /* returns UINT32 */, 
    pFontDataOwner /* ownerObject, owns the memory with font data and implements IUknown */, 
    &pFontFile 
); 
```



   
6. Adicione o [**objeto IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) ao construtor do conjunto de fontes usando o [**método AddFontFile,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) conforme mostrado acima.  Se houver uma necessidade, o aplicativo poderá criar objetos [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) individuais com base no **IDWriteFontFile**, opcionalmente definir propriedades personalizadas para cada referência facial de fonte e, em seguida, adicionar a referência facial da fonte com propriedades personalizadas ao conjunto de fontes usando o método [**AddFontFaceReference,**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) conforme mostrado acima.   
7. Depois que todas as fontes foram adicionadas ao construtor do conjunto de fontes, crie o conjunto de fontes personalizado, conforme mostrado acima.   
8. Em algum momento, quando as fontes na memória não serão mais usadas, anulhe o carregador de arquivo de fonte na memória. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pInMemoryFontFileLoader);
```



  
</dl>

 

## <a name="advanced-scenarios"></a>Cenários avançados

Alguns aplicativos podem ter requisitos especiais que exigem processamento mais avançado do que o descrito acima. 

### <a name="combining-font-sets"></a>Combinando conjuntos de fontes

Alguns aplicativos talvez precisem criar um conjunto de fontes que compõe alguma combinação de itens de outros conjuntos de fontes. Por exemplo, um aplicativo pode querer criar um conjunto de fontes que combine todas as fontes instaladas no sistema com uma seleção de fontes personalizadas ou que combine fontes instaladas correspondentes a determinados critérios com outras fontes. DirectWrite tem APIs para dar suporte à manipulação e à combinação de conjuntos de fontes. 

Para combinar dois ou mais conjuntos de fontes, o método [**IDWriteFontSetBuilder::AddFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) adiciona todas as fontes em determinado conjunto de fontes a serem adicionadas a um construtor de conjunto de fontes em uma única chamada. Se apenas determinadas fontes de um conjunto de fontes existentes são procuradas no novo conjunto de fontes, o método [**IDWriteFontSet::GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) pode ser usado para derivar um novo objeto de conjunto de fontes que foi filtrado para incluir apenas fontes correspondentes às propriedades especificadas. Esses métodos fornecem uma maneira fácil de criar um conjunto de fontes personalizado combinando fontes de dois ou mais conjuntos de fontes existentes 

### <a name="using-local-woff-or-woff2-font-data"></a>Usando dados de fonte WOFF ou WOFF2 locais

Se um aplicativo tiver arquivos de fonte no sistema de arquivos local ou em um buffer de memória, mas usar os formatos de contêiner WOFF ou WOFF2, o DirectWrite (atualização do criador do Windows 10 ou posterior) fornece um método para desempacotar o formato de [**contêiner, IDWriteFactory5::UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile), que retorna [**um IDWriteFontFileStream.**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 

No entanto, o aplicativo precisará de uma maneira de obter [**o IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) em um objeto de carregador de arquivo de fonte. Uma maneira de fazer isso é criar uma implementação [**personalizada de IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) que envolve o fluxo. Assim como acontece com outros carregadores de arquivo de fonte, isso deve ser registrado antes do uso e ter o registro não registrado antes que a fábrica saia do escopo.  

Se o carregador personalizado também for usado com arquivos de fonte brutos (não empacotados), o aplicativo também precisará fornecer uma implementação personalizada da interface [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) para lidar com esses arquivos. No entanto, há maneiras mais fáceis de usar APIs discutidas acima para lidar com arquivos de fonte brutos. A necessidade de uma implementação de fluxo personalizado pode ser evitada usando caminhos de código separados para arquivos de fonte empacotados versus arquivos de fonte brutos. 

Depois que um objeto de carregador de arquivo de fonte personalizado é criado, os dados de arquivo de fonte empacotados são adicionados ao carregador por meios específicos do aplicativo. O carregador pode manipular vários arquivos de fonte, cada um deles identificado usando uma chave definida pelo aplicativo que é opaca para DirectWrite. Depois que um arquivo de fonte empacotado for adicionado ao carregador, o método [**IDWriteFactory::CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) será usado para obter [**um IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) com base nesse carregador para os dados de fonte identificados por uma determinada chave.  

A desempacotamento real dos dados da fonte pode ser feita à medida que as fontes são adicionadas ao carregador, mas também podem ser tratadas no método [**IDWriteFontFileLoader::CreateStreamFromKey,**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) que o DirectWrite chamará quando precisar ler os dados da fonte pela primeira vez. 

Depois que um objeto IDWriteFontFile tiver sido criado, as etapas restantes para adicionar as fontes a um conjunto de fontes personalizado serão conforme descrito acima. 

Uma implementação que usa essa abordagem é ilustrada no exemplo DirectWrite conjuntos de [fontes personalizados.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/) 

### <a name="using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation"></a>Usando DirectWrite de fonte remota com implementação de rede de baixo nível personalizada

Os mecanismos DirectWrite para lidar com fontes remotas podem ser divididos em mecanismos de nível superior – ter conjuntos de fontes que incluem referências de face de fonte para fontes remotas, verificar a localidade dos dados da fonte e gerenciar a fila para solicitações de download de fonte – e os mecanismos de nível inferior que manipulam o download real. Alguns aplicativos podem querer utilizar os mecanismos de fonte remota de nível superior, mas também exigem interações de rede personalizadas, como a comunicação com servidores que usam protocolos diferentes de HTTP. 

Para essa situação, um aplicativo precisará criar uma implementação personalizada da interface [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) que interage com outras interfaces de nível inferior das maneiras necessárias. O aplicativo também precisará fornecer implementações personalizadas dessas interfaces de nível inferior: [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream)e [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult). Essas três interfaces têm métodos de retorno de chamada que DirectWrite chamar durante as operações de download. 

Quando [**IDWriteFontDownloadQueue::BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) for chamado, o DirectWrite fará consultas ao carregador de arquivo de fonte remota sobre a localidade dos dados e solicitará o fluxo remoto. Se os dados não são locais, ele chamará o método BeginDownload do fluxo. A implementação do fluxo não deve bloquear essa chamada, mas deve retornar imediatamente, passando de volta um objeto [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) que fornece o identificador de espera que DirectWrite usará para aguardar a operação de download assíncrona. A implementação de fluxo personalizado é responsável por lidar com a comunicação remota. Quando o evento de conclusão tiver ocorrido, DirectWrite [**chamará IDWriteAsyncResult::GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) para determinar o resultado da operação. Se o resultado for bem-sucedido, espera-se que as chamadas subsequentes de ReadFragment para o fluxo para os intervalos baixados serão bem-sucedidas. 

> [!IMPORTANT]
> Observação de segurança/desempenho: quando é feita uma tentativa de buscar uma fonte remota, o potencial existe em geral para que um invasor espoque o servidor pretendido que está sendo chamado ou que o servidor não possa responder. Se você estiver implementando interações de rede personalizadas, poderá ter maior controle sobre mitigações do que ao lidar com servidores de terceiros. No entanto, você deve considerar as mitigações apropriadas para evitar a divulgação de informações ou negação de serviço. Protocolos seguros, como HTTPS, são recomendados. Além disso, você deve criar em algum tempoout para que o handle de evento retornado DirectWrite eventualmente seja definido. 

 

### <a name="supporting-scenarios-on-earlier-windows-versions"></a>Cenários de suporte em versões Windows anteriores

Os cenários descritos podem ter suporte no DirectWrite em versões anteriores do Windows, mas exigiriam uma implementação muito mais personalizada por parte do aplicativo usando as APIs mais limitadas disponíveis antes do Windows 10. Para obter mais informações, consulte [Coleções de fontes personalizadas (Windows 7/8)](custom-font-collections.md).

 

 