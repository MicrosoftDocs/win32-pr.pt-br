---
description: Um conjunto de acompanhamento especifica os protocolos que seguem um protocolo. Monitor de Rede usa um conjunto de acompanhamento quando o analisador não pode identificar o próximo protocolo dos dados em uma instância de protocolo.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Especificando um conjunto de acompanhamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e36268be82d2fed7c3d0c56a078e41dff1733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789629"
---
# <a name="specifying-a-follow-set"></a>Especificando um conjunto de acompanhamento

Um conjunto de acompanhamento especifica os protocolos que seguem um protocolo. Monitor de Rede usa um conjunto de acompanhamento quando o analisador não pode identificar o próximo protocolo dos dados em uma instância de protocolo.

Por exemplo, o analisador NetBIOS especifica um conjunto de acompanhamento porque os dados no protocolo NetBIOS não identificam qual protocolo é o próximo. Como resultado, o analisador NetBIOS deve criar um conjunto de todos os protocolos que podem ser seguidos.

O exemplo de código a seguir identifica o conjunto de acompanhamento de NetBIOS no arquivo de [*Parser.ini*](p.md) . O conjunto de acompanhamento contém o protocolo SMB e os protocolos de chamada de procedimento remoto da Microsoft (MSRPC). Esses são os únicos protocolos que podem seguir uma instância do protocolo NetBIOS.

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

Um analisador especifica um conjunto de acompanhamento durante a implementação da função [**ParserAutoInstallInfo**](parserautoinstallinfo.md) . Um analisador pode especificar quais protocolos são precedidos e quais protocolos seguem. Quando um analisador especifica os protocolos que precedem, Monitor de Rede adiciona o protocolo analisador aos seguintes conjuntos de protocolos especificados. Quando um analisador especifica os protocolos a seguir, Monitor de Rede cria uma nova seção no arquivo de Parser.ini que inclui o conjunto de acompanhamento do analisador.

 

 



