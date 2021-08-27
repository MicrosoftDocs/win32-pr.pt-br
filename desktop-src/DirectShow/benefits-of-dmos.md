---
description: Benefícios dos DMOs
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Benefícios dos DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b13a9ef7f91446d03732b935648b689ab65a33c9d10dcfca26051d9284404db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103366"
---
# <a name="benefits-of-dmos"></a>Benefícios dos DMOs

Os DMOs oferecem as seguintes vantagens:

-   Em geral, eles são menores e mais simples do que DirectShow filtros, porque eles suportam menos funcionalidade.
-   Eles são mais flexíveis do que DirectShow filtros porque não exigem um grafo de filtro. Você pode usá-los com DirectShow quando precisar dos serviços que DirectShow fornece, como sincronização, conexão inteligente, manipulação automática de fluxo de dados e gerenciamento de threads. Os clientes que não precisam desses serviços podem acessar DMOs diretamente.
-   Os DMOs sempre executam o processamento de dados síncrono, o que elimina muitos dos problemas de threading que você deve considerar se você escreve um filtro.
-   Ao contrário dos codecs ACM e VCM tradicionais, os DMOs são baseados no COM (Component Object Model), para que possam ser estendidos por meio de **QueryInterface**.
-   Os DMOs são suportados por um modelo de streaming mais generalizado do que os codecs ACM ou VCM. Assim como DirectShow filtros, os DMOs podem dar suporte a várias entradas e várias saídas.

Por esses motivos, os DMOs agora são recomendados como a solução para escrever codificadores, decodificadores e efeitos de áudio. Muitos outros cenários também são possíveis, dependendo das necessidades do aplicativo.

Como os DMOs diferem dos DirectShow filtros

DirectShow filtros não podem funcionar fora de um grafo DirectShow filtro. No DirectShow, o Gerenciador de Graph filtra entre o aplicativo e os filtros. DirectShow filtros fazem a maior parte do trabalho necessário para transmitir dados, incluindo:

-   Alocando buffers.
-   Negociando tipos de mídia e conexões com outros filtros.
-   Endossar dados por meio do grafo de filtro.
-   Enviando eventos para o Gerenciador de Graph Filtro.
-   Sincronizando vários threads.

Por outro lado, um DMO faz nada disso. Em vez disso, esses tipos de tarefas são de responsabilidade do cliente usando o DMO. O cliente aloca buffers, os preenche com dados e os entrega ao DMO. O DMO processa os dados e o cliente recupera os buffers de saída resultantes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre DMOs](about-dmos.md)
</dt> </dl>

 

 



