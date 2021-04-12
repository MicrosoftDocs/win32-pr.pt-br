---
title: Usando a substituição de URL e de servidor
description: Usando a substituição de URL e de servidor
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Playlists do metarquivo do Windows Media, substituições de URL
- listas de reprodução, substituições de URL
- listas de reprodução de metarquivo, substituições de URL
- Playlists do metarquivo do Windows Media, substituições do servidor
- listas de reprodução, substituições de servidor
- listas de reprodução de metarquivo, substituições de servidor
- Playlists do metarquivo do Windows Media, substituições de protocolo
- listas de reprodução, sobreposições de protocolo
- listas de reprodução de metarquivo, substituições de protocolo
- Windows Media Player, substituições de URL
- Windows Media Player, substituições de servidor
- Windows Media Player, substituições de protocolo
- Substituições de URL
- substituições do servidor
- sobreposições de protocolo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: eae38e81f8ae23199628e543f65f2766491f1a2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292253"
---
# <a name="using-url-and-server-rollover"></a>Usando a substituição de URL e de servidor

Você pode usar listas de reprodução de metarquivo para fornecer um meio de reverter automaticamente para fontes de conteúdo alternativas quando um fluxo não pode ser acessado ou reproduzido. Você pode usar esse método de substituição para especificar fontes do mesmo conteúdo em servidores diferentes ou diferentes tipos de servidores. Você pode, por exemplo, especificar uma primeira alternativa em um Windows Media Server diferente. Se esse conteúdo não for reproduzido, o cliente poderá passar para uma segunda alternativa em um servidor Web. O Windows Media Player tenta automaticamente se sobrepor a protocolos diferentes de acordo com suas configurações de Propriedade do Windows Media antes de tentar as URLs de substituição na playlist.

Defina a substituição de servidor e protocolo colocando vários elementos **ref** sucessivamente dentro de um elemento **entry** . Cada elemento **ref** especifica um local alternativo ou protocolo para um fluxo ou arquivo de mídia.

Código de exemplo


```XML
<!--Server and protocol rollover is set for the file Rollover.wma.-->
<ASX version="3.0">
    <TITLE>MyServer Rollover</TITLE>
   <ENTRY>
      <REF HREF="mms://Server1.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server2.proseware.com/Path/Rollover.wma"/>
      <REF HREF="mms://Server3.proseware.com/Path/Rollover.wma"/>
      <REF HREF="https://www.proseware.com/Path/Rollover.wma"/>
   </ENTRY>
</ASX>

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Criando listas de reprodução de metarquivo**](creating-metafile-playlists.md)
</dt> <dt>

[**Usando listas de reprodução de metarquivo**](using-metafile-playlists.md)
</dt> </dl>

 

 




