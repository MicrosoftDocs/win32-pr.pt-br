---
title: Usando anúncios
description: Usando anúncios
ms.assetid: c372a4f8-2355-4c69-bba2-72b224879c4d
keywords:
- Listas de reprodução do metarquivo do Windows Media, anúncios
- listas de reprodução, anúncios
- listas de reprodução de metarquivo, anúncios
- Windows Media Player, anúncios
- comunicados
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0c16fafee1984d08992b96c39d7c3893ea54f682
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105765627"
---
# <a name="using-announcements"></a>Usando anúncios

Um comunicado é um arquivo que contém informações sobre a URL para um fluxo de mídia, incluindo o endereço IP de multicast, a porta, o formato de fluxo e outras configurações de estação. Os anúncios são criados pelo administrador do Windows Media quando um fluxo de publicação unicast ou multicast é criado. O cliente pode carregar rapidamente o arquivo de anúncio e, em seguida, continuar a acessar o arquivo de mídia de streaming.

Para um ponto de publicação unicast, o fluxo de mídia do ponto de publicação é aberto. Para um ponto de publicação multicast, a URL é extraída de um arquivo de estação de difusão com uma extensão. NSC e a mídia de streaming é acessada. Ao contrário de um fluxo unicast, nenhuma informação de cabeçalho está contida em um fluxo de multicast. Essas informações são provenientes do arquivo de estação de difusão com uma extensão. NSC. O Windows Media Player geralmente abre primeiro um arquivo de anúncio, que é usado para listas de reprodução de metarquivo, que aponta para o local do arquivo de estação de difusão.

Código de exemplo


```XML
<ASX VERSION="3.0">
    <TITLE>title</TITLE>
    <ENTRY>
        <REF HREF="mms://proseware.com/pubpoint"/>
    </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando listas de reprodução de metarquivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Usando listas de reprodução de metarquivo**](using-metafile-playlists.md)
</dt> </dl>

 

 




