---
description: DMO Tipos de mídia
ms.assetid: 40958e12-09c7-4ce5-aa4d-5ed8b1f40aa3
title: DMO Tipos de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d67be6775163695189c2dc2c2742f65bcd0181032d9935b2a2a3ce2df2e900
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016124"
---
# <a name="dmo-media-types"></a>DMO Tipos de mídia

Um tipo de mídia descreve o formato associado a um fluxo de dados de mídia. Este artigo descreve como os DMOs lidam com tipos de mídia. Ele destina-se principalmente a desenvolvedores que estão escrevendo seus próprios DMOs personalizados.

Os tipos de mídia são definidos usando [**a estrutura DMO MEDIA \_ \_ TYPE.**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) Essa estrutura inclui as seguintes informações:

-   O *tipo principal* é um GUID (identificador global exclusivo) que define uma categoria ampla, como áudio ou vídeo.
-   O *subtipo* é um GUID que define aspectos mais específicos do tipo. Por exemplo, em vídeo, os subtipos incluem RGB de 16 bits, RGB de 24 bits, UYVY, vídeo codificado em DV e assim por diante.
-   O *bloco de* formato é uma estrutura secundária que especifica totalmente o formato. O layout do bloco de formato depende do tipo de dados. Por exemplo, o áudio PCM usa a **estrutura WAVEFORMATEX.** O vídeo usa várias outras estruturas, incluindo **VIDEOINFOHEADER** **e VIDEOINFOHEADER2.** O layout do bloco de formato é identificado por um TIPO de formato GUID. Por exemplo, FORMAT \_ WaveFormatEx especifica uma **estrutura WAVEFORMATEX.**

Quando um DMO é criado pela primeira vez, os fluxos não têm um tipo de mídia. Antes que DMO possa processar dados, o cliente deve definir um tipo de mídia para cada fluxo. Esse processo é descrito da perspectiva do cliente em [Configurando tipos de mídia em um DMO](setting-media-types-on-a-dmo.md).

**Tipos de mídia no Registro**

Um DMO pode adicionar uma lista de tipos de mídia compatíveis com o Registro chamando a [**função DMORegister.**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) Um aplicativo pode usar essas informações para pesquisar DMOs que corresponderem a um formato específico. As informações no Registro não devem ser abrangentes. Normalmente, você incluiria apenas os principais tipos aos quais o DMO dá suporte. A entrada do Registro tem chaves separadas para tipos de entrada e saída, mas não faz distinção entre fluxos individuais.

A **função DMORegister** usa a estrutura [**DMO PARTIAL \_ \_ MEDIATYPE**](/previous-versions/windows/desktop/api/Dmoreg/ns-dmoreg-dmo_partial_mediatype) para descrever tipos de mídia. Essa estrutura contém um subconjunto das informações encontradas na estrutura **DMO \_ MEDIA \_ TYPE** , ou seja, o tipo principal e o subtipo. Ele não inclui um bloco de formato, porque o bloco de formato normalmente contém informações que são muito granulares para incluir no Registro, como a altura e a largura de uma imagem de vídeo.

**Tipos de mídia preferenciais**

Depois que o aplicativo tiver criado um DMO, ele poderá consultar o DMO para os tipos de mídia aos quais ele dá suporte. Para cada fluxo, o DMO cria uma lista de tipos de mídia (possivelmente vazios), classificados em ordem de preferência. Os [**métodos IMediaObject::GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) e [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) enumeram os tipos preferenciais. Os tipos preferenciais de um fluxo podem mudar dinamicamente quando o aplicativo define tipos de mídia em outros fluxos. Por exemplo, a lista de tipos de saída preferenciais pode mudar depois que o tipo de entrada é definido ou vice-versa. No entanto, o DMO é necessário para atualizar dinamicamente seus tipos preferenciais. O aplicativo não pode assumir que cada tipo recebido é válido. Por esse motivo, os métodos [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) e [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) suportam um sinalizador para testar um tipo específico.

Os **métodos GetInputType** e **GetOutputType** retornam uma **estrutura DMO MEDIA \_ \_ TYPE.** O DMO pode deixar algumas das informações nessa estrutura em branco, para indicar um intervalo de tipos. O tipo principal ou subtipo pode ser GUID \_ NULL e o bloco de formato pode estar vazio (zero bytes). Se o bloco de formato estiver vazio, o tipo de formato deverá ser GUID \_ NULL.

Depois que o aplicativo define todos os DMO de entrada de um DMO, o DMO geralmente deve retornar pelo menos um tipo completo para cada fluxo de saída. Um tipo de saída completo facilita o teste e os aplicativos podem usá-lo como um padrão razoável. O DMO de teste depende desse comportamento. (Consulte [Usando o aplicativo DMOTest](using-the-dmotest-application.md).)

**Definindo os tipos de mídia**

Os aplicativos usam os métodos **SetInputType** e **SetOutputType** para testar, definir ou limpar tipos em um fluxo especificado. O aplicativo deve especificar totalmente o tipo. O DMO verifica se ele pode aceitar o tipo proposto. A resposta pode depender de quais tipos foram definidos em outros fluxos. O DMO sinalizador SET TYPEF CLEAR limpa o tipo de um fluxo, para que o aplicativo possa \_ \_ \_ "fazer back-out" e tentar outra combinação.

**Cenários de exemplo**

Os exemplos a seguir descrevem alguns cenários típicos para ilustrar os pontos feitos nas seções anteriores.

-   **Decodificadores de vídeo.** Em um decodificador de vídeo típico, o tipo de entrada determina parcialmente o tipo de saída. Por exemplo, geralmente ambos os fluxos devem ter a mesma taxa de quadros e dimensões de imagem. Uma opção é não definir nenhum tipo de saída preferencial até que o tipo de entrada seja definido. Outra opção é enumerar um conjunto de tipos incompletos, omitindo o bloco de formato. Use o subtipo para indicar os tipos descompactados com suporte, como RGB de 16 bits, RGB de 24 bits e assim por diante. Além disso, os decodificadores de vídeo geralmente não são suportados para definir o tipo de saída antes do tipo de entrada. O cenário comum é decodificar de um formato de entrada conhecido, portanto, essa limitação é razoável.
-   **Decodificadores de áudio.** Um decodificador de áudio pode dar suporte a um conjunto limitado e fixo de formatos de saída. Nesse caso, pode ser possível criar uma lista de formatos de saída preferenciais antes que o formato de entrada seja conhecido.
-   **Compressores.** Na maioria dos casos, um video não pode especificar totalmente seus formatos de saída preferenciais até que o aplicativo define o formato de entrada e vice-versa. Em vez disso, DMO deve retornar um tipo incompleto sem bloco de formato. Para compactação de áudio e vídeo, o aplicativo geralmente precisa definir vários parâmetros de saída, como a taxa de bits. No entanto, depois que o tipo de entrada for definido, o deve retornar pelo menos um tipo de saída completo, pelos motivos mencionados anteriormente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo um DMO](writing-a-dmo.md)
</dt> </dl>

 

 



