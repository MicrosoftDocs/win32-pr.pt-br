---
description: Aplicativos de DVD
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: Aplicativos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acaddc683078acff84b7c90689f82becfb7b1d7c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296019"
---
# <a name="dvd-applications"></a>Aplicativos de DVD

O DirectShow fornece um componente chamado de filtro de origem do [navegador de DVD](dvd-navigator-filter.md) , que simplifica as tarefas de navegação de DVD em C++. O navegador de DVD tem todos os recursos que você encontra em um player de DVD autônomo completo, além de recursos adicionais específicos para a reprodução de DVDs em computadores pessoais. Usando o DVD Navigator, o C++ e os desenvolvedores de scripts podem criar aplicativos de DVD completos sem referir-se à especificação do DVD. O navegador de DVD, em coordenação com os filtros de decodificador, também lida com gerenciamento regional e proteção de direitos autorais (CSS e proteção de cópia analógica), isolando os desenvolvedores de aplicativos desses detalhes.

O filtro de navegador de DVD funciona em um volume DVD-Video inteiro, que consiste nos arquivos no \_ diretório TS de vídeo. Ao contrário da maioria dos filtros de origem do DirectShow que funcionam com fluxos ou arquivos individuais, o navegador de DVD usa a estrutura DVD-Video de títulos, capítulos e códigos de tempo. Os desenvolvedores que desejam reproduzir arquivos MPEG-2 individuais no DirectShow devem usar o [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) em vez do filtro do navegador de DVD. Consulte [suporte a MPEG-2 no DirectShow](mpeg-2-support-in-directshow.md) para obter mais informações.

> [!Note]  
> Para reproduzir DVDs, o usuário deve ter um decodificador MPEG-2.

 

Esta seção contém os seguintes tópicos.

-   [Recursos de suporte a DVD no DirectShow](dvd-support-features-in-directshow.md)
-   [Noções básicas de DVD](dvd-basics.md)
-   [Criando o grafo de filtro de DVD](building-the-dvd-filter-graph.md)
-   [Obtendo os ponteiros de interface de DVD](obtaining-the-dvd-interface-pointers.md)
-   [Comandos de DVD](dvd-commands.md)
-   [Identificando operações de DVD válidas](identifying-valid-dvd-operations.md)
-   [Sincronizando comandos de DVD](synchronizing-dvd-commands.md)
-   [Fluxo de dados no navegador de DVD](data-flow-in-the-dvd-navigator.md)
-   [Manipulando notificações de eventos de DVD](handling-dvd-event-notifications.md)
-   [Trabalhando com menus de DVD](working-with-dvd-menus.md)
-   [Fluxos de áudio e subimagem](audio-and-subpicture-streams.md)
-   [Impondo níveis de gerenciamento de pais](enforcing-parental-management-levels.md)
-   [Salvando e restaurando objetos DvdState](saving-and-restoring-dvdstate-objects.md)
-   [Trabalhando com cadeias de caracteres de texto em DVD](working-with-dvd-text-strings.md)
-   [Reprodução de fluxos de áudio do karaokê](playing-karaoke-audio-streams.md)
-   [Lidando com Ejetações de disco](handling-disc-ejections.md)
-   [Aprimoramentos na reprodução de DVD no Windows Vista](dvd-playback-enhancements-in-windows-vista.md)
-   [Configuração de grafo de filtro de DVD](dvd-filter-graph-configuration.md)
-   [Atalhos para páginas de referência de DVD do C++](shortcuts-to-c-dvd-reference-pages.md)

Para obter referências sobre o desenvolvimento de decodificadores de DVD/MPEG2, consulte [desenvolvimento de decodificador de DVD no DirectShow](dvd-decoder-development-in-directshow.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o DirectShow](using-directshow.md)
</dt> </dl>

 

 



