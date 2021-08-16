---
title: XML Buffer
description: Um Buffer XML fornece armazenamento na memória eficiente para dados XML arbitrários.
ms.assetid: e379628b-c6f8-48b1-8109-59fb604f2bcb
keywords:
- Serviços Web de buffer XML para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd4e4725f2ad3345dcef7c33b694a8e327f4d8a6c43fbce39f9c57babfa467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192332"
---
# <a name="xml-buffer"></a>XML Buffer

Um Buffer XML fornece armazenamento na memória eficiente para dados XML arbitrários.


Para ler dados de um Buffer XML, use um Leitor [de XML](xml-reader.md) e chame [**WsSetInputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetinputtobuffer) com o Buffer XML. O leitor será posicionado no início do documento.

Para inserir dados em um buffer, use um [Xml Writer e](xml-writer.md) chame [**WsSetOutputToBuffer**](/windows/desktop/api/WebServices/nf-webservices-wssetoutputtobuffer) com o Buffer XML. O autor será posicionado no final do documento.

Depois que um leitor tiver sido definido como um Buffer XML, além de todas as APIs de Leitor de XML, o [**WsMoveReader**](/windows/desktop/api/WebServices/nf-webservices-wsmovereader) poderá ser usado para navegar pelo leitor por meio do documento. [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) e [**WsSetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetreaderposition) também podem ser usados para registrar uma posição no documento e retornar a ele mais tarde.

Depois que um autor tiver sido definido como um Buffer XML, além de todas as APIs do Xml Writer, [**o WsMoveWriter**](/windows/desktop/api/WebServices/nf-webservices-wsmovewriter) poderá ser usado para navegar pelo autor por meio do documento. [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) [**e WsSetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wssetwriterposition) também podem ser usados para registrar uma posição no documento e retornar a ele mais tarde. O autor sempre insere dados antes do nó no qual ele está posicionado.

Os nós podem ser excluídos do buffer XML obtendo a posição do nó usando [**WsGetReaderPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetreaderposition) ou [**WsGetWriterPosition**](/windows/desktop/api/WebServices/nf-webservices-wsgetwriterposition) e, em seguida, chamando [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode) com essa posição. Para elementos, isso excluirá o elemento , todos os seus filhos, incluindo seu elemento final correspondente.

Uma posição é representada pelo valor [**POSIÇÃO DO NÓ XML \_ \_ \_ do WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position) As posições são específicas para um buffer XML específico e só são válidas desde que o Buffer XML seja válido.

As enumerações a seguir são usadas com buffers XML:

-   [**WS \_ MOVE \_ TO**](/windows/desktop/api/WebServices/ne-webservices-ws_move_to)
-   [**ID DA \_ PROPRIEDADE DO BUFFER XML \_ \_ \_ DO WS**](/windows/win32/api/webservices/ne-webservices-ws_xml_reader_property_id)

As seguintes funções são usadas com buffers XML:

-   [**WsCreateXmlBuffer**](/windows/desktop/api/WebServices/nf-webservices-wscreatexmlbuffer)
-   [**WsRemoveNode**](/windows/desktop/api/WebServices/nf-webservices-wsremovenode)

O seguinte handle é usado com buffers XML:

-   [BUFFER \_ XML do WS \_](ws-xml-buffer.md)

As seguintes estruturas são usadas com buffers XML:

-   [**PROPRIEDADE \_ BUFFER XML \_ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_buffer_property)
-   [**POSIÇÃO DO \_ NÓ XML \_ \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_node_position)

 

 




