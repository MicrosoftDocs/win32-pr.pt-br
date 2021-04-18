---
title: Visão geral dos metaarquivos do Windows Media
description: Visão geral dos metaarquivos do Windows Media
ms.assetid: 5b7742c0-f416-4bf4-ae03-9554b51fe620
keywords:
- Metaarquivos do Windows Media, sobre
- Windows Media Player, metaarquivos
- Windows Media Player, metaarquivos do Windows Media
- metaarquivos, sobre
- Windows Media, metaarquivos
- Listas de reprodução do metarquivo do Windows Media, sobre
- listas de reprodução, sobre
- Metaarquivos de mídia do Windows, sintaxe
- metaarquivos, sintaxe
- listas de reprodução de metarquivo, sobre
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e7ed86cca023103c044f28141e0212542d83d200
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105771396"
---
# <a name="windows-media-metafiles-overview"></a>Visão geral dos metaarquivos do Windows Media

A parte mais importante do uso bem-sucedido dos metarquivos de mídia do Windows é usar a sintaxe correta para os elementos Metafile. Os erros de sintaxe em um metarquivo do Windows Media podem fazer com que algo de um único atributo seja ignorado, para que o metarquivo não seja reconhecido como válido e não funcione.

Quase tão importante é a ordem na qual os elementos aparecem em um metarquivo do Windows Media. Os atributos de alguns elementos substituem temporariamente os atributos de elementos semelhantes em seções diferentes do metarquivo. Há uma [ordem de precedência](order-of-precedence.md)definida.

As listas de reprodução do Windows Media Metafile são metarquivos do Windows Media que fornecem informações que o Windows Media Player usa para receber fluxos unicast, fluxos multicast e outras mídias com suporte de uma intranet ou da Internet. Uma lista de reprodução de metarquivo é basicamente um atalho para conteúdo de mídia. Uma lista de reprodução de metarquivo pode ser enviada como email, usada como uma referência de link em uma página da Web, criada dinamicamente usando páginas de Active Server (ASP) ou existir como um arquivo autônomo em uma unidade de disco local. Uma lista de reprodução de metarquivo pode fazer referência a outra lista de reprodução de metarquivo, uma página ASP ou um arquivo de estação de mídia do Windows (com uma extensão de nome de arquivo. NSC). Um arquivo. NSC é usado para definir uma estação de mídia do Windows para o Windows Media Player. O processo básico de manipulação é o mesmo para cada caso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre os metaarquivos de mídia do Windows**](about-windows-media-metafiles.md)
</dt> </dl>

 

 




