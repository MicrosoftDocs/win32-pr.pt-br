---
title: Canonização XML
description: A canonização XML resolve o problema de converter um conjunto de nós XML em bytes de forma que alterações triviais no XML (como alterar a ordem dos atributos em um elemento) não alterem o formulário de byte resultante.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Serviços Web de Canonicalização XML para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8db77e449c4e3d6ee5f6e2cb474c84a6b1161a4fee87c35d01d278882b178cc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082980"
---
# <a name="xml-canonicalization"></a>Canonização XML

A canonização XML resolve o problema de converter um conjunto de nós XML em bytes de forma que alterações triviais no XML (como alterar a ordem dos atributos em um elemento) não alterem o formulário de byte resultante. Os bytes obtidos da canonicalização normalmente são usados para gerar uma assinatura criptográfica sobre o conteúdo XML.


Os algoritmos de canonicalização XML comumente usados padronizam os seguintes aspectos:

-   Codificação de caracteres (UTF-8 sem preâmbulo)
-   Linefeed e outros formulários de caractere
-   Ordem de atributo em um elemento
-   Formulário de elemento vazio
-   Declarações de namespace de renderização

As APIs [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) e [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) fornecem a funcionalidade de canonização XML ao ler um documento.

As APIs [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) e [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) fornecem a funcionalidade de canonicalização XML ao escrever um documento.

As enumerações a seguir são usadas com canonicalização:

-   [**ALGORITMO DE \_ CANONICALIZAÇÃO DE XML \_ DO WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [**ID DA PROPRIEDADE \_ \_ CANONICALIZATION \_ DO \_ WS XML**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

As seguintes funções são usadas com canonicalização:

-   [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

As seguintes estruturas são usadas com canonicalização:

-   [**\_ \_ PREFIXOS INCLUSIVOS DE \_ CANONICALIZAÇÃO XML \_ DO WS**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [**PROPRIEDADE \_ CANONICALIZATION DO WS XML \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




