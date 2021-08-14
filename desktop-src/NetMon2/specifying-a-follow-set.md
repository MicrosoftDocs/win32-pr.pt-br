---
description: Um conjunto a seguir especifica os protocolos que seguem um protocolo. Monitor de Rede usa um conjunto a seguir quando o analisador não pode identificar o próximo protocolo dos dados em uma instância de protocolo.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Especificando um conjunto a seguir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b11320872cc07d69f5796e344a1d5ed4dea4594e48f9697901126d915fd7b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363042"
---
# <a name="specifying-a-follow-set"></a>Especificando um conjunto a seguir

Um conjunto a seguir especifica os protocolos que seguem um protocolo. Monitor de Rede usa um conjunto a seguir quando o analisador não pode identificar o próximo protocolo dos dados em uma instância de protocolo.

Por exemplo, o analisador NetBIOS especifica um conjunto a seguir porque os dados no protocolo NetBIOS não identificam qual protocolo é o próximo. Como resultado, o analisador NetBIOS deve criar um conjunto de acompanhamento de todos os protocolos que podem ser seguidos.

O exemplo de código a seguir identifica o netBIOS a seguir definido no [*arquivoParser.ini*](p.md) dados. O conjunto a seguir contém protocolos SMB (server message block) e MSRPC (chamada de procedimento remoto da Microsoft). Esses são os únicos protocolos que podem seguir uma instância do protocolo NetBIOS.

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

Um analisador especifica um conjunto a seguir durante a implementação da [**função ParserAutoInstallInfo.**](parserautoinstallinfo.md) Um analisador pode especificar quais protocolos precedem e quais protocolos seguem. Quando um analisador especifica os protocolos que precedem, Monitor de Rede adiciona o protocolo de analisador aos conjuntos a seguir dos protocolos especificados. Quando um analisador especifica os protocolos a seguir, Monitor de Rede cria uma nova seção no arquivo Parser.ini que inclui o conjunto a seguir do analisador.

 

 



