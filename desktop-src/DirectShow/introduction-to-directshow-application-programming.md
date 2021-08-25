---
description: Introdução à programação DirectShow aplicativo
ms.assetid: 21a72efa-95df-4754-8304-ad56965a914d
title: Introdução à programação DirectShow aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a448d49939e69b7c8a3b244b27a91a93eaf941eebf1960b7b2a53e4ad9137341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823506"
---
# <a name="introduction-to-directshow-application-programming"></a>Introdução à programação DirectShow aplicativo

Este artigo apresenta a terminologia básica e os conceitos que são usados no DirectShow. Depois de ler esta seção, você estará pronto para escrever seu primeiro DirectShow aplicativo.

**Filtros e grafos de filtro**

O bloco de construção do DirectShow é um componente de software chamado de *filtro*. Um filtro é um componente de software que executa alguma operação em um fluxo multimídia. Por exemplo, DirectShow filtros podem

-   ler arquivos
-   obter vídeo de um dispositivo de captura de vídeo
-   decodificar vários formatos de fluxo, como vídeo MPEG-1
-   passar dados para os gráficos ou a placa de som

Os filtros recebem entrada e produzem a saída. Por exemplo, se um filtro decodificar o vídeo MPEG-1, a entrada será o fluxo codificado em MPEG e a saída será uma série de quadros de vídeo descompactados.

No DirectShow, um aplicativo executa qualquer tarefa conectando cadeias de filtros, para que a saída de um filtro se torne a entrada para outro. Um conjunto de filtros conectados é chamado de *grafo de filtro.* Por exemplo, o diagrama a seguir mostra um grafo de filtro para a reprodução de um arquivo AVI.

![grafo de filtro para reproduzir um arquivo avi](images/avi-filter-graph.png)

O filtro Fonte de Arquivo lê o arquivo AVI do disco rígido. O filtro divisor AVI analisará o arquivo em dois fluxos, um fluxo de vídeo compactado e um fluxo de áudio. O filtro de descompactador AVI decodifica os quadros de vídeo. O filtro Renderador de Vídeo desenha os quadros para a exibição, usando DirectDraw ou GDI. O filtro Dispositivo DirectSound Padrão reproduz o fluxo de áudio usando DirectSound.

O aplicativo não precisa gerenciar todo esse fluxo de dados. Em vez disso, os filtros são controlados por um componente de alto nível chamado Gerenciador Graph Filtro. O aplicativo faz chamadas à API de alto nível, como "Executar" (para mover dados pelo grafo) ou "Parar" (para interromper o fluxo de dados). Se você precisar de mais controle sobre as operações de fluxo, poderá acessar os filtros diretamente por meio de interfaces COM. O Gerenciador Graph Filtro também passa notificações de eventos para o aplicativo.

O Gerenciador Graph Filtro também serve para outra finalidade: ele fornece métodos para o aplicativo criar o grafo de filtro, conectando os filtros juntos. (DirectShow também fornece vários objetos auxiliares que simplificam esse processo. Eles são descritos detalhadamente na documentação.)

**Escrevendo um DirectShow aplicativo**

Em termos gerais, há três tarefas que qualquer DirectShow aplicativo deve executar. Eles são ilustrados no diagrama a seguir.

![aplicativo directshow típico](images/fgm.png)

1.  O aplicativo cria uma instância do Gerenciador Graph Filtro.
2.  O aplicativo usa o Gerenciador Graph Filtro para criar um grafo de filtro. O conjunto exato de filtros no grafo dependerá do aplicativo.
3.  O aplicativo usa o Gerenciador de Graph filtro para controlar o grafo de filtro e transmitir dados por meio dos filtros. Ao longo desse processo, o aplicativo também responderá a eventos do Gerenciador de Graph Filtro.

Quando o processamento é concluído, o aplicativo libera o Gerenciador Graph Filtro e todos os filtros.

DirectShow é baseado em COM; O Gerenciador Graph filtros e os filtros são todos objetos COM. Você deve ter uma compreensão geral da programação de cliente COM antes de começar a programar DirectShow. Muitos livros sobre programação COM estão disponíveis.

Para começar a usar DirectShow, leia o artigo [How To Play a File](how-to-play-a-file.md), que apresenta um aplicativo de console simples para reproduzir um arquivo de vídeo. A seção Sobre [DirectShow](about-directshow.md) explica a arquitetura do DirectShow mais detalhadamente, enquanto a seção Usando [DirectShow](using-directshow.md) examina os principais cenários com suporte do DirectShow, como captura, edição de vídeo, reprodução de DVD e tv.

 

 



