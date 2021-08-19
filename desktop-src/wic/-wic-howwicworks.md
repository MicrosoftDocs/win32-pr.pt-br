---
description: 'Saiba mais sobre: Como funciona o Windows de imagens'
ms.assetid: c233e25b-bec6-4e67-8fbf-2bf9b70c7522
title: Como funciona o Windows de imagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a63fe341bbb16afe78b159caa5c50c13fdb2cb8ee7a92f4c482dd03f8d9b8a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965105"
---
# <a name="how-the-windows-imaging-component-works"></a>Como funciona o Windows de imagens

Este tópico contém as seguintes seções:

-   [Descoberta e mediação](#discovery-and-arbitration)
-   [Decodificação](#decoding)
-   [Codificação](#encoding)
-   [O tempo de vida de um codec](#the-lifetime-of-a-codec)
-   [Como habilitar um Codec habilitado para WIC](#how-to-wic-enabled-a-codec)
-   [Suporte a apartments multi-threaded no WIC](#multi-threaded-apartment-support-in-wic)
-   [Tópicos relacionados](#related-topics)

## <a name="discovery-and-arbitration"></a>Descoberta e mediação

Antes que uma imagem possa ser decodificada, é necessário encontrar um codec apropriado que possa decodificar esse formato de imagem. Na maioria dos sistemas, como os formatos de imagem com suporte são codificados, nenhum processo de descoberta é necessário. Como a plataforma Windows WIC (componente de imagens) é extensível, é necessário ser capaz de identificar o formato de uma imagem e corresponder a ele com um codec apropriado.

Para dar suporte à descoberta em tempo de executar, cada formato de imagem deve ter um padrão de identificação que possa ser usado para identificar o decodificador apropriado para esse formato. (É altamente recomendável que, para novos formatos de arquivo, você use um GUID para o padrão de identificação, pois é garantido que ele seja exclusivo.) O padrão de identificação deve ser inserido em cada arquivo de imagem que esteja em conformidade com esse formato de imagem. Cada decodificador tem uma entrada do Registro que especifica o padrão de identificação ou os padrões dos formatos de imagem que ele pode decodificar. Quando um aplicativo precisa abrir uma imagem, ele solicita um decodificador do WIC. O WIC procura os decodificadores disponíveis no Registro e verifica cada entrada do Registro em busca de um padrão de identificação que corresponde ao padrão inserido no arquivo de imagem. Para obter mais informações sobre entradas do Registro do Decodificador, consulte Entradas do Registro [específicas do codificador](-wic-decoderregentries.md)

Quando o WIC encontra um único decodificador que corresponde ao padrão de identificação na imagem, ele cria uma instância do decodificador e passa o arquivo de imagem para ela. Se o WIC encontrar mais de uma correspondência, ele invocará um método chamado [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) em cada decodificador correspondente para que ele seja arbitrário e encontre a melhor correspondência. Para obter mais informações, consulte [a seção QueryCapabilities](-wic-imp-iwicbitmapdecoder.md) em [Implementando IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

## <a name="decoding"></a>Decodificação

Depois que o decodificador apropriado tiver sido selecionado e instautado, o aplicativo se fala diretamente com o decodificador. O decodificador tem várias responsabilidades, que ele implementa por meio de várias interfaces. Esses serviços podem ser classificados como:

-   Serviços de nível de contêiner
-   Serviços no nível do quadro
-   Serviços de enumeração de metadados
-   Transformaçãos nativas do decodificador
-   Notificações de progresso e suporte ao cancelamento
-   Serviços de processamento brutos

Os serviços de nível de contêiner incluem a recuperação da miniatura de nível superior (se há suporte), versão prévia, contextos de cores, paleta (se aplicável) e formato de contêiner, bem como o fornecimento de acesso aos quadros de imagem individuais dentro do contêiner. (Alguns contêineres contêm apenas um único quadro, enquanto outros, como TIFF (Formato de Arquivo de Imagem Marcada), podem conter vários quadros.) Esse conjunto de serviços também inclui o fornecimento de informações sobre o próprio decodificador e seus recursos em relação a um arquivo de imagem específico.

Quadros individuais têm suas próprias miniaturas e também podem ter seus próprios contextos de cores, paletas e outras propriedades, que são expostas no nível do quadro. No entanto, a operação mais importante executada no nível do quadro é a decodificação real dos bits de imagem para esse quadro.

O WIC fornece leitores de metadados para os formatos de metadados mais comuns (IFD, EXIF, IPTC, XMP, APP0, APP1 e outros formatos) e também dá suporte à extensibilidade para formatos de metadados de terceiros. Isso libera o codec da responsabilidade de analisar metadados. No entanto, o codec é responsável por enumerar os blocos de metadados e solicitar um leitor de metadados para cada bloco. O WIC executa a descoberta para manipuladores de metadados da mesma maneira que faz para codecs, com base em um padrão no header de bloco que corresponde a um padrão na entrada do registro do manipulador de metadados. Para obter mais informações, consulte As Entradas do Registro [específicas do codificador](-wic-decoderregentries.md)

Os decodificadores não são necessários para dar suporte nativo a operações de transformação, mas isso permite otimizações de desempenho significativas que fornecem uma melhor experiência do usuário final. Por exemplo, um aplicativo pode criar um pipeline de várias transformação (dimensionamento, corte, rotação e conversão de formato de pixel) para executar em uma imagem antes que a imagem seja renderizada. Para obter mais informações sobre como transformar pipelines, consulte [IWICBitmapSource](-wic-imp-iwicbitmapsource.md). Depois de criar um pipeline de transformação, o aplicativo solicita a transformação final no pipeline para produzir o bitmap que resulta da aplicação de todas as transformaçãos à origem da imagem. Nesse ponto, se o decodificador em si for capaz de executar operações de transformação, o WIC perguntará qual das transformaçãos solicitadas ele pode executar. As transformaçãos solicitadas que o decodificador não puder executar serão executadas pelo WIC na imagem decodificada antes de retorá-la ao chamador. Esse pipeline de transformação otimizado fornece melhor desempenho do que executar cada transformação sequencialmente na memória, especialmente quando algumas ou todas as transformaçãos podem ser realizadas durante o processo de decodificação.

As notificações de progresso e o suporte ao cancelamento permitem que um aplicativo solicite notificações de progresso para operações demoradas e também permita que o aplicativo dê ao usuário a oportunidade de cancelar uma operação que está demorando muito. Isso é importante porque, se um usuário não puder cancelar uma operação, ele poderá sentir que o processo foi suspenso e tentar cancelá-lo fechando o aplicativo.

Essas interfaces são descritas em detalhes na seção sobre Como [implementar um WIC-Enabled decodificador](-wic-implementingwicdecoder.md).

Os serviços de processamento bruto incluem o ajuste das configurações da câmera, como exposição, contraste e ajuste, ou alteração do espaço de cores antes de processar os bits brutos.

## <a name="encoding"></a>Codificação

Assim como os decodificadores, os codificadores têm responsabilidades que implementam por meio de interfaces. Os serviços que os codificadores fornecem são complementares aos serviços fornecidos pelos decodificadores, exceto que eles escrevem dados de imagem em vez de lê-los. Os codificadores também fornecem serviços nas seguintes categorias:

-   Serviços de nível de contêiner
-   Serviços no nível do quadro
-   Enumeração de metadados e serviços de atualização
-   Notificação de progresso e suporte ao cancelamento

Os serviços de nível de contêiner para um codificador incluem a configuração da miniatura de nível superior (se há suporte), a visualização e a paleta (se aplicável) e a iteração por meio dos quadros de imagem individuais para que possam ser serializados no contêiner.

Os serviços em nível de quadro para um codificador espelham aqueles para o decodificador, exceto que eles escrevem os dados da imagem, a miniatura e qualquer paleta associada ou outro componente, em vez de lê-los.

Além disso, os serviços de enumeração de metadados para um codificador incluem a iteração pelos blocos de metadados a serem gravados e a invocação dos autores de metadados apropriados para serializar os metadados no disco.

Essas interfaces são descritas em detalhes na seção sobre [Implementando um codificador WIC-Enabled .](-wic-implementingwicencoder.md)

## <a name="the-lifetime-of-a-codec"></a>O tempo de vida de um codec

Um codec do WIC é instautado para lidar com uma única imagem e geralmente tem um tempo de vida curto. Ele é criado quando uma imagem é carregada e é liberada quando a imagem é fechada. Um aplicativo pode usar um grande número de codecs simultaneamente com tempos de vida sobrepostos (pense em rolar por um diretório que contém centenas de imagens) e vários aplicativos podem estar fazendo isso ao mesmo tempo.

Embora alguns codecs tenham um tempo de vida com escopo para o tempo de vida do processo em que eles estão, esse não é o caso com codecs WIC. O Windows Vista Galeria de Fotos, Windows Explorer e Visualizador de Fotos, bem como vários outros aplicativos, são construídos no WIC e usarão seu codec para exibir imagens e miniaturas. Se o tempo de vida do codec tiver como escopo o tempo de vida do processo, sempre que uma imagem ou miniatura for exibida no Windows Vista Explorer, o codec instaurou para decodificar essa imagem permaneceria na memória até a próxima vez que o usuário reiniciasse seu computador. Se o codec nunca for descarregado, seus recursos serão, na verdade, "vazados" porque não podem ser usados por nenhum outro componente no sistema.

## <a name="how-to-wic-enabled-a-codec"></a>Como habilitar um Codec habilitado para WIC

1.  Implemente uma classe de decodificador no nível do contêiner e uma classe de decodificador no nível do quadro que expõe as interfaces WIC necessárias para decodificar imagens e iterar por meio de blocos de metadados. Isso permite que todos os aplicativos baseados em WIC interajam com seu codec da mesma maneira que interagem com formatos de imagem padrão.
2.  Implemente uma classe de codificador no nível de contêiner e uma classe de codificador no nível do quadro que expõe as interfaces WIC necessárias para codificar imagens e serializar blocos de metadados em um arquivo de imagem.
3.  Se o formato de contêiner não for baseado em um contêiner TIFF ou JPEG, talvez seja necessário escrever manipuladores de metadados para os formatos de metadados comuns (EXIF, XMP). No entanto, se você usar um formato de contêiner baseado em TIFF ou JPEG, isso não será necessário porque você pode delegar aos manipuladores de metadados fornecidos pelo sistema.
4.  Inserir um padrão de identificação exclusivo (recomendamos um GUID) em todos os arquivos de imagem. Isso permite que o formato de imagem seja corresponder ao codec durante a descoberta. Se você estiver escrevendo um wrapper WIC para um formato de imagem existente, deverá encontrar um padrão de bits que o codificador sempre grava em seus arquivos de imagem exclusivos para esse formato de imagem e usá-lo como o padrão de identificação.)
5.  Registre seu codec no momento da instalação. Isso permite que seu codec seja descoberto em tempo de executar correspondendo o padrão de identificação no Registro com o padrão inserido no arquivo de imagem.
6.  A partir Windows 7, o WIC exige que os codecs sejam do tipo de apartment COM "Both". Isso significa que você deve fazer o bloqueio apropriado para lidar com chamadores e chamadores entre apartments em cenários de vários threads. Para obter mais informações, consulte a próxima seção sobre suporte a apartments multi-threaded.
7.  Suporte para plataformas de 64 bits: para o Windows 7, o WIC exigirá que os codecs WIC de terceiros sejam entregues como binários nativos de 32 bits e 64 bits. Além disso, o formulário de 32 bits deve ser instalado e executado em sistemas de 64 bits, e o instalador de codec do Windows 7 de terceiros deve instalar os binários de 32 bits e 64 bits em sistemas de 64 bits.

## <a name="multi-threaded-apartment-support-in-wic"></a>Suporte a apartments multi-threaded no WIC

Objetos dentro de um MTA (Multi-Threaded Apartment) podem ser chamados simultaneamente por qualquer número de threads dentro do MTA. Isso permite um melhor desempenho em sistemas de vários núcleos e em determinados cenários de servidor. Além disso, os codecs do WIC em um MTA podem chamar outros objetos no MTA sem o custo de marshaling associado à chamada entre threads em diferentes apartments STA. No Windows 7, todos os codecs WIC in-box foram atualizados para dar suporte a MTAs, incluindo JPEG, TIFF, PNG, GIF, ICO e BMP. É altamente recomendável que codecs de terceiros sejam gravados para dar suporte a MTAs. Codecs de terceiros que não suportam MTAs causam custos significativos de desempenho em aplicativos multi-threaded devido ao marshaling. A habilitação do suporte ao MTA requer que a sincronização adequada seja implementada no codec de terceiros. A implementação exata dessas técnicas de sincronização está além do escopo deste artigo. Para obter mais informações sobre como sincronizar objetos COM, consulte [Noções básicas e uso de modelos de threading COM.](/previous-versions/ms809971(v=msdn.10))

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Introdução (Como escrever uma WIC-Enabled CODEC)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Implementando um WIC-Enabled decodificador](-wic-implementingwicdecoder.md)
</dt> <dt>

[Como escrever um codec WIC-Enabled código](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Visão geral do componente de imagens](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Visão geral dos metadados do WIC](-wic-about-metadata.md)
</dt> </dl>

 

 



