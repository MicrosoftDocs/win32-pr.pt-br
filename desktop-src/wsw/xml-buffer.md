---
title: Buffer XML
description: Um buffer XML fornece armazenamento eficiente na memória para dados XML arbitrários.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Serviços Web de buffer XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab71121dc451c9ccb186c754d537836f9e899fa9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917796"
---
# <a name="xml-buffer"></a>Buffer XML

Um buffer XML fornece armazenamento eficiente na memória para dados XML arbitrários.


Para ler dados de um buffer XML, use um [leitor de XML](xml-reader.md) e chame [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) com o buffer XML. O leitor será posicionado no início do documento.

Para inserir dados em um buffer, use um [gravador de XML](xml-writer.md) e chame [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) com o buffer XML. O gravador será posicionado no final do documento.

Depois que um leitor tiver sido definido como um buffer XML, além de todas as APIs do leitor XML, [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) poderá ser usado para navegar pelo leitor pelo documento. [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) e [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) também podem ser usados para registrar uma posição no documento e retornar a ela mais tarde.

Depois que um gravador tiver sido definido como um buffer XML, além de todas as APIs do gravador de XML, [**WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) poderá ser usado para navegar pelo gravador por meio do documento. [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) e [**WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) também podem ser usados para registrar uma posição no documento e retornar a ela mais tarde. O gravador sempre insere dados antes do nó no qual ele está posicionado.

Os nós podem ser excluídos do buffer XML obtendo a posição do nó usando [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) ou [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) e, em seguida, chamando [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) com essa posição. Para elementos, isso excluirá o elemento, todos os seus filhos, incluindo seu elemento final correspondente.

Uma posição é representada pelo valor [**posição do \_ \_ nó WS \_ XML**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position). As posições são específicas para um buffer XML específico e só são válidas desde que o buffer XML seja válido.

As seguintes enumerações são usadas com buffers XML:

-   [**WS \_ mover \_ para**](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [**\_ID da \_ Propriedade do buffer XML \_ WS \_**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

As funções a seguir são usadas com buffers XML:

-   [**WsCreateXmlBuffer**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

O seguinte identificador é usado com buffers XML:

-   [\_buffer XML do WS \_](ws-xml-buffer.md)

As seguintes estruturas são usadas com buffers XML:

-   [**\_propriedade de \_ buffer \_ XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [**\_posição do \_ nó \_ XML do WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




