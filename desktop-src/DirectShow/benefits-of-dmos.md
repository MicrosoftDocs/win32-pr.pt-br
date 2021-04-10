---
description: Benefícios do DMOs
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Benefícios do DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163841"
---
# <a name="benefits-of-dmos"></a>Benefícios do DMOs

O DMOs oferece as seguintes vantagens:

-   Eles são geralmente menores e mais simples que os filtros do DirectShow, pois oferecem suporte a menos funcionalidade.
-   Eles são mais flexíveis do que os filtros do DirectShow porque não exigem um grafo de filtro. Você pode usá-los com o DirectShow quando precisar dos serviços que o DirectShow fornece, como sincronização, conexão inteligente, manipulação automática de fluxo de dados e gerenciamento de threads. Os clientes que não precisam desses serviços podem acessar o DMOs diretamente.
-   O DMOs sempre executa o processamento de dados síncrono, o que elimina muitos dos problemas de Threading que você deve considerar se escrever um filtro.
-   Ao contrário dos codecs ACM e VCM tradicionais, os DMOs são baseados na Component Object Model (COM), para que possam ser estendidos por meio de **QueryInterface**.
-   O DMOs dá suporte a um modelo de streaming mais generalizado que os codecs ACM ou VCM. Assim como os filtros do DirectShow, o DMOs pode dar suporte a várias entradas e várias saídas.

Por esses motivos, DMOs agora são recomendados como a solução para escrever codificadores, decodificadores e efeitos de áudio. Muitos outros cenários também são possíveis, dependendo das necessidades do aplicativo.

Como o DMOs difere dos filtros do DirectShow

Os filtros do DirectShow não podem funcionar fora de um grafo de filtro do DirectShow. No DirectShow, o Gerenciador de gráfico de filtro é corrigido entre o aplicativo e os filtros. Os filtros do DirectShow fazem a maior parte do trabalho necessário para transmitir dados, incluindo:

-   Alocando buffers.
-   Negociando tipos de mídia e conexões com outros filtros.
-   Enviar dados por push pelo grafo de filtro.
-   Enviando eventos para o Gerenciador de gráfico de filtro.
-   Sincronizando vários threads.

Por outro lado, um DMO não faz nenhuma dessas coisas. Em vez disso, esses tipos de tarefas são responsabilidade do cliente usando o DMO. O cliente aloca buffers, preenche-os com dados e os entrega para o DMO. O DMO processa os dados e o cliente recupera os buffers de saída resultantes.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o DMOs](about-dmos.md)
</dt> </dl>

 

 



