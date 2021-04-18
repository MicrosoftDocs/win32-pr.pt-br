---
description: Tipos de mídia DMO
ms.assetid: 40958e12-09c7-4ce5-aa4d-5ed8b1f40aa3
title: Tipos de mídia DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1997abb1cc3c8eb10301778982ef7a46690855ed
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506360"
---
# <a name="dmo-media-types"></a>Tipos de mídia DMO

Um tipo de mídia descreve o formato associado a um fluxo de dados de mídia. Este artigo descreve como o DMOs lida com tipos de mídia. Ele destina-se principalmente a desenvolvedores que estão escrevendo seu próprio DMOs personalizado.

Os tipos de mídia são definidos usando a estrutura do [**\_ \_ tipo de mídia DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Essa estrutura inclui as seguintes informações:

-   O *tipo principal* é um GUID (identificador global exclusivo) que define uma categoria ampla, como áudio ou vídeo.
-   O *subtipo* é um GUID que define aspectos mais específicos do tipo. Por exemplo, no vídeo, os subtipos incluem RGB de 16 bits, RGB de 24 bits, UYVY, vídeo codificado por DV e assim por diante.
-   O *bloco de formato* é uma estrutura secundária que especifica totalmente o formato. O layout do bloco de formato depende do tipo de dados. Por exemplo, o áudio PCM usa a estrutura **WAVEFORMATEX** . O vídeo usa várias outras estruturas, incluindo **VIDEOINFOHEADER** e **VIDEOINFOHEADER2**. O layout do bloco de formato é identificado por um GUID de tipo de formato. Por exemplo, FORMAT \_ WaveFormatEx especifica uma estrutura **WaveFormatEx** .

Quando um DMO é criado pela primeira vez, os fluxos não têm um tipo de mídia. Antes que o DMO possa processar quaisquer dados, o cliente deve definir um tipo de mídia para cada fluxo. Esse processo é descrito da perspectiva do cliente na [definição de tipos de mídia em um DMO](setting-media-types-on-a-dmo.md).

**Tipos de mídia no registro**

Um DMO pode adicionar uma lista de tipos de mídia que ele dá suporte ao registro, chamando a função [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) . Um aplicativo pode usar essas informações para procurar DMOs que correspondam a um formato específico. As informações no registro não devem ser abrangentes. Normalmente, você deve incluir apenas os tipos principais aos quais o DMO dá suporte. A entrada do registro tem chaves separadas para tipos de entrada e saída, mas não faz distinção entre fluxos individuais.

A função **DMORegister** usa a estrutura de [**\_ \_ MediaType parcial do DMO**](/previous-versions/windows/desktop/api/Dmoreg/ns-dmoreg-dmo_partial_mediatype) para descrever os tipos de mídia. Essa estrutura contém um subconjunto das informações encontradas na estrutura **do \_ \_ tipo de mídia DMO** , ou seja, o tipo principal e o subtipo. Ele não inclui um bloco de formato, porque o bloco de formato normalmente contém informações que são muito granulares para serem incluídas no registro, como a altura e a largura de uma imagem de vídeo.

**Tipos de mídia preferenciais**

Depois que o aplicativo tiver criado um DMO, ele poderá consultar o DMO para os tipos de mídia aos quais ele dá suporte. Para cada fluxo, o DMO cria uma lista de tipos de mídia (possivelmente vazio), classificados em ordem de preferência. Os métodos [**IMediaObject:: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) e [**IMediaObject:: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) enumeram os tipos preferenciais. Os tipos preferenciais de um fluxo podem ser alterados dinamicamente quando o aplicativo define os tipos de mídia em outros fluxos. Por exemplo, a lista de tipos de saída preferenciais pode mudar depois que o tipo de entrada é definido, ou vice-versa. No entanto, o DMO não é necessário para atualizar seus tipos preferenciais dinamicamente. O aplicativo não pode pressupor que todos os tipos recebidos são válidos. Por esse motivo, os métodos [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) são compatíveis com um sinalizador para testar um tipo específico.

Os métodos **GetInputType** e **GetOutputType** retornam uma estrutura **de \_ \_ tipo de mídia DMO** . O DMO pode deixar algumas das informações nessa estrutura em branco, para indicar um intervalo de tipos. O tipo ou subtipo principal pode ser \_ NULL GUID e o bloco de formato pode estar vazio (zero bytes). Se o bloco de formato estiver vazio, o tipo de formato deverá ser \_ NULL GUID.

Depois que o aplicativo define todos os tipos de entrada de DMO, o DMO geralmente deve retornar pelo menos um tipo completo para cada fluxo de saída. Um tipo de saída completo facilita os testes, e os aplicativos podem usá-lo como um padrão razoável. O aplicativo de teste do DMO depende desse comportamento. (Consulte [usando o aplicativo DMOTest](using-the-dmotest-application.md).)

**Definindo os tipos de mídia**

Os aplicativos usam os métodos **SetInputType** e **SetOutputType** para testar, definir ou limpar os tipos em um fluxo especificado. O aplicativo deve especificar totalmente o tipo. O DMO verifica se ele pode aceitar o tipo proposto. A resposta pode depender de quais tipos foram definidos em outros fluxos. O \_ sinalizador de \_ limpeza Set TYPEF do DMO limpa o \_ tipo de um fluxo, portanto, o aplicativo pode "fazer backup" e tentar outra combinação.

**Cenários de exemplo**

Os exemplos a seguir descrevem alguns cenários típicos, para ilustrar os pontos feitos nas seções anteriores.

-   **Decodificadores de vídeo.** Em um decodificador de vídeo típico, o tipo de entrada determina parcialmente o tipo de saída. Por exemplo, geralmente ambos os fluxos devem ter a mesma taxa de quadros e dimensões de imagem. Uma opção não define nenhum tipo de saída preferencial até que o tipo de entrada seja definido. Outra opção é enumerar um conjunto de tipos incompletos, omitindo o bloco de formato. Use o subtipo para indicar os tipos descompactados com suporte, como RGB de 16 bits, RGB de 24 bits e assim por diante. Além disso, os decodificadores de vídeo geralmente não dão suporte à definição do tipo de saída antes do tipo de entrada. O cenário usual é decodificar de um formato de entrada conhecido, portanto, essa limitação é razoável.
-   **Decodificadores de áudio.** Um decodificador de áudio pode dar suporte a um conjunto fixo limitado de formatos de saída. Nesse caso, talvez seja possível criar uma lista de formatos de saída preferenciais antes que o formato de entrada seja conhecido.
-   **Compactadores.** Na maioria dos casos, um compressor de vídeo não pode especificar totalmente seus formatos de saída preferenciais até que o aplicativo defina o formato de entrada e vice-versa. Em vez disso, o DMO deve retornar um tipo incompleto sem nenhum bloco de formato. Para a compactação de áudio e vídeo, o aplicativo geralmente precisa definir vários parâmetros de saída, como a taxa de bits. No entanto, depois que o tipo de entrada é definido, o compressor deve retornar pelo menos um tipo de saída completo, pelos motivos mencionados anteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo um DMO](writing-a-dmo.md)
</dt> </dl>

 

 



