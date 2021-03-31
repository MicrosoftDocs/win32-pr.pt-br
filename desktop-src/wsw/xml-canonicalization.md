---
title: Canonização XML
description: A canonização XML resolve o problema de conversão de um conjunto de nós XML em bytes de forma que as alterações triviais no XML (como alterar a ordem dos atributos em um elemento) não alterem o formulário de byte resultante.
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- Serviços Web de canonização XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8b1aa00b99b604276a479f1a47aacb5bd8b1e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103824071"
---
# <a name="xml-canonicalization"></a>Canonização XML

A canonização XML resolve o problema de conversão de um conjunto de nós XML em bytes de forma que as alterações triviais no XML (como alterar a ordem dos atributos em um elemento) não alterem o formulário de byte resultante. Os bytes obtidos da canonização são comumente usados para gerar uma assinatura criptográfica sobre o conteúdo XML.


Os algoritmos de canonização XML comumente usados padronizam os seguintes aspectos:

-   Codificação de caracteres (UTF-8 sem preâmbulo)
-   Alimentação de linha e outros formulários de caracteres
-   Ordem de atributo em um elemento
-   Formulário de elemento vazio
-   Renderizando declarações de namespace

As APIs [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) e [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) fornecem a funcionalidade de canonização XML ao ler um documento.

As APIs [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) e [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) fornecem a funcionalidade de canonização XML durante a gravação de um documento.

As seguintes enumerações são usadas com canonização:

-   [**\_algoritmo de \_ canonização \_ XML do WS**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [**\_ID da \_ propriedade de canonização do WS XML \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

As funções a seguir são usadas com canonização:

-   [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

As seguintes estruturas são usadas com canonização:

-   [**prefixos do WS \_ XML em \_ formato \_ inclusivo \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [**\_propriedade de \_ canonização do WS XML \_**](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




