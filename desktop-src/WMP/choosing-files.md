---
title: Escolhendo arquivos
description: Escolhendo arquivos
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- Criando capas, escolhendo arquivos
- Capas do Windows Media Player, escolhendo arquivos
- capas, escolhendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160259"
---
# <a name="choosing-files"></a>Escolhendo arquivos

Se você quiser escolher um arquivo, poderá usar um código semelhante ao exemplo de playlist, mas substitua o seguinte pela seção PLAYelement:


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



Essa linha usará o método **openDialog** de **Theme** para definir uma **URL** para o Player. Você pode usar isso para escolher arquivos que não estão em listas de reprodução.

Você pode ver um exemplo de **openDialog** de trabalho semelhante na seção de exemplo do SDK.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de criação de capa**](skin-creation-guide.md)
</dt> </dl>

 

 




