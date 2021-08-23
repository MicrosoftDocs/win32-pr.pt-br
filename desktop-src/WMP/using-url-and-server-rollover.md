---
title: Usando a substituição de URL e de servidor
description: Usando a substituição de URL e de servidor
ms.assetid: d0d15b1c-5631-486e-8490-b85ec51bd355
keywords:
- Windows Playlists de metarquivo de mídia, substituições de URL
- listas de reprodução, substituições de URL
- listas de reprodução de metarquivo, substituições de URL
- Windows Playlists de metarquivo de mídia, substituições de servidor
- listas de reprodução, substituições de servidor
- listas de reprodução de metarquivo, substituições de servidor
- Windows Playlists de metarquivo de mídia, substituições de protocolo
- listas de reprodução, sobreposições de protocolo
- listas de reprodução de metarquivo, substituições de protocolo
- Windows Media Player, substituições de URL
- Windows Media Player, substituições do servidor
- Windows Media Player, sobreposições de protocolo
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
ms.openlocfilehash: 3988ff019fba838e86ea1d0e7b0f6124c367bb8b505a0f2d2e2f639b94d93e52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465666"
---
# <a name="using-url-and-server-rollover"></a>Usando a substituição de URL e de servidor

Você pode usar listas de reprodução de metarquivo para fornecer um meio de reverter automaticamente para fontes de conteúdo alternativas quando um fluxo não pode ser acessado ou reproduzido. Você pode usar esse método de substituição para especificar fontes do mesmo conteúdo em servidores diferentes ou diferentes tipos de servidores. você pode, por exemplo, especificar uma primeira alternativa em um servidor de mídia Windows diferente. Se esse conteúdo não for reproduzido, o cliente poderá passar para uma segunda alternativa em um servidor Web. Windows Media Player automaticamente tenta passar para protocolos diferentes de acordo com suas configurações de propriedade de mídia Windows antes de tentar as URLs de substituição na playlist.

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

 

 




