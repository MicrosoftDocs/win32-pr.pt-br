---
title: Referenciando capas em URLs
description: Referenciando capas em URLs
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Capas do Windows Media Player, referências de URL
- capas, referências de URL
- Referências de URL em capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637084"
---
# <a name="referencing-skins-in-urls"></a>Referenciando capas em URLs

Se você usar uma URL para carregar um arquivo de mídia que será reproduzido pelo Windows Media Player, você poderá solicitar que uma determinada capa seja usada com esse arquivo. Se a capa já estiver instalada no computador do usuário, ela será usada; caso contrário, a capa anterior será usada.

Para solicitar uma capa, adicione o seguinte ao final da URL:


```C++
?WMPSkin=skinname
```



*skinname* é o nome da capa que você deseja solicitar. Não use aspas em volta do nome da capa.

Por exemplo, para solicitar que a capa headspace seja usada, digite a seguinte URL http:


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as capas**](about-skins.md)
</dt> </dl>

 

 




