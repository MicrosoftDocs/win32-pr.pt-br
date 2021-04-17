---
description: Introdução à programação de aplicativo do DirectShow
ms.assetid: 21a72efa-95df-4754-8304-ad56965a914d
title: Introdução à programação de aplicativo do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6218a346a7eb9711259c025aef09133ef2e58f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370169"
---
# <a name="introduction-to-directshow-application-programming"></a>Introdução à programação de aplicativo do DirectShow

Este artigo apresenta a terminologia básica e os conceitos que são usados no DirectShow. Depois de ler esta seção, você estará pronto para escrever seu primeiro aplicativo DirectShow.

**Filtros e gráficos de filtro**

O bloco de construção do DirectShow é um componente de software chamado de *filtro*. Um filtro é um componente de software que executa alguma operação em um fluxo de multimídia. Por exemplo, os filtros do DirectShow podem

-   ler arquivos
-   obter vídeo de um dispositivo de captura de vídeo
-   decodificar vários formatos de fluxo, como vídeo MPEG-1
-   passar dados para a placa gráfica ou de som

Os filtros recebem a entrada e produzem a saída. Por exemplo, se um filtro decodifica o vídeo MPEG-1, a entrada é o fluxo codificado em MPEG e a saída é uma série de quadros de vídeo descompactados.

No DirectShow, um aplicativo executa qualquer tarefa conectando cadeias de filtros em conjunto, para que a saída de um filtro se torne a entrada para outra. Um conjunto de filtros conectados é chamado de *grafo de filtro*. Por exemplo, o diagrama a seguir mostra um gráfico de filtro para reproduzir um arquivo AVI.

![gráfico de filtro para reproduzir um arquivo AVI](images/avi-filter-graph.png)

O filtro de origem de arquivo lê o arquivo AVI do disco rígido. O filtro de Splitter AVI analisa o arquivo em dois fluxos, um fluxo de vídeo compactado e um fluxo de áudio. O filtro de descompactação AVI decodifica os quadros de vídeo. O filtro de processador de vídeo desenha os quadros para a exibição, usando o DirectDraw ou GDI. O filtro de dispositivo DirectSound padrão desempenha o fluxo de áudio, usando o DirectSound.

O aplicativo não precisa gerenciar todo esse fluxo de dados. Em vez disso, os filtros são controlados por um componente de alto nível chamado Gerenciador de gráfico de filtro. O aplicativo faz chamadas de API de alto nível, como "Run" (para mover dados através do grafo) ou "Stop" (para interromper o fluxo de dados). Se você precisar de mais controle sobre as operações de fluxo, poderá acessar os filtros diretamente por meio de interfaces COM. O Gerenciador de gráficos de filtro também passa notificações de eventos para o aplicativo.

O Gerenciador de gráfico de filtro também serve para outra finalidade: ele fornece métodos para que o aplicativo crie o gráfico de filtro, conectando os filtros juntos. (O DirectShow também fornece vários objetos auxiliares que simplificam esse processo. Eles são descritos detalhadamente na documentação.)

**Escrevendo um aplicativo do DirectShow**

Em termos gerais, há três tarefas que qualquer aplicativo DirectShow deve executar. Eles são ilustrados no diagrama a seguir.

![aplicativo DirectShow típico](images/fgm.png)

1.  O aplicativo cria uma instância do Gerenciador de gráfico de filtro.
2.  O aplicativo usa o Gerenciador de gráfico de filtro para criar um grafo de filtro. O conjunto exato de filtros no grafo dependerá do aplicativo.
3.  O aplicativo usa o Gerenciador de gráfico de filtro para controlar o grafo de filtro e transmitir dados por meio dos filtros. Durante todo esse processo, o aplicativo também responderá a eventos do Gerenciador do grafo de filtro.

Quando o processamento é concluído, o aplicativo libera o Gerenciador do gráfico de filtro e todos os filtros.

O DirectShow é baseado em COM; o Gerenciador de gráficos de filtro e os filtros são todos os objetos COM. Você deve ter uma compreensão geral da programação de cliente COM antes de começar a programar o DirectShow. Muitos livros sobre a programação COM estão disponíveis.

Para começar a usar o DirectShow, leia o artigo [como reproduzir um arquivo](how-to-play-a-file.md), que apresenta um aplicativo de console simples para reproduzir um arquivo de vídeo. A seção [sobre o DirectShow](about-directshow.md) explica a arquitetura do DirectShow mais detalhadamente, enquanto a seção [usando o DirectShow](using-directshow.md) examina os principais cenários com suporte do DirectShow, como captura, edição de vídeo, reprodução de DVD e televisão.

 

 



