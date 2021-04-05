---
description: 'Saiba mais sobre: como funciona o Windows Imaging Component'
ms.assetid: c233e25b-bec6-4e67-8fbf-2bf9b70c7522
title: Como funciona o Windows Imaging Component
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc9fe31ae4346f2c2d1f0b273e78ed10a0ec7e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662600"
---
# <a name="how-the-windows-imaging-component-works"></a>Como funciona o Windows Imaging Component

Este tópico contém as seguintes seções:

-   [Descoberta e arbitragem](#discovery-and-arbitration)
-   [Decodificação](#decoding)
-   [Codificação](#encoding)
-   [O tempo de vida de um codec](#the-lifetime-of-a-codec)
-   [Como habilitar um codec por WIC](#how-to-wic-enabled-a-codec)
-   [Suporte a multi-threaded apartment no WIC](#multi-threaded-apartment-support-in-wic)
-   [Tópicos relacionados](#related-topics)

## <a name="discovery-and-arbitration"></a>Descoberta e arbitragem

Antes que uma imagem possa ser decodificada, é necessário encontrar um codec apropriado que possa decodificar esse formato de imagem. Na maioria dos sistemas, como os formatos de imagem com suporte são embutidos em código, nenhum processo de descoberta é necessário. Como a plataforma do Windows Imaging Component (WIC) é extensível, é necessário poder identificar o formato de uma imagem e fazer a correspondência com um codec apropriado.

Para dar suporte à descoberta de tempo de execução, cada formato de imagem deve ter um padrão de identificação que possa ser usado para identificar o decodificador apropriado para esse formato. (É altamente recomendável que, para novos formatos de arquivo, você use um GUID para o padrão de identificação, porque é garantido que ele seja exclusivo.) O padrão de identificação deve ser inserido em cada arquivo de imagem que esteja de acordo com esse formato de imagem. Cada decodificador tem uma entrada de registro que especifica o padrão de identificação ou padrões dos formatos de imagem que pode decodificar. Quando um aplicativo precisa abrir uma imagem, ele solicita um decodificador do WIC. O WIC pesquisa os decodificadores disponíveis no registro e verifica cada entrada do registro em busca de um padrão de identificação que corresponda ao padrão inserido no arquivo de imagem. Para obter mais informações sobre entradas de registro de decodificador, consulte [entradas de registro específicas do codificador](-wic-decoderregentries.md)

Quando o WIC encontra um único decodificador que corresponde ao padrão de identificação na imagem, ele cria uma instância do decodificador e passa o arquivo de imagem para ele. Se o WIC encontrar mais de uma correspondência, ele invocará um método chamado [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) em cada decodificador correspondente para arbitrar entre eles e encontrará a melhor correspondência. Para obter mais informações, consulte a seção [QueryCapabilities](-wic-imp-iwicbitmapdecoder.md) em [Implementing IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

## <a name="decoding"></a>Decodificação

Depois que o decodificador apropriado tiver sido selecionado e instanciado, o aplicativo se comunica diretamente com o decodificador. O decodificador tem várias responsabilidades, que ele implementa por meio de várias interfaces. Esses serviços podem ser classificados como:

-   Serviços de nível de contêiner
-   Serviços de nível de quadro
-   Serviços de enumeração de metadados
-   Transformações de decodificador nativo
-   Notificações de progresso e suporte ao cancelamento
-   Serviços de processamento bruto

Os serviços de nível de contêiner incluem a recuperação da miniatura de nível superior (se houver suporte), visualização, contextos de cor, paleta (se aplicável) e formato de contêiner, além de fornecer acesso aos quadros de imagem individuais no contêiner. (Alguns contêineres contêm apenas um único quadro, enquanto outros, como TIFF, podem conter vários quadros.) Esse conjunto de serviços também inclui fornecer informações sobre o próprio decodificador e seus recursos em relação a um arquivo de imagem específico.

Quadros individuais têm suas próprias miniaturas e também podem ter seus próprios contextos de cor, paletas e outras propriedades, que são expostos no nível do quadro. No entanto, a operação mais importante executada no nível de quadro é a decodificação real dos bits de imagem para esse quadro.

O WIC fornece leitores de metadados para os formatos de metadados mais comuns (IFD, EXIF, IPTC, XMP, APP0, APP1 e outros formatos) e também oferece suporte a extensibilidade para formatos de metadados de terceiros. Isso libera o codec da responsabilidade de análise de metadados. No entanto, o codec é responsável por enumerar os blocos de metadados e solicitar um leitor de metadados para cada bloco. O WIC executa a descoberta de manipuladores de metadados da mesma maneira que faz para codecs, com base em um padrão no cabeçalho de bloco que corresponde a um padrão na entrada de registro do manipulador de metadados. Para obter mais informações, consulte as [entradas de registro específicas do codificador](-wic-decoderregentries.md)

Os decodificadores não são necessários para dar suporte nativo a operações de transformação, mas isso permite otimizações de desempenho significativas que fornecem uma melhor experiência do usuário final. Por exemplo, um aplicativo pode criar um pipeline de várias transformações (dimensionamento, corte, rotação e conversão de formato de pixel) para executar em uma imagem antes que a imagem seja renderizada. Para obter mais informações sobre pipelines de transformação, consulte [IWICBitmapSource](-wic-imp-iwicbitmapsource.md). Depois de criar um pipeline de transformação, o aplicativo solicita a transformação final no pipeline para produzir o bitmap resultante da aplicação de todas as transformações à origem da imagem. Nesse ponto, se o próprio decodificador for capaz de executar operações de transformação, o WIC perguntará quais das transformações solicitadas ele pode executar. Todas as transformações solicitadas que o decodificador não pode executar serão executadas pelo WIC na imagem decodificada antes de retorná-la ao chamador. Esse pipeline de transformação otimizado fornece melhor desempenho do que executar cada transformação sequencialmente na memória, especialmente quando algumas ou todas as transformações podem ser realizadas durante o processo de decodificação.

As notificações de progresso e o suporte ao cancelamento permitem que um aplicativo solicite notificações de progresso para operações demoradas e também permite que o usuário dê uma oportunidade para cancelar uma operação que está demorando muito. Isso é importante porque, se um usuário não puder cancelar uma operação, ele poderá sentir que o processo foi suspenso e tentar cancelá-lo fechando o aplicativo.

Essas interfaces são descritas em detalhes na seção sobre como [implementar um decodificador de WIC-Enabled](-wic-implementingwicdecoder.md).

Os serviços de processamento bruto incluem o ajuste das configurações da câmera, como exposição, contraste e nitidez, ou a alteração do espaço de cores antes de processar os bits brutos.

## <a name="encoding"></a>Codificação

Como os decodificadores, os codificadores têm responsabilidades que eles implementam por meio de interfaces. Os serviços que os codificadores fornecem são complementares aos serviços fornecidos pelos decodificadores, exceto pelo fato de eles gravarem dados de imagem em vez de lê-los. Os codificadores também fornecem serviços nas seguintes categorias:

-   Serviços de nível de contêiner
-   Serviços de nível de quadro
-   Serviços de enumeração e atualização de metadados
-   Notificação de progresso e suporte ao cancelamento

Os serviços de nível de contêiner para um codificador incluem a definição da miniatura de nível superior (se houver suporte), a visualização e a paleta (se aplicável) e a iteração por meio de quadros de imagem individuais para que eles possam ser serializados no contêiner.

Os serviços de nível de quadro para um codificador espelham aqueles para o decodificador, exceto que eles gravam os dados da imagem, a miniatura e qualquer paleta associada ou outro componente, em vez de lê-los.

Além disso, os serviços de enumeração de metadados para um codificador incluem a iteração através dos blocos de metadados a serem gravados e a invocação dos gravadores de metadados apropriados para serializar os metadados no disco.

Essas interfaces são descritas em detalhes na seção sobre como [implementar um codificador de WIC-Enabled](-wic-implementingwicencoder.md).

## <a name="the-lifetime-of-a-codec"></a>O tempo de vida de um codec

Um codec do WIC é instanciado para lidar com uma única imagem e geralmente tem um tempo de vida curto. Ele é criado quando uma imagem é carregada e liberada quando a imagem é fechada. Um aplicativo pode usar um grande número de codecs simultaneamente com tempos de vida sobrepostos (imagine a rolagem por meio de um diretório contendo centenas de imagens) e vários aplicativos podem estar fazendo isso ao mesmo tempo.

Embora alguns codecs tenham um tempo de vida definido para o tempo de vida do processo no qual residem, esse não é o caso dos codecs do WIC. A Galeria de fotos do Windows Vista, o Windows Explorer e o Visualizador de fotos, bem como vários outros aplicativos, se baseiam no WIC e usarão seu codec para exibir imagens e miniaturas. Se o tempo de vida do seu codec estivesse no escopo da vida útil do processo, sempre que uma imagem ou miniatura fosse exibida no Windows Vista Explorer, o codec instanciado para decodificar essa imagem permaneceria na memória até a próxima vez que o usuário reiniciou seu computador. Se o codec nunca for descarregado, seus recursos estarão, em vigor, "vazados" porque não podem ser usados por nenhum outro componente no sistema.

## <a name="how-to-wic-enabled-a-codec"></a>Como habilitar um codec por WIC

1.  Implemente uma classe de decodificador de nível de contêiner e uma classe de decodificador de nível de quadro que expõe as interfaces WIC necessárias para decodificar imagens e iterar por meio de blocos de metadados. Isso permite que todos os aplicativos baseados em WIC interajam com o codec da mesma maneira que interagem com formatos de imagem padrão.
2.  Implemente uma classe de codificador de nível de contêiner e uma classe de codificador de nível de quadro que exponha as interfaces WIC necessárias para codificar imagens e serializar blocos de metadados em um arquivo de imagem.
3.  Se o formato do contêiner não for baseado em um contêiner TIFF ou JPEG, talvez seja necessário gravar manipuladores de metadados para os formatos de metadados comuns (EXIF, XMP). No entanto, se você usar um formato de contêiner baseado em TIFF ou JPEG, isso não é necessário porque você pode delegar aos manipuladores de metadados fornecidos pelo sistema.
4.  Insira um padrão de identificação exclusivo (recomendamos um GUID) em todos os arquivos de imagem. Isso permite que seu formato de imagem seja correspondido em relação ao seu codec durante a descoberta. Se você estiver escrevendo um wrapper de WIC para um formato de imagem existente, deverá encontrar um padrão de bits que o codificador sempre grava em seus arquivos de imagem que sejam exclusivos desse formato de imagem e usá-lo como o padrão de identificação.)
5.  Registre seu codec no momento da instalação. Isso permite que o codec seja descoberto em tempo de execução, combinando o padrão de identificação no registro com o padrão inserido no arquivo de imagem.
6.  A partir do Windows 7, o WIC exige que os codecs sejam do tipo apartment COM "both". Isso significa que você deve fazer o bloqueio apropriado para lidar com chamadores entre apartamento e chamadores em cenários multi-threaded. Para obter mais informações, consulte a próxima seção sobre o suporte a multi-threaded apartment.
7.  Suporte para plataformas de 64 bits: para o Windows 7, o WIC exigirá que os codecs de WIC de terceiros sejam entregues como binários nativos de 32 bits e de 64 bits. Além disso, o formato de 32 bits deve ser instalado e executado em sistemas de 64 bits, e o instalador de codecs do Windows 7 de terceiros deve instalar os binários de 32 bits e de 64 bits em sistemas de bits de 64.

## <a name="multi-threaded-apartment-support-in-wic"></a>Suporte a multi-threaded apartment no WIC

Os objetos em um multi-threaded apartment (MTA) podem ser chamados simultaneamente por qualquer número de threads dentro do MTA. Isso permite um melhor desempenho em sistemas de vários núcleos e em determinados cenários de servidor. Além disso, os codecs do WIC em um MTA podem chamar outros objetos no MTA sem o custo de Marshalling associado à chamada entre threads em apartments STA diferentes. No Windows 7, todos os codecs de WIC na caixa foram atualizados para dar suporte a MTAs, incluindo JPEG, TIFF, PNG, GIF, ICO e BMP. É altamente recomendável que os codecs de terceiros sejam escritos para dar suporte a MTAs. Os codecs de terceiros que não oferecem suporte a MTAs causam custos de desempenho significativos em aplicativos multi-threaded devido ao marshaling. Habilitar o suporte ao MTA requer que a sincronização adequada seja implementada no codec de terceiros. A implementação exata dessas técnicas de sincronização está além do escopo deste documento. Para obter mais informações sobre a sincronização de objetos COM, consulte [compreendendo e usando modelos de THREADING com](/previous-versions/ms809971(v=msdn.10)).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Introdução (como escrever um CODEC de WIC-Enabled)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Implementando um decodificador de WIC-Enabled](-wic-implementingwicdecoder.md)
</dt> <dt>

[Como escrever um CODEC de WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Visão geral do Windows Imaging Component](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral dos metadados do WIC](-wic-about-metadata.md)
</dt> </dl>

 

 



