---
description: Aplicativos de DVD
ms.assetid: 6f41e0f1-e550-4ca6-9a80-ce4d498289e2
title: Aplicativos de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d601fdbf94ef2a2d9a70d1f28f68854200b58f9fb44d23c3738994f3001e3a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102956"
---
# <a name="dvd-applications"></a>Aplicativos de DVD

DirectShow fornece um componente chamado filtro de origem do Navegador de [DVD](dvd-navigator-filter.md) que simplifica as tarefas de navegação de DVD no C++. O Navegador de DVD tem todos os recursos que você encontra em um player de DVD autônomo completo, além de recursos adicionais específicos para reprodução de DVDs em computadores pessoais. Usando o Navegador de DVD, o C++ e os desenvolvedores de script podem criar aplicativos de DVD completos sem se referir à especificação de DVD. O Navegador de DVD, em coordenação com os filtros do decodificador, também lida com o gerenciamento regional e a proteção de direitos autorais (CSS e proteção contra cópia análoga), isolando os desenvolvedores de aplicativos desses detalhes.

O filtro Navegador de DVD funciona em um volume DVD-Video inteiro, que consiste nos arquivos no diretório \_ VIDEO TS. Ao contrário da DirectShow de origem que funcionam com fluxos ou arquivos individuais, o Navegador de DVD usa a estrutura DVD-Video de títulos, capítulos e códigos de tempo. Os desenvolvedores que desejam reproduzir arquivos MPEG-2 individuais no DirectShow devem usar o [Demultiplexer MPEG-2](mpeg-2-demultiplexer.md) em vez do filtro Navegador de DVD. Confira [Suporte ao MPEG-2 no DirectShow](mpeg-2-support-in-directshow.md) para obter mais informações.

> [!Note]  
> Para reproduzir DVDs, o usuário deve ter um decodificador MPEG-2.

 

Esta seção contém os seguintes tópicos.

-   [Recursos de suporte de DVD DirectShow](dvd-support-features-in-directshow.md)
-   [Noções básicas de DVD](dvd-basics.md)
-   [Criando o filtro de DVD Graph](building-the-dvd-filter-graph.md)
-   [Obtendo os ponteiros da interface de DVD](obtaining-the-dvd-interface-pointers.md)
-   [Comandos de DVD](dvd-commands.md)
-   [Identificando operações de DVD válidas](identifying-valid-dvd-operations.md)
-   [Sincronizando comandos de DVD](synchronizing-dvd-commands.md)
-   [Dados Flow no Navegador de DVD](data-flow-in-the-dvd-navigator.md)
-   [Manipulando notificações de eventos de DVD](handling-dvd-event-notifications.md)
-   [Trabalhando com menus de DVD](working-with-dvd-menus.md)
-   [Audio e Subpicture Fluxos](audio-and-subpicture-streams.md)
-   [Impondo níveis de gerenciamento dos pais](enforcing-parental-management-levels.md)
-   [Salvando e restaurando objetos DvdState](saving-and-restoring-dvdstate-objects.md)
-   [Trabalhando com cadeias de caracteres de texto de DVD](working-with-dvd-text-strings.md)
-   [Como tocar o Fluxos](playing-karaoke-audio-streams.md)
-   [Manipulando ejetos de disco](handling-disc-ejections.md)
-   [Aprimoramentos de reprodução de DVD no Windows Vista](dvd-playback-enhancements-in-windows-vista.md)
-   [Configuração de filtro Graph DVD](dvd-filter-graph-configuration.md)
-   [Atalhos para páginas de referência de DVD do C++](shortcuts-to-c-dvd-reference-pages.md)

Para referências sobre desenvolvimento de decodificador DVD/MPEG2, consulte [Desenvolvimento de decodificador de DVD no DirectShow](dvd-decoder-development-in-directshow.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DirectShow](using-directshow.md)
</dt> </dl>

 

 



